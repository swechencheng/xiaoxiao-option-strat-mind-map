# Xiaoxiao Options Strategy Knowledge Base & Mind Map

An exhaustive, systematic knowledge base and interactive mind map synthesizing institutional-grade options trading strategies, risk management frameworks, and defensive roll playbooks from renowned options trader **xx1what Xiaoxiao (晓晓老师)**.

---

## 💐 Special Acknowledgments & Gratitude

This repository exists to preserve and honor the invaluable knowledge generously shared by **Teacher Xiaoxiao (晓晓老师, Discord: `xx1what晓晓`)** within the free, publicly readable `#📈options-discussion` channel of the MeiTou Discord community between June 1, 2026 and September 18, 2026.

In an industry often clouded by paywalled courses, commercialized trading signals, and conflicted market commentary, Xiaoxiao spent countless hours daily dissecting live market swings, answering hundreds of member questions with extraordinary rigor, and imparting institutional-level insights on mathematical expectancy, volatility skew, and multi-dimensional Greeks management—completely free of charge.

His selfless dedication, intellectual honesty, and unyielding focus on discipline, risk control, and emotional detachment have profoundly impacted everyone fortunate enough to learn from him. **We express our deepest, heartfelt gratitude to Teacher Xiaoxiao for giving our community such a precious and lasting educational treasure.**

---

## 📚 Repository Overview

The repository consists of complete chronological archives, an exhaustive 12-section taxonomy, and interactive browser-based visualizers in both Chinese and English:

| File                                                                                               |  Language  | Description                                                                                                                                                                              |
| :------------------------------------------------------------------------------------------------- | :--------: | :--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| [`期权知识库_晓晓.md`](./期权知识库_晓晓.md)                                                       |  🇨🇳 中文   | The complete chronological archive of **354 real-world Q&A case studies** across 4 months (June to September 2026), capturing complete member inquiries and Xiaoxiao's in-depth answers. |
| [`期权知识库_晓晓_思维导图.md`](./期权知识库_晓晓_思维导图.md)                                     |  🇨🇳 中文   | Complete 12-section structured taxonomy and mind map distilling all 354 cases into quantitative trading rules, setup parameters, and defensive playbooks.                                |
| [`期权知识库_晓晓_思维导图.html`](./期权知识库_晓晓_思维导图.html)                                 |  🇨🇳 中文   | Interactive HTML mind map powered by Markmap with pan, zoom, and collapsible nodes.                                                                                                      |
| [`options_knowledge_base_xiaoxiao_mind_map.md`](./options_knowledge_base_xiaoxiao_mind_map.md)     | 🇬🇧 English | Precise, full-length English translation of the 12-section taxonomy and strategy mind map.                                                                                               |
| [`options_knowledge_base_xiaoxiao_mind_map.html`](./options_knowledge_base_xiaoxiao_mind_map.html) | 🇬🇧 English | Interactive English Markmap visualization ready to open in any web browser.                                                                                                              |
| [`LICENSE`](./LICENSE)                                                                             |   Legal    | Creative Commons Attribution-NonCommercial 4.0 International (CC BY-NC 4.0).                                                                                                             |

---

## 🧭 Core Philosophy & Strategic Framework

### 1. The Three Pillars of Xiaoxiao's Trading Philosophy

1. **Trade strictly defined-risk strategies with capped maximum loss** (Bearish Broken Wing Butterflies, Iron Condors); aggressively eliminate uncapped, undefined risk (naked single legs, wide strangles, 1:2 put ratios).
2. **Execute strictly Delta-0 (delta-neutral) structures; never gamble on direction**—do not attempt to predict tops or bottoms; harvest edge from time decay (Theta) and volatility mechanics rather than directional guesswork.
3. **Focus on committing fewer errors rather than pursuing theoretical maximum returns**, adhering firmly to:
   > _"Don't worry about where it came from, only worry about where it's going."_  
   > Entry costs and historical P&L are sunk costs; evaluate trades solely on whether the forward structure holds positive mathematical expectancy (+EV).

