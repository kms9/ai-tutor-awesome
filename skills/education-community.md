# 社区 / 产品自带：教育向 Agent Skills

格式尽量是 Agent Skills（`SKILL.md` + 可选 references/scripts）。只收「教人」或「做课」，不收泛开发 Skill。

## 产品自带

| 来源 | Skill | 链接 | 备注 |
|---|---|---|---|
| OpenMAIC | openmaic | https://github.com/THU-MAIC/OpenMAIC/blob/main/skills/openmaic/SKILL.md | 安装、生成课堂、二开 SOP |
| DeepTutor | 多枚 + EduHub | https://github.com/HKUDS/DeepTutor ；文档称 EduHub 为教育 Skill 注册表 | 苏格拉底导师、闪卡、文章反馈、考试蓝图、概念讲解 |
| Heptabase | heptabase-cli | https://github.com/heptameta/heptabase-cli-skills | 操作白板/卡片/课程/课时 |
| Heptabase App | 用户自定义 AI Skills | 产品内，无统一公开仓 | 主张图、顺页摘要等阅读工作流 |

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
| https://github.com/weibifan/ai-tutor-awesome | 开源 AI 学习助手 |
| https://github.com/anthropics/skills | 官方规范与示例 |
| https://agentskills.io/specification | 跨产品 Skill 标准 |

## 收录规则（草案）

1. 必须能打开到 `SKILL.md` 或明确产品内 Skill 说明
2. 写清触发条件（description）和教学动作（教 / 练 / 备 / 评 / 做课）
3. 官方与社区分文件，避免把 PR 写成已发布
4. DeepTutor EduHub、Heptabase 用户 Skill 市场若出现公开索引，在此加一节
