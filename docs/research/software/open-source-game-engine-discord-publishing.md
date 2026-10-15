# Publishing an open-source game engine through Discord

**Reviewed:** 14 October 2026  
**Status:** translated and consolidated planning note; no Discord server, integration or application has been created.

This note combines two Spanish drafts about promoting an open-source game engine on Discord. They describe two separate routes: building a developer community around the project, and making a web game or demo available as a Discord Activity. A community can support any engine; an Activity requires a web application that can run in Discord's embedded environment.

## 1. Community and project updates

The source proposes a Community-enabled Discord server with channels for announcements, general discussion, user projects, support and development contributions. An announcement channel can distribute selected updates to other servers that follow it. Discord documents announcement channels as a Community-server feature; this does not itself connect GitHub or guarantee that every event is reposted.

Repository updates can be sent through an integration or a webhook receiver that subscribes to GitHub events such as pushes, pull requests and releases. GitHub describes webhooks as event notifications delivered to an external server. The source's suggested webhook URL format and setup steps are examples, not a universal GitHub-to-Discord configuration: the receiving integration must accept GitHub's payload and validate its signature. Keep webhook credentials private and out of repository files.

Suggested channel roles:

| Channel | Purpose |
| --- | --- |
| `#announcements` | Releases, roadmap changes and project news |
| `#general` | Community discussion |
| `#showcase` | Games and tools made with the engine |
| `#support` | User questions and troubleshooting |
| `#development` | Contribution discussion, issues and pull requests |

These are source recommendations, not a required Discord structure. Set clear moderation, contribution and support expectations before inviting a larger audience.

## 2. Web game or demo as a Discord Activity

The second route applies when the engine or a sample project can be exported as a web application, for example HTML5/WebGL/WebAssembly or a JavaScript/TypeScript application. Discord's Embedded App SDK supports web apps embedded in Discord as Activities. It does not turn a desktop-only engine into an Activity automatically; the project needs a compatible web build and hosting configuration.

The translated drafts propose this sequence:

1. Create an application in the Discord Developer Portal.
2. Follow Discord's current Activities setup guide, including the required URL mapping and Activity settings.
3. Add the Embedded App SDK to the web application and implement the initialization and authorization flow described by the current SDK documentation.
4. Test with the intended development audience, then review Discord's current discovery, verification and policy requirements before wider distribution.

The source snippets are illustrative only. In particular, `YOUR_CLIENT_ID` is a placeholder, and the minimal `ready()` example is not a complete production integration. Do not expose application secrets in browser code. The available launch and discovery paths depend on Discord's current verification and distribution rules; directory listing is not assured.

## 3. Source claims and implementation boundary

The drafts' feature names and navigation labels can change. Use Discord's current developer documentation for Activity setup and the current SDK package instructions, rather than treating the translated UI paths as stable. The community route and the embedded-app route can be pursued separately; neither establishes demand, compatibility across all engines, or acceptance into Discord's application directory.

No server, webhook, Discord application, SDK integration, web build or public listing was created as part of this documentation migration.

## References

- Discord, [Introducing the Embedded App SDK](https://support-dev.discord.com/hc/en-us/articles/21204423970071-Introducing-the-Embedded-App-SDK).
- Discord, [Announcement Channel FAQ](https://support.discord.com/hc/en-us/articles/360032008192-Announcement-Channel-FAQ).
- GitHub, [About webhooks](https://docs.github.com/en/webhooks/about-webhooks).

## Source and coverage

The two source files were added together in commit [`7a98dc96b0c9b7f11d19f08c6c62d1d888265d45`](https://github.com/robotics-intelligent-systems/jfxai4mad/commit/7a98dc96b0c9b7f11d19f08c6c62d1d888265d45):

- [`docs/Publicar un motor de videojuegos.txt`](https://github.com/robotics-intelligent-systems/jfxai4mad/blob/7a98dc96b0c9b7f11d19f08c6c62d1d888265d45/docs/Publicar%20un%20motor%20de%20videojuegos.txt) — community/server setup, channel roles, repository notifications and the Activity option.
- [`docs/estrategias principales.txt`](https://github.com/robotics-intelligent-systems/jfxai4mad/blob/7a98dc96b0c9b7f11d19f08c6c62d1d888265d45/docs/estrategias%20principales.txt) — community structure, webhook steps, Activity configuration, SDK example, testing and publication.

Both drafts are represented above. Platform-specific statements have been qualified against selected official documentation; this is not a full implementation or policy review.
