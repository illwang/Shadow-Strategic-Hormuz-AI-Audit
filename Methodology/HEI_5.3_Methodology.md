# HEI 5.3 Methodology / HEI 5.3 方法论说明

**Version**: HEI 5.3 (2026-05-22)  
**Core**: Discrete Geopolitical State Machine + HEI Composite Index  
**Nature**: Structured Expert Judgment (SEJ), not a quantitative prediction model  
**性质**：结构化专家评分，非量化预测模型

---

## 1. Core Philosophy / 核心哲学

Geopolitical crisis assessment faces a fundamental contradiction: the most critical variables are often the hardest to quantify. "Diplomatic confidence" cannot be extracted from a Bloomberg terminal. "Conflict intensity" has a non-linear relationship with market pricing. Attempting to calculate these with a mathematical formula is not only technically infeasible but epistemologically misleading — it implies a false sense of control over complex systems.

Therefore, this framework chooses the **Structured Expert Judgment (SEJ)** route. This is a long-validated approach in nuclear safety assessment, intelligence early warning, and disaster response. Its core idea: acknowledge that subjective judgment is inevitable, so make it structured, transparent, and auditable — rather than hiding it behind seemingly objective formulas.

地缘政治危机评估面临根本矛盾：最关键的变量往往最难量化。"外交置信度"无法从彭博终端提取，"冲突烈度"与市场定价之间存在非线性跳跃。试图用数学公式精确计算这些变量，技术上不可行，认识论上具有误导性——它暗示着对复杂系统的虚假控制。

因此，本框架选择**结构化专家评分（SEJ）**路线。这是在核安全评估、情报预警、灾害响应等领域经过长期验证的方法。核心思想：承认主观判断不可避免，因此将其结构化、透明化、可审计化，而非隐藏在看似客观的数学公式背后。

---

## 2. General Skeleton (Immutable Layer) / 通用骨架（不动层）

### 2.1 Discrete State Machine / 离散状态机

| State | Identifier | Core Feature | HEI Range |
|-------|-----------|------------|-----------|
| Peaceful Passage | S0 | Strait freely navigable | 0.00-0.25 |
| Tense Standoff | S1 | Military deployment increased | 0.25-0.45 |
| Factual Confrontation | S2 | Selective interdiction | 0.45-0.70 |
| Institutionalized Rule Competition | S3 | Rule systems opposed, institutions operating, permanent fee negotiations, digital control expansion, UN resolution confrontation | 0.65-0.85 |
| Full Military Conflict | S4 | Strait closed, large-scale engagement | 0.85-1.00 |

### 2.2 Three-Axis Model / 三轴模型

**Formula**: HEI = F×0.40 + M×0.30 + D×0.25 + Buffer×0.05

| Dimension | Weight | Role in Current Phase |
|-----------|--------|----------------------|
| F (Physical Conflict Intensity) | 0.40 | Highest weight. Defines institutionalized passage blockage as part of physical conflict intensity. |
| M (Market Panic) | 0.30 | Captures inventory consumption, institutional uncertainty pricing. |
| D (Diplomatic Process Confidence) | 0.25 | Slightly reduced from 5.1's 0.30 to acknowledge D's quality depreciation in S3 state. |

### 2.3 Three-Level Information / 三级信息

| Level | Definition | Label in Report |
|-------|-----------|----------------|
| Anchor | Verifiable facts from public sources | 【锚】 |
| Inference | Logical extrapolation based on anchors | 【推】 |
| Projection | Conditional hypothesis | 【演】 |

### 2.4 Uncertainty Annotation / 不确定性标注

HEI = X ± 0.08

This is **not** a statistical confidence interval. It reflects the analyst's current uncertainty range under SEJ. The true position may lie anywhere within this interval. Qualitative state determination (S2→S3 jump) is more important than quantitative HEI movement.

---

## 3. Scoring Anchors / 评分锚定

### 3.1 F (Physical Conflict Intensity) / 物理冲突烈度

