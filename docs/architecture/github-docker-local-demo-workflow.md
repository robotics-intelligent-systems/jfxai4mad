# Running a GitHub Application Demo Locally with Docker

[Documentation index](../README.md) · [KVM demo sandbox hosting](./kvm-hosting-ephemeral-demo-sandbox.md) · [Interactive demo plan](../business/interactive-demo-b2b-conversion-and-sandbox-plan.md)

## Purpose and status

This note consolidates the supplemental Spanish guide for cloning an application from GitHub, building a Docker image and running a local demo. It describes a generic workflow; it does not identify a particular repository, verify that a given project has a Dockerfile or Compose file, or deploy an application.

## 1. Choose the repository's documented path

Start with the repository's README and inspect its `Dockerfile`, `compose.yaml` or `docker-compose.yml`, `.dockerignore`, and any `.env.example`. Use the files and commands maintained by the project. A generic clone is:

```sh
git clone https://github.com/OWNER/REPOSITORY.git
cd REPOSITORY
```

For a multi-service project with a Compose file, build and start the configured services:

```sh
docker compose up --build
```

This runs in the foreground and shows service logs. Add `-d` to run in the background; use `docker compose logs -f` to follow logs. Stop the project with `docker compose down`. Compose can coordinate application dependencies such as a database or cache when the repository defines them. `--build` asks Compose to build images before starting services; it does not mean that Compose fetches arbitrary newer GitHub source.

For a repository that documents a single Dockerfile and no Compose setup, a simple example is:

```sh
docker build -t demo-local .
docker run --rm -p 127.0.0.1:8080:80 --name demo-local demo-local
```

Replace ports and options with the application's actual configuration. The mapping above binds the host port to loopback, so it is reachable at `http://localhost:8080` from that machine. The source's `-p 8080:80` example publishes on all host interfaces by default; that can make the service reachable from other machines, subject to network controls. Docker's [published-port documentation](https://docs.docker.com/engine/network/port-publishing/) describes this behavior.

## 2. Keep local changes in sync

An image build copies the source selected by its build context into an image. Editing host files afterward does not update that image by itself. The source guide suggests bind mounts for live editing, but a broad mount such as `.:/app` can hide files already present in the image, including platform-specific dependencies such as `node_modules`.

Use the development workflow the repository supports. A bind mount can suit simple projects when paths and dependency handling are configured carefully. Docker Compose Watch provides file-level sync or rebuild rules for services built from source and is available with Compose 2.22.0 and later. See [Use Compose Watch](https://docs.docker.com/compose/how-tos/file-watch/) and the [Compose Develop specification](https://docs.docker.com/reference/compose-file/develop/).

Illustrative development configuration (adapt paths and commands to the project):

```yaml
services:
  app:
    build: .
    ports:
      - "127.0.0.1:3000:3000"
    develop:
      watch:
        - action: sync
          path: ./src
          target: /app/src
          ignore:
            - node_modules/
```

Run `docker compose up --watch` when the service and watch rules are configured. Hot reload still depends on the framework and application process responding to the synced files.

## 3. Local-demo safeguards

- Check the repository's prerequisites, startup command, health endpoint, ports, and required environment variables before starting services. Copy `.env.example` only as directed and fill in local values.
- Keep credentials out of source, Dockerfiles, image layers, and committed `.env` files. Compose secrets can grant a service access to selected secret files; see [Docker Compose secrets](https://docs.docker.com/compose/how-tos/use-secrets/). Build credentials should use BuildKit secret or SSH mounts rather than build arguments; see [Build secrets](https://docs.docker.com/build/building/secrets/).
- Inspect the Dockerfile and Compose configuration before building. A Dockerfile can execute arbitrary build steps, and Compose can mount host paths, expose ports, or start privileged services.
- Treat a local demo as a development environment. It does not by itself provide production hardening, backups, monitoring, isolation between visitors, or a temporary-session lifecycle. Public multi-user demos need a separately designed and tested deployment; see the [KVM sandbox note](./kvm-hosting-ephemeral-demo-sandbox.md).

## Source and coverage

The source guide covers the clone/build/run sequence, Compose and Dockerfile alternatives, bind mounts and hot reload, plus isolation, consistency and quick evaluation as claimed advantages. The note qualifies the broad bind-mount example, adds a loopback-only port mapping, distinguishes Git retrieval from image build, and records current Compose Watch and credential-handling guidance.

[Immutable original: Para desplegar y ejecutar.txt](https://github.com/robotics-intelligent-systems/jfxai4mad/blob/408891777007f61adc69af6e857fa5f70c4107c1/docs/Para%20desplegar%20y%20ejecutar.txt). Baseline commit: `408891777007f61adc69af6e857fa5f70c4107c1`; Git blob: `a5b4cd0071ad15904ac667c17a8eaa58510e1f47`.

No application was cloned, built or run. Commands are examples and must be matched to the selected repository.
