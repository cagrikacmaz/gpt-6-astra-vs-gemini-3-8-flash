# Limitations

This repository documents a qualitative comparison under a shared product brief. It is not a controlled scientific benchmark and should not be used to claim universal model superiority.

## 1. Divergent Agent Harnesses
The models ran in different product harnesses with different toolsets:
- **GPT-6 Astra High** ran in ChatGPT's agentic build environment.
- **Gemini 3.8 Flash High** ran in Google Antigravity.

Differences in tool implementations, browser automation, system prompts, file management, and context window handling directly affected execution.

## 2. Unnormalized Compute and Time
Compute resources, token budgets, and runtime duration were not controlled:
- GPT-6 Astra High reached plan usage limits mid-build and resumed after a quota reset.
- Sampling parameters, internal retries, and reasoning budgets were managed by the respective platforms rather than a standardized harness.

## 3. Single Qualitative Run
Each build represents a single qualitative run. Autonomous agent behavior varies between runs; this vertical slice does not characterize the full distribution of either system's capabilities.

## 4. Subjective vs. Reproducible Evidence
Interaction results (such as whether the camera perspective shifted when buttons were clicked) are directly reproducible from the recorded sessions. Aesthetic assessments—including art direction, layout balance, and color palette—reflect qualitative engineering judgment.

## 5. Reviewer Context
The reviewer evaluated both builds with knowledge of which model produced each artifact. No blinded evaluation protocol was applied.

## 6. Simulation Correctness Was Not Formally Audited
Visual activity and Chronicle entries were manually observed, but long-term economic and demographic invariants were not verified through formal code audits. Apparent plausibility in a brief test session does not guarantee mathematical stability or simulation depth.

## 7. Proprietary Code Withheld
Because the underlying game source code is not public, this comparison does not evaluate line-by-line code architecture, test coverage, or runtime profiling.

## 8. Fictional Simulation Domain
The product brief specifies a fictional civilization simulation. Societal behaviors, historical events, and ideological developments are game mechanics and do not model real-world political or historical dynamics.
