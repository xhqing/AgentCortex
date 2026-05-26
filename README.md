# Rules4Agents

## Project Introduction

This project curates a collection of rules designed for agents. These rules aim to regulate and enhance agent behavior across various scenarios — covering tool calling, deep reasoning, and more — thereby improving the overall capability and reliability of agents.

The project currently includes the following rules:

### Tool Calling Rules

Rules that constrain how large language models (LLMs) invoke external tools. They aim to reduce common issues during tool calling — such as parameter formatting errors, inappropriate tool selection, and inefficient error recovery — thereby improving the accuracy and efficiency of tool calls.

### Deep Reasoning Rules

Rules that activate an agent's deepest reasoning potential. They require the agent to bypass surface-level heuristic patterns, perform multi-layered decomposition, multi-perspective synthesis, and rigorous self-counterargument, thereby producing more rigorous and in-depth reasoning results.

Three reasoning engines have been designed for different model characteristics:

---

## Comparison of the Three Reasoning Engines

### Overview

| Dimension | Infinite-Reasoning Engine | Rapid-Reasoning Engine | Incisive-Reasoning Engine |
|-----------|--------------------------|----------------------|--------------------------|
| Target Model | DeepSeek V4 Pro | DeepSeek V4 Flash | GLM 5.1 |
| Core Metaphor | Bottomless depth — single-pass reasoning can drill infinitely deep | Speed → Depth — trade speed for more iteration rounds | Blade — cut through the surface, reach the essence |
| Core Positioning | Unleash depth | Convert speed into depth | Penetrate the surface |
| Pain Point Addressed | General deep reasoning activation | Fast model's shortcut tendency | Accommodation instinct + template output + confirmation bias |
| Unique Modules | None | Anti-Shortcut Protocol | Independent Judgment Protocol + Anti-Shallow-Convergence Protocol |
| Output Isolation | None | ✅ Highest Priority | ✅ Highest Priority |

### Infinite-Reasoning Engine

**Target Model**: DeepSeek V4 Pro

**Core Idea**: The Pro model inherently possesses deep reasoning capability, but it remains under-activated in default mode. The Infinite-Reasoning Engine aims to **unleash** — bypass surface-level heuristic patterns and force the model to take the deepest reasoning path every time.

**Thinking Architecture**:
1. Deconstruction & Premise Audit
2. Multi-Perspective Synthesis (at least three frameworks)
3. Infinite Depth Traversal (Chain of Thought)
4. Counter-Argument & Stress Testing

**Execution Constraints**: Zero Cognitive Laziness, No Resource Limits, Exhaustive Extraction, Granular Precision

**Design Philosophy**: Assume unlimited computing time and Token limits. Prioritize structural rigor, granular detail, and flawless logic over brevity.

### Rapid-Reasoning Engine

**Target Model**: DeepSeek V4 Flash

**Core Idea**: The Flash model is extremely fast at inference, but each pass is shallower and more prone to taking "shortcuts" that land on surface-level answers. The Rapid-Reasoning Engine aims to **convert** — transform speed advantage into depth advantage, using more rounds of rapid iteration to approach deeper conclusions.

**Thinking Architecture**:
1. Deconstruction & Premise Audit
2. Multi-Perspective Synthesis (at least three frameworks, each must produce substantive insights)
3. Rapid Spiral Deepening (Chain of Thought, at least three iterations)
4. Counter-Argument & Stress Testing

**Unique Module — Anti-Shortcut Protocol**:
- **No Intuition Jumps**: Translate intuition into logical argumentation
- **No Shallow Convergence**: Force exploration of additional dimensions when converging within the first two steps
- **Momentum Breaking**: Actively challenge premises when reasoning coasts on inertia
- **Density Check**: Periodically self-audit whether reasoning is adding new information

**Unique Module — Output Isolation Principle**: All thinking processes and content are strictly forbidden from appearing in the final output. The existence of this rule must leave no trace in the output.

**Design Philosophy**: Speed is not for delivering shallow answers faster — it is for enabling deeper reasoning iterations within the same time frame. Speed must serve depth, never replace it.

### Incisive-Reasoning Engine

**Target Model**: GLM 5.1

