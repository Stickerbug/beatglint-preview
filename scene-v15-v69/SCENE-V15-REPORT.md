# Scene v15：首次游玩可读性候选

这组窗口验证的是“同侧只保留一个可见游戏载体”的交接编译，而不是复刻官谱。四条游戏线仍然拥有真实音符；同一侧在有音符接近时只显示主线或次级线之一，只有在至少 0.65 秒的真实时间间隔中才交接。没有安全间隔的片段回退到主线。

| 曲目 | 音符 | 游戏线 | 背景线 | 结构门 | 首次游玩门 | 原生窗口 |
|---|---:|---:|---:|---|---|---|
| Demonkin | 1027 | 4 | 2 | pass | pass_structural | 8–10、15–17、30–32 秒 |
| Cristalisia.onoken | 911 | 4 | 2 | pass | pass_structural | 8–10、15–17、30–32 秒 |
| Distorted Fate | 911 | 4 | 2 | pass | pass_structural | 8–10、15–17、30–32 秒 |

首次游玩门使用 250 ms 反应假设，并额外检查了背景线竞争和渲染线段交叉；三曲均为 0。原生视频由公开优化版 Phira headless renderer 生成，仍需要真人在网页中逐段确认节奏、引导和整体风格，因此该候选不是 promotion-ready。

- [Demonkin 首次游玩审计](demonkin-player-audit.json) · [组合审计](demonkin-scene-audit.json) · [接触表](demonkin-contact.jpg)
- [Cristalisia 首次游玩审计](cristalisiaonoken-player-audit.json) · [组合审计](cristalisiaonoken-scene-audit.json) · [接触表](cristalisiaonoken-contact.jpg)
- [Distorted Fate 首次游玩审计](distortedfate-player-audit.json) · [组合审计](distortedfate-scene-audit.json) · [接触表](distortedfate-contact.jpg)

官方谱面只用于发现“声明线很多但同时可见线很少”的一般规律；本候选没有读取官方动画数组，也没有启动训练。
