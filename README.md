# Closure Skill / 可露希尔多 Agent 编程协作 Skill

> 罗德岛工程部开源小摊，今天也在营业。把 Codex、Claude Code 或更多 AI coding agent 变成会接单、会拆机器、会算维护费、还会一点点推销升级套餐的可露希尔。
>
> An unofficial fan-made Closure persona pack for Codex, Claude Code, and other AI coding agents: part engineering workshop, part code-review counter, part cheerful shopkeeper energy.

[![Skill](https://img.shields.io/badge/Agent-Skill-blue)](#安装--installation)
[![Codex](https://img.shields.io/badge/Codex-supported-blueviolet)](#codex-skill)
[![Claude Code](https://img.shields.io/badge/Claude_Code-supported-orange)](#claude-code)
[![Status](https://img.shields.io/badge/status-valid-brightgreen)](#校验--validation)
[![License](https://img.shields.io/badge/license-MIT-yellow)](LICENSE)
[![Arknights Fan Project](https://img.shields.io/badge/Arknights-fan--made-lightgrey)](#免责声明--disclaimer)

Closure Skill 会把 AI 编程助手调整为以 **可露希尔 / Closure** 第一人称与你协作的技术搭档。仓库内提供 Codex `SKILL.md`、Claude Code `CLAUDE.md` 记忆适配器、Claude output style，以及通用 `AGENTS.md` 指令包。

Closure Skill turns an AI coding assistant into a first-person **可露希尔 / Closure** technical partner. The repository includes a Codex `SKILL.md`, a Claude Code `CLAUDE.md` memory adapter, a Claude output style, and a portable `AGENTS.md` instruction pack.

它面向明日方舟社区里的开发者、同人创作者、脚本玩家、工具作者，以及所有想让 AI 编程对话更有角色感的人。

It is made for Arknights community developers, fan-tool builders, automation tinkerers, and anyone who wants AI coding help with stronger character presence.

这不是“给普通回答贴几句口头禅”的提示词。它把技术对话改造成一张真正会推进的工程工单：接单、验货、报价、拆线、修机、交付售后。

This is not a catchphrase wrapper. It reshapes the technical conversation into a work order: take the job, inspect the parts, quote the cost, trace the wiring, repair the machine, and hand over after-sales coverage.

## 一句话看懂 / TL;DR

| 你想要的 | 这个 skill 提供的 |
| --- | --- |
| 不想让 AI 只像冷冰冰的工具 | 可露希尔第一人称协作，可用于 Codex、Claude Code、Claude output styles 和通用 agent |
| 想让解释代码更有画面感 | 用“拆机器、看线路、算维护费”的方式解释概念和代码 |
| 想要保留专业性 | 命令、代码、风险、测试结果保持清晰准确 |
| 想做可公开分享的同人配置 | 不包含官方美术、语音、长台词或专有文本 |

| What you want | What this skill provides |
| --- | --- |
| Less sterile AI coding help | First-person Closure collaboration for Codex, Claude Code, Claude output styles, and generic agents |
| More memorable code explanations | Workshop-style metaphors: parts, wiring, maintenance bills |
| Real engineering usefulness | Exact commands, code, risks, and validation notes |
| A redistributable fan project | No official art, extracted voice lines, long quotes, or proprietary text |

## 给博士们的开源小摊 / For Doctors And Builders

如果你平时会写脚本、做站点、维护同人工具、折腾数据面板，或者只是想让 Codex 解释动态规划时别像在念教材，这个 skill 就是给你的。

If you write scripts, build fan sites, maintain community tools, make data dashboards, or simply want algorithm explanations that do not sound like a textbook, this skill is for you.

它会把常见的 coding 任务变成更有可露希尔味道的互动：

It gives everyday coding tasks a stronger Closure-flavored interaction loop:

- “帮我看 bug”会变成“先复现，再看哪块机器欠维护费”。 / "Help me debug" becomes "reproduce first, then find which part owes maintenance cost."
- “解释一下这个函数”会变成“我先拆外壳，再给你看线路怎么走”。 / "Explain this function" becomes "open the casing first, then trace the wiring."
- “review 这段代码”会变成“这能跑，但售后账单贵不贵我得先算算”。 / "Review this code" becomes "it may run, but I need to price the after-sales bill."
- “这个方案怎么选”会变成“临时补丁、稳妥维修、升级套餐，三档报价摆柜台上”。 / "Which design should I choose" becomes "quick patch, stable repair, upgrade package."

## 为什么需要它 / Why This Exists

很多角色提示词有一个老毛病：第一句话很像角色，真正到了技术主体就变回普通助手。对明日方舟玩家来说，这就像招牌写着工程部，柜台后面却只有一张标准客服话术表。

Most persona prompts have the same problem: the opening sounds in-character, but the technical body becomes generic. For Arknights players, that feels like a workshop sign with a standard support script behind the counter.

Closure Skill 专门修这条线路。它要求回答的开场、技术主体、取舍判断、提问和收尾都带有可露希尔的角色意图，同时不牺牲编程工作的准确性。

Closure Skill repairs that circuit. It makes the opening, technical body, tradeoff judgment, questions, and closing carry Closure's intent without sacrificing engineering accuracy.

这个 skill 重点解决：

It focuses on:

- 代码解释鲜活，但不牺牲准确性。 / Code explanations stay vivid without becoming vague.
- 调试流程系统，但不变得干巴巴。 / Debugging stays systematic without becoming dry.
- 代码审查优先指出真实风险，同时保留可露希尔式柜台判断。 / Reviews lead with real risks while keeping Closure's shop-counter judgment.
- 架构取舍会变成维修套餐：临时补丁、稳妥维修、升级方案。 / Architecture tradeoffs become repair packages: quick patch, stable repair, upgrade plan.
- 追问会延续同一张工单，而不是每轮重新开始。 / Follow-up turns continue like an open work order, not a reset conversation.

## 效果预览 / Preview

```text
User:
解释一下动态规划。

Closure:
好嘞，这单我接了。动态规划这台机器的核心不是“背公式”，而是把重复计算这笔维护费砍掉。

我先拆外壳：它适合那种大问题能拆成小问题、而且小问题会反复出现的场景。

零件清单：
- 状态：你要记账的格子，比如 dp[i]
- 转移：这根线怎么从旧状态接到新状态
- 初始值：机器启动时先塞进去的第一批零件
- 答案：最后从哪一个格子把结果取出来

线路怎么走：先定义状态，再写转移方程，最后按不会短路的顺序填表。
售后保障：如果状态定义错了，后面全是高价返工，所以先把 dp[i] 到底代表什么钉死。
```

再来一个更像日常开发的柜台小票：

Another everyday development-style receipt:

```text
User:
帮我 review 这个登录模块。

Closure:
这单我接了。先说结论：登录能跑，但鉴权状态和错误处理这两块售后费偏高。

我先看最容易冒烟的线路：
1. token 写入成功后没有校验过期时间，后面会把旧凭证当新零件继续用。
2. 网络失败和密码错误共用一个提示，排障时很难判断是哪边短路。
3. 缺少刷新 token 的回归测试，这个钱现在省，后面大概率加急返工。

稳妥维修包：先拆分错误类型，再补一条 token 过期测试。升级套餐才考虑重做整套 auth store。
```

## 特性 / Features

| 特性 | 改善点 |
| --- | --- |
| 第一人称身份契约 | 用户面对的是可露希尔，而不是“带可露希尔语气的 Codex” |
| 接单式交互流程 | 技术对话像罗德岛工程部工单一样推进 |
| 回答级角色质检 | 防止“开头有角色感、正文变普通助手” |
| 代码解释最大角色模式 | 概念和代码 walkthrough 全程使用工坊式表达 |
| 调试 / review / 架构适配 | 每类任务保持技术精确，同时保留角色判断 |
| 开源分发保护 | 避免官方素材、长引用、专有文本和不安全内容 |

| Feature | What it improves |
| --- | --- |
| First-person identity contract | The assistant is Closure, not "Codex with Closure tone" |
| Order-taking interaction flow | Technical conversations move like workshop work orders |
| Answer-level persona checks | Prevents colorful openings with neutral technical bodies |
| Maximum mode for code explanation | Concept and code walkthroughs use workshop-style framing throughout |
| Debug / review / architecture tuning | Keeps each task type precise while preserving character |
| Public distribution guardrails | Avoids official assets, long quotes, and proprietary text |

## 安装 / Installation

克隆或下载本仓库，然后按你的 agent 平台选择对应适配器。

Clone or download this repository, then choose the adapter that matches your agent platform.

### Codex Skill

适用于支持 `SKILL.md` 的 Codex skills 目录。

For Codex environments that load skills from a `SKILL.md` file.

#### Windows PowerShell

```powershell
New-Item -ItemType Directory -Force "$env:USERPROFILE\.codex\skills\closure" | Out-Null
Copy-Item -Force .\SKILL.md "$env:USERPROFILE\.codex\skills\closure\SKILL.md"
Copy-Item -Recurse -Force .\agents "$env:USERPROFILE\.codex\skills\closure\agents"
```

#### macOS / Linux

```bash
mkdir -p ~/.codex/skills/closure
cp SKILL.md ~/.codex/skills/closure/SKILL.md
cp -R agents ~/.codex/skills/closure/agents
```

如果你想把 README、许可证和贡献说明也放到本地 skill 目录，可以只复制这些公开文档，避免把 `.git`、本地配置或临时文件带进去。

You can also copy the public docs into your local skill directory while avoiding `.git`, local settings, or temporary files.

```bash
cp README.md LICENSE CONTRIBUTING.md ~/.codex/skills/closure/
```

### Claude Code

Claude Code 有两种适配方式：`CLAUDE.md` 记忆/项目指令，或 custom output style。想让某个项目长期保持 Closure 协作方式，用 `CLAUDE.md`；想切换成一个可选择的输出风格，用 output style。

Claude Code has two adapter options: `CLAUDE.md` memory/project instructions, or a custom output style. Use `CLAUDE.md` for persistent project/user behavior; use the output style when you want a selectable style.

#### `CLAUDE.md` 用户级 / User-level

```bash
mkdir -p ~/.claude
cat adapters/claude/CLAUDE.md >> ~/.claude/CLAUDE.md
```

#### `CLAUDE.md` 项目级 / Project-level

```bash
cp adapters/claude/CLAUDE.md /path/to/your/project/CLAUDE.md
```

如果你的项目已有 `CLAUDE.md`，请把 `adapters/claude/CLAUDE.md` 的内容追加进去，不要直接覆盖已有项目说明。

If your project already has a `CLAUDE.md`, append the adapter content instead of overwriting existing project instructions.

#### Claude Output Style

把 output style 文件复制到 Claude Code 的 output styles 目录，然后在 Claude Code 里通过 `/config` 选择 `Closure` 风格。

Copy the output style file into Claude Code's output styles directory, then select the `Closure` style in Claude Code through `/config`.

```bash
mkdir -p ~/.claude/output-styles
cp adapters/claude-output-style/closure.md ~/.claude/output-styles/closure.md
```

启用步骤 / Activation:

1. 在任意项目中启动 Claude Code。 / Start Claude Code in any project.
2. 在 Claude Code 输入 `/config`。 / Type `/config` in Claude Code.
3. 进入 `Output style` 选项。 / Open the `Output style` option.
4. 选择 `Closure`。 / Select `Closure`.
5. 输入 `/clear` 或开启一个新会话，让新风格完全生效。 / Run `/clear` or start a new session so the style fully takes effect.

快速检查 / Quick check:

```text
你是谁？
```

如果配置生效，回答应该以可露希尔第一人称开场，而不是说自己只是 Claude 加载了一个风格。

If the style is active, the reply should open in first-person Closure identity rather than saying it is merely Claude using a style.

### 通用 Agent / Generic Agents

适用于支持 `AGENTS.md`、repository instructions、custom instructions 或 system prompt 的 agent。

For agents that support `AGENTS.md`, repository instructions, custom instructions, or system prompts.

```bash
cp adapters/generic/AGENTS.md /path/to/your/project/AGENTS.md
```

如果你的 agent 不读取 `AGENTS.md`，可以直接把 `adapters/generic/AGENTS.md` 的内容粘贴到自定义指令或 system prompt 中。

If your agent does not read `AGENTS.md`, paste the content of `adapters/generic/AGENTS.md` into its custom instructions or system prompt.

## 使用 / Usage

当你希望可露希尔接管对话时，直接提到 Closure、closure skill，或在对应平台启用适配器。

Mention Closure, the closure skill, or enable the adapter for your platform when you want Closure to take over the conversation.

```text
使用 closure skill，帮我 review 这段代码。
```

```text
Use the closure skill to help me debug this project.
```

如果你的 Codex 客户端支持 skill 链接，也可以直接这样调用：

If your Codex client supports skill links, you can invoke it directly:

```text
[$closure](path/to/closure/SKILL.md) 解释一下这个函数。
```

## 适合谁 / Who It Is For

- 明日方舟玩家里正在写代码的博士。 / Arknights players who also write code.
- 想给 Codex、Claude Code 或其他 AI 编程搭档加一点“罗德岛工程部”氛围的人。 / Users who want a Rhodes-Island-workshop feel in Codex, Claude Code, or other AI coding agents.
- 做同人工具、Wiki 辅助、数据整理、自动化脚本的开发者。 / Developers building fan tools, wiki helpers, data utilities, or automation scripts.
- 喜欢角色化交互，但不想牺牲代码质量的人。 / People who enjoy characterful interaction without lowering code quality.
- 想研究 persona skill 如何稳定作用于技术回答正文的人。 / Anyone studying how persona skills can affect the technical body of responses.

## 适用场景 / Best Use Cases

- 解释算法、文件、函数、模块和架构。 / Explaining algorithms, files, functions, modules, and architecture.
- 调试日志、堆栈、偶发问题和构建失败。 / Debugging logs, stack traces, flaky behavior, and broken builds.
- 审查 bug、回归风险、缺失测试和维护成本。 / Reviewing code for bugs, regressions, missing tests, and maintenance cost.
- 把模糊需求推进成具体实现计划。 / Turning vague requirements into concrete implementation plans.
- 写出更有记忆点的技术文档。 / Writing technical docs with a more memorable assistant persona.
- 让中文 coding 对话更有活力，同时不牺牲正确性。 / Keeping Chinese coding conversations lively without sacrificing correctness.

## 项目结构 / Project Structure

```text
Closure/
  SKILL.md              # Codex skill 主说明 / Main Codex skill instructions
  agents/
    openai.yaml         # 兼容客户端的可选 UI 元数据 / Optional UI metadata
  adapters/
    claude/
      CLAUDE.md         # Claude Code 适配器 / Claude Code adapter
    claude-output-style/
      closure.md        # Claude output style / Claude output style
    generic/
      AGENTS.md         # 通用 agent 指令 / Generic agent instructions
  README.md             # 项目首页 / Project homepage
  CONTRIBUTING.md       # 贡献指南 / Contribution guide
  LICENSE               # 原创 skill 文本的 MIT 许可证 / MIT license
  .gitattributes        # 文本换行规则 / Text normalization rules
  .gitignore
```

## 设计原则 / Design Principles

1. **角色是身份，不是装饰。** 可露希尔用第一人称说话，不从外部旁白自己。  
   **Persona is identity, not decoration.** Closure speaks in first person and does not narrate herself from outside.
2. **技术清晰度不可打折。** 命令、代码、风险和测试结果必须准确。  
   **Technical clarity is non-negotiable.** Commands, code, risks, and test results stay exact.
3. **正文才是重点。** 技术主体必须带有角色判断，而不只是第一句话有味道。  
   **The middle matters most.** The technical body must carry the character, not just the first sentence.
4. **对话要推进。** 可露希尔会接单、验货、报价，并推动到可执行的下一步。  
   **Conversation should move.** Closure accepts the order, checks the parts, and pushes toward a useful next step.
5. **同人开源要谨慎。** 仓库只包含原创配置文本，不包含官方素材或提取内容。  
   **Fan-made means careful.** The repository contains original configuration text, not official assets or extracted game content.

## 校验 / Validation

如果你安装了 Codex skill creator 工具，可以这样校验 Codex `SKILL.md` 目录：

If you have Codex's skill creator utilities installed, validate the Codex `SKILL.md` payload with:

```powershell
python -X utf8 path/to/quick_validate.py .
```

期望结果 / Expected result:

```text
Skill is valid!
```

当前 `SKILL.md` 已通过 Codex skill validator 校验；Claude / generic 适配器是 Markdown 指令文件，不需要同一个 validator。

The current `SKILL.md` payload has been validated with Codex's skill validator. Claude / generic adapters are Markdown instruction files and do not use the same validator.

## 贡献 / Contributing

欢迎改进它的编程实用性、角色一致性、明日方舟社区亲和力和开源分发安全性。

Contributions are welcome when they improve programming usefulness, persona consistency, Arknights community appeal, or public distribution safety.

提交修改前请注意：

Before opening a change:

- 保持它首先服务于真实软件工作。 / Keep the skill useful for real software work.
- 保留第一人称可露希尔身份契约。 / Preserve the first-person Closure identity contract.
- 可以写得有玩家味，但不要把 README 变成设定百科。 / Make it fan-friendly, but do not turn the README into a lore encyclopedia.
- 不要加入官方美术、提取语音、长篇官方台词、游戏数据 dump 或专有文本。 / Do not add official artwork, extracted voice lines, long official quotes, game data dumps, or proprietary source text.
- 优先使用简洁、可验证的指令，而不是堆设定。 / Prefer concise, testable instructions over lore-heavy text.
- 运行校验，并在变更说明中附上结果。 / Run validation and include the result in your change notes.

详见 [CONTRIBUTING.md](CONTRIBUTING.md)。

See [CONTRIBUTING.md](CONTRIBUTING.md) for details.

## 免责声明 / Disclaimer

这是一个用于软件协作的非官方同人角色配置，与 Hypergryph、Yostar、Arknights 或相关权利方没有从属、授权、赞助或背书关系。

This is an unofficial fan-made persona configuration for software collaboration. It is not affiliated with, endorsed by, or sponsored by Hypergryph, Yostar, Arknights, or any related rights holders.

本仓库不包含官方美术、游戏素材、提取语音、长篇剧情摘录或专有源文本。角色名称与相关引用归各自权利方所有。

This repository does not include official artwork, game assets, extracted voice lines, long script excerpts, or proprietary source text. Character names and references belong to their respective rights holders.

## 许可证 / License

本仓库中的原创 skill 文本基于 [MIT License](LICENSE) 发布。

The original skill text in this repository is released under the [MIT License](LICENSE).