| Score | Combat Dimension | Institutional Blockade Dimension (5.3 Added) | Historical Ref |
|-------|-----------------|-------------------------------------------|--------------|
| 0.0-0.2 | No military friction, strait open | No institutional passage restrictions | Peace time |
| 0.2-0.4 | Sporadic warning shots | — | 2016 US-Iran maritime standoff |
| 0.4-0.6 | Small-scale engagement, vessel damage | — | 2019 Gulf of Oman incident |
| 0.6-0.8 | Frequent engagement, casualties on both sides | Institutional screening causing significant passage volume drop | — |
| 0.8-0.95 | Sinking of capital ships; conflict spreading to land/oil fields/nuclear facilities | Passage volume drops below 5% of pre-war level due to institutional screening | 1987 USS Stark |
| 0.95-1.0 | Full-scale war | — | 1980-88 Iran-Iraq War |

**OSINT Observability**: High. Combat events verified via multi-source news cross-check; passage volume tracked via AIS public platforms; institutional blockade determined by matching Iranian official statements with passage patterns.

### 3.2 M (Market Panic) / 市场恐慌度

| Score | Anchor Scenario | Key Indicator Ref |
|-------|----------------|-------------------|
| 0.0-0.3 | Market operating normally | War risk <0.5% |
| 0.3-0.5 | Concerns rising but trading normal | War risk 0.5%-2% |
| 0.5-0.7 | Significant uncertainty pricing | War risk 2%-5% |
| 0.7-0.85 | High uncertainty, inventory accelerating consumption | War risk 3%-8% |
| 0.85-0.95 | Panic emerging, liquidity narrowing | War risk >8% |
| 0.95-1.0 | Systemic panic | Strait substantive closure |

### 3.3 D (Diplomatic Process Confidence) — S3 Calibrated / 外交进程置信度—S3校准版

| Score | Anchor Scenario | S3 Specificity |
|-------|----------------|---------------|
| 0.0-0.2 | All diplomatic channels closed | — |
| 0.2-0.4 | Channels exist but extremely fragile; institutional track parallel to diplomatic track | D's recovery "quality" lower than S2 period |
| 0.4-0.6 | Effective communication channels, framework consensus | Must withstand "execution entropy" test |
| 0.6-0.8 | Clear commitment to negotiations, specific roadmap | — |
| 0.8-1.0 | Comprehensive agreement reached, being implemented | — |

---

## 4. Source Depth Tags / 信源深度标签

| Tag | Meaning | Example |
|-----|---------|---------|
| [P] Primary | First-hand source (official statement, raw data, direct observation) | EIA SPR data, Foreign Ministry press conference |
| [S] Secondary | Second-hand compilation (news agency report, think tank citation) | Reuters, ISW citing Bloomberg |
| [T] Terminal | Real-time terminal data (not yet in news archive) | Intraday oil price 104-105 (May 22) |
| [U] Unverified | Direction confirmed but original source not found | Trump "open and free" statement (May 22, pending archive verification) |
| [E] Estimated | Estimate based on public data | Global inventory daily consumption rate |

**Degradation Rule**: [U] automatically downgrades to [E] or is deleted if not archived within 7 days.

---

## 5. Version Iteration / 版本迭代

| Version | Date | Major Changes |
|---------|------|--------------|
| V15 | 2026-05-22 | Internet-verified correction edition. Corrected Goldman inventory data (8.7M→11-12M bbl/d, April data). Corrected oil price to range expression. Corrected Saudi action description. Deleted statements without original source. Restored missing chapters. Added industry calibration layer. |
| V14 | 2026-05-22 | Internet verification edition (pre-correction) |
| V13 | 2026-05-22 | OSINT real-time update edition |
| V12 | 2026-05-22 | Framework upgrade: HEI 5.3 methodology fully embedded |

---

*Disclaimer: HEI values reflect trend judgment ranges, not statistical prediction results. Past event patterns do not represent future performance.*
