# Heptabase

- 形态：商业视觉知识库 + AI Tutor + App Skills + CLI
- 链接：[官网](https://heptabase.com) · [Wiki](https://wiki.heptabase.com) · [路线图](https://wiki.heptabase.com/roadmap/) · [定价](https://heptabase.com/pricing) · [CLI Skills](https://github.com/heptameta/heptabase-cli-skills)
- 状态：重点对照

## 简介

底座是白板、卡片、PDF/视频和双向链接。AI Tutor（2026-03-31 随 v1.88.0 上线）按目标开课、课中带读空间里的源、课末检查。2026-08-14 的 v1.103.0 加上 App 内 AI Skills：把「抽主张做思维导图并链回 PDF」做成 slash command。CLI Skills 让 Claude Code / Codex 操作同一空间。更细拆解见 [../../capabilities/heptabase.md](../../capabilities/heptabase.md)。它解决的是「在一张桌上读懂一本书/一个领域」，不是播放式课堂。

## 建议使用场景

适合：

- 读难书、啃领域，需要主张之间的空间关系。
- 研究与学习不要分开：高亮、引用、续课留在知识库。
- 要外部编码 Agent 通过 CLI 读写白板/卡片/课程。

不适合：

- 要 AI 同学举手讨论。
- 要机构 LMS 分发、证书、学员门户。
- 要完全开源自托管。
- 只要便宜刷闪卡（Pro 档 AI 额度很小，Tutor 在 Premium）。

## Skill

两层，不要混：

| 层 | 形态 | 做什么 |
|---|---|---|
| AI Tutor | 产品对象，不是 SKILL.md | 目标 → 大纲 → 课时；课中带读；课末提问 |
| App AI Skills | 产品内可复用工作流 | 用户描述 → Agent 写成 slash command；官方演示：300 页哲学书 → 主张图卡片链回 PDF，或按页序摘要 |
| heptabase-cli | 公开 Agent Skill | 笔记、journal、标签、卡片、文件、白板布局、思维导图、目标、课程与课时 |

没有像 EduHub 那样的可浏览市场。Tutor 开课要 Premium 档。总表见 [capabilities/skill-map.md](../../capabilities/skill-map.md)。

## 能力对照

| 维度 | 本产品 |
|---|---|
| 资料摄入 | 强：PDF 页级、YT 转写、Web Clipper、Readwise、Zotero |
| 一键成课 | 强：目标驱动课程对象，不是课堂场景 |
| 直播课堂 | 弱：白板是思考桌不是讲台 |
| 解题/出题 | 弱：课末检查，题库/FSRS 弱 |
| 主动规划 | 中：续课，不抢日程 |
| 长期记忆 | 强：空间即记忆 |
| 视觉知识结构 | 极强：白板 / 卡片 / 主张图 |
| 可复用 Skill | 强：App Skills + CLI；无私有市场目录 |
| 自托管 / 换模型 | 否；部分 BYOK / 开源模型入口 |
| 导出 | 空间内为主；白板可导出图；卡片可拷 Markdown |

相对锚点：1+2+5（源、视觉、阅读 Skill）最强；演课弱于 OpenMAIC；解题与可审计记忆层弱于 DeepTutor；备考主动弱于 Hyperknow。

## 调研

巡查 2026-09-22。来源：Public Wiki 路线图（更新至 2026-09-17）、定价页、CLI Skills README、产品公告。

| 项 | 记录 |
|---|---|
| 版本锚点 | AI Tutor v1.88.0（2026-03-31）；CLI v1.91.0 + CLI Skills v1.91.3（2026-04）；App AI Skills v1.103.0（2026-08-14）；移动端 Tutor/Agent v1.38.0（2026-08-18） |
| 当前在做 | 白板/移动性能；Agent 与 Codex & Claude Code 更深集成。内部测试：LLM Wiki、白板小地图 |
| 定价（官网年付） | Pro $8.99/月（100 AI 点、Gemini Agent，无 Tutor）；Premium $17.99/月（1800 点、Tutor、GPT/Claude/Gemini）；Premium+ $53.99/月（8100 点）。月付约高 25%。7 天试用 |
| 风险 | Tutor 课时能否导出未核；用户 Skill 不能像 EduHub 那样浏览安装；额度不滚动 |

## 使用体验

未上手。下次试用记下：

- 账号档（Tutor 是否解锁）
- 从一本书开课要几步
- 课末问题是否基于你的笔记而不是泛泛提问
- 自建 Skill 能否稳定复用到第二本书
- CLI 改一张卡片后 App 里是否立刻可见
