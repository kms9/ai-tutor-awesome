# OpenMAIC

- 形态：开源自托管 / 官方云演示
- 团队：清华大学 THU-MAIC
- 协议：MIT
- 链接：[GitHub](https://github.com/THU-MAIC/OpenMAIC) · [演示](https://open.maic.chat) · [包装 Skill](https://github.com/THU-MAIC/OpenMAIC/blob/main/skills/openmaic/SKILL.md)
- 状态：重点对照

## 简介

Open Multi-Agent Interactive Classroom。主题或 PDF/PPTX 进，一节完整互动课出：幻灯、测验、HTML 模拟、PBL，AI 教师和 AI 同学讲解、讨论、在白板上写画。v1.0 起有 Pro workbench：对话规划、改页、从材料施工，会话可取消/恢复。课堂能导出 PPTX / HTML / ZIP。它解决的是「把一节课演出来」，不是跨学期家教。

## 建议使用场景

适合：

- 要把一节课演出来：老师、同学、白板、语音同时在场。
- 教研试用多智能体课堂，或基于 `@openmaic/*` SDK / OpenClaw Skill 二开。
- 可自托管、换模型（含 Ollama），要把生成结果拿去改幻灯。
- 从 IM（飞书 / Slack / Telegram）或 IDE 里触发生成课堂。

不适合：

- 只要闪卡刷题或一页纸 cheatsheet。
- 完全离线又不想跑 Node / 容器。
- 要跨学期可审计记忆（公开资料偏会话级）。
- 要机构 LMS、证书、合规分发（去 ClassroomIO / Coursebox）。

## Skill

公开 Skill 是这个清单里最完整的一套「做课 + 演课」playbook。

| 层 | 路径 | 做什么 |
|---|---|---|
| 包装 | `skills/openmaic` | 安装、Live Demo 访问码、生成课堂、`@openmaic/*` 二开；分阶段确认 |
| 运行时 | `skills/agent-runtime` | Pro workbench 持久会话 |
| 导入 | `packages/@openmaic/importer/SKILL.md` | 导入契约 |
| 姉妹 | [dsh-openmaic](https://github.com/THU-MAIC/dsh-openmaic) | DeepSeek Harness：generate / slide / widget / render + `openmaic-teach` |

课内 `skills/agent-runtime/<name>/SKILL.md`（本轮已点名 24 条）：

| 动作 | Skill |
|---|---|
| 备课结构 | curriculum-planner, spiral-curriculum, understanding-by-design, k12-core-literacy-planning |
| 教法 / 人设 | lecture-style, workshop-style, vocational, feynman-learning, learning-to-learn, social-emotional-learning, zone-of-proximal-development, teacher-style-clone |
| 互动深度 | deep-interactive, deep-research, fact-check |
| 幻灯 / 舞台 | slide-dsl, slide-craft, stage-dsl, stage-design, pptx-import, page-clone, style-clone, pro-editing |
| 元 | build-personal-skill |

产品 README 称「Course tools + 24 built-in skills」。用户自写 Skill 按所有者存在 Settings。对照总表见 [capabilities/skill-map.md](../../capabilities/skill-map.md)。

## 能力对照

| 维度 | 本产品 |
|---|---|
| 资料摄入 | 主题 / PDF / 材料面板 / .pptx 导入；可开 web search |
| 一键成课 | 极强：大纲→场景→整堂课；Pro 可边聊边改页 |
| 直播课堂 | 极强：AI 老师 + AI 同学 + 白板 + TTS/ASR + 测验/PBL |
| 解题/出题 | 有随堂测验与实时点评，不是模考引擎 |
| 主动规划 | 弱；有 curriculum-planner Skill，但不是抢日程的 Orbie |
| 长期记忆 | 会话 / runtime store，跨学期可审计弱于 DeepTutor |
| 视觉知识结构 | 课堂白板与幻灯，不是知识库主张图 |
| 可复用 Skill | 最强之一：包装 + 24 课内 + 用户 Skill + 外部 Agent |
| 自托管 / 换模型 | 是；演示站要 `sk-` 访问码 |
| 导出 | PPTX / HTML / Classroom ZIP；仓库演进中出现 MP4 管线 |

相对锚点：演课强于另外三个；记忆与备考规划弱于 DeepTutor / Hyperknow；源级卡片弱于 Heptabase。

## 调研

巡查 2026-09-22。来源：GitHub README / releases / `skills/**/SKILL.md`。未实机上课。

| 项 | 记录 |
|---|---|
| 仓库 | 约 38.5k star / 6.0k fork；`main` 当日仍有推送 |
| 版本 | 产品叙事以 v1.0.0（2026-08-27）为准；页面可见 v1.0.3。更早 v0.3.x 含 PBL v2、编辑器直接操作、MP4 管线 |
| 部署 | 云演示 `open.maic.chat` 需访问码；本地自备 provider key |
| 风险 | 生成耗时、中文语音、角色是否站得住、24 条 Skill 质量，均未实机验证 |

## 使用体验

未上手。下次试用记下：

- 日期 / 环境（云演示或 Docker） / 模型
- 输入：纯主题 vs PDF vs PPTX
- 生成时长、能否中途改一页
- AI 同学是否抢话、测验能否打断
- 导出 PPTX/HTML 能否打开再改
- 装一条课内 Skill 前后，生成课有无可见差别
