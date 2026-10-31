# v20 Flick 所属线修复

含 Flick 的多线和弦现在按 `note_to_actor` 选择真正拥有 Flick 的承载线；不会再把和弦的第一条线误当作目标。v20 保留 v19 的承载/表演/引导复合架构，并重新原生渲染相同窗口。

| 曲目 | 窗口 | 操作种类 | 引导 | Flick 门 |
|---|---:|---:|---:|---|
| Demonkin | 8–10 s | 11 | 0 | 无 Flick |
| Cristalisia.onoken | 8–10 s | 11 | 0 | 无 Flick |
| Distorted Fate | 6.7–8.1 s | 13 | 2（dual_role 1、empty_actor 1） | 2/2，错误 0 |

Distorted Fate 视频使用优化版 Phira 原生渲染器、960×540、30 fps、高仿官皮 v6.4。候选仍是 `candidate_only`；这是归属正确性与组合审计的修复证据，不是官谱复刻或最终真人可玩性结论。

[Manifest](V20-FLICK-OWNER-MANIFEST.json) · [Distorted Fate contact](distortedfate.v20c1-contact.jpg)
