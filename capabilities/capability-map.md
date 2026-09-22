# 能力图谱

巡查日期：2026-09-22。用同一组维度打产品，避免「都叫 AI Tutor」却不可比。

评分是公开资料判断，不是实机实测。`—` 表示该产品本来就不做这件事。

## 四锚点

| 维度 | 含义 | OpenMAIC | DeepTutor | Hyperknow | Heptabase |
|---|---|---|---|---|---|
| 资料摄入 | PDF/PPT/视频/LMS | 强（含 pptx） | 强（多引擎 RAG） | 强（约 1000 页）+ Canvas | 强（PDF/YT/Zotero/Readwise） |
| 一键成课 | 大纲+场景生成 | 极强（课堂场景） | 中（Book/Mastery/空间） | 强（1:1 Deep Learn） | 强（目标→课程） |
| 直播课堂 | 老师/同学/白板/语音 | 极强 | 弱 | 弱 | 弱（白板是思考桌不是讲台） |
| 解题/出题 | 多步推理、仿考试 | 有测验 | 极强 | 强 | 课末提问，题库弱 |
| 主动规划 | 未问先准备 | 弱 | Partners 可主动 | 极强（Orbie） | 中（续课，非抢日程） |
| 长期记忆 | 跨会话可审计 | 会话级 | 三层 Memory | 学习风格 / Memory 档 | 空间即记忆 |
| 视觉知识结构 | 卡片/白板/主张图 | 课堂白板 | 可视化模式 | 讲解视频 | 极强 |
| 可复用 Skill | Agent playbook | openmaic + agent-runtime 已点名 24 课内 Skill + importer | deeptutor-cli + EduHub 74 | 产品内流程，无公开仓 | App Skills + heptabase-cli |
| 自托管 / 换模型 | | 是 | 是 | 否 | 否（部分 BYOK / 开源模型入口） |
| 导出 | | PPTX/HTML | MD/笔记本 | cheatsheet/视频 | 空间内为主；白板可导出图 |

## 其余产品（同一组维度）

| 维度 | OpenTutor | Course Navigator | ClassroomIO | StudyFetch | YouLearn | Scholarly | Coursebox | X-Pilot | NotebookLM | Khanmigo |
|---|---|---|---|---|---|---|---|---|---|---|
| 资料摄入 | 强（PDF/Office/Canvas） | 视频/字幕 | 课包+视频转写 | 课件/音视频/手写 | PDF/YT/录音 | PDF/录音/笔记 | 文档/视频/URL | PDF/PPT/MD/URL | 笔记本源 | Khan 内容库 |
| 一键成课 | 中（笔记+测验包） | — | 中（AI 大纲/讲义） | 弱（复习包） | 中（笔记+测+播客） | 中（积分创作） | 强（培训课） | 强（视频课） | 弱（指南/概览） | — |
| 直播课堂 | — | — | — | 转写助手 | — | — | — | — | — | — |
| 解题/出题 | 强（7 题型+FSRS） | — | 练习+辅助批改 | 测验 | 测验/模考 | 测验/模考 | 课内测验 | — | 学习指南 | 站内练习+追问 |
| 主动规划 | 中（日历） | — | 合规截止日期 | 弱 | 弱 | 弱 | — | — | — | — |
| 长期记忆 | 工作区状态 | — | LMS 进度 | 弱 | 错题聚焦 | 工作区 | LMS 进度 | 项目文件 | 笔记本 | 账号历史 |
| 视觉知识结构 | 知识图谱（实验） | — | — | — | — | 思维导图/幻灯 | 数字人口播 | 分镜视频 | 幻灯/视频概览 | — |
| 可复用 Skill | 未见 | 无 | MCP，非教学 Skill | 无 | 无 | 无 | 无 | 无 | 无 | 无公开文件 |
| 自托管 / 换模型 | 是 | 本地 App | 是 | 否 | 否 | 聊天可选模型 | 否 | 否 | 否 | 否 |
| 导出 | 会话/复习内容 | 字幕/文本 | SCORM 弱于 Coursebox | 复习集 | Anki（Pro） | Word/PPT/Anki（付费） | PDF/HTML/SCORM | MP4 | 音频下载 | — |

新增产品时只加列，不改行名，除非开 Issue 讨论维度本身。

Skill 名称与「锁死流程」对照见 [skill-map.md](skill-map.md)。产品页内也有同一组十维的单列版。
