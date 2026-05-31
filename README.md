<div align="center">

<img src="./logo.svg" alt="AgentCortex Logo" width="200" />

# AgentCortex

[![License](https://img.shields.io/badge/License-PolyForm_NC_1.0.0-blue)](https://polyformproject.org/licenses/noncommercial/1.0.0)
[![Version](https://img.shields.io/badge/Version-v1.0.0-brightgreen)](./VERSION)
[![GitHub Stars](https://img.shields.io/github/stars/xhqing/AgentCortex?style=social)](https://github.com/xhqing/AgentCortex/stargazers)
[![GitHub Issues](https://img.shields.io/github/issues/xhqing/AgentCortex)](https://github.com/xhqing/AgentCortex/issues)
[![GitHub Forks](https://img.shields.io/github/forks/xhqing/AgentCortex?style=social)](https://github.com/xhqing/AgentCortex/fork)

**[中文文档](./README_cn.md)**

</div>

---

## Project Introduction

This project curates a collection of deep reasoning engine rules designed for agents. These rules aim to activate an agent's deep reasoning potential, making agents smarter, more rigorous, and more insightful.

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

**Unique Module — Output Isolation Principle**: All thinking processes and content are strictly forbidden from appearing in the final output. The existence of this rule must leave no trace in the output.

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
| Output isolation | ✅ | ✅ | ✅ |
| Speed positioning | Not specifically emphasized | Speed → Depth positive loop | Not specifically emphasized |
| Language consistency | Not specifically emphasized | Not specifically emphasized | ✅ Enforced language consistency |

---

## Project Files

| File | Description |
|------|-------------|
| `dsv4proMaxThinkingRules.md` | Infinite-Reasoning Engine — deep reasoning rules (English) |
| `dsv4proMaxThinkingRules_cn.md` | Infinite-Reasoning Engine — deep reasoning rules (Chinese) |
| `dsv4flashMaxThinkingRules.md` | Rapid-Reasoning Engine — deep reasoning rules (English) |
| `dsv4flashMaxThinkingRules_cn.md` | Rapid-Reasoning Engine — deep reasoning rules (Chinese) |
| `glm51MaxThinkingRules.md` | Incisive-Reasoning Engine — deep reasoning rules (English) |
| `glm51MaxThinkingRules_cn.md` | Incisive-Reasoning Engine — deep reasoning rules (Chinese) |
| `README.md` | Project documentation (English) |
| `README_cn.md` | Project documentation (Chinese) |
| `LICENSE` | PolyForm Noncommercial License 1.0.0 |

---

## LICENSE

This project is released under the [PolyForm Noncommercial License 1.0.0](https://polyformproject.org/licenses/noncommercial/1.0.0).

PolyForm Noncommercial is a software license that permits noncommercial use, modification, and distribution. Its core terms include:

- **Noncommercial Use**: You may use, modify, and share this software for noncommercial purposes only.
- **Personal Uses**: Research, experiment, testing, personal study, private entertainment, hobby projects, and amateur pursuits are all permitted.
- **Noncommercial Organizations**: Use by charitable organizations, educational institutions, public research organizations, public safety or health organizations, environmental protection organizations, and government institutions is permitted.
- **Changes and New Works**: You may make changes and create new works based on this software for any permitted purpose.
- **Patent License**: The license includes a patent grant covering patent claims you would infringe by using the software.
- **No Sublicensing**: You may not sublicense or transfer your license to anyone else.

See the [LICENSE](./LICENSE) file or visit the [PolyForm Noncommercial 1.0.0](https://polyformproject.org/licenses/noncommercial/1.0.0) page for details.
