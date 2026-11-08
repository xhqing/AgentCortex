# AgentCortex · 项目硬约束

身份与角色见本仓库根 `AGENTS.md`；团队通用规则见全局 `~/.pi/agent/AGENTS.md`，此处不重述。

## 本项目是什么

一套面向智能体的深度推理引擎规则集：三套引擎，每套一中一英两个文件、内容一一对应。

| 引擎 | 面向模型 | 中文 | 英文 |
|------|---------|------|------|
| 无限推理引擎 Infinite-Reasoning | DeepSeek V4 Pro | `dsv4proMaxThinkingRules_cn.md` | `dsv4proMaxThinkingRules.md` |
| 极速推理引擎 Rapid-Reasoning | DeepSeek V4 Flash | `dsv4flashMaxThinkingRules_cn.md` | `dsv4flashMaxThinkingRules.md` |
| 锐利推理引擎 Incisive-Reasoning | GLM 5.1 | `glm51MaxThinkingRules_cn.md` | `glm51MaxThinkingRules.md` |

规则正文是**直接注入 system prompt 的提示词**，不是给人读的说明文：不写「TODO」「见 docs/xxx」这类元信息，不带维护者视角的叙述。

## 硬约束

- **一套引擎一个文件，不合并、不抽公共片段**：三套引擎各自针对对应模型的短板设计，改一套不得顺手改另两套，三条规则文件之间不共享内容。
- **章节骨架固定**：`# 角色` → `## 核心指令` → `## 思维架构执行`（四步）→ 独有协议（有则单列一个 `##`）→ `## 执行约束` → `## 输出隔离原则` → `## 输出指令`。可以改内容，但不改顺序、不改章节名。
- **四步思维架构的名称固定**：解构与前提审计 / 多视角综合 / 第三层 / 反驳与压力测试。第三层是引擎专属叫法——Pro 用「无限深度遍历」、Flash 用「快速螺旋深化」、GLM 用「递进深化」，不得跨引擎移植。
- **独有协议不得跨引擎移植**：反捷径协议只属于 Flash；独立判断协议 + 反浅层收敛协议只属于 GLM；Pro 没有独有协议。同理，轮次下限（Flash 至少三轮、GLM 至少三层）、GLM 的「语言一致性」约束也都是引擎专属。README 两版的对比表已固化这些差异，移植等于让文档说谎。
- **输出隔离原则是最高优先级，措辞不许弱化**：五条（思考过程不可见 / 标题隔离 / 元认知不可见 / 纯粹回答 / 无例外原则）一条都不能删、不能改软，三套引擎这一节保持等价。
- **中文版与英文版同轮改**：任何规则内容改动必须在同一次提交里改完 `_cn.md` 与英文版，条款数、协议名、约束条数一一对应；只改一边算未完成。英文按地道美式英语写，不逐字硬译。
- **README 两版跟着改**：`README.md` / `README_cn.md` 的「三大推理引擎对比」表格与正文（独有模块、轮次下限、条数、语言一致性标记）描述的是规则文件的现状，规则改了这里必须同轮同步。
- `docs/` 下是评测体系规划（题目 / 实验组 / 对照组 / 评审），不是规则文本；改规则不碰 `docs/`。

## 验证

改完跑下面这段，每对文件的两个数字必须相等（当前基线：Pro 5 个 `##` / 9 条 `*`，Flash 6 / 14，GLM 7 / 18）：

```bash
for b in dsv4proMaxThinkingRules dsv4flashMaxThinkingRules glm51MaxThinkingRules; do
  echo "$b  cn: $(grep -c '^## ' ${b}_cn.md)/$(grep -c '^\* ' ${b}_cn.md)  en: $(grep -c '^## ' ${b}.md)/$(grep -c '^\* ' ${b}.md)"
done
```

- 数字变了就同步更新这里的基线，别让基线漂成假的。
- 关键短语对账：三套文件都应有输出隔离原则（中文 `grep -c '输出隔离原则'`、英文 `grep -c 'Output Isolation Principle'` 各为 1）；独有协议名（`反捷径协议` / `独立判断协议` / `反浅层收敛协议`）只应出现在对应引擎的文件里。

## 详细说明

`README.md` / `README_cn.md`（三套引擎的定位与差异）、`CONTRIBUTING_cn.md`（贡献约定）、`docs/`（评测规划）；通用工作规则见全局 `~/.pi/agent/AGENTS.md`。
