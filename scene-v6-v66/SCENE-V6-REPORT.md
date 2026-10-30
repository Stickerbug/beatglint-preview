# Scene v6 时钟模式验证

| 曲目 | 音符保留 | 音频模式 | FlowPhi | 未规划 | 几何问题 |
|---|---|---|---:|---:|---:|
| demonkin | 是 | timing_only / 幅度禁用 | 1027/1027 | 0 | 0 |
| cristalisiaonoken | 是 | timing_only / 幅度禁用 | 911/911 | 0 | 0 |
| distortedfate | 是 | timing_only / 幅度禁用 | 911/911 | 0 | 0 |

v6 只允许 onset 边界作为场景时钟候选；当前全混音控制不足以调制动画幅度。
状态仍为 blocked，待优化 headless/native 视觉窗口和真人读谱复核。


## 优化 headless 窗口

三首歌各生成 10–12 秒和 30–32 秒两个 960×540、30fps、60 帧窗口；六个窗口均完成，stderr 无异常。视频 SHA 与窗口清单见 `SCENE-V6-MANIFEST.json`。
