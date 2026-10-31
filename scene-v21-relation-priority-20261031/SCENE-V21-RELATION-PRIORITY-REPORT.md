# v21 结构关系优先候选

候选操作不再只按候选编号轮换：`handoff`、`split`、`merge`、`hold_continuity` 和 `chord_continuation` 会优先选择对应的交接、分裂、合并保护、Hold 连续和并行保护原子操作；同一语法内仍保持确定性变化。

| 曲目 | 窗口 | 操作种类 | 引导 | 自动审计 |
|---|---:|---:|---:|---|
| Demonkin | 8–10 s | 11 | 0 | role/motion/player/multigameplay 通过 |
| Cristalisia.onoken | 8–10 s | 11 | 0 | role/motion/player/multigameplay 通过 |
| Distorted Fate | 6.7–8.1 s | 13 | 2（dual_role 1、empty_actor 1） | Flick 2/2；其余结构门通过 |

视频由优化版 Phira 原生渲染器生成，960×540、30 fps、高仿官皮 v6.4。候选仍是 `candidate_only`；机器门通过不代表真人首次游玩或整曲审查已经完成。

[Manifest](V21-RELATION-PRIORITY-MANIFEST.json) · [Distorted Fate contact](distortedfate.v21c1-contact.jpg)
