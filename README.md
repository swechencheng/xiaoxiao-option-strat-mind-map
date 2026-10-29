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
| [`期权知识库_晓晓_思维导图.md`](./期权知识库_晓晓_思维导图.md)                                     |  🇨🇳 中文   | Complete 12-section structured taxonomy and mind map distilling all 354 cases into trading rules, setup parameters, Greeks mechanics, and defensive playbooks.                           |
| [`期权知识库_晓晓_思维导图.html`](./期权知识库_晓晓_思维导图.html)                                 |  🇨🇳 中文   | Interactive HTML mind map powered by Markmap with pan, zoom, and collapsible nodes.                                                                                                      |
| [`options_knowledge_base_xiaoxiao_mind_map.md`](./options_knowledge_base_xiaoxiao_mind_map.md)     | 🇬🇧 English | Precise, full-length English translation of the 12-section taxonomy and strategy mind map.                                                                                               |
| [`options_knowledge_base_xiaoxiao_mind_map.html`](./options_knowledge_base_xiaoxiao_mind_map.html) | 🇬🇧 English | Interactive English Markmap visualization ready to open in any web browser.                                                                                                              |
| [`LICENSE`](./LICENSE)                                                                             |   Legal    | Creative Commons Attribution-NonCommercial 4.0 International (CC BY-NC 4.0).                                                                                                             |

---

## 🧭 Core Philosophy & Strategic Framework

### 1. The Three Pillars of Xiaoxiao's Trading Philosophy

1. **Trade strictly defined-risk strategies with capped maximum loss** (Bearish Broken Wing Butterflies, Iron Condors, Vertical Spreads); aggressively eliminate uncapped, undefined risk (naked single legs, wide strangles, 1:2 put ratios).
2. **Execute Delta-0 (delta-neutral) structures and adjust via Delta-0 rolls; never gamble on short-term direction**—do not attempt to predict tops or bottoms; on IBKR's NQ order screen (which displays Delta multiplied by 20), any combo reading `0.0xx` in its first two digits (e.g., `0.037`, `-0.076`, `+0.080`) is compliant; harvest edge from time decay (Theta), index Put Skew, and non-Delta Greeks rather than directional guesswork.
3. **Focus on committing fewer errors rather than pursuing theoretical maximum returns**, adhering firmly to:
   > _"Don't worry about where it came from, only worry about where it's going."_  
   > Combined with **Buffett's "Overnight Cash" Rule** (imagine your portfolio were liquidated into cash every night—would you re-enter the exact same position tomorrow?), entry costs and historical P&L are sunk costs; evaluate trades solely on whether the forward structure holds positive mathematical expectancy (+EV).

### 2. Core Strategy Architectures

- **Bearish Broken Wing Butterfly (BWB — Signature Setup)**:
  - _Two Configurations_:
    1. **4-Strike Split BWB (`0.50 / 0.40 / 0.15 / 0.05` Put Deltas — Standard Benchmark)**: Buy 1 upper `0.50/0.40` Put Spread + Sell 1 lower `0.15/0.05` Deep OTM Put Spread for a small net debit and Net Delta 0.
    2. **3-Strike Classic BWB (`0.50 / 0.30 / 0.30 / 0.10` Put Deltas)**: Buy 1 ATM `0.50` Put + Sell 2 OTM `0.30` Puts + Buy 1 Deep OTM `0.10` Put.
  - _Wing-Width Ratio Rule_: The lower sold spread width must be **at least 2x** the upper bought spread width (e.g., 200–300 pts upper vs. 600–1000 pts lower). Because index Put Skew makes the wide lower put spread rich in premium, rallies barely lose money as lower put gains offset upper spread decay.
  - _Expiration Regimes_: **0DTE / 1DTE** when single-day expected move (`sd`) is high and rapid intraday decay differentiation is desired; **1–3 Weeks (8–28 DTE)** during elevated VXN or frequent 3sd whipsaw regimes (earning `+$50 to +$178/day` in positive Theta on NQ with wide downside room).
