# Claude / Anthropic 官方教育相关 Skill

巡查：2026-09-22。官方分层未变。

Skill 是带 `SKILL.md` 的文件夹（Agent Skills 开放标准：https://agentskills.io/specification）。  
官方教育向分三层：**通用官方仓**、**K-12 教师专用仓**、**产品内能力（不一定是 Skill 文件）**。

## A. anthropics/skills（官方示例仓）

https://github.com/anthropics/skills（体量很大，示例 + 规范 + 文档 Skill）

教育/学习直接相关：

| Skill | 路径 | 做什么 |
|---|---|---|
| academy-guide | `skills/academy-guide` | 用户问「怎么用 Claude / 怎么学 AI」时，对照 Claude Academy 课程/教程/用例再推荐，禁止编造 Academy 内容 |

文档与制作课资产相关（教师/教研常用，但不是「家教」）：

| Skill | 路径 |
|---|---|
| docx / pptx / pdf / xlsx | 官方文档读写 |
| doc-coauthoring | 共写文档 |
| skill-creator | 教 Claude 帮你写新 Skill |
| web-artifacts-builder | 交互网页/教具原型 |
| canvas-design / frontend-design | 视觉与前端 |

其余（brand-guidelines、internal-comms、mcp-builder、claude-api、theme-factory 等）偏办公与工程，教育清单里标「非教学核心」即可。

Claude Academy 本身：https://academy.claude.com  
配套产品能力：Learning Mode（苏格拉底追问，帮助自答，不是独立 SKILL.md）。

## B. anthropics/k12-teacher-skills（官方教育 Skill 正源）

https://github.com/anthropics/k12-teacher-skills  
公告：https://www.anthropic.com/news/claude-for-teachers  
产品：https://claude.com/solutions/teachers  
协议：Apache-2.0，与 Learning Commons 共创，对齐美国各州课标图谱连接器。

| Skill | 做什么 |
|---|---|
| k12-lesson-plan-creation | 课标对齐的可上课教案，可挂教师已有教材 |
| k12-lesson-differentiation | 同一课拆低于/符合/高于水平及特殊需要版本，核心内容一致 |
| k12-lesson-prep | 已有教案的备课搭档：先把学生关键任务做一遍，留教师备忘 |
| k12-check-for-understanding | 1–3 道形成性检测（数学课标），干扰项来自已知迷思，教师指南按作答分流 |

安装（非 Teachers 账号）：

```
git clone https://github.com/anthropics/k12-teacher-skills
claude plugin marketplace add ./k12-teacher-skills
claude plugin install k12-education@k12-teacher-skills
```

仓内还有 `evals/`：官方如何评这些 Skill，做教育 Agent 时值得当评测样板。

## C. 官方「教育」但不是 Skill 文件

| 名称 | 形态 | 链接 | 记什么 |
|---|---|---|---|
| Claude Learning Mode | 产品模式 | https://claude.com/solutions/education | 追问、不直接给答案 |
| Claude Academy | 课程站 | https://academy.claude.com | AI 流畅度、平台 101 |
| Claude for Teachers | 美国 K-12 教师产品 | 见上 | 预装 B 组 Skill + Learning Commons 连接器 |
| 教师连接器生态 | MCP/连接器 | ASSISTments, Brisk, Canva Education, Coteach, Diffit, Eedi, MagicSchool, Snorkl, TeachFX | 出题、分层阅读、课堂活动 |
| Agent Skills 规范 | 标准 | https://agentskills.io/specification | 自研教育 Skill 应对齐这个格式 |

## D. 官方仓里出现过、尚未合入的教育向 PR（观察）

- `structured-learning`（PR #790，天津大学）：简/详双模式教知识点、应试要点。未进 main，作社区信号，不当官方。
