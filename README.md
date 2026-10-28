# 香薰疗法 Max (Aromatherapy-Max)

**目标：收集、整理与评估当前已存在的「精细定制化香味 / AI 原生香薰机」硬件与软件方案。**

仓库名称灵感来源于「1000 万以内最好的香薰机」与「香薰疗法 Max」。

所有内容均基于公开搜索结果与项目页面，列出来供参考与进一步验证。部分项目为原型 / Hackathon / 艺术装置，并非已商业化量产产品。

## 仓库结构

- `README.md` — 本文件（总览）
- `projects/` — 各个具体方案详细说明
- `printers/` — 开源 DIY 打印机 / 喷头 / 液体分配方案
- `hardware/` — 硬件组件与开源参考
- `ai-agent/` — AI / Agent 控制思路与软件参考
- `sources.md` — 原始链接与引用

## 核心方案列表

### 1. AI “Scent Songs” 打印机（Devpost）
- **状态：** 真实存在的 Hackathon / 研究原型
- **核心能力：** 自然语言 Prompt → LLM (gpt-oss-120b) 生成 `plan.json`（配方 + 时间线）→ 硬件执行
- **硬件：** ~100 个注射器阵列 + 微线性执行器，3 轴龙门架，双雾化器（A/清新、B/温暖），微升级（±2 µL）精度
- **AI 特点：** 严格 JSON Schema，支持 crossfade、阶段控制、冲洗防串味
- **详情：** 见 `projects/ai-scent-songs.md`

### 2. MIT Anemoia Device（气味记忆机器）
- **状态：** MIT Media Lab 原型（真实存在）
- **核心能力：** 照片 → VLM 描述 + 用户旋钮调整（主体 / 生命周期 / 情绪）→ 泵混合
- **硬件：** 约 50 种香味储液 + 泵，秒级增量交付
- **详情：** 见 `projects/anemoia.md`

### 3. Index（对话式 AI 香水机器）
- **状态：** 真实商业 / 艺术项目（London 基地，2025 成立）
- **核心能力：** 3–5 分钟对话记忆 → AI Agent 分析叙事+情绪+物理元素 → 从 9 个基香中选 1–3 个并混合
- **特点：** Agent 有详细基香档案（香调、场景、情绪），有规则避免简单关键词映射
- **详情：** 见 `projects/index.md`

### 4. Scent-o-Matic（定制香水售卖机）
- **状态：** Hackathon 原型（Olin College / Formlabs）
- **硬件：** XY 龙门架 + 伺服移液器，支持多种精油按强度组合（6748 种组合）
- **详情：** 见 `projects/scent-o-matic.md`

### 5. Raspberry Pi 香气电话（Techpla Lab）
- **状态：** 真实 DIY 项目
- **能力：** 语音 → Whisper + ChatGPT → 从 6 种香味中选择并喷洒

### 6. 其他相关
- SCircle：AI 数字调香师 + 胶囊混合机
- Algorithmic Perfumery / ScenTronix：问卷 + AI → 机器人定量混合
- 开源多通道控制板（tristan-yk/Aroma）、Smell Engine、sniff_ai 等

## 开源 DIY 打印机 / 喷头方案

详见 `printers/` 目录：
- `diy-inkjet-and-liquid-dispensers.md` — IPJ-Bio、Sidekick、Open Printer、DIY Piezo/CIJ 等相关项目
- `jlcpcb-and-eda-related.md` — 嘉立创 / EasyEDA 相关开源工具（注：未发现开源打印机控制方案）

## AI 原生 / Agent 控制思路

现有方案已证明可行：
- LLM / Agent 生成结构化计划（JSON）
- 硬件只负责精确执行（泵、阀、雾化器 duty cycle）
- 可加入随机性：提高采样温度、惊喜模式、多轮迭代、用户反馈闭环
- 深度控制：记忆用户偏好、约束（过敏）、前中尾调分层、时间演变

详见 `ai-agent/` 目录。

## 使用说明

本仓库为资料汇总与参考，不保证所有链接永久有效。请自行验证硬件可行性、安全性（易燃液体、过敏、泄漏）与法规合规性。

更新时间：2026-10-28
