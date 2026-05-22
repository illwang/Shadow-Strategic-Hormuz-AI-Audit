# Front B: AI Supply Chain (HBM Four-Layer Bottleneck) Experiment Notes
# Front B：AI 供应链（HBM 四层瓶颈）实验笔记

**Status**: Experimental. HEI readings not recommended for publication.
**状态**：实验性。不建议发布 HEI 读数。

---

## Core Problem / 核心问题

HEI 5.3 relies on high-frequency public observation indicators in Front A (Hormuz): AIS passage volume, oil prices, EIA inventory. Front B (AI supply chain / HBM) lacks equivalent high-frequency observation indicators.

HEI 5.3 在 Front A（霍尔木兹）的锚定依赖于 AIS 通行量、油价、EIA 库存等高频公开观测指标。Front B（AI 供应链/HBM）缺乏等价的高频观测指标。

---

## F Dimension Redefinition Attempt / F 维度重新定义尝试

| Front A Definition | Front B Attempted Definition | Problem |
|-------------------|------------------------------|---------|
| Physical conflict intensity + institutional passage blockage | Physical supply disruption intensity + institutional export control intensity | HBM has no AIS data. "Passage volume" indicator失效. Alternative: foundry capacity utilization? Downstream inventory days? Neither is real-time public data. |

**Preliminary Conclusion**: F in Front B may only rely on **institutional export control events** (e.g., BIS rule updates, Netherlands/Japan licensing policy changes), rather than continuous physical observation.

---

## M Dimension Redefinition Attempt / M 维度重新定义尝试

| Front A Definition | Front B Attempted Definition | Problem |
|-------------------|------------------------------|---------|
| Oil price / war risk / inventory | HBM spot price / foundry capacity utilization / downstream inventory | HBM prices are opaque, public data lagging (quarterly earnings rather than weekly). M coefficient may be severely distorted. |

**Preliminary Conclusion**: M in Front B may need to use **indirect proxy indicators**:  
- NVIDIA/AMD supply chain disclosure wording changes regarding "geopolitical risk"  
- TSMC/Samsung earnings call capacity allocation statements  
- US BIS Entity List update frequency  

But these indicators' "panic degree" mapping is far less intuitive than oil prices.

---

## D Dimension Redefinition Attempt / D 维度重新定义尝试

| Front A Definition | Front B Attempted Definition | Observation |
|-------------------|------------------------------|-------------|
| Diplomatic process confidence | Technical agreement negotiation confidence (US-Japan-Netherlands-South Korea coordination) | D in chip issues seems more stable (Quad Alliance already institutionalized), but execution entropy同样 exists: Samsung/TSMC actual execution vs government statements. |

**Preliminary Conclusion**: Front B's D coefficient may remain in "medium quality" range (0.4-0.6) for extended periods, because technical alliance institutionalization reduces diplomatic signal discreteness, but execution-level friction persists.

---

## State Machine Redefinition Attempt / 状态机重定义尝试

| Front A State | Front B Equivalent Attempt |
|--------------|---------------------------|
| S0 Peaceful Passage | S0 Free supply chain (no export controls) |
| S1 Tense Standoff | S1 Export control预警 (BIS review strengthening) |
| S2 Factual Confrontation | S2 Selective supply disruption (specific companies added to Entity List) |
| S3 Institutionalized Rule Competition | S3 Institutionalized export control competition (US BIS rules vs Korea/Netherlands autonomous licensing) |
| S4 Full Military Conflict | S4 Full technology decoupling (equipment/materials/talent full chain blockage) |

**Problem**: S3 boundary in Front B (HEI 0.65-0.85) how to anchor? Lacking continuous quantitative input, state determination may沦为 "post-hoc追认".

---

## Current Conclusion / 当前结论

**Do not recommend publishing Front B HEI readings** until finding a core high-frequency observation indicator to replace AIS.

Possible paths:  
1. Establish tracking with semiconductor industry media (e.g., EE Times, SemiEngineering) for institutional announcement real-time streams  
2. Replace "foundry capacity utilization" with "TSMC/Samsung earnings call geopolitical risk wording intensity" (text analysis)  
3. Replace "HBM price" with "NVIDIA supply chain disclosure inventory days anomaly"

All require further verification.

---

*Record Date: 2026-05-22*  
*Status: Experiment paused, awaiting Front A validation completion before further investment*
