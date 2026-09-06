# Methodology

## Overview
This study evaluated how two frontier agentic coding systems—**GPT-6 Astra High** and **Gemini 3.8 Flash High**—independently interpreted and executed the exact same long-form product brief to autonomously build a playable 3D AI civilization simulation game: **WHAT IF? Civilization Lab**.

The goal was to examine how agentic systems navigate complex, multi-layered product briefs that demand product judgment, visual composition, 3D graphics, simulation architecture, progressive disclosure, and self-directed quality assurance.

## Evaluated Systems
- **GPT-6 Astra High** (ChatGPT agentic build environment)
- **Gemini 3.8 Flash High** (Google Antigravity environment)

*Note: UI labels reflect the environments used during testing. No claim is made that harnesses, execution sandboxes, or token budgets were equivalent.*

## The Shared Brief
Both agents received the verbatim product specification preserved in [`PROMPT.md`](PROMPT.md). The brief instructed the agent to act as:
> *Lead game engineer, simulation architect, gameplay designer, technical artist, and product designer responsible for building the first playable vertical slice of a potentially commercial premium PC simulation game.*

Key constraints established in the prompt:
1. **Build and Run**: Do not return a mere design document or code snippet; autonomously scaffold, install dependencies, run, visually inspect in-browser, interact, test, debug, and deliver a working browser build.
2. **Distinct Architectural Layers**: Separation between Simulation Core, Rendering Layer (Three.js/WebGL), UI Layer, Content/Data, and AI Adapter.
3. **Emergent History & Memory**: Three distinct civilizations, persistent historical memory, causal history generation ("Why Did This Happen?"), and player interventions ("Change one thing").
4. **Visual Target**: "Modern Stylized Realism" rather than crude low-poly or flat dashboards; world-first composition readable from afar and attractive up close.
5. **Multiple Camera Perspectives**: Global orbit, strategic top-down, settlement inspection, and cinematic observation.

## Execution & First-Run Fairness
- **Autonomous Scaffolding**: Both systems initialized and built their projects independently without human code guidance.
- **No Cross-Pollination**: Neither system was exposed to the other system's code, design decisions, or screenshots during its build.
- **Evaluation Scope**: Analysis is strictly based on the initial delivered vertical slice from this shared brief.

## Manual QA Protocol
Upon delivery, the reviewer conducted hands-on manual QA in the browser:
1. **Playability & Stability**: Verifying that the build loaded, rendered a 3D scene, and maintained an interactive loop.
2. **Camera Perspective Verification**: Actively testing camera controls (global orbit, strategic top-down, close-up settlement framing, cinematic UI toggles) to verify whether viewpoints physically adjusted in 3D space.
3. **Information Hierarchy & UX**: Evaluating whether the interface prioritized world observation or felt overwhelmed by persistent metric panels.
4. **Feature Verification**: Exercising Scenario Lab, Genesis world creation, intervention tools, Chronicle timelines, and comparison screens.
5. **Data Sanity Check**: Observing numerical values across simulated centuries to identify scaling anomalies or runaway counters.

## Evidence Collection
- **High-Resolution Screenshots**: 7 representative captures from each build covering world views, UI panels, scenario tools, and perspectives.
- **Interaction Video Recordings**: Recorded browser sessions testing camera switching, time controls, and UI navigation.
- **Side-by-Side Comparisons**: Direct image comparisons highlighting world staging, intervention framing, and camera responsiveness.

## Separation of Observations and Interpretations
In evaluating the results, this case study strictly delineates:
- **Observed Behaviors (Objective Facts)**: e.g., camera controls failed to change viewport coordinates in the tested Gemini build; Wealth Reserve displayed runaway numbers at Year 117; Astra displayed multi-tier zoom and camera angles; both builds produced running browser simulations.
- **Design & Product Judgments (Qualitative Analysis)**: e.g., Astra's palette feels more restrained and cinematic; Gemini's visual styling evokes an AI-SaaS dashboard; Astra's copywriting feels more player-centric.

## No Artificial Winner Metric
This study intentionally avoids assigning synthetic numeric benchmark scores (e.g., "Astra: 9.2/10, Gemini: 7.8/10"). Reducing multi-dimensional product engineering and design trade-offs to an arbitrary score obscures the nuanced ways agentic models interpret requirements.
