# Limitations

This case study documents a real-world, same-brief product-build comparison. It is explicitly **not** a controlled scientific benchmark, and should not be used to assert universal model superiority.

## 1. Uncontrolled Agent Harnesses & Tooling
The two models operated within entirely different agent environments and runtime harnesses:
- **GPT-6 Astra High** operated within ChatGPT's agentic build environment.
- **Gemini 3.8 Flash High** operated within Google Antigravity.

Differences in tool implementations, browser-automation harnesses, hidden system instructions, file-system interaction mechanisms, and context-window management directly affect autonomous execution.

## 2. Unnormalized Compute, Token Budgets, and Time
The systems were not constrained to identical token counts, compute budgets, or wall-clock execution limits. 
- GPT-6 Astra High reached the user's plan usage limit during the build process and was resumed after quota reset.
- Execution speed, retry policies, model sampling parameters, and reasoning budgets were determined by the respective platforms rather than a standardized benchmark protocol.

## 3. Single-Run Sample Size
Each system's output represents a single qualitative product-generation run. Autonomous agent behavior exhibits stochastic variance across runs; a single vertical slice does not represent the entire distribution of potential outcomes.

## 4. Subjective Design Judgments vs. Objective QA
While interaction flaws (such as non-responsive camera perspective shifts) are directly observable facts, evaluations of art direction, aesthetic taste, typography, and visual hierarchy necessarily involve qualitative human judgment.

## 5. Absence of Blinded Review
The reviewer was aware of which model produced which build during interaction testing, screenshot capture, and qualitative analysis.

## 6. Simulation Correctness Remains Open
Neither build underwent an exhaustive code-level simulation audit for long-run economic or demographic equilibrium. While visual plausibility and immediate causal feedback were tested, deeper state correctness (such as runaway compounding or invariant violations) requires dedicated formal verification.

## 7. Proprietary Source Code Excluded
Because the commercial game source code is withheld, this public repository does not evaluate lines of code, static analysis lints, architectural unit-test coverage, or runtime profiling data.

## 8. Fictional Simulation Domain
The product brief specifies a fictional civilization simulation. Societal behaviors, historical events, and ideological developments are game mechanics and should not be interpreted as models of real-world historical or political phenomena.