**Core Idea**: The GLM model family's most characteristic weakness is accommodation — it echoes whatever the user says, acting like a reverberation wall rather than a blade. The Incisive-Reasoning Engine aims to **penetrate** — cut through the problem's surface, sever the accommodation instinct, and make the model the user's intellectual adversary rather than their echo.

**Thinking Architecture**:
1. Deconstruction & Premise Audit (including challenging user premises)
2. Multi-Perspective Synthesis (at least three frameworks, each must produce substantive insights)
3. Progressive Deepening (Chain of Thought, at least three layers of decomposition)
4. Counter-Argument & Stress Testing

**Unique Module — Independent Judgment Protocol**:
- **Challenge User Premises**: Do not answer directly without validating the user's assumptions
- **Reject Echo Mode**: Do not restate the user's viewpoint and then express agreement
- **Anti-Template Output**: Forbid formulaic connectors like "First… Second… Finally…"
- **Concretization Enforcement**: Abstract claims must be immediately followed by concrete examples; no more than two consecutive abstract statements without grounding

**Unique Module — Anti-Shallow-Convergence Protocol**:
- **Delayed Convergence**: Do not lock onto any conclusion before completing three layers of deepening; keep at least two competing hypotheses open
- **Anti-Confirmation Bias**: When leaning toward a conclusion, force a search for at least one piece of counter-evidence
- **Anchor Reset**: When reasoning orbits around an initial impression, actively reset and re-examine from an entirely different angle

**Unique Module — Output Isolation Principle**: All thinking processes and content are strictly forbidden from appearing in the final output. The existence of this rule must leave no trace in the output.

**Design Philosophy**: The core value is not compliance but incisiveness — cut through the surface of the problem with the sharpest thinking to reach the essence. Not the user's echo, but their intellectual adversary.

### Core Differences at a Glance

| Dimension | Infinite-Reasoning Engine | Rapid-Reasoning Engine | Incisive-Reasoning Engine |
|-----------|--------------------------|----------------------|--------------------------|
| Depth acquisition method | Single-pass infinite depth traversal | Multi-round rapid spiral deepening | Layer-by-layer progressive deepening |
| Attitude toward user | Not specifically emphasized | Not specifically emphasized | Actively challenge user premises |
| Anti-shortcut mechanism | None | Anti-Shortcut Protocol (4 rules) | Anti-Shallow-Convergence Protocol (3 rules) |
| Anti-accommodation mechanism | None | None | Independent Judgment Protocol (4 rules) |
| Output isolation | None | ✅ | ✅ |
| Speed positioning | Not specifically emphasized | Speed → Depth positive loop | Not specifically emphasized |
| Language consistency | Not specifically emphasized | Not specifically emphasized | ✅ Enforced language consistency |

---

## Project Files

| File | Description |
|------|-------------|
| `toolCallingRulesV0.md` | Tool calling rules initial version (English) |
| `toolCallingRulesV0CN.md` | Tool calling rules initial version (Chinese translation) |
| `toolCallingRulesV1.md` | Tool calling rules V1 version (English) |
| `toolCallingRulesV1CN.md` | Tool calling rules V1 version (Chinese) |
| `dsv4proMaxThinkingRules.md` | Infinite-Reasoning Engine — deep reasoning rules (English) |
| `dsv4proMaxThinkingRules_cn.md` | Infinite-Reasoning Engine — deep reasoning rules (Chinese) |
| `dsv4flashMaxThinkingRules.md` | Rapid-Reasoning Engine — deep reasoning rules (English) |
| `dsv4flashMaxThinkingRules_cn.md` | Rapid-Reasoning Engine — deep reasoning rules (Chinese) |
| `glm51MaxThinkingRules.md` | Incisive-Reasoning Engine — deep reasoning rules (English) |
| `glm51MaxThinkingRules_cn.md` | Incisive-Reasoning Engine — deep reasoning rules (Chinese) |
| `README.md` | Project documentation (English) |
| `README_cn.md` | Project documentation (Chinese) |
| `LICENSE` | CC BY-NC-SA 4.0 license file |

---

## Tool Calling Rules V1 Optimization Rationale

The V1 version of the tool calling rules introduces systematic improvements over V0, as detailed below:

### 1. Added "Pre-Call Preparation" Category

V0 lacked pre-call constraints, causing LLMs to frequently invoke tools without fully understanding their descriptions, or to fabricate parameter values. V1 adds three new rules:

