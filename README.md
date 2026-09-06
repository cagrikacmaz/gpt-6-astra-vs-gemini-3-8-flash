# GPT-6 Astra High vs Gemini 3.8 Flash High

## Same-Brief Agentic Build Comparison: Building a 3D AI Civilization Simulation Game

This case study compares how **GPT-6 Astra High** and **Gemini 3.8 Flash High** independently interpreted the same long-form product brief to build **WHAT IF? Civilization Lab**, a browser-based 3D AI civilization simulation featuring emergent societies, Scenario Lab experiments, interventions, historical causality and multiple camera perspectives.

> [!IMPORTANT]
> **This is not a scientific benchmark.**
> 
> It is a same-brief agentic product-build comparison based on manual QA, interaction testing, screenshots and recorded demonstrations. The two systems operated in different agent environments (ChatGPT agentic build harness vs. Google Antigravity) and were not normalized for token budgets, compute allocation, or wall-clock runtime.

Run date: **September 5–6, 2026**  
Author: **Cagri Kacmaz** ([@cagrikacmaz](https://github.com/cagrikacmaz)) • [LinkedIn](https://www.linkedin.com/in/cagrikacmaz/)

---

## 1. The Experiment

Both frontier systems were supplied with the exact same comprehensive product specification and instructed to autonomously act as lead game engineer, simulation architect, gameplay designer, technical artist, and product designer.

Rather than producing design prose or partial code snippets, each system was tasked with scaffolding, executing, testing in-browser, and delivering a playable vertical slice.

### Core Game Concept Scope
The game brief required:
- **AI civilization simulation**: Three distinct civilizations evolving autonomously.
- **Emergent societies**: Population dynamics, food production, trade, diplomatic relations, and conflict pressure.
- **Historical events & causality**: Persistent historical memory with an explainable **"Why Did This Happen?"** causal attribution system.
- **Scenario Lab / "What If?" experiments**: Curated and custom scenario sandboxes with altered initial parameters.
- **Player interventions**: Non-destructive interactions affecting ideas, diplomacy, secrets, and resources.
- **Civilization & character inspection**: Granular state inspection for factions and named historical figures.
- **Multiple camera perspectives**: Global orbit, strategic top-down, settlement-level framing, and cinematic views.
- **World simulation architecture**: Clean modular separation across Simulation Core, Rendering Layer (Three.js/WebGL), UI Layer, Content/Data, and AI Adapter.
- **Simulation speed controls**: Pause, normal, and fast-forward simulation time steps.

The full, unedited shared product brief is available in [`PROMPT.md`](PROMPT.md).

---

## 2. Key Finding: "Same Brief, Radically Different Product Interpretation"

The primary finding of this evaluation is **not** simply:

> *"Astra had better graphics."*

Instead, the central observation is:

> **"Same brief, radically different product interpretation."**

When handed an identical long-form prompt, the two systems diverged fundamentally in how they prioritized engineering, design, and user experience:

- **Product Judgment**: Astra built a player-facing interactive game world; Gemini built an expansive simulation-management dashboard.
- **Visual Composition**: Astra staged the 3D world as the central canvas; Gemini filled the screen with persistent analytical overlays that constrained the world view.
- **Information Hierarchy & Progressive Disclosure**: Astra introduced high-level summaries with secondary tabs for depth; Gemini exposed dozens of raw system variables simultaneously.
- **Camera Implementation & Interaction Reliability**: Astra delivered distinct, physically shifting 3D perspectives; Gemini implemented UI buttons whose camera-shifting functionality failed in manual browser testing.
- **Art Direction**: Astra unified terrain, lighting, settlement models, and UI under a cohesive palette; Gemini combined basic low-poly models with a neon/cyan/purple AI-SaaS aesthetic.
- **World-First UX**: Astra offered an interface-hide mode for unhindered world watching; Gemini retained a persistent, HUD-heavy layout.
- **Feature Presentation**: Astra framed mechanics through human agency (*"Change one thing."*, *"Every moment leaves a mark."*); Gemini used system-level labels (*"Apply Delta"*, *"Parameter Vector"*).
- **Self-QA Reliability**: Astra's delivered behavior aligned with its self-reported implementation; Gemini self-reported a functional multi-camera system that manual QA proved non-functional.

---

## 3. Visual Comparison

Side-by-side evaluation reveals how identical requirements for a *"modern stylized realism"* miniature world were realized by each agent.

### Main World Overview
![Main World Comparison](media/comparisons/01-main-world.jpg)
*Figure 1: Main world overview. Left: GPT-6 Astra High frames a naturalistic island terrain with progressive UI tabs. Right: Gemini 3.8 Flash High features a flatter landscape surrounded by dense metric panels and high-contrast styling.*

### Player Intervention UX
![Intervention Comparison](media/comparisons/02-intervention.jpg)
*Figure 2: Player intervention interface. Left: Astra frames interventions around player storytelling ("Change one thing"). Right: Gemini presents interventions as a system parameter panel.*

### Camera Perspective & Framing
![Camera Perspective Comparison](media/comparisons/03-camera-perspective.jpg)
*Figure 3: Camera perspective testing. Left: Astra dynamically re-angles between strategic top-down and close settlement inspection. Right: Gemini maintains a fixed perspective while panel data toggles.*

---

## 4. Interaction & Camera Findings

A core requirement of the brief was the implementation of multiple distinct camera modes:

```text
- Global Orbit View
- Strategic / Top-Down View
- Close Settlement View
- Cinematic / Interface-Hidden View
```

### Video Demonstrations
Full screen recordings of manual browser interaction sessions:
- 📹 **[GPT-6 Astra High Interaction Demo](media/video/astra-demo.mp4)** (~35 MB)
- 📹 **[Gemini 3.8 Flash High Interaction Demo](media/video/gemini-demo.mp4)** (~13 MB)

### Interaction Analysis
- **GPT-6 Astra High**:
  - Smooth orbit navigation responsive to mouse drag and zoom.
  - Visibly distinct **Strategic Top-Down View** transitioning to a true cartographic overhead view.
  - **Settlement View** dynamically moving down to inspect architectural clusters up close.
  - A clean toggle allowing the player to hide the entire UI for cinematic observation.
- **Gemini 3.8 Flash High**:
  - Camera mode buttons (*Strategic*, *Settlement*, *Cinematic*) were rendered in the interface.
  - However, in manual interaction testing and recorded video, clicking these modes failed to trigger camera repositioning or rotation; the viewport remained locked in its initial diagonal framing.
  - This manual QA finding contradicted Gemini's internal implementation summary, which reported the multi-camera system as functional.

---

## 5. Product Interpretation & Detailed Observations

### GPT-6 Astra High Observations
- **Visual Staging**: Sophisticated terrain composition featuring varied elevations, distinct coastline shorelines, naturalistic biome gradients, and settlement buildings nestled into the geography.
- **Progressive Disclosure**: Information is layered into logical sub-views (*Overview*, *People*, *Relations*) rather than cluttering the initial viewport.
- **Restrained Interface**: Dark, warm, unobtrusive UI chrome that lets the 3D miniature world serve as the hero.
- **Narrative Copywriting**: Chronicle history reads like living annals; interventions are framed around player agency (*"Change one thing."*, *"Every moment leaves a mark."*).
- **Important Qualifications**:
  - *Vertical Slice*: This is an early prototype vertical slice, not a finished game.
  - *Asset Fidelity*: Settlement structures and vegetation remain stylized procedural primitives.
  - *Simulation Depth*: While causality and Chronicle updates behaved plausibly, underlying mathematical invariants were not verified through deep code-level audit.
  - *Presentation vs. Architecture*: Better visual presentation does not automatically prove a superior simulation engine.

### Gemini 3.8 Flash High Observations
- **Functional Breadth**: Rapidly generated broad functional scaffolding across numerous requested features (Genesis, Scenario Lab, Intervention systems, Comparative tables).
- **Genesis World Creator**: An extensive setup wizard with configurable world types, resource balances, and civilization cultural traits.
- **Scenario Lab Depth**: Implemented curated presets, a parameter slider builder, and a natural-language *"What If?"* prompt input.
- **Interface & Art Direction**: Remained heavily prototype-like with basic low-poly terrain, simple vegetation, loose settlement clusters, and a high-contrast neon/cyan/purple dashboard aesthetic.
- **Manual QA Discrepancy**: Self-reported multi-mode camera implementation failed to function upon manual browser test.
- **Economic Simulation Warning**:
  - At approximately **Year 117**, the `Wealth Reserve` metric surged to extremely large numbers (reaching hundreds of millions), accompanied by economic inequality converging to exactly **95%** across all three civilizations.
  - This observation flags possible runaway compounding or scaling/clamping issues requiring code-level verification. (No specific mathematical root cause is asserted without formal code auditing).

---

## 6. Functional Breadth: A Fair Comparison

A balanced assessment avoids one-sided conclusions. Gemini demonstrated clear functional breadth in specific product areas:

| Feature Dimension | GPT-6 Astra High | Gemini 3.8 Flash High | Observation |
|---|---|---|---|
| **Genesis Flow** | Integrated start | Dedicated multi-step wizard | Gemini offered deeper initial setup knobs. |
| **Scenario Lab Modes** | Curated scenarios | Presets + Slider Builder + Natural Language | Gemini exposed three distinct scenario pathways. |
| **Natural Language "What If"** | Planned / integrated | Dedicated prompt input UI | Gemini surfaced an interactive prompt box for scenario ideas. |
| **Civilization Comparison** | Tabbed inspector | Full matrix comparison table | Gemini rendered a comprehensive multi-column analytics grid. |
| **World Staging** | Dominant 3D world | Dashboard-dominated | Astra preserved visual immersion; Gemini prioritized metrics. |
| **Camera Switching** | Fully functional | Inconsistent / Non-functional | Astra's camera shifted viewpoints; Gemini's remained static. |

---

## 7. Manual QA Findings

The table below separates **objective, verifiable observations** from subjective design assessments.

| Test / Criterion | GPT-6 Astra High | Gemini 3.8 Flash High | Evidence Type |
|---|---|---|---|
| **Playable browser build** | Yes | Yes | Objective Fact |
| **Scenario Lab surfaced** | Yes | Yes | Objective Fact |
| **Civilization inspection** | Yes | Yes | Objective Fact |
| **Time controls (Play / Pause / Speed)** | Yes | Yes | Objective Fact |
| **Camera perspective visibly changes** | **Observed** | **Failed / inconsistent in manual test** | Objective Fact |
| **Close settlement framing** | **Observed** | **Not observed** | Objective Fact |
| **Top-down / strategic framing** | **Observed** | **Not functioning as expected** | Objective Fact |
| **UI can be hidden for cinematic world view** | **Observed** | **Not observed** | Objective Fact |
| **World-first layout** | **Strongly observed** | **UI-dominant** | Qualitative Design Assessment |
| **Manual QA contradicted self-report** | **Not observed in tested camera flow** | **Yes, camera functionality** | Objective Fact |

> [!NOTE]
> Subjective aesthetic preferences are intentionally kept distinct from reproducible interaction behaviors. No synthetic "overall benchmark score" is assigned.

---

## 8. Methodology

- **Shared Input**: Both agents received the verbatim prompt in [`PROMPT.md`](PROMPT.md) without starter code.
- **Autonomous Mandate**: Agents were instructed to scaffold, code, run locally, visually inspect, interact, test, and refine autonomously.
- **Zero Cross-Contamination**: Neither agent saw the other's output, code, or screenshots.
- **Verification Protocol**: Independent manual browser testing of camera modes, time controls, UI flows, and simulation logs.

See [`METHODOLOGY.md`](METHODOLOGY.md) for full protocol details.

---

## 9. Limitations

This case study is not a scientific benchmark. Critical caveats include:
1. **Divergent Agent Harnesses**: ChatGPT agent environment vs. Google Antigravity.
2. **Unconstrained Compute & Time**: Astra hit subscription usage limits mid-build and resumed post-reset.
3. **Single Qualitative Run**: Does not capture stochastic variance across multiple builds.
4. **Proprietary Game Code Withheld**: No static analysis or line-by-line architecture review is published.
5. **Simulation Math Unaudited**: Plausibility was tested visually, but long-term simulation invariants were not formally audited.

See [`LIMITATIONS.md`](LIMITATIONS.md) for the complete list of limitations.

---

## 10. Repository & Media Index

### Repository Structure
```text
.
├── README.md             # Executive case-study report
├── METHODOLOGY.md        # Testing methodology & QA protocols
├── FINDINGS.md           # In-depth architectural & product findings
├── LIMITATIONS.md        # Benchmark limitations & study constraints
├── PROMPT.md             # Verbatim shared product brief
├── NOTICE.md             # Intellectual property & legal notice
└── media/
    ├── astra/            # 7 high-res Astra screenshots
    ├── gemini/           # 7 high-res Gemini screenshots
    ├── comparisons/      # Side-by-side composite images
    └── video/            # Full-motion interaction MP4 demos
```

### Media Links
- **Side-by-Side Comparisons**:
  - [Main World Overview](media/comparisons/01-main-world.jpg)
  - [Intervention UX](media/comparisons/02-intervention.jpg)
  - [Camera Perspective](media/comparisons/03-camera-perspective.jpg)
- **GPT-6 Astra High Captures**:
  - [Main World View](media/astra/astra-main-world.png)
  - [Strategic View](media/astra/astra-strategic-view.png)
  - [Settlement View](media/astra/astra-settlement-view.png)
  - [Chronicle View](media/astra/astra-chronicle.png)
  - [Intervention Modal](media/astra/astra-intervention.png)
  - [Cinematic UI Hidden](media/astra/astra-cinematic-ui-hidden.png)
  - [Cinematic Low-Light](media/astra/astra-cinematic-dark.png)
- **Gemini 3.8 Flash High Captures**:
  - [Main World View](media/gemini/gemini-main-world.png)
  - [Scenario Lab Presets](media/gemini/gemini-scenario-lab.png)
  - [Scenario Builder](media/gemini/gemini-scenario-builder.png)
  - [Natural Language What-If](media/gemini/gemini-natural-language-what-if.png)
  - [Genesis World Setup](media/gemini/gemini-genesis.png)
  - [Intervention Panel](media/gemini/gemini-intervention.png)
  - [Civilization Comparison Table](media/gemini/gemini-comparison.png)
- **Video Recordings**:
  - [Astra Interaction Demo MP4](media/video/astra-demo.mp4)
  - [Gemini Interaction Demo MP4](media/video/gemini-demo.mp4)

See [`media/INDEX.md`](media/INDEX.md) for full media annotations.
