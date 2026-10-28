# AI 原生 / Agent 控制概述

## 核心思路
把「生成」与「执行」解耦：
- Agent / LLM 负责理解用户意图（自然语言、照片、记忆对话），生成结构化计划（JSON）
- 硬件只接收计划并精确执行（泵时序、duty cycle、冲洗）

## 增加随机性与深度
- 提高采样温度 / 多次采样
- 「惊喜模式」：在约束内引入非预期香调
- 多轮 Agent：基础配方 → 情绪映射 → 时间演变 → 用户反馈迭代
- 用户偏好记忆与约束（过敏清单、强度上限）

## 参考软件
- sniff_ai（GitHub）：NLP + Agent 式把自然语言/诗歌转成专业香水金字塔配方
- Smell Engine（GitHub）：虚拟环境气味合成框架

## 建议 JSON Schema 示例
```json
{
  "recipe": [
    {"oil": "lavender", "volume_ul": 50, "atomizer": "A"},
    {"oil": "sandalwood", "volume_ul": 30, "atomizer": "B"}
  ],
  "timeline": [
    {"minute": 0, "A_duty": 0.8, "B_duty": 0.2, "stage": "intro"},
    {"minute": 5, "A_duty": 0.4, "B_duty": 0.6, "stage": "crossfade"}
  ],
  "constraints": {"max_intensity": 0.7, "avoid": ["citrus"]}
}
```
