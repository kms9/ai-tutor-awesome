# DeepTutor

- 形态：开源自托管 / CLI / Docker / pip
- 团队：香港大学 HKUDS
- 协议：Apache-2.0
- 链接：[GitHub](https://github.com/HKUDS/DeepTutor) · [文档](https://deeptutor.info) · [EduHub](https://eduhub.deeptutor.info/) · [CLI Skill](https://github.com/HKUDS/DeepTutor/blob/main/SKILL.md)
- 状态：重点对照

## 简介

Agent 原生学习工作区。Chat、解题、出题、研究、可视化、掌握路径、沉浸阅读/观看跑在同一套循环上，共享知识库、笔记本和 L1/L2/L3 可审计记忆。Partners 可接到 IM。技能默认走 EduHub（约 74 个教学 Skill），也兼容 ClawHub。CLI Skill 名 `deeptutor-cli`。它解决的是「长期跟学 + 可安装教法」，不是一节课的舞台演出。

## 建议使用场景

适合：

- 教材、论文、代码、本地文件夹要进自己的库，答案要带出处。
- 同一条对话里切换「讲 / 解 / 出题 / 综述 / 可视化」。
- 要本地部署、换模型、把学伴接到飞书或 Telegram。
- 要从 EduHub 安装苏格拉底、闪卡、作文反馈等教法，而不是写死一个 tutor prompt。

不适合：

- 只要精美课堂演出（去 OpenMAIC）。
- 完全不想维护 Python / Docker。
- 只要机构发证 LMS（去 ClassroomIO / Coursebox）。
- 备考要「未问先排日程 + 打印 cheatsheet」（去 Hyperknow）。

## Skill

| 层 | 名称 | 做什么 |
|---|---|---|
| CLI | `deeptutor-cli`（仓根 `SKILL.md`） | 配置、能力、知识库、Partners、记忆、会话、笔记本、启服务、skill search/install |
| 注册表 | EduHub | 74 skills / 4 tracks，可装进 DeepTutor / Claude Code / Codex |
| 兼容 | ClawHub | CLI 文档仍写 `<hub>:<slug>`，默认 hub 文案两边都出现过 |

EduHub 四条 track：Academics、Companions、Skills & Interests、For Educators。

本轮已点名：

| Skill | Track | 动作 |
|---|---|---|
| Socratic Tutor | Academics / Universal | 教：追问，不直接给答案 |
| Flashcard Deck | Academics / Universal | 练：Q/A 与 cloze，可进 Anki |
| Essay Feedback | Educators / 语文 | 评：按量规反馈，不代写 |

文档还提到考试蓝图、概念讲解，未打开逐条页。其余约 70 条下一轮巡目录。总表见 [capabilities/skill-map.md](../../capabilities/skill-map.md)。

## 能力对照

| 维度 | 本产品 |
|---|---|
| 资料摄入 | 强：多引擎 RAG、文件夹工作区、可选视频字幕、可接自建 WeKnora |
| 一键成课 | 中：Book / Mastery Path / 学习空间，不是课堂场景生成 |
| 直播课堂 | 弱：对话与可视化，无 AI 同学舞台 |
| 解题/出题 | 极强：深解题、出题、每日练习 |
| 主动规划 | 中：Partners 可主动；日程抢占弱于 Hyperknow |
| 长期记忆 | 极强：L1 痕迹 / L2 摘要 / L3 综合 + Memory Graph |
| 视觉知识结构 | 中：可视化目录（SVG/Mermaid/Manim 等），不是白板知识库 |
| 可复用 Skill | 极强：CLI + EduHub 74 |
| 自托管 / 换模型 | 是 |
| 导出 | Markdown / 笔记本 / 归档；Skill 与知识库可迁工作区 |

相对锚点：记忆、解题、Skill 市场强于另外三个；演课弱于 OpenMAIC；源级白板弱于 Heptabase；备考资产弱于 Hyperknow。

## 调研

巡查 2026-09-22。来源：官方 README（含 2026-09-21 发行说明）、deeptutor.info、eduhub.deeptutor.info、GitHub API。未实机登录。

| 项 | 记录 |
|---|---|
| 仓库 | 约 40.1k star / 5.0k fork；2026-09-20 官宣 9 个月 4 万星 |
| 版本 | v1.6.9（2026-09-20/21）：文件夹学习空间、每日练习、设置重做、用量记账、可恢复归档 |
| 安装 | `pip install -U deeptutor` 或 `deeptutor-cli`；`deeptutor init` |
| 风险 | EduHub 74 条未逐条核验质量；安装与模型配置仍可能是试用门槛 |

## 使用体验

未上手。下次试用记下：

- pip / Docker 是否一次跑通
- 一份教材进库后引用是否对准页/段
- `deeptutor skill install` 装 Socratic Tutor 前后，追问姿态有无变化
- L2/L3 记忆能否打开、改、删
- Partners 接到一个 IM 后会不会主动找你
