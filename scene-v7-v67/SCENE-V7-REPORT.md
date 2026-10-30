# Scene v7 多层动画候选

这一版把“主判定线”和“背景表演线”分开：两条主线保留音符、来向和读谱职责；四条背景线没有音符，只在场景边界附近短暂进入，做边缘斜线、分裂、脉冲、轨道回旋和淡出回收。

| 曲目 | 场景动作 | 样式族 | 背景线 | 音符身份 | 审计 |
| --- | ---: | --- | ---: | --- | --- |
| Demonkin | 95 | orbit 38 / pulse 17 / ribbon 36 / split 4 | 4 | 保留 | pass |
| Cristalisia.onoken | 95 | orbit 40 / pulse 15 / ribbon 34 / split 6 | 4 | 保留 | pass |
| Distorted Fate | 111 | orbit 48 / pulse 18 / ribbon 40 / snap 1 / split 4 | 4 | 保留 | pass |

音频只提供有界 cue 的进入时刻；当前音频控制门仍禁止用响度直接调幅度。背景线透明度上限为 0.28，所有动作在场景内回收到 0，不能变成隐藏判定线。

这仍是 candidate-only：它证明生成层拥有多层场景和回收机制，不等于三首歌已经通过真人全曲验收。

- [SCENE-V7-MANIFEST.json](SCENE-V7-MANIFEST.json)
- 每首歌的 `*-audit.json` 是机器审计，`*-choreography.json` 是动作来源和样式记录。
