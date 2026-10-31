# v23 场景形状族

候选操作现在使用不同的有界路径：`split` 以横向分裂为主，`staggered_entry` 延迟进入，`handoff` 使用不对称交接轨迹，`parallel_guard` 以保护性角度变化为主，`hold_axis` 保持轴向，`hold_ribbon` 使用耦合的横纵路径。所有路径在事件边界回到基线，仍受屏幕空间与首次游玩门约束。

| 曲目 | 窗口 | 操作种类 | 几何 | 首次游玩/组合 | Flick |
|---|---:|---:|---|---|---|
| Demonkin | 8–10 s | 11 | candidate_only，错误 0 | pass_structural | 无 Flick |
| Cristalisia.onoken | 8–10 s | 11 | candidate_only，错误 0 | pass_structural | 无 Flick |
| Distorted Fate | 6.7–8.1 s | 13 | candidate_only，错误 0 | pass_structural | 2/2，错误 0 |

视频由优化版 Phira 原生渲染器生成，960×540、30 fps、高仿官皮 v6.4。形状族是通用参数化路径，不读取官谱动画数组；候选仍需要真人首次游玩和整曲验收。

[Manifest](V23-SHAPE-FAMILIES-MANIFEST.json) · [Demonkin contact](demonkin.v23c1-contact.jpg) · [Cristalisia contact](cristalisiaonoken.v23c1-contact.jpg) · [Distorted Fate contact](distortedfate.v23c1-contact.jpg)
