# Changelog

All notable changes to the AgentCortex project will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/), and this project adheres to [Semantic Versioning](https://semver.org/).

## [Unreleased]

### Changed
- Changed project license from PolyForm Noncommercial License 1.0.0 to MIT License: open up the project for commercial use and redistribution, making it easier to promote and adopt. Updated LICENSE.md to the MIT License text; synced the license badge, file table, and LICENSE section in README.md and README_cn.md; simplified the contribution licensing section in CONTRIBUTING.md and CONTRIBUTING_cn.md (the noncommercial restrictions, patent clause, and extra commercial grant to maintainers are no longer needed under MIT)
- Enhanced the LLM-as-Judge evaluation plan (`.trae/documents/evaluation-plan/llm-as-judge-evaluation-plan.md`) to make the evaluation of the Rapid-Reasoning Engine statistically sound and budgeted: added an evaluation condition baseline enforcing the same "max reasoning effort" (reasoning_effort=max, temperature=1.0, top_p=0.95) for both experimental and control groups so the engine rule is the only variable (motivated by DeepSeek-V4-Flash-0731's built-in max-level deep reasoning, which would otherwise confound the attribution); added sample-size planning (12/30/60 tiers with Cohen's dz power analysis and Wilcoxon/t-test decision criteria); added length-bias control (answer_tokens covariate, explicit judge rule, and matched-length robustness check) since the engine's exhaustive-extraction rules systematically lengthen answers; added a budget estimation section based on official DeepSeek-V4-Flash-0731 API pricing (input $0.14/M cache-miss, output $0.28/M), estimating ~$0.03 for a minimal 12-question run, ~$0.25 for the recommended 30-question ×3-averaged run, and up to ~$0.95 for a fully robust 60-question ×3×3 run with one retest round — concluding token cost is not the bottleneck, the recommended tier can detect a 1-point/10 improvement

## [1.0.0] - 2026-05-27

### Added
- Tool calling rules V0 (English and Chinese)
- Tool calling rules V1 (English and Chinese)
- DeepSeek V4 Pro Max Thinking rules (Infinite-Reasoning Engine, English and Chinese)
- DeepSeek V4 Flash Max Thinking rules (Rapid-Reasoning Engine, English and Chinese)
- GLM 5.1 Max Thinking rules (Incisive-Reasoning Engine, English and Chinese)
- CONTRIBUTING.md and CONTRIBUTING_cn.md guidelines
- README.md and README_cn.md project documentation
- LICENSE.md (PolyForm Noncommercial License 1.0.0)
- .gitignore (exclude monetization-plan.md, an internal business plan that must not be committed to the public repository; also exclude tmp/ and .DS_Store)

### Changed
- Expanded project scope from tool calling rules to a comprehensive agent rules collection
- Enhanced tool calling rules from V0 to V1 with systematic improvements
- Updated documentation with detailed comparison of three reasoning engines
- Refreshed CONTRIBUTING, LICENSE, and README files

## [0.2.0] - 2026-05-25

### Added
- DeepSeek V4 Pro deep reasoning rules (initial version)
- DeepSeek V4 Flash deep reasoning rules
- Sublicense clause to CONTRIBUTING.md
- Markdown code block wrapping for all rule files

### Changed
- Updated LICENSE, README, and README_cn documentation
- Added CONTRIBUTING.md file

## [0.1.0] - 2026-05-23

### Added
- Initial deep reasoning rules framework
- Project refactoring to support multiple rule types

### Changed
- Expanded project positioning to agent-oriented rules collection

## [0.0.1] - 2026-05-11

### Added
- Initial project structure
- Tool calling rules V0 (English and Chinese)
- Tool calling rules V1 (English and Chinese)
- AGPL-3.0 LICENSE file
- README.md and README_cn.md documentation

---

## Version History Summary

- **1.0.0**: Complete agent rules collection with three reasoning engines
- **0.2.0**: Added deep reasoning rules for DeepSeek models
- **0.1.0**: Project refactoring and deep reasoning framework
- **0.0.1**: Initial release with tool calling rules