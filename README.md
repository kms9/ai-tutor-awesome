# AI Tutor Awesome

基于 AI / Agent 辅助学习的产品与工具收集。

仓库：https://github.com/kms9/ai-tutor-awesome

最近巡查：2026-09-22（公开页与仓库，未实机登录）。体验栏一律待补。

本仓库只做一件事：把「能把资料变成可学过程」的产品放在一起，并给每个产品留调研与使用体验的位置。问答机器人、纯题库、纯录播课平台默认不收录。

## 怎么用这份清单

1. 先看下面的索引，按场景选产品。
2. 点进 `product/<名称>/` 看简介、场景（含不适合）、Skill、能力对照、调研、体验占位。
3. 跨产品维度看 [capabilities/capability-map.md](capabilities/capability-map.md)；Skill 和能力怎么分看 [capabilities/skill-map.md](capabilities/skill-map.md)。
4. 新加产品：复制 [product/_TEMPLATE.md](product/_TEMPLATE.md)，并在本 README 的索引表里加一行。

## 目录约定

```
README.md                 本页：总索引
product/_TEMPLATE.md      单个产品页字段
product/<slug>/README.md  简介、场景、Skill、能力对照、调研、体验
skills/                   教育向 Agent Skills（Claude 官方与社区）
capabilities/             跨产品能力对照、Heptabase 拆解、Skill 对照
```

每个产品目录后续可以继续放：截图、试用记录、对比笔记、Skill 摘录。不要把长文写进本 README。

## 产品索引

### 重点对照

这四个是当前的锚点：互动课堂、Agent 家教、主动备考、视觉知识库家教。

| 产品 | 简介 | 建议场景 | 详情 |
|---|---|---|---|
| OpenMAIC | 清华开源多智能体互动课堂。主题或 PDF 一键生成有 AI 老师、AI 同学、白板、测验、PBL 的整堂课。 | 要把一节课「演出来」；教研试用多智能体课堂；可自托管、可换模型。不适合只要闪卡或跨学期记忆。 | [product/openmaic](product/openmaic/README.md) |
| DeepTutor | 港大开源 Agent 原生学习工作区。对话、解题、出题、研究、可视化共享同一会话与记忆。 | 长期跟学、文献/教材进知识库、要可审计记忆与本地部署。不适合只要课堂演出。 | [product/deeptutor](product/deeptutor/README.md) |
| Hyperknow | 商业主动式学习 Agent。资料变成 1:1 课程、cheatsheet、练习和讲解视频，可接学校 LMS。 | 备考赶进度、要系统主动规划、不自托管也行。不适合要公开 Skill 或自托管。 | [product/hyperknow](product/hyperknow/README.md) |
| Heptabase | 视觉知识库上的 AI Tutor + AI Skills。目标开课、课中带读自己的源，主张可铺在白板上。 | 深度主题研究、读书与笔记一体、要「主张图 / 页级引用」。不适合演课或机构 LMS。 | [product/heptabase](product/heptabase/README.md) |

### 开源 / 可自托管

| 产品 | 简介 | 建议场景 | 详情 |
|---|---|---|---|
| OpenTutor | 本地优先自适应学习工作区。上传资料后生成笔记、闪卡、测验和导师，支持 FSRS。 | 数据不能出本机；只要复习闭环，不要完整课堂 UI。 | [product/opentutor](product/opentutor/README.md) |
| Course Navigator | 网课视频转可检索文本、大纲和摘要。 | 先消化已有视频课，再交给家教或课堂系统。 | [product/course-navigator](product/course-navigator/README.md) |
| ClassroomIO | 开源 LMS，带 AI 大纲和课程交付。 | 机构要托管和分发，不需要 AI 同学实时演课。 | [product/classroomio](product/classroomio/README.md) |

### 商业学生端