- **Iron Condor (IC)**:
  - _Structure_: Sell ATM Call Spread (short `0.50` / long `0.40`) + Sell Deep OTM Put Spread (short `0.15` / long `0.05`) for a net credit at Net Delta 0 (Put-Call Parity equivalent to the `0.50/0.40/0.15/0.05` BWB, distinguished by avoiding illiquid ITM calls).
  - _Expiration Regimes_: **1–3 Weeks DTE** in high IV; **0DTE / 1DTE (`末日铁鹰`)** in low IV or when actively monitoring the screen.
- **Deep OTM Put Credit Spreads (Post-Crash Dip-Buying)**:
  - _Prerequisite ("Delta Kills")_: Only accounts holding a strong negative-delta short base are qualified to dip-buy crashes; bullish/long-stock accounts must **never** dip-buy with put spreads, as doing so accelerates account liquidation.
  - _Two Methods_: **Method 1** tilts the 4-leg upper spread downward roll to `+0.03 to +0.07` positive delta (adds zero new downside breach risk, ideal when the upper spread is already OTM); **Method 2** sells a standalone 1–5 day (often 1–3 day) deep OTM put credit spread (`0.15/0.05` delta, `+0.04 to +0.05` net delta per tranche). Scale in every 100–200 pt NQ drop across **staggered expirations**; never combine a 4-leg roll and a 2-leg directional put spread into a single 6-leg order.

### 3. Quantitative Risk & Defense Playbooks

- **Downside Roll of Upper Spreads**:
  - When spot drops 150–200 pts (or upper short call delta drops to `0.35`, with `0.40` prepare / `0.30` mandatory), close the upper spread and roll down and out (+1 week) into a new ATM Call Spread at 4-leg Delta 0. Delaying until 650–800 pts OTM causes "Double-Sided Losses (`两头亏`)."
- **Rescuing Breached Lower Short Puts (6-Leg Butterfly Roll & Second-Breach Leg Cancellation)**:
  - When a short put is touched or breached (`0.50–0.65` delta), buy a same-expiry Butterfly or Broken-Wing Butterfly (~1 sd / 200–400 pts wide, ideally during an intraday bounce) + sell next week's deep OTM put spread to balance negative Delta back to 0.
  - **Why Equal-Width Wings Are Preferred**: An equal-width butterfly ($K_{\text{upper}} - K_{\text{body}} = K_{\text{body}} - K_{\text{wing}}$) has zero net payoff below the lowest wing at expiration, adding **zero extra maximum downside risk** beyond the original spread.
  - **Second-Breach Automatic Leg Cancellation**: If breached a second time, the 2 newly sold center puts of the second butterfly land directly on the strikes of your existing 2 protective long puts, automatically closing out the old legs without accumulating leg count.
- **Upside Defense ( rallies pushing Upper Long Call to `0.65` Delta or BWB Upper Long Put to `0.35` Delta)**:
  - For an ITM Short Call Spread (`Long Call >= 0.65` delta): Close the call spread and buy an ATM Put Spread (`0.50/0.40`) or sell a new ITM Call Spread (`0.60/0.50`) at Delta 0—and because **low IV during a rally favors *buying* longer-dated extrinsic value**, extending DTE by 4–7 days into next week is advantageous.
  - For a BWB's upper `Long Put` dropping to `0.35` delta: Either build a higher-strike same-expiry BWB using the old `0.35` Long Put as one of the new Short Put legs to cancel it out, or roll the upper put spread out 1 week.

### 4. Execution & Instrument Efficiency

- **NQ Futures Options as Primary Vehicle**: 23-hour liquidity, punctual 4:00 PM cash close, CME SPAN margin efficiency (5–10%), 4% annual quarterly futures contango tailwind for shorts (+200–300 pts), and $>70\%$ lower transaction drag compared to QQQ ETF options.
- **Direct Broker Routing**: Interactive Brokers (IBKR) Margin Account with Non-Professional CME Level 1 data, ungrouped portfolio legs sorted by instrument, and never leaving high-credit limit orders resting for adverse-selection fills.

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
