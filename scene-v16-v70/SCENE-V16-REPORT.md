# Scene v16：Hold 安全的首次游玩候选

这版沿用 v15 的同侧独占交接，并把 Hold 结束时间纳入短句切分。上一条线仍有 Hold 身体时不会回收或换线；所有交接都需要真实时间间隔。

| 曲目 | 音符 | 游戏线 | 背景线 | 组合门 | Hold 门 | 首次游玩门 |
|---|---:|---:|---:|---|---|---|
| Demonkin | 1027 | 4 | 2 | pass | 0 errors | pass_structural |
| Cristalisia.onoken | 911 | 4 | 2 | pass | 0 errors | pass_structural |
| Distorted Fate | 911 | 4 | 2 | pass | 0 errors | pass_structural |

视频为优化版 Phira headless renderer 的 960×540、30 fps 原生窗口。机器门不能替代真人读谱，候选仍需在网页中检查音符压力、Flick 引导、动画节奏和整体风格。

- [Demonkin 视频接触表](demonkin-contact.jpg) · [首次游玩审计](demonkin-player-audit.json) · [组合/Hold 审计](demonkin-scene-audit.json)
- [Cristalisia 视频接触表](cristalisiaonoken-contact.jpg) · [首次游玩审计](cristalisiaonoken-player-audit.json) · [组合/Hold 审计](cristalisiaonoken-scene-audit.json)
- [Distorted Fate 视频接触表](distortedfate-contact.jpg) · [首次游玩审计](distortedfate-player-audit.json) · [组合/Hold 审计](distortedfate-scene-audit.json)