| 产品 | 简介 | 建议场景 | 详情 |
|---|---|---|---|
| StudyFetch | 课件生成闪卡/测验，家教 Spark.E 基于你的材料回答。 | 大学生日常复习，要低门槛 Quizlet 替代。 | [product/studyfetch](product/studyfetch/README.md) |
| YouLearn | YC 项目。PDF / YouTube / 幻灯片变成笔记、对话家教、测验和播客。 | 课业材料杂、想边听边问、接受 SaaS。 | [product/youlearn](product/youlearn/README.md) |
| Scholarly | 家教 + 间隔重复 + 模考 + 音视频概览 + 思维导图。 | 想把多种复习形态收在一个订阅里。 | [product/scholarly](product/scholarly/README.md) |

### 成课与相邻工具

| 产品 | 简介 | 建议场景 | 详情 |
|---|---|---|---|
| Coursebox | 文档/视频/链接生成带测验和导师的课，并带简易 LMS。 | 企业培训、需要快速出可交付课程。 | [product/coursebox](product/coursebox/README.md) |
| X-Pilot | PDF/PPT 生成可核验的讲解视频课。 | 要讲义变视频、强调少幻觉、可导出 MP4。 | [product/x-pilot](product/x-pilot/README.md) |
| NotebookLM | 源材料问答、学习指南、音频对话。 | 只要基于我的 PDF 问得准，先不需要教学运行时。 | [product/notebooklm](product/notebooklm/README.md) |
| Khanmigo | Khan Academy 苏格拉底家教。 | 对照「成熟教辅家教」的教学姿态，不作为自托管方案。 | [product/khanmigo](product/khanmigo/README.md) |
| Brilliant | 专家写好的 STEM 交互画布 + 课内导师 Koji。拖切线、改天平、跟踪代码，不吃用户 PDF。 | 把抽象概念练成手感；每天短课；对照「看见画布、不代做」的导师。不适合自有课件成课。 | [product/brilliant](product/brilliant/README.md) |

## 按场景选

| 你更想做的事 | 先看 |
|---|---|
| 一节课被老师和同学讲出来 | OpenMAIC |
| 跨周的解题、出题、研究 | DeepTutor |
| 考试前主动排计划、出 cheatsheet | Hyperknow |
| 在白板上看懂一本书/一个领域 | Heptabase |
| 资料不出机器 | OpenMAIC / DeepTutor / OpenTutor |
| 上传课件就刷卡和测验 | StudyFetch / YouLearn / Scholarly |
| 给组织做培训课 | Coursebox / ClassroomIO |
| 讲义变成讲解视频 | X-Pilot、Hyperknow 的视频能力 |
| 可安装的教法 Skill | DeepTutor EduHub、OpenMAIC 课内 Skill、Claude k12-teacher-skills |
| 源材料变成主张图 | Heptabase App Skills |
| 把抽象概念练成可操作手感 | Brilliant |
| 对照「不代做」的课内导师 | Khanmigo / Brilliant Koji |

更细的维度对照见 [capabilities/capability-map.md](capabilities/capability-map.md)。Skill 对照见 [capabilities/skill-map.md](capabilities/skill-map.md)。

## Skills

产品是「别人做好的学习软件」；Skill 是「教 Agent 怎么教 / 怎么备课」的 playbook。两者分开收。

- [Claude 官方教育相关 Skill](skills/official-claude.md)
- [社区与产品自带教育 Skill](skills/education-community.md)
- [Skill 和能力对照](capabilities/skill-map.md)

## 收录标准

满足至少两条再进索引：

- 能吃进 PDF / PPT / 视频 / 知识库，而不是只靠模型记忆
- 能产出课、测验、闪卡、讲解或可视化结构
- 有教学过程：讲解、追问、练习、规划、课堂，而不止一次摘要

## 维护

- 索引只保留一行简介 + 场景 + 链接；细节写进对应产品目录。
- 每个产品页固定六段：简介、建议使用场景（含不适合）、Skill、能力对照、调研、使用体验。
- 试用后把日期、账号类型、模型、结论写进该产品目录，不要只改心情化形容词。
- 官方 Skill 与社区 Skill 分文件，未合并的 PR 不当作已发布。
