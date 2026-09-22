# Skill 和能力对照

巡查：2026-09-22。产品能力 ≠ Skill。Skill 是可复用 playbook（通常 `SKILL.md`）；能力是产品自己会做的事。

对照维度与 [capability-map.md](capability-map.md) 相同。`—` 表示没有可安装 / 可打开的 Skill，不等于产品不会做这件事。

## 谁真正有 Skill

| 来源 | 形态 | 数量（公开可见） | 主要教学动作 | 能接到外部 Agent |
|---|---|---|---|---|
| OpenMAIC | 仓内 `skills/openmaic` + `skills/agent-runtime/*` + `@openmaic/importer` | 包装 2 + 课内约 24 + importer 1 | 备 / 做课 / 演课 | 是（OpenClaw / Codex / DeepSeek Harness） |
| DeepTutor | 仓根 `deeptutor-cli` + EduHub 注册表 | 1 条 CLI + EduHub 74 | 教 / 练 / 评 / 规划 | 是（DeepTutor / Claude Code / Codex） |
| Heptabase | App 内 AI Skills + `heptabase-cli` | App 不限（无私有市场目录）；CLI 1 条 | 备 / 整理库 / 开课对象 | 是（Claude Code / Codex） |
| Claude 官方 | `academy-guide` + `k12-teacher-skills` | 1 + 4 | 备 / 评（教师侧） | 是 |
| 社区教学仓 | 见 [skills/education-community.md](../skills/education-community.md) | 7 个仓 | 教 / 练 / 做课 | 视仓而定 |
| Hyperknow / StudyFetch / YouLearn / Scholarly / Coursebox / X-Pilot / NotebookLM / Khanmigo / OpenTutor / Course Navigator | 产品内流程或按钮 | 0 份公开 SKILL.md | — | 否 |

ClassroomIO 有 MCP，不是教学 Skill。

## OpenMAIC 课内 Skill（agent-runtime，已点名）

路径前缀：`skills/agent-runtime/<name>/SKILL.md`。

| Skill | 更靠近哪一维 | 动作 |
|---|---|---|
| curriculum-planner | 一键成课 / 主动规划 | 备：排课程结构 |
| spiral-curriculum | 一键成课 | 备：螺旋上升大纲 |
| understanding-by-design | 一键成课 | 备：先目标后活动 |
| k12-core-literacy-planning | 一键成课 | 备：K12 素养课 |
| zone-of-proximal-development | 直播课堂 | 教：卡在最近发展区 |
| feynman-learning | 解题/出题 | 教：以教为学 |
| learning-to-learn | 主动规划 | 教：学法本身 |
| social-emotional-learning | 直播课堂 | 教：社会情感 |
| lecture-style | 直播课堂 | 演：讲授 |
| workshop-style | 直播课堂 | 演：工作坊 |
| vocational | 直播课堂 | 演：职业任务控件 |
| deep-interactive | 直播课堂 | 演：深互动场景 |
| deep-research | 资料摄入 | 备：先检索再上课 |
| fact-check | 资料摄入 | 评：核材料 |
| slide-dsl / slide-craft / stage-dsl / stage-design | 视觉知识结构 | 做课：幻灯与舞台 |
| pptx-import | 资料摄入 | 做课：吃 PPTX |
| page-clone / style-clone / teacher-style-clone | 一键成课 | 做课：复用页与教风 |
| pro-editing | 一键成课 | 做课：Pro 改页 |
| build-personal-skill | 可复用 Skill | 元：用户自写 Skill |
| openmaic（包装） | 全流程 | 安装 / 演示 / 生成课堂 / 二开 |
| @openmaic/importer | 资料摄入 | 导入契约 |

另：`dsh-openmaic` 提供 `openmaic-teach`（苏格拉底）及 generate/slide/widget/render 工具，不在主仓 skills/ 下。

## EduHub（DeepTutor 默认注册表）

首页写 74 skills / 4 tracks。目录页是前端渲染，本轮只核到精选三条，其余未逐条打开。

