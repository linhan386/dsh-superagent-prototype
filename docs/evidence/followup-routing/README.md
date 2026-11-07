# Follow-up routing evidence

Captured from the live panel at Settings → Eval, 1440×1000, light theme, zh-CN, by driving the
real page with Chromium. Neither capture contains Feishu message content, credentials or private
threads: the view is the settings page only.

| | `before.png` | `after.png` |
| --- | --- | --- |
| Revision | `8c32a9d`, the commit before this ticket's work | `bd46f53`, this ticket's commit |
| Panel bundle | `lib/client.js` built from `8c32a9d` | `lib/client.js` built from `bd46f53` |
| Policy version | `dac0ada8` | `467728a7` |

`after.png` also shows this deployment switched to `主 Session 先判定` (main Session decides
first), so the selected segment differs as well as the presence of the control.

The only structural difference in the Policy block is the new **追问路由 / Follow-up routing**
control between the policy version and the accept rules. The version line, both accept rules, the
sources and the admission table are unchanged, which is the point of the default: nothing else
moves.
