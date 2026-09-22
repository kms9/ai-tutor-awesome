# 社区 / 产品自带：教育向 Agent Skills

巡查：2026-09-22。格式尽量是 Agent Skills（`SKILL.md` + 可选 references/scripts）。只收「教人」或「做课」。

## 产品自带

| 来源 | Skill | 链接 | 备注 |
|---|---|---|---|
| OpenMAIC | openmaic | https://github.com/THU-MAIC/OpenMAIC/blob/main/skills/openmaic/SKILL.md | 安装、Live Demo 访问码、生成课堂、`@openmaic/*` 二开 SOP；分阶段确认 |
| OpenMAIC | agent-runtime | https://github.com/THU-MAIC/OpenMAIC/tree/main/skills/agent-runtime | Pro workbench 持久会话 |
| OpenMAIC | 约 20 个课内工具 Skill | v1.0 发行说明 | 规划、幻灯、测验、互动、PBL、图、视频、语音、文件夹、材料、pptx、搜索；Settings 里按所有者管理 |
| DeepTutor | deeptutor-cli | https://github.com/HKUDS/DeepTutor/blob/main/SKILL.md | 配置、能力、知识库、Partners、记忆、会话、笔记本、Skill、启服务 |
| DeepTutor | EduHub 注册表 | https://eduhub.deeptutor.info/ | 约 72–74 个教学 Skill、4 条 track；默认可 `deeptutor skill install` |
| Heptabase | heptabase-cli | https://github.com/heptameta/heptabase-cli-skills | 笔记、白板、思维导图、目标、课程与课时 |
| Heptabase App | 用户自定义 AI Skills | 产品内，无统一公开仓 | 主张图、顺页摘要等阅读工作流 |
| ClassroomIO | MCP `@classroomio/mcp` | npm / 仓库 README | 不是教学 playbook，是系统集成 |

### EduHub 已点名（未穷尽）

来源：https://eduhub.deeptutor.info/ 首页精选 + 文档举例。

| Skill | 轨道 | 做什么 |
|---|---|---|
| Socratic Tutor | Academics / Universal | 用追问带理解，不直接给答案 |
| Flashcard Deck | Academics / Universal | 笔记/章节 → Q/A 与 cloze，可进 Anki |
| Essay Feedback | Educators / 语文 / K12 / 大学 | 按量规反馈，不代写 |
| Exam blueprint / 概念讲解 | 文档提及 | 尚未在本轮打开逐条页 |

## 社区教学 Skill

| 仓库 | 内容 | 链接 |
|---|---|---|
| bevibing/tutor-skills | `tutor-setup` 文档→Obsidian StudyVault；`tutor` 按概念测验与仪表盘 | https://github.com/bevibing/tutor-skills |
| malberich/skill-tutor | 把任意 Skill/领域变成带诊断与间隔重复的学习路径 | https://github.com/malberich/skill-tutor |
| cdmorozov/claude-tutors | tutor / math-tutor / programming-tutor：讲解 vs 练习分流 | https://github.com/cdmorozov/claude-tutors |
| mattpocock/skills `teach` | 多会话教学工作区：MISSION/RESOURCES/HTML 课、不信任模型内置知识 | https://github.com/mattpocock/skills |
| minicoursegenerator/skills-for-course-creators | 做课、角色扮演练习、培训分析；`edu-role-play` | https://github.com/minicoursegenerator/skills-for-course-creators |
| kevintsai1202/teaching-site-skills | 11 个 Skill：从零做章节化互动教学站 | https://github.com/kevintsai1202/teaching-site-skills |
| HughYau/AcademicForge `learn` | 学术理解模式：一步一问，发现 vs 直讲 | https://github.com/HughYau/AcademicForge |

## 元清单

| 仓库 | 用途 |
|---|---|
| https://github.com/kms9/ai-tutor-awesome | 本清单 |
| https://github.com/weibifan/ai-tutor-awesome | 另一份开源 AI 学习助手精选 |
| https://github.com/anthropics/skills | 官方规范与示例 |
| https://agentskills.io/specification | 跨产品 Skill 标准 |

## 收录规则

1. 必须能打开到 `SKILL.md` 或明确产品内 Skill 说明
2. 写清触发条件（description）和教学动作（教 / 练 / 备 / 评 / 做课）
3. 官方与社区分文件，未合并的 PR 不当作已发布
4. EduHub 其余 70 条、OpenMAIC 20 条课内 Skill 名称，下一轮逐条打开后再补
