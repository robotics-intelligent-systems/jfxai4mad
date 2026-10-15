# Interactive Scientific Simulations in WebGL

[Documentation index](../../README.md) · [Interactive demo plan](../../business/interactive-demo-b2b-conversion-and-sandbox-plan.md) · [KVM sandbox plan](../../architecture/kvm-hosting-ephemeral-demo-sandbox.md)

## Purpose and evidence status

This note consolidates the supplemental Spanish source, `docs/Las simulaciones científicas.txt`. It evaluates WebGL as one possible browser technology for interactive scientific visualizations and simulations, and translates the source's examples into a bounded project concept.

The source is an overview, not a design specification or evidence that a particular model runs in a browser. No simulation, benchmark, lesson, GPU workload, or mobile-device test was supplied or performed. Claims about millions of particles, 60 frames per second, “universal” access, and improved learning are not accepted as general guarantees.

## 1. What WebGL does

[WebGL](https://developer.mozilla.org/en-US/docs/Web/API/WebGL_API) is a JavaScript API for rendering interactive 2D and 3D graphics in an HTML canvas, based on OpenGL ES. JavaScript controls the application and supplies data; GLSL shaders run on the graphics pipeline. A compatible browser and device may use hardware acceleration, but available performance and features vary by browser, operating system, driver and GPU.

WebGL is primarily a graphics API, not a general-purpose compute interface with compute shaders. Some numerical techniques can be expressed through shader passes and textures, but they have constraints and need validation against a CPU reference. If general GPU compute is central, assess [WebGPU](https://developer.mozilla.org/en-US/docs/Web/API/WebGPU_API) as a separate option: it adds compute capabilities, but MDN still marks it as limited availability and it requires a secure context in supported browsers.

## 2. Appropriate uses and limits

Potential project uses include interactive geometry, molecular or spatial viewers, fields, trajectories, and explanatory visual models. The [NGL Viewer](https://nglviewer.org/ngl/api/manual/) is a concrete WebGL-based molecular-structure viewer. It is an example of browser visualization, not evidence that every molecular workload or scientific model is suitable for WebGL.

Rendering a plausible picture does not validate the underlying science. A simulation needs an explicit model, units, boundary and initial conditions, numerical method, error checks, and comparison with analytical results or a trusted reference where available. Keep visualization, numerical solver and scientific interpretation distinct in the design and documentation.

The source's claims of “millions” of simultaneous particles and 60 frames per second are workload-dependent targets, not WebGL capabilities that can be promised in advance. Data transfer, shader complexity, resolution, memory, thermal limits and the user's device all affect results. Establish representative scenarios and measure them on a named browser/device matrix.

## 3. Candidate tools

| Tool | Candidate role | Qualification |
| --- | --- | --- |
| [Three.js](https://threejs.org/docs/pages/WebGLRenderer.html) | Higher-level 3D scenes, camera, materials and rendering | Its WebGL renderer requires WebGL 2; check current library documentation and supported-device needs. |
| [Babylon.js](https://doc.babylonjs.com/) | 3D applications and interactive scenes | Select modules and physics integrations against the actual use case; a framework does not validate a scientific model. |
| regl or TWGL | Lower-level WebGL setup and custom shader workflows | Useful when direct control matters; confirm current maintenance, browser requirements and license before selection. |
| [D3](https://d3js.org/) | Data transformations, scales and 2D visualization | Can complement a WebGL view; it is not itself a WebGL rendering engine. |

The list is a shortlist from the source, not a comparative evaluation or project technology decision. Before selection, prototype the smallest representative scene, confirm accessibility and export requirements, and review current project maintenance and licensing.

## 4. Numerical precision and device compatibility

WebGL shader calculations commonly use floating-point formats whose precision and availability differ from JavaScript's Number type. JavaScript Number uses binary64 semantics, while common GPU shader paths use 32-bit floats; available shader precision and renderable texture formats are device-dependent. See [MDN's WebGL best practices](https://developer.mozilla.org/en-US/docs/Web/API/WebGL_API/WebGL_best_practices) and [extension guidance](https://developer.mozilla.org/en-US/docs/Web/API/WebGL_API/Using_Extensions).

This difference can matter for large coordinate ranges, long integrations, small increments, cancellation and unstable systems. Do not infer suitability for astrophysical, quantum, fluid or other demanding calculations from the graphics API alone. Specify acceptable error, test precision-sensitive cases, and use a CPU or validated server-side solver when the browser implementation cannot meet the tolerance.

WebGL support is widespread but not universal across every device/configuration, and GPU access may be disabled or constrained. Provide a clear fallback (static/2D view, reduced-detail mode, or explanatory message), handle context loss, and test target browsers and lower-powered devices. “Runs in a browser” does not guarantee no installation, offline access, mobile compatibility or equal performance.

## 5. Educational and project evaluation

PhET describes its simulations as HTML5 and research-based, with design principles such as interactivity and multiple representations; its documentation does not establish that all PhET simulations use WebGL. Use PhET as an example of an educational simulation program, not as proof of a particular rendering technology or a causal learning effect. See [PhET about and design](https://phet.colorado.edu/en/about) and [current system requirements](https://phet.colorado.edu/cs/help-center/running-sims).

For a project prototype, define a single learning or demonstration objective, one user task, the scientific model, and its validation evidence before choosing the rendering stack. Evaluate task completion, comprehension or model interpretation with an appropriate study design; interaction counts or frame rate alone are not learning outcomes.

## Proposed next step

Specify one browser-based digital-twin or scientific visualization scenario already contemplated by the [interactive demo plan](../../business/interactive-demo-b2b-conversion-and-sandbox-plan.md). Document inputs, units, equations or reference data, acceptable numerical error, expected device/browser coverage, fallback behavior, and one measurable task. Then compare a browser-rendered view with the existing synthetic-data demo plan; do not assume that WebGL moves ROS 2, Gazebo or solver execution into the browser.

No performance or learning claim should be published until that scenario is implemented and measured. WebGL rendering, WebGPU compute, headless simulation and remote 3D streaming are distinct workload choices; the hosting note's VPS sizing does not establish GPU availability or simulation capacity.

## Source and coverage

Original: [Las simulaciones científicas.txt](https://github.com/robotics-intelligent-systems/jfxai4mad/blob/21ae9fadeaf372def3f6f80f6a60ef4489f31eec/docs/Las%20simulaciones%20cient%C3%ADficas.txt). Source commit: `21ae9fadeaf372def3f6f80f6a60ef4489f31eec`; Git blob: `0a203b1fe333cf77754ec9b4bcfc289ddfb43fc9`.

Coverage includes the definition and proposed scientific uses of WebGL, claimed accessibility and performance benefits, the named libraries, molecular/astronomical/fluid examples, numerical precision, device limitations and WebGPU. Claims are qualified or reframed where the source supplied no benchmark or supporting evidence. The working TXT is removed in this migration; Git history preserves the original.
