# Scene v17：Flick 会聚引导候选（首次游玩组合门）

这版在 v16 四线音符承载和 Hold 安全交接的基础上，为真实 Flick 增加短时、无音符的视觉引导载体。引导从画外进入，在命中前保持分离，命中附近与所属判定线会聚，命中后退回画外；它不会新增判定、音符或第二次击打。

所有三首歌都从独立生成候选编译；没有读取官谱动画数组，没有把官谱动画作为输入，也没有启动训练。机器门只证明结构一致性，仍需真人首次游玩检查。

| 曲目 | 音符 | 总线数 | Flick/引导 | 首次游玩门 | 引导生命周期 | 组合门 |
|---|---:|---:|---:|---|---|---|
| demonkin | 1027 | 6（4 游戏线） | 0/0，回退 0 | pass_structural | pass | pass_structural |
| cristalisiaonoken | 911 | 6（4 游戏线） | 0/0，回退 0 | pass_structural | pass | pass_structural |
| distortedfate | 911 | 7（4 游戏线） | 2/2，回退 0 | pass_structural | pass | pass_structural |

## 首次游玩审计重点

| 曲目 | 同侧近目标 | 可见平行竞争 | 背景竞争 | 迟到次级线 | 声明的引导近接 |
|---|---:|---:|---:|---:|---:|
| demonkin | 0 | 0 | 0 | 0 | 0 |
| cristalisiaonoken | 0 | 0 | 0 | 0 | 0 |
| distortedfate | 0 | 0 | 0 | 0 | 7 |

## 原生 Phira 窗口

使用 `phira-render-beatglint` resident renderer，960×540、30 fps；Distorted Fate 的两个 Flick 窗口使用修正后的“命中后回收到目标相反画外侧”逻辑重新渲染。

- **demonkin**：`demonkin.v17-8-10.mp4` · `demonkin.v17-15-17.mp4` · `demonkin.v17-30-32.mp4`
- **cristalisiaonoken**：`cristalisiaonoken.v17-8-10.mp4` · `cristalisiaonoken.v17-15-17.mp4` · `cristalisiaonoken.v17-30-32.mp4`
- **distortedfate**：`distortedfate.v17-6.7-7.9.mp4` · `distortedfate.v17-8-10.mp4` · `distortedfate.v17-15-17.mp4` · `distortedfate.v17-25.7-26.9.mp4` · `distortedfate.v17-30-32.mp4`

## 场景图结构

本版同时生成只读的 `beatglint_scene_graph_v1`，把音符承载、表演和引导作为不同功能记录；它不读取判定线动画数组。

| 曲目 | 音符组 | 多线组 | 引导义务组 | 双重功能候选 |
|---|---:|---:|---:|---:|
| demonkin | 755 | 118 | 0 | 416 |
| cristalisiaonoken | 667 | 100 | 0 | 389 |
| distortedfate | 667 | 120 | 2 | 399 |

## 组合候选（未渲染）

场景图已为每首曲目生成 4 个确定性组合候选；候选只记录原子操作和演员功能，仍未写入最终动画坐标。

| 曲目 | 候选数 | 每个候选的操作词汇数 | 缺失 Flick 引导组 | 状态 |
|---|---:|---:|---:|---|
| cristalisiaonoken | 4 | 3/9/9/9 | 0/0/0/0 | `candidate_search_only` |\n| demonkin | 4 | 3/9/9/9 | 0/0/0/0 | `candidate_search_only` |\n| distortedfate | 4 | 4/11/10/10 | 0/0/0/0 | `candidate_search_only` |\n
操作词汇数是搜索空间覆盖量，不是质量评分；所有候选仍需要真实 Phira 渲染、屏幕空间、首次游玩、FlowPhi 和回收审计。

- [组合候选摘要](SCENE-V17-CANDIDATE-SUMMARY.json)

## 运动门

游戏线使用原有速度/位移/连续性门；Flick 载体的快速画外回收按单独的 recycle 策略审计，不把它误报成游戏线异常。

| 曲目 | 游戏线最大 y 速度 | Flick 载体最大 y 速度 | 运动门 |
|---|---:|---:|---|
| demonkin | 0.0075 | 0.0000 | diagnostic_clear |
| cristalisiaonoken | 0.0073 | 0.0000 | diagnostic_clear |
| distortedfate | 0.0097 | 20.2500 | diagnostic_clear |

## 状态和限制

- 当前状态：`candidate_only`，不是 promotion-ready。
- 引导线是临时空载体，不能替代复杂作者化表演；重叠 Flick 超过有限载体池时会显式回退。
- 机器审计使用中心线和 alpha；精确 sprite 外接范围、视觉遮挡、手部运动和音乐贴合仍须真人检查。
- 当前证据只覆盖这三个诊断窗口，不宣称任意歌曲已达到官谱级。

## 文件

- [demonkin 场景图](demonkin.v17.scene-graph.json)
- [demonkin 接触表](demonkin-v17-contact.jpg) · [demonkin Flick 审计](demonkin-v17.flick.audit.json) · [demonkin 首次游玩审计](demonkin-v17.player.audit.json) · [demonkin 组合审计](demonkin-v17.scene.audit.json)
- [cristalisiaonoken 场景图](cristalisiaonoken.v17.scene-graph.json)
- [cristalisiaonoken 接触表](cristalisiaonoken-v17-contact.jpg) · [cristalisiaonoken Flick 审计](cristalisiaonoken-v17.flick.audit.json) · [cristalisiaonoken 首次游玩审计](cristalisiaonoken-v17.player.audit.json) · [cristalisiaonoken 组合审计](cristalisiaonoken-v17.scene.audit.json)
- [distortedfate 场景图](distortedfate.v17.scene-graph.json)
- [distortedfate 接触表](distortedfate-v17-contact.jpg) · [distortedfate Flick 审计](distortedfate-v17.flick.audit.json) · [distortedfate 首次游玩审计](distortedfate-v17.player.audit.json) · [distortedfate 组合审计](distortedfate-v17.scene.audit.json)
