# Heptabase

- 形态：商业视觉知识库 + AI Tutor + App Skills + CLI
- 链接：[官网](https://heptabase.com) · [Wiki](https://wiki.heptabase.com) · [路线图](https://wiki.heptabase.com/roadmap/) · [CLI Skills](https://github.com/heptameta/heptabase-cli-skills)
- 状态：重点对照

## 简介

底座是白板、卡片、PDF/视频和双向链接。AI Tutor（2026-03-31 随 v1.88.0 上线）按目标开课、课中带读空间里的源、课末检查。2026-08-14 的 v1.103.0 加上 App 内 AI Skills：把「抽主张做思维导图并链回 PDF」做成 slash command。CLI Skills 让 Claude Code / Codex 操作同一空间。更细拆解见 [../../capabilities/heptabase.md](../../capabilities/heptabase.md)。

## 建议使用场景

- 读难书、啃领域，需要主张之间的空间关系。
- 研究与学习不要分开：高亮、引用、续课留在知识库。
- 要外部编码 Agent 通过 CLI 读写白板/卡片/课程。
- 不适合：要 AI 同学举手讨论；要机构 LMS 分发；要完全开源自托管。

## 调研（巡查 2026-09-22）

| 项 | 记录 |
|---|---|
| 版本锚点 | AI Tutor v1.88.0（2026-03-31）；CLI v1.91.0 + CLI Skills v1.91.3（2026-04）；App AI Skills v1.103.0（2026-08-14）；移动端 Tutor/Agent v1.38.0（2026-08-18） |
| 当前在做 | 白板/移动性能；Agent 与 Codex & Claude Code 更深集成。内部测试中：LLM Wiki、白板小地图（截至 2026-09-17 路线图） |
| Skill | App 内用户自定义工作流（无统一公开市场）。对外：`heptabase-cli` 一条 Skill，覆盖笔记、journal、标签、卡片、文件、白板布局、思维导图、目标、课程与课时 |
| 定价 | 第三方汇总写过年付约 $8.99/月起 + AI 额度档；Tutor 曾发过体验额度。以官网现价为准 |
| 风险 | Tutor 课时能否导出未核；用户 Skill 不能像 EduHub 那样浏览安装 |

来源：Heptabase Public Wiki 路线图与更新信、CLI Skills README、产品公告。

## 使用体验

未上手。下次试用请记下：从一本书开课要几步、课末问题是否基于你的笔记、自建 Skill 能否稳定复用到第二本书。
