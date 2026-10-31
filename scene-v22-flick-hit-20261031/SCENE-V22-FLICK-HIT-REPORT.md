# v22 Flick 命中时刻曲线

双角色 Flick 载体不再在提前量中点达到峰值，而是命中前单调靠近、命中达到峰值、命中后衰减；空演员会聚仍保留延迟关键帧。这样视觉引导与判定时刻一致，不需要让 Flick 从片段开头悬停。

| 曲目 | 窗口 | 引导 | Flick 门 | 状态 |
|---|---:|---:|---|---|
| Demonkin | 8–10 s | 0 | 无 Flick | candidate_only |
| Cristalisia.onoken | 8–10 s | 0 | 无 Flick | candidate_only |
| Distorted Fate | 6.7–8.1 s | 2（dual_role 1、empty_actor 1） | 2/2，错误 0 | candidate_only |

视频由优化版 Phira 原生渲染器生成，960×540、30 fps、高仿官皮 v6.4。此次是 Flick 时序与归属修复证据，仍需真人首次游玩和整曲审查。

[Manifest](V22-FLICK-HIT-MANIFEST.json) · [Distorted Fate contact](distortedfate.v22c1-contact.jpg)
