# Rules4Agents

## Project Introduction

This project curates a collection of rules designed for agents. These rules aim to regulate and enhance agent behavior across various scenarios — covering tool calling, deep reasoning, and more — thereby improving the overall capability and reliability of agents.

The project currently includes the following rules:

### Tool Calling Rules

Rules that constrain how large language models (LLMs) invoke external tools. They aim to reduce common issues during tool calling — such as parameter formatting errors, inappropriate tool selection, and inefficient error recovery — thereby improving the accuracy and efficiency of tool calls.

### Deep Reasoning Rules

Rules that activate an agent's deepest reasoning potential. They require the agent to bypass surface-level heuristic patterns, perform multi-layered decomposition, multi-perspective synthesis, and rigorous self-counterargument, thereby producing more rigorous and in-depth reasoning results.

---

## Project Files

| File | Description |
|------|-------------|
| `toolCallingRulesV0.md` | Tool calling rules initial version (English) |
| `toolCallingRulesV0CN.md` | Tool calling rules initial version (Chinese translation) |
| `toolCallingRulesV1.md` | Tool calling rules V1 version (English) |
| `toolCallingRulesV1CN.md` | Tool calling rules V1 version (Chinese) |
| `dsv4proMaxThinkingRules.md` | Deep reasoning rules (English) |
| `dsv4proMaxThinkingRules_cn.md` | Deep reasoning rules (Chinese) |
| `README.md` | Project documentation (English) |
| `README_cn.md` | Project documentation (Chinese) |
| `LICENSE` | CC BY-SA 4.0 license file |

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

This project is released under the [Creative Commons Attribution-ShareAlike 4.0 International (CC BY-SA 4.0)](https://creativecommons.org/licenses/by-sa/4.0/) license.

CC BY-SA 4.0 is a copyleft license suitable for creative works and documentation. Its core requirements include:

- **Attribution (BY)**: You must give appropriate credit, provide a link to the license, and indicate if changes were made.
- **ShareAlike (SA)**: If you remix, transform, or build upon the material, you must distribute your contributions under the same license as the original.
- **Free to share and adapt**: Anyone is free to copy, redistribute, remix, transform, and build upon the material for any purpose, even commercially.

See the [LICENSE](./LICENSE) file or visit the [CC BY-SA 4.0 official page](https://creativecommons.org/licenses/by-sa/4.0/) for details.