### 2. Core Strategy Architectures

- **Bearish Broken Wing Butterfly (BWB)**:
  - _Standard Configuration_: Buy 1 ATM Put (0.50 $\Delta$) + Sell 2 OTM Puts (0.40 $\Delta$) + Buy 1 Deep OTM Put (0.05–0.15 $\Delta$) on NQ / QQQ.
  - _Edge_: Zero upside tail risk (max loss capped at initial entry debit), positive theta decay, vega-neutral balance, and rapid profitability in 0DTE/short cycles.
- **Iron Condor (IC)**:
  - _Structure_: Sell ATM Call Spread (short 0.50 / long 0.40) + Sell Deep OTM Put Spread (short 0.15 / long 0.05).
  - _Mechanics_: Net credit entry monetizing time decay and index put skew.
- **Deep OTM Put Credit Spreads (Dip-Buying Engine)**:
  - Selling delta 0.10–0.15 put spreads (+0.04 to +0.05 net delta per tranche) post-selloff to capitalize on inflated OTM put IV while staggering expirations.

### 3. Quantitative Risk & Defense Playbooks

- **Strict Quantitative Triggers**:
  - Upper short call drops 200 points below spot $\rightarrow$ initiate a roll downward and outward.
  - Spot breaches the short strike by $>100$ points $\rightarrow$ evaluate defense; breaches by $>300$ points $\rightarrow$ execute roll immediately.
  - Short call delta reaches 0.35 $\rightarrow$ roll down to ATM to avoid holding negative-EV OTM calls under index put skew.
- **The Textbook 6-Leg Roll (Rescuing Breached Short Puts)**:
  - Convert the breached short put into a same-expiry, 1-sd wide Classic Symmetric Butterfly (equal wings, neutral vega/gamma) + sell a deep OTM put credit spread for the subsequent week to balance net Delta back to 0.
- **Zero Panic Liquidations**:
  - Only three legitimate operational paths: let options expire worthless, scale into new tranches, or roll out in time. No mechanical stop-losses at the bottom.

### 4. Execution & Instrument Efficiency

- **NQ Futures Options as Primary Vehicle**: 24/5 liquidity, punctual 4:00 PM cash close, CME SPAN margin efficiency (5–10%), and $>70\%$ lower transaction drag compared to trading equivalent notional in QQQ ETF options.
- **Direct Broker Routing**: Using Interactive Brokers (IBKR) to avoid retail Payment-for-Order-Flow (PFOF) slippage.

---

## 🖥️ How to View the Interactive Mind Map

You can interactively explore the mind map directly in your browser:

1. Double-click or open either of the HTML files in any modern web browser:
   - English: [`options_knowledge_base_xiaoxiao_mind_map.html`](./options_knowledge_base_xiaoxiao_mind_map.html)
   - Chinese: [`期权知识库_晓晓_思维导图.html`](./期权知识库_晓晓_思维导图.html)
2. **Interaction Tips**:
   - **Click on any circle node** to expand or collapse branches.
   - **Click & drag** to pan across the canvas.
   - **Scroll** to zoom in and out.

---

## 📄 License & Non-Commercial Terms

This project is licensed under the **Creative Commons Attribution-NonCommercial 4.0 International License (CC BY-NC 4.0)**.

- **Non-Commercial Only**: You are strictly prohibited from selling, monetizing, paywalling, or incorporating any portion of this repository into paid courses, subscription groups, or commercial services.
- **Educational & Personal Use**: You are free to share, copy, and adapt these materials for personal research and educational purposes, provided proper attribution is given.

_Disclaimer: All strategies, case studies, and quantitative frameworks contained herein are for educational and historical study purposes only. Options trading involves substantial risk of loss and is not suitable for all investors._
