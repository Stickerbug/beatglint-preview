# Scene v18 可组合场景候选

本版是第一批真正经过“音符所有权场景图 → 确定性组合候选 → 承载/表演/引导事件 → 有界屏幕空间编译 → 原生 Phira”链路的可见候选。使用 `scene-candidate-02`，没有读取官谱动画数组，也没有训练。

## 原生渲染窗口

| 曲目 | 窗口 | 游戏线 | 空引导线 | 组合门 | 首玩门 | Flick 门 | 运动门 |
|---|---|---:|---:|---|---|---|---|
| demonkin | 8–10 秒 | 4 | 0 | `pass_structural` | `pass_structural` | `pass` | `diagnostic_clear` |
| cristalisiaonoken | 8–10 秒 | 4 | 0 | `pass_structural` | `pass_structural` | `pass` | `diagnostic_clear` |
| distortedfate | Flick 窗口 6.7–8.1 秒 | 4 | 2 | `pass_structural` | `pass_structural` | `pass` | `diagnostic_clear` |

## 关键结果

- 承载、表演和引导是独立事件通道；同一条承载线可以声明双重角色，`carrier_rest`/`hold_static` 也允许只承载而不表演。
- 三首曲目的游戏线渲染交叉为 0，同侧可见平行竞争为 0，首次游玩同侧目标竞争为 0。
- Distorted Fate 的两个 Flick 使用空载体会聚；命中前保持分离，命中附近才会聚，随后回收到画外。两个 Flick 均通过生命周期和引导几何审计。
- 引导曲线保留了中间关键帧，避免 Phigros 分段线性插值把延迟会聚变成过早直线靠近。

## 限制

- 这是 `candidate_only`，不是 promotion-ready；视频只覆盖诊断窗口。
- 当前几何编译器使用安全幅度上限和角色基线，仍需在 Demonkin、Cristalisia、Distorted Fate 之外验证更多音符组和音乐段落。
- 操作词汇数量是搜索空间覆盖量，不是官谱相似度或质量评分。

## 文件

- [SHA256 清单](SCENE-V18-MANIFEST.json)
- [组合候选摘要](../scene-v17-v71/SCENE-V17-CANDIDATE-SUMMARY.json)
- [v18c 接触图](v18c-contact-grid.jpg)
- [Distorted Fate Flick 密集接触图](distortedfate-v18c-dense-grid.jpg)
