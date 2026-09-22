# Heptabase：能力拆解

Heptabase 不是「另一个 OpenMAIC」。底座是视觉知识库（白板 + 卡片 + PDF/视频），AI Tutor 和 AI Skills 叠在上面。对标时要拆开，不要整型比较。

官网：https://heptabase.com  
Wiki：https://wiki.heptabase.com  
Work with AI：https://wiki.heptabase.com/work-with-ai  
CLI Skills：https://github.com/heptameta/heptabase-cli-skills

## 1. 知识底座（Tutor 能站在上面的原因）

- 无限白板 + 嵌套白板：一个主题一张桌面，子题再拆子板
- 卡片：块编辑、双向链接、标签与属性
- 源材料：PDF 标注、YouTube 转写、Web Clipper、Journal
- 外部库：Readwise、Zotero
- Research a topic：上传 PDF/链接/图 → 自动建白板、解析、打开带引用的 Chat
- 全空间检索：关键词 + 语义，回答带卡片/页码/时间戳引用
- 回答可拖回白板变成卡片，学习痕迹留在空间里

含义：家教不是漂在聊天框里，而是和「你正在读、正在标、正在连」的同一块桌面共享上下文。

## 2. AI Tutor（约 2026 年 3–5 月公测后转正）

来源：官网 AI Tutor 页、Reddit 公测帖、创始人课例（西方哲学等）。

| 能力 | 具体表现 | 和三锚点怎么比 |
|---|---|---|
| 目标驱动开课 | 提出目标（系统学西方哲学、过司法考试），一起商量大纲 | 近 Hyperknow「把目标变成 1:1 课」；OpenMAIC 更偏一节课演出来 |
| 个性化大纲 | 按程度与偏好拆课、课时、目标 | DeepTutor Mastery Path / Hyperknow Deep Learn |
| 课中带读 | 按阶段生成/调出当前该读的材料，你只问不懂的 | Heptabase 独点：读的是知识库里的源，不是另开一个课件播放器 |
| 课末检查 | 结束前关键问题讨论，确认抓住核心 | 近形成性评价；弱于正式题库/FSRS |
| 进度与续课 | 课程/课时列表，Welcome back 接上次 | DeepTutor 记忆层更可审计；Heptabase 进度绑在课程对象上 |
| 和笔记一体 | 高亮、批注、卡片与课同步 | OpenMAIC/多数 SaaS 家教做不到这块 |

产品哲学（官方口径）：人负责读、想、问、练、做决定；Agent 负责教、导研究、整理库、规模化执行。

## 3. AI Skills（约 2026-08 发布，和 Tutor 不同层）

Skill = 可复用工作流，教 Agent 怎么做一件具体任务，不是一堂课。

官方演示：

- 对 300 页哲学书「抽出所有主张并可视化关系」→ 白板上多张思维导图，每张卡片一条主张并链回 PDF 原文
- 同一本书也可改成「按页序拆成连续摘要卡片」
- 用户描述流程，Agent 帮写成可改、可复用的 Skill，用 slash command 再跑

含义：Tutor 管「跟我学一门课」；Skills 管「按我的阅读法处理这份源」。对做教育 Agent 的人，第二层往往更可迁移。

## 4. Heptabase CLI Skills（Agent Skills 标准）

仓库：https://github.com/heptameta/heptabase-cli-skills

`heptabase-cli`：笔记、journal、标签、卡片、文件、白板结构与布局、思维导图、截图、目标、课程与课时。

可给 Claude Code / Codex 等兼容 Agent 用。这是「把 Heptabase 空间交给外部 Agent 操作」的接口，和 App 内 AI Skills 是姐妹关系。

## 5. 对标时建议盯的缺口

若自研要「像 Heptabase 那样教」，清单里至少要有这些格：

1. 源材料进空间（PDF 页级引用，不只整篇 RAG）
2. 可视结构（白板/卡片/主张图），不只线性聊天
3. 目标 → 大纲 → 课时对象（可续、可回看）
4. 课中带读 + 课末检查
5. 可复用阅读/整理 Skill（主张图、顺页摘要、概念卡）
6. 外部 Agent 能操作同一知识空间（CLI / MCP / Skills）

OpenMAIC 强在第 4 的「演课」；DeepTutor 强在记忆与多模式；Hyperknow 强在主动规划与备考资产；Heptabase 强在 1+2+5。