| Track | 覆盖 |
|---|---|
| Academics | 课内家教、练习、评分、备考 |
| Companions | 人设、动机、节律、规划 |
| Skills & Interests | 编程、乐器、烹饪、职业自学 |
| For Educators | 教师/家长：备课、课堂、教养 |

已点名：

| Skill | Track | 动作 | 对哪一维 |
|---|---|---|---|
| Socratic Tutor | Academics / Universal | 教（追问） | 解题/出题、直播课堂（对话版） |
| Flashcard Deck | Academics / Universal | 练（间隔重复） | 解题/出题 |
| Essay Feedback | Educators / 语文 | 评（量规、不代写） | 解题/出题 |

文档还提到考试蓝图、概念讲解，未打开逐条页。安装：`deeptutor skill install`，默认 hub 现为 EduHub（CLI Skill 文案仍可见 ClawHub 写法）。

## Heptabase

| 层 | 代表动作 | 对哪一维 |
|---|---|---|
| AI Tutor（产品，不是 SKILL.md） | 目标开课、课中带读、课末检查 | 一键成课、长期记忆 |
| App AI Skills | 主张图、顺页摘要、用户自描述工作流 | 视觉知识结构、可复用 Skill |
| heptabase-cli | 笔记/白板/思维导图/目标/课程课时 | 视觉知识结构、外部 Agent |

## Claude 官方教育 Skill → 产品能力缺口

这些 Skill 补的是「教师侧备课」，不是学生端运行时。自研若要对齐：

| 官方 Skill | 清单里谁最接近 | 谁明显没有 |
|---|---|---|
| k12-lesson-plan-creation | OpenMAIC curriculum-planner；ClassroomIO AI 大纲 | 学生端 SaaS 家教 |
| k12-lesson-differentiation | OpenMAIC 课内分层弱；ClassroomIO 机构向 | Hyperknow / StudyFetch |
| k12-lesson-prep | Heptabase「先读源」；OpenMAIC Pro 材料面板 | NotebookLM（只有问答） |
| k12-check-for-understanding | DeepTutor 出题；OpenTutor 形成性题型；Khanmigo 追问 | X-Pilot（纯视频） |
| academy-guide | 无对应产品 Skill | — |
| Learning Mode（产品模式，非文件） | EduHub Socratic Tutor；Khanmigo | 成课平台的数字人讲解 |

## 不会写 Skill 的产品，能力仍要对照

把按钮当成「锁死的 Skill」看，避免漏比：

| 产品 | 锁死流程（不是 Skill） | 缺的开放面 |
|---|---|---|
| Hyperknow | Orbie 抽截止日期、Deep Learn、cheatsheet/视频 | 不能把 Orbie 装进 Claude Code |
| StudyFetch | Spark.E + 闪卡/测验/Arcade | 不能换教学姿态文件 |
| YouLearn | 笔记 + 对话 + 播客 + 测验 | 同上 |
| Scholarly | 积分驱动的多形态创作 | 同上 |
| Coursebox | 文档→培训课+导师+SCORM | 教学姿态不可导出 |
| X-Pilot | 大纲/分镜→MP4 | 没有练习闭环 |
| NotebookLM | Studio 指南/音频/幻灯 | 没有课程对象 |
| Khanmigo | 苏格拉底 + Khan 内容库 | 不能吃任意 PDF 当主库 |
| OpenTutor | Block 工作区 + FSRS | 未见 SKILL.md |
| Course Navigator | 视频→字幕/笔记 | 上游工具，无教 |

## 自研时怎么用这张表

1. 要演课：抄 OpenMAIC 课内 Skill 的分工（planner / style / slide / interactive），不要只做一条「生成课堂」。
2. 要可安装教法：走 EduHub + Agent Skills 规范，四条 track 比单条 tutor prompt 完整。
3. 要源级视觉：Heptabase App Skill（主张→卡片→页级引用）比聊天里画 Mermaid 更接近知识库。
4. 要对齐教师产品：直接挂 `k12-teacher-skills`，不要自己发明教案格式。
5. 商业家教对标时，把它们的按钮映射到上表动作，再标「不可复用」。
