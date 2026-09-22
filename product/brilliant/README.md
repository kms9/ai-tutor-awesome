# Brilliant

- 形态：商业交互课平台 + 课内导师 Koji（Web / iOS / Android）
- 链接：[官网](https://brilliant.org) · [帮助：交互件](https://brilliant.org/help/features/how-do-i-use-interactives-on-brilliant/) · [Koji](https://brilliant.org/help/features/how-does-koji-work/) · [教师计划](https://brilliant.org/educators/)
- 状态：相邻对照
- 注意：与设计工具 brilliant.design 不是同一产品

## 简介

专家写好的 STEM 交互画布，不是「资料进、整课出」。课由可拖、可改、可试的关卡组成：切线看斜率、天平解方程、滑块看概率、跟踪 Python 变量。卡住时家教 Koji 能看见当前交互件，只带思路、不直接给答案。深度中心是数学和编程，另有数据、科学、神经网络 / LLM、量子计算。教学过程锁在官方课里，不吃用户 PDF。

## 建议使用场景

适合：

- 把抽象概念变成手感：导数、向量、概率、电路、神经网络结构。
- 每天 10 分钟的 STEM 习惯，短课 + 连续天数。
- 成人回炉数学 / 编程，不为学分，要计算思维。
- 5–12 年级课前热身、课中探究、课后有反馈的练习（教师走 Educators）。
- 对照「画布感知、不代做」的导师姿态，写自己的 tutor Skill。

不适合：

- 要把自己的 PDF / 课件 / 网课变成课（去 DeepTutor / YouLearn / Hyperknow）。
- 要一节课被老师和同学演出来（去 OpenMAIC）。
- 要在白板上铺自己的主张和页级引用（去 Heptabase）。
- 要对齐课标、应试、学分、职业证书（去 Khan Academy / Coursera）。
- 要可安装 `SKILL.md`、自托管、换模型。

## Skill

无公开 Agent Skills。Koji 是产品内导师，装不进 Claude Code。

| 产品流程 | 动作 | 对应维度 |
|---|---|---|
| 交互关卡（拖、改、试、数学键盘） | 练 / 教 | 解题/出题、视觉知识结构 |
| Koji 看画布追问、高亮、改排布 | 教 | 解题/出题（苏格拉底，不代做） |
| Home 用自己的话问路 → 路由到课 | 规划 | 主动规划（弱） |
| Learning Path + Skills Check | 练 / 评 | 解题/出题、长期记忆 |
| 掌握度 → 个性化复习 | 练 | 主动规划 |

不能 fork、不能改触发条件。总表见 [capabilities/skill-map.md](../../capabilities/skill-map.md)。

## 能力对照

| 维度 | 本产品 |
|---|---|
| 资料摄入 | —（官方课；不吃用户 PDF / LMS） |
| 一键成课 | —（关卡手写；AI 只辅助实现，不过关卡设计） |
| 直播课堂 | — |
| 解题/出题 | 强：官方交互题 + Skills Check + 间隔复习；不是按你的考纲出题 |
| 主动规划 | 中：Path、按掌握度推下一课；不抢截止日期 |
| 长期记忆 | 中：掌握记录、家庭/教师仪表盘；不可审计 Memory Graph |
| 视觉知识结构 | 极强（课内画布 / 模拟）；不是用户知识库主张图 |
| 可复用 Skill | 无公开文件；Koji 锁在产品内 |
| 自托管 / 换模型 | 否 |
| 导出 | 弱：进度在账号；无证书、无学分、无 SCORM |

相对锚点：课内交互教具强于四锚点；资料摄入、成课、演课、可安装 Skill 都不是它的战场。姿态上近 Khanmigo，画布感知比 Khanmigo 深，学科面比 Khan 窄。

## 调研

巡查 2026-09-22。来源：brilliant.org 帮助中心、定价资源页、Educators、官方教法文。未登录后台。勿与 brilliant.design 混淆。

| 项 | 记录 |
|---|---|
| 体量口径 | 官方写千万级学习者、十万以上五星评价 |
| 课量 | 资源页写 40+ 交互课；数学最深，编程其次 |
| Koji | 几乎全部数学和编程课；能看交互件并改画布；免费仅预览 |
| 定价（美国网页 2026-08） | Free：每天约两课、课序锁定、Koji 预览；Premium $30/月或 $240/年。家庭 / 集团另计。评测里有过 $149/年等旧数字，以结算页为准 |
| 教师 | K–12 Educators 可免费开班（学生不能自己申请） |
| 安全 | kidSAFE / COPPA；第三方聊天与音频零留存 |
| 风险 | 免费很快见顶；订阅价是主要差评；不发证书；交互题质量未实机抽查 |

## 使用体验

未上手。下次试用记下：

- 日期 / 账号档（Free 或 Premium） / 平台（Web 或 App）
- 选一门微积分或 Python 课：一节里有几种交互件、能否不看讲解先做出来
- Koji：卡住时是否只问不给答案、会不会在画布上高亮
- Free 每天两课是否立刻见顶
- 教师仪表盘能看到哪些字段（若走 Educators）
