# Tool Calling Rules

## Project Introduction

This project defines a set of rules that constrain how large language models (LLMs) invoke external tools. These rules aim to reduce common issues during tool calling — such as parameter formatting errors, inappropriate tool selection, and inefficient error recovery — thereby improving the accuracy and efficiency of tool calls.

The project contains the following files:

| File | Description |
|------|-------------|
| `toolCallingRulesV0.md` | Initial version of the rules (English) |
| `toolCallingRulesV0CN.md` | Initial version of the rules (Chinese translation) |
| `toolCallingRulesV1CN.md` | Optimized V1 version of the rules (Chinese) |

---

## V1 Optimization Rationale

The V1 version introduces systematic improvements over V0, as detailed below:

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

This project is released under the [GNU Affero General Public License v3.0 (AGPL-3.0)](https://www.gnu.org/licenses/agpl-3.0.html).

AGPL-3.0 is a supplementary version of GPL-3.0. Its core requirements include:

- **Free use and distribution**: Anyone is free to use, modify, and distribute the code of this project.
- **Copyleft**: Any derivative works based on this project must likewise be released under the AGPL-3.0 license.
- **Network interaction clause**: If users interact with modified software based on this project over a network, the modified source code must be made available to those users. This is the key distinction between AGPL and GPL.
- **Source code provision obligation**: When distributing or providing software based on this project over a network, the complete source code must be provided simultaneously.

See the [LICENSE](./LICENSE) file or visit the [AGPL-3.0 official page](https://www.gnu.org/licenses/agpl-3.0.html) for details.
