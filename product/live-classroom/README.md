# Live Classroom

- 形态：开源 Web App（Next.js，MIT），自带 fal key 本地跑
- 链接：[GitHub](https://github.com/internetphysics/live-classroom) · [作者演示帖](https://x.com/internetphysics/status/2094848844987347409)
- 状态：观察

## 简介

打一个主题，LLM 一次规划出 12 个 5 秒节拍（旁白 + 画面），MiniMax H3 Max Turbo 在播出前几秒逐段渲染成 70 年代风卡通，放在 3D 教室里的 CRT 上播，老师是 meme 角色 Tung Tung Tung Sahur。看的同时可以在节目单里排下一课或追问，没排就 10 秒后自动进建议的后续课。它是「即时生成讲解视频」的样板，不吃资料、没有练习，作者自己说还很粗糙、经济上不划算。

## 建议使用场景

适合：

- 研究「生成式视频课堂」怎么做：一次规划 + 渲染缓冲 + 节目单排队的工程结构。
- 想看视频模型 prompt 怎么写给 fal 的改写器（编号角色表、看实际渲染用的 `expanded_prompt`）。
- 随口一个概念想先看一分钟动画讲解，能接受按课付费。

不适合：

- 讲义 / PDF 变讲解视频（去 X-Pilot，或 Hyperknow 的视频能力）。
- 要测验、追踪掌握度、跨会话记忆。
- 部署到 Vercel 类 serverless（README 明说会话和渲染会丢）。
- 不想为每节课付视频生成费。

## Skill

无公开 `SKILL.md`。流程写死在服务端：

| 产品流程 | 动作 | 对应维度 |
|---|---|---|
| 主题 → 一次 LLM 规划 12 节拍 | 做课 | 一键成课（1 分钟单课） |
| H3 Max Turbo 即时渲染 + 播放缓冲 | 教 | 视觉知识结构（视频） |
| 节目单排下一课 / 追问 | 规划 | 主动规划（弱：自动进建议后续课） |
| 换老师（改 `TEACHER` + 精灵图） | 做课 | — |

总表见 [capabilities/skill-map.md](../../capabilities/skill-map.md)。

## 能力对照

| 维度 | 本产品 |
|---|---|
| 资料摄入 | —（只吃一句主题） |
| 一键成课 | 中：1 分钟 12 节拍讲解视频 |
| 直播课堂 | 弱：3D 教室 + 单向播放，可排队追问，无对话 |
| 解题/出题 | — |
| 主动规划 | 弱：无排队时自动播建议后续课 |
| 长期记忆 | —（内存单例，无数据库） |
| 视觉知识结构 | 中：卡通讲解视频 |
| 可复用 Skill | 无 |
| 自托管 / 换模型 | 是：规划可选 Gemini / OpenRouter / Anthropic / OpenAI / OpenAI 兼容本地模型；视频固定 fal |
| 导出 | 渲染片段与 prompt 默认存本地 `recordings/` |

相对锚点：OpenMAIC 演的是有同学、白板、测验的整堂课，它只有一个会讲的视频老师；DeepTutor / Hyperknow 的资料摄入和练习它都没有；Heptabase 的主张图不在它的方向上。

## 调研

巡查 2026-11-05。来源：GitHub 仓库 README、作者 X 帖（2026-09-01）及其转述。未本地运行。

| 项 | 记录 |
|---|---|
| 版本 / 星标 | 仓库 2026-09-02 建，约 100 星，MIT |
| 定价 | 开源；每课 1 次规划调用（约 1 美分）+ 60 秒 480p H3 Max Turbo 视频，按 fal 价目计；`localCeilingCents` 可设单会话上限 |
| 依赖 | Node 22.6+、`FAL_KEY`（必需）、`GEMINI_API_KEY`（推荐）；需常驻进程（VM / Fly / Railway） |
| 风险 | 作者自评「rudimentary、not really economically feasible yet」；无公开托管 Demo；讲解准确性无核查环节（未核） |

## 使用体验

未上手。下次试用记下：

- 日期 / 规划模型 / fal 实际账单
- 一个理科概念（如核能）讲解是否有事实错误
- 首段开播延迟、中途是否卡顿
- 追问排队后的后续课是否接得上
