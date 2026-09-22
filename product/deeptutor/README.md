# DeepTutor

- 形态：开源自托管 / CLI / Docker / pip
- 团队：香港大学 HKUDS
- 链接：[GitHub](https://github.com/HKUDS/DeepTutor) · [文档](https://deeptutor.info) · [EduHub](https://eduhub.deeptutor.info/) · [CLI Skill](https://github.com/HKUDS/DeepTutor/blob/main/SKILL.md)
- 状态：重点对照

## 简介

Agent 原生学习工作区。Chat、解题、出题、研究、可视化、掌握路径、沉浸阅读/观看跑在同一套循环上，共享知识库、笔记本和 L1/L2/L3 可审计记忆。Partners 可接到 IM。技能默认走 EduHub（约 72–74 个教学 Skill），也兼容 ClawHub。CLI Skill 名 `deeptutor-cli`。

## 建议使用场景

- 教材、论文、代码要进自己的库，答案要带出处。
- 同一条对话里切换「讲 / 解 / 出题 / 综述 / 可视化」。
- 要本地部署、换模型、把学伴接到飞书或 Telegram。
- 不适合：只要精美课堂演出；完全不想维护 Python 环境。

## 调研（巡查 2026-09-22）

| 项 | 记录 |
|---|---|
| 仓库活跃 | 约 40.1k star；2026-09-20 官宣 9 个月 4 万星 |
| 版本 | v1.6.9（2026-09-20/21）：文件夹学习空间、每日练习、设置重做、用量记账、可恢复归档 |
| 安装 | `pip install -U deeptutor` 或 `deeptutor-cli`；`deeptutor init` 向导 |
| Skill | 仓根 `SKILL.md` = `deeptutor-cli`。EduHub 可见精选：Socratic Tutor、Flashcard Deck、Essay Feedback；文档还提到考试蓝图、概念讲解。CLI：`deeptutor skill search/install`，默认 hub 为 EduHub |
| 记忆 | L1 痕迹、L2 摘要、L3 综合 + Memory Graph |
| 风险 | EduHub 72+ 条目未逐条核验质量；安装与模型配置仍可能是试用门槛 |

来源：官方 README（含 2026-09-21 发行说明）、deeptutor.info、eduhub.deeptutor.info。

## 使用体验

未上手。下次试用请记下：pip/Docker 是否一次跑通、知识库引用是否准、EduHub 安装一个 Skill 后行为有无变化。
