# OpenMAIC

- 形态：开源自托管 / 官方云演示
- 团队：清华大学 THU-MAIC
- 协议：MIT
- 链接：[GitHub](https://github.com/THU-MAIC/OpenMAIC) · [演示](https://open.maic.chat) · [Skill](https://github.com/THU-MAIC/OpenMAIC/blob/main/skills/openmaic/SKILL.md)
- 状态：重点对照

## 简介

Open Multi-Agent Interactive Classroom。主题或资料进，一节完整互动课出：幻灯片、测验、HTML 模拟、PBL，AI 教师和 AI 同学讲解、讨论、在白板上写画。v1.0（2026-08-27）加上 Pro workbench：对话规划、改页、从材料施工，会话可取消/恢复。仓库内有 `openmaic` 与 `agent-runtime` 两套 Agent Skills；产品内另有约 20 个课程工具 Skill。

## 建议使用场景

- 要把一节课演出来：老师、同学、白板、语音同时在场。
- 教研试用多智能体课堂，或基于 `@openmaic/*` SDK 二开。
- 可自托管、换模型（含 Ollama），可导出 PPTX / HTML。
- 不适合：只要闪卡刷题；完全离线又不想跑 Node；要跨学期可审计记忆（会话级偏多）。

## 调研（巡查 2026-09-22）

| 项 | 记录 |
|---|---|
| 仓库活跃 | `main` 当日仍有提交；约 38.5k star / 6k fork |
| 版本 | v1.0.0（2026-08-27）：Pro workbench、持久 Agent runtime、材料面板、.pptx 导入 |
| 姥妹仓 | MAIC-UI、MAIC-Core、dsh-openmaic、Awesome-AI-Era-Edu |
| Skill | `skills/openmaic`：安装/演示/二开 SOP，强调分阶段确认；`skills/agent-runtime`：Pro 会话运行时。产品内约 20 个课程工具 Skill（规划、幻灯、测验、PBL、图、视频、语音） |
| 部署 | 云演示需访问码（`sk-`）；本地需自备 provider key |
| 风险 | 生成耗时、中文语音、课堂角色是否站得住，均未实机验证 |

来源：GitHub README / v1.0.0 说明 / `skills/openmaic/SKILL.md`。

## 使用体验

未上手。下次试用请记下：环境（云/Docker）、模型、输入材料、生成时长、互动是否可打断、导出是否能拿去改。
