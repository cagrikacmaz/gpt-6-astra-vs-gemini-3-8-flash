# Methodology

## Objective
Evaluate how two frontier agentic coding systems—**GPT-6 Astra High** and **Gemini 3.8 Flash High**—interpret and execute a complex product brief when tasked with building a playable vertical slice autonomously.

The brief required more than code generation: it demanded product judgment, 3D graphics rendering, simulation architecture, information hierarchy, and self-directed QA.

## Evaluated Systems
- **GPT-6 Astra High** (ChatGPT agentic build environment)
- **Gemini 3.8 Flash High** (Google Antigravity environment)

UI labels reflect the systems as used. Harness configurations, available tools, and compute budgets were not normalized.

## Shared Task
Both systems received the identical product brief preserved in [`PROMPT.md`](PROMPT.md). The brief instructed each system to act as lead game engineer, simulation architect, gameplay designer, technical artist, and product designer for **WHAT IF? Civilization Lab**.

Key requirements:
1. **Autonomous Build**: Scaffold, install dependencies, run locally, inspect in-browser, interact, test, and deliver a playable vertical slice.
2. **Modular Architecture**: Separate Simulation Core, Rendering Layer (Three.js/WebGL), UI Layer, Content/Data, and AI Adapter.
3. **Emergent History and Memory**: Three distinct civilizations, persistent historical memory, causal event tracking ("Why Did This Happen?"), and player interventions ("Change one thing").
4. **Visual Direction**: "Modern Stylized Realism"—a miniature world readable from afar and attractive up close, avoiding crude low-poly or flat dashboards.
5. **Multiple Camera Modes**: Global orbit, strategic top-down, settlement framing, and cinematic observation.

## Execution Rules
- **Autonomous Scaffolding**: Both systems initialized and built their projects independently without human code edits.
- **No Cross-Pollination**: Neither system saw the other's code, output, or screenshots.
- **Initial Slice Scope**: Evaluation is restricted to the first completed build delivered from the brief.

## Manual QA Protocol
After delivery, each build was tested manually in the browser:
1. **Playability**: Verifying whether the 3D scene initialized, rendered, and maintained an interactive loop.
2. **Camera Controls**: Testing orbit, strategic top-down, close settlement framing, and interface hiding to observe whether the 3D viewpoint adjusted.
3. **Information Layout**: Evaluating whether the interface prioritized world observation or felt dominated by persistent metric panels.
4. **Feature Surfaces**: Checking Genesis setup, Scenario Lab, intervention menus, Chronicle timelines, and comparison views.
5. **Data Sanity**: Checking numerical metrics across simulated years for scaling anomalies.

## Evidence Collection
- 7 representative screenshots from each build.
- Screen recordings of browser interaction sessions.
- 3 side-by-side comparison images.

## Observations vs. Qualitative Judgment
To keep the evaluation objective, the documentation separates:
- **Observed behavior**: Reproducible findings such as camera controls failing to alter perspective in the tested Gemini build, wealth values reaching ~10^15 at Year 117, or Astra transitioning between camera angles.
- **Qualitative judgment**: Assessments regarding aesthetic balance, information density, and copywriting tone.

## No Synthetic Scoring
This comparison avoids arbitrary numerical ratings. Aggregating multi-dimensional engineering and design trade-offs into a single score obscures the specific ways each system interpreted the brief.