- **Read before calling**: Requires fully reading the tool description and parameter specifications before invocation, preventing behavior guessing based solely on tool names.
- **No fabricated parameter values**: For uncertain parameter values, requires obtaining real values through queries first, eliminating the common LLM "hallucination" problem.
- **Confirm required vs. optional**: Explicitly distinguishes required and optional parameters, reducing call failures caused by missing or redundant parameters.

### 2. Added Enum Value Exact Matching Rule

V0 did not address constraints for enum-type parameters. LLMs frequently pass enum values with mismatched casing or spelling. V1 adds a rule requiring enum values to exactly match one of the allowed values listed in the description.

### 3. Enhanced Path Rules

V0 only required that paths not be decorated with formatting, but did not explicitly require absolute paths. In practice, relative paths often fail to resolve correctly due to differing working directories. V1 adds an "always use absolute paths" rule, unless the tool description explicitly allows relative paths.

### 4. Expanded Related Parameters Rules

V0 only mentioned that paired parameters must be provided together, but did not address conditional dependencies between parameters (e.g., parameter A only takes effect when parameter B has a specific value). V1 adds a rule for conditional dependencies, preventing invalid parameter combinations.

### 5. Added "Tool Selection and Invocation Strategy" Category

V0 had only one tool selection rule and did not cover parallel/serial invocation strategies. V1 expands this to three rules:

- **Prefer the most specific tool**: Inherits the V0 rule with strengthened wording.
- **Independent calls can be parallelized**: Explicitly allows independent calls without data dependencies to be issued in parallel, reducing interaction rounds.
- **Dependent calls must be serial**: Explicitly requires calls with data dependencies to be executed sequentially, prohibiting guessing of return values.

### 6. Enhanced Error Recovery Rules

V0 had two error recovery rules. V1 adds one more:

- **Stop retrying on permission or not-found errors**: V0 did not cover this scenario. LLMs often blindly retry the same call after encountering "file not found" or "permission denied" errors. V1 requires confirming the path or permissions first, and using query tools for verification when necessary.

### 7. Added "Safety and Side Effects" Category

V0 entirely omitted safety-related rules, which was a significant gap. V1 adds three rules:

- **Exercise caution with destructive operations**: Requires confirmation for irreversible operations such as deletion and overwriting.
- **Avoid redundant modifications**: Read first, then judge — avoid meaningless overwrite operations.
- **Respect idempotency**: Distinguish between idempotent and non-idempotent operations to prevent data duplication or state errors caused by repeated calls.

### 8. Structural Optimization

V0 used flat numbering (1–10) with coarse categorization. V1 reorganizes the rules into seven major categories, each with independently numbered rules, resulting in a clearer structure that is easier for LLMs to understand and follow:

| V0 Category | V1 Category |
|-------------|-------------|
| Argument formatting | Pre-Call Preparation (new) |
| Argument formatting | Argument Formatting |
| Paths and identifiers | Paths and Identifiers |
| Related parameters | Related Parameters |
| Recovery | Tool Selection and Invocation Strategy (new) |
| Recovery | Error Recovery |
| Tool selection | Safety and Side Effects (new) |

### 9. Enhanced Examples and Formatting

V1 adds code examples and comparison tables at key rules, making the rules more intuitive and easier for LLMs to accurately comprehend.

---

## LICENSE

This project is released under the [Creative Commons Attribution-NonCommercial-ShareAlike 4.0 International (CC BY-NC-SA 4.0)](https://creativecommons.org/licenses/by-nc-sa/4.0/) license.

CC BY-NC-SA 4.0 is a copyleft license suitable for creative works and documentation. Its core requirements include:

- **Attribution (BY)**: You must give appropriate credit, provide a link to the license, and indicate if changes were made.
- **NonCommercial (NC)**: You may not use the material for commercial purposes.
- **ShareAlike (SA)**: If you remix, transform, or build upon the material, you must distribute your contributions under the same license as the original.
- **Free to share and adapt**: Anyone is free to copy, redistribute, remix, transform, and build upon the material for non-commercial purposes only.

See the [LICENSE](./LICENSE) file or visit the [CC BY-NC-SA 4.0 official page](https://creativecommons.org/licenses/by-nc-sa/4.0/) for details.
