# v19 承载/表演/引导复合候选

这一版验证的是功能复用，而不是增加固定判定线：同一条线可以承载音符并做有界表演或引导，空演员只能表演/引导，不能拥有判定。几何基准来自角色审计或固定中性姿态，源谱面的移动/旋转数组没有参与生成。

## 原生预览

| 曲目 | 窗口 | 组合 | 引导 | 自动门 |
|---|---:|---|---:|---|
| Demonkin | 8–10 s | candidate-01，11 种操作 | 0 | role pass；geometry candidate_only；player/multigameplay pass_structural |
| Cristalisia.onoken | 8–10 s | candidate-01，11 种操作 | 0 | role pass；geometry candidate_only；player/multigameplay pass_structural |
| Distorted Fate | 6.7–8.1 s | candidate-01，13 种操作 | 2（1 dual_role + 1 empty_actor） | Flick pass；role pass；geometry candidate_only；player/multigameplay pass_structural |

视频由优化版 Phira 原生渲染器生成，960×540、30 fps、高仿官皮 v6.4。Distorted Fate 窗口含两个 Flick：一个由承载线自身做受限脉冲引导，另一个由无音符临时线延迟会聚；两种模式分别审计，不把承载线误判为空线，也不把空线变成判定。

## 读法与限制

- `candidate-01` 不是最终发布谱面，仍需真人首次游玩和整曲审查。
- `pass_structural` 只表示机器结构门通过；它不代表动画已经好看，也不代表官谱级复刻。
- 这次的可见变化是功能组合与来源链，不是把官谱动画数组作为输入。

[Manifest](V19-ROLE-MULTIPLEX-MANIFEST.json) · [Demonkin contact](demonkin.v19c1-contact.jpg) · [Cristalisia contact](cristalisiaonoken.v19c1-contact.jpg) · [Distorted Fate contact](distortedfate.v19c1-contact.jpg)
