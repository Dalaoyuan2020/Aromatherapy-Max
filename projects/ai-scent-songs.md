# AI “Scent Songs” 打印机（Devpost）

**状态：** 真实存在的原型（Devpost 项目，2025 年）

**链接：** https://devpost.com/software/a-printer-for-smell-ai-scent-songs

## 概述
Prompt-to-Scent Printer：把自然语言转成单一计划文件（plan.json），然后由硬件执行。

## AI / 软件部分
- 模型：gpt-oss-120b（开源权重）
- 流程：Prompt（偏好、时长、强度、敏感成分）→ 严格 JSON Schema 生成 plan.json
- plan.json 内容：
  - Recipe：精油、体积（µL）、分配到雾化器（A = 清新/明亮，B = 温暖/扎实）
  - Timeline：每分钟 duty cycle（功率）+ 阶段标签（intro → crossfade → finish）
  - 预/后冲洗体积、安全约束

## 硬件
- 注射器阵列：~100 个 2.5 ml 注射器 + 微线性执行器/注射泵
- 精度：±2 µL
- 3 轴运动控制：龙门架定位雾化器到注射器下加料，再回中心扩散
- 双雾化器：水基，独立 duty cycle，支持 crossfade 和分层
- 冲洗循环防止串味
- 安全：物理急停、通风提醒、强度上限、过敏列表

## 评估
非常接近「Agent 生成 + 硬件精确执行」的理想形态。结构化输出使得可重复、可调试。适合作为 DIY 参考。
