# Review 10: "HAN reader CZ" (C10), ECONOMICS lens

Reviewer: unit-economics and time skeptic. Date: 2026-09-29. FX: 1 € = 25 CZK (as in the dossier).

I read: `00-brief.md`, `dossiers/10-han-reader.md`, `02-main-loop-evidence.md`, `06-verification.md`, `cz-legal-tax-quickstart.md` (§0, §2, §3.3, §4.4–4.5, §5.3–5.4, §5.7) and the C10 rows of `scores/scorer-A/B/C.md`.

I ran one WebSearch, on the Stage 1 module price. Every other figure is labelled **[verified: URL]** (a search snippet only), **[knowledge]** (unverified background) or **[estimate: reasoning]**.

---

## Verdict: **WEAK, 3/10**

- **The per-unit margin is real, but the business around it is too small.** The own-hardware unit clears about €31–33, which confirms the dossier. The kit that must fund the test clears only about **€10–15**, not €17.
- **Volume decides everything.** At the realistic national flow, the founder most likely stays below the dossier's own Stage 2 trigger.
- **Month-12 profit is about €120/month, not €500.** That is roughly **€8/h** on ongoing hours and **about €3/h** for year 1 once build hours are counted.
- **The €500 case is the pass-mark case.** The dossier's "realistic" month 12 assumes the Stage 2 gate is passed at exactly its threshold (16 units/month). That is the success branch of a gate the dossier itself expects many ideas to fail, so it is not a realistic central case.
- **Stage 2 barely pays back before the CRA date.** At 16 units/month, the €2.5k sunk into Stage 2 does **not** pay back before the CRA cut-off on 11 Dec 2027, about 7 months after own hardware would launch. The only ways out are more volume or committing to CRA compliance, which adds cost and a multi-year support duty.
- **Even on the dossier's own numbers, year 1 is about break-even.** Its realistic path nets about **€470 cash in year 1 for about 350 h** of work, roughly €1.5/h (see §4).

---

## 1. Claims checked

| # | Dossier claim | What I found | Effect |
|---|---|---|---|
| 1 | Kit hardware (CE ESP32 + RS485 module from an EU distributor) costs **€19** | Waveshare's own list price for the ESP32-S3-RS485-CAN is **$17.99–19.99** [verified: https://www.waveshare.com/esp32-s3-rs485-can.htm, snippet]. The rpishop.cz price was not captured [https://rpishop.cz/642120/waveshare-prumyslovy-esp32-s3-modul-s-rs485-can/]. A CZ distributor's retail price, including 21% VAT that a non-payer can't reclaim, is typically about 1.4–1.6× the USD list price, so **€24 (range €20–28)** [estimate]. M5Stack Atom Lite + Atomic RS485 Base land in the same range [knowledge]. The dossier's own Stage 1 budget of €450 for 20 kits (€22.50 each including cables) leaves no slack. | Kit net falls from **€17 to ≈ €10.5 with ads, ≈ €15 without** |
| 2 | Own PCBA costs **€6.5 landed** at 100 pcs | Plausible. LCSC BOM of about $3–3.5, JLC setup, stencil and extended-part fees of about $25 per batch, hand-soldering of the THT RJ12, DHL, 21% import VAT and a DHL clearance fee come to **€5.5–7.5** [estimate]. The €3 EU low-value duty doesn't apply, because a 100-pc batch is over €150. | Confirmed |
| 3 | Returns cost **5% of price** | The withdrawal rate will be higher than for a plain gadget. Compatibility is conditional: EG.D reads only certain meter types, PRE needs activation by a technician, and pillar boxes have no socket. A PRE buyer whose activation takes longer than the 14-day withdrawal window is likely to send the unit back. I expect **10–15% withdrawals in the kit phase**. Most returned units are resellable, though, so the cash cost stays about **€2.5/unit**. The real cost is 30–45 min of handling per return. | Cash ≈ same; **time up** |
| 4 | Ads cost **€4 + 21% VAT per unit** | €4 is plausible only as a *blended* cost with mostly organic forum sales. Paid Meta CAC for a niche HA gadget is more like €10–25 per sale [knowledge]. Any ad spend also makes the founder an identified person (monthly VAT return by the 25th, quickstart §3.3). | Drop paid ads in Stage 1 (see fixes) |
| 5 | **26 min** per unit including support | That figure is for Stage 2. For the kit, realistic per-unit time is **≈ 45 min**: reorder 3, crimp and wire RJ12 to terminals + continuity test 8, bench test 4, pack and label 5, bookkeeping 2, pre-sale questions 5, setup support 15 (the dossier's own kit estimate is about 20), returns amortised 3. For Stage 2 it is **≈ 30–35 min**, since enclosure cut-outs, pillar-box and Wi-Fi-range questions and the long tail of support all add time. | Time up by about 40–70% |
| 6 | Fixed hours: community 4 h + admin 2 h per month | Firmware upkeep is missing: ESPHome breaking changes, 4 meter types and 3 distributors. Budget about 1.5–2 h/month. An identified-person VAT return adds about 0.5 h/month if ads are used. | About **15 h/month** at 12–16 units |
| 7 | Fixed costs **€30–40/month** | That is fine for Stage 1. Stage 2 is missing the WEEE scheme fee (€150/yr, which the dossier budgets but leaves out of the monthly P&L), product-liability insurance (about €100–200/yr [estimate]; the new EU Product Liability Directive 2024/2853 covers firmware defects for products placed from 9 Dec 2026 [knowledge]) and a yearly tax-advisor hour. | Stage 2 fixed costs are **€55–70/month** |
| 8 | Stage 2 sunk cost is "€1,600 over ~380 units ≈ €4/unit" and "pays back in 10–12 months" | 380 units takes 24 months at 16/month. The dossier's own risk table, though, says to "exit or transfer the design" by the **CRA date of 11 Dec 2027**. Own hardware starts around May 2027, so the window is about 7 months: **≈ 110 units, not 380**. The real sunk cost is about €2.5k (design €300, pre-scan €1,200, EN 18031 €400, WEEE €150, shop €250, labels €200), which is **≈ €22/unit** over that window. The uplift over the kit (€31 − €12 ≈ €19) × 110 units ≈ **€2.1k < €2.5k**. | Stage 2 is NPV-negative at 16/month unless the founder takes on CRA compliance |
| 9 | Pessimistic month 12 = **€70** (6 kits/month) | That contradicts the dossier's own kill criteria: fewer than 12 paid kits by day 60 means stop. The pessimistic case is **€0 at month 12, with about €350–450 and about 100 h lost**. | Corrected |
| 10 | Optimistic = **40 units/month → €1,300** | The dossier sizes the whole national market at **30–100 units/month at peak**. My flow estimate is **≈ 25–70/month nationally**: about 47k new AMM meters/month (ČEZ ≈ 29k, EG.D ≈ 17k, PRE ≈ 1k, per the dossier's cited rollout figures) × about 1% HA households × 5–15% who want real-time HAN, won't DIY and aren't served by their inverter [estimate]. Selling 40/month means capturing most of that flow with no clone, while LaskaKit already sells the ESPlan ESP32 + MAX485 board [verified: https://www.laskakit.cz/en/laskakit-esplan-esp32-lan8720a-max485-poe/, per `06-verification.md`]. | Optimistic capped at about **25/month, ≈ €700** |
| 11 | The realistic case "crosses the social-insurance cliff, so budget ~38%" | This is wrong on both counts. **(a)** Year-1 real profit is far below 12 × the month-12 run rate, because of the ramp and about €3k of sunk costs; with a mid-year start the part-year threshold also shrinks. **(b)** In a steady own-hardware year, the **60% flat-rate expense allowance (výdajový paušál)** beats actual expenses, because real costs are only about 45% of revenue. For example, 16 × €56 × 12 = €10.75k revenue gives a deemed profit of €4.3k ≈ 107k CZK, **under 117,521 CZK**. Levies are then 21.75% of the deemed profit, ≈ €935/yr, or about 16% of real profit. For a kits-only year, actual expenses are better, since real margin (≈ 25%) is below the 40% deemed profit. | The tax drag is smaller than the dossier says, but this doesn't rescue the volume problem |
| 12 | "100 units (€1,300) covers ~5 months" | At a realistic 10–16/month it is **6–10 months of stock**, bought in one batch just before a clone or CRA window. A custom PCBA without the founder's support has a liquidation value close to €0. | Cash risk up (see §4) |

---

## 2. Rebuilt unit economics (€ per unit)

### Stage 1 kit at 1,190 CZK (€47.6)

| Line | Dossier | Corrected | Basis |
|---|---|---|---|
| ESP32 + RS485 module, retail incl. VAT | 19.0 | **24.0** (20–28) | Claim 1 |
| RJ12 cable wired to terminals + USB-C cable | 2.5 | 3.0 | [estimate] |
| Box, label, printed guide | 1.0 | 1.2 | [estimate] |
| Payment (mix of free QR bank transfer and card) | 0.8 | 0.7 | [knowledge] |
| Packaging + Zásilkovna subsidy (its invoice carries VAT a non-payer can't reclaim) | 0.5 | 0.8 | Quickstart §5.4 |
| Withdrawals (10–15% × ≈ €10) + warranty (2% × €30) | 2.4 | 2.5 | Claim 3 |
| Ads incl. 21% VAT | 4.8 | 4.8 **or 0** | Claim 4 |
| **Net** | **17.0** | **≈ 10.6 with ads / ≈ 15.4 without; realistic mix ≈ €12** | |

### Stage 2 "HAN Reader Wi-Fi" at 1,390 CZK (€56)

| Line | Dossier | Corrected |
|---|---|---|
| PCBA landed | 6.5 | 6.7 |
| Enclosure with cut-outs, RJ12 and USB-C cables | 3.5 | 4.0 |
| CE 5 V PSU | 3.5 | 4.0 |
| Box, label, guide | 1.0 | 1.0 |
| Payment | 0.9 | 0.8 |
| Pack + shipping subsidy | 0.5 | 0.8 |
| Withdrawals + 24-month warranty as the **manufacturer** | 2.8 | 3.0 |
| Ads (mixed) | 4.8 | 2.4 |
| WEEE per-unit fee | 0.2 | 0.2 |
| **Net before sunk costs** | **32.3** | **≈ 33 (≈ 31 with full ads)** |
| Sunk-cost amortisation | −4 (over 380 units) | **−22 over the ≈ 110 units sold before 11 Dec 2027**, or −7 over 380 units if the founder commits to CRA compliance (+30–60 h plus a security-support duty over a period declared under the CRA, for which the dossier budgets nothing) |

**Conclusion:** the dossier's own-hardware margin holds. Its kit margin is about 30% too high, and its sunk-cost amortisation is optimistic by a factor of 3–5.

---

## 3. Hours

| | Kit phase (12/month) | Stage 2 (16/month) | Stage 2 (25/month) |
|---|---|---|---|
| Per-unit time | 45 min → 9.0 h | 32 min → 8.5 h | 30 min → 12.5 h |
| Community posting | 3 h | 4 h | 4 h |
| Admin, bookkeeping, VAT return if ads | 2 h | 3 h | 3 h |
| Firmware and config upkeep | 1.5 h | 2 h | 2 h |
| **Ongoing hours/month** | **≈ 15.5 h** | **≈ 17.5 h** | **≈ 21.5 h** |
| One-off hours (unpaid) | Stage 1 build ≈ 110–130 h (weeks 1–11 at 10–12 h/wk, per the dossier) | + Stage 2 design, prototypes, pre-scan, technical file, EN 18031 and GPSR ≈ 60–100 h. **Double this if the founder hasn't designed an RF PCB before**, and budget €600–1,000 for an EMC retest. | same |

Time is **not** the constraint: the business needs only 3.5–5 h/week once running. The binding constraint is demand. The upside is that the founder's other 8–10 h/week stay free for a second line.

---

## 4. Sell-through, cash tied up, payback

- **Demand shape [estimate].** A forum-led niche launch typically gives a **pent-up spike** in months 1–2 of about 15–30 units, then decays to the new-AMM flow. That makes my realistic month-12 run rate about **10–14 kits/month**.
- **The launch spike can fake the gate.** The dossier's gate is "≥ 15/month for 2 consecutive months". The spike alone can pass it, triggering the €4.3k Stage 2 spend just as demand settles to about 12. This is the costliest trap in the plan.
- **Cash tied up.**
  - Stage 1: about €450–600, of which 20 kits (≈ €560 at corrected cost) is about 1.5–2 months of stock. That is low risk.
  - Stage 2: peak outlay of about **€4.5–5k around month 7–8**. That covers about €2.5k sunk, about €1.5k for a 100-unit PCBA batch and about €300 of ads. At that point cumulative profit is only about €0.6–1k. The PCBA batch amounts to 6–10 months of stock with near-zero salvage value.
- **Year-1 cash walk on the dossier's own realistic path** [estimate, using its unit numbers]:
  - Kits over months 2–7: 70 units × €17 = €1,190.
  - Own units over months 8–12: 80 × €33 = €2,640.
  - Less fixed costs (€410), the Stage 1 non-inventory spend (€450) and the Stage 2 sunk cost (€2,500).
  - Result: **≈ +€470 cash, plus about €300 of leftover stock, for about 330–370 h ≈ €1.3–2.3/h in year 1.**
- **Year-1 on my realistic path** (kits only, ≈ 135 kits): 135 × €12 − €300 fixed − €450 sunk ≈ **+€870 for about 285 h ≈ €3/h.** Kits-only actually beats the dossier's Stage 2 path in year 1.
- **Cumulative cash breakeven on the Stage 2 path** comes at about months 16–20 at 16/month. That is **after** the CRA decision point.

---

## 5. Fatal flaws (economics)

1. **The market caps the founder below the brief's bar.**
   - The whole CZ flow is about 25–70 units/month [estimate]; the dossier says 30–100 at peak. Only CZ is served, because every other country needs its own WEEE registration and uses different meters.
   - A clone-free first mover realistically keeps 20–40% of that flow. The ceiling is therefore about **€600–1,000/month for a 12–24-month window**, reachable only in the optimistic branch, and it decays as the existing stock of HA + AMM households gets served and LaskaKit or forum clones appear.
   - The central outcome is about €120/month. For a founder who is "burned before" and needs something that "actually makes money", this is near-fatal.
2. **The realistic case is conditional, not central.**
   - €500/month assumes the gate is passed exactly at 16/month.
   - Probability-weighted [estimate]: about 45–50% stop at day 60–90 (€0), about 20% hold on kits at 12–14/month (≈ €130), about 25% reach Stage 2 at 15–20/month (≈ €450 cash), and about 5% reach 25+/month (≈ €700). The expected value is **≈ €175–200/month**, and the median is about €100–130.
3. **Stage 2 has no payback window at realistic volume.** Measured against the CRA date the dossier itself names, the €2.5k sunk cost needs **≥ 20–25 units/month** to recover before Dec 2027. Continuing past that date means taking on CRA duties, including a multi-year security-support obligation for a one-person side business.

## 6. Fixable issues and fixes

| Issue | Fix |
|---|---|
| Kit BOM is understated (€19 vs ≈ €24) | Get B2B quotes from rpishop, botland and TME before launch. Test **1,290 CZK** against 1,190, or use cheaper M5Stack/LaskaKit parts. Accept that the kit is a curation fee with thin pricing power next to an ≈ €8 DIY build. |
| Paid ads in Stage 1 | **No Meta or Google ads before Stage 2.** Buyers are on homeassistant-cz.cz and FB groups, where organic posts reach them. This saves €4.8/unit and keeps the founder out of identified-person status (monthly returns, penalties). |
| The launch spike can trigger Stage 2 | Gate Stage 2 on **paid pre-orders with deposits (≥ 60)**, or on **≥ 15/month in months 3 and 4 after launch with no new promo posts**. Reservations without payment don't count. |
| Stage 2 payback ignores the CRA date | Decide up front: either (a) Stage 2 only at ≥ 20–25/month or with pre-order funding, or (b) plan for CRA compliance from the design stage and amortise over about 30 months, with the support-period cost priced in. |
| 100-unit PCBA batch | Order batches of **30–50**. PCBA costs about €2–3/unit more, but cash in stock halves and stranded stock falls. |
| Withdrawals from incompatible meters | Pre-qualify at checkout: a meter photo or type, the distributor, PRE activation confirmed, and power or cable route at the meter. Ship PRE orders only after activation. |
| Fixed costs omit WEEE, liability insurance and the tax advisor | Budget **€55–70/month** in Stage 2. |
| Tax plan ("38%") | Use **actual expenses** in the kit and sunk-cost year and the **60% paušál** in steady own-hardware years. Levies then stay around 21.75% of profit, and the social-insurance cliff isn't reached. Register the živnost on **1 Jan 2027** unless Q4 2026 shows a profit: the part-year 2026 threshold is only 29,375 CZK, although it's moot while there's a loss. |
| Founder skill is not stated | If the founder hasn't laid out an RF PCB before, add about €1k (external design or an EMC retest) and 60+ h to Stage 2, or stay on kits. |

---

## 7. Corrected month-12 estimate (pre-levies; after levies at 21.75%, below the social threshold)

| Case | What happens | Units at M12 | M12 profit €/month | After levies | Ongoing h/month | €/h ongoing | €/h year 1 incl. build hours |
|---|---|---|---|---|---|---|---|
| **Pessimistic** | Day-60 stop; leftover kits sold at cost | 0 | **€0** (≈ €350–450 and ≈ 100 h lost) | €0 | 0 | – | **negative (≈ −€4/h)** |
| **Realistic** | Kits hold at about 12/month, just below the Stage 2 gate | 12 kits × €12 − €25 | **≈ €120** | ≈ €95 | ≈ 15.5 | **≈ €8/h** | ≈ €3/h |
| **Optimistic** | Stage 2 triggered, no clone yet | 25 × €31 − €60 | **≈ €715 cash** (≈ €550 after sunk-cost amortisation) | ≈ €560 | ≈ 21.5 | ≈ €33/h | ≈ €5/h (≈ €2.2k net for ≈ 440 h) |
| *Dossier, for comparison* | | 16 | €500 (realistic) / €1,300 (optimistic) | | ≈ 13 | ≈ €38/h | not given |

The probability-weighted month-12 profit is about **€175–200/month** [estimate].

**Where the ceiling is:** about **€1,000/month at a CZ-only peak** (35–40 units/month, requiring near-monopoly of the national flow). It is time-limited by clones and the CRA, and declines once the existing stock of HA + AMM households is served. It can't grow by working more hours, only by entering new countries, and each new country means new meter protocols plus a WEEE registration (an authorised representative, about €300–600/yr per country [knowledge]).

---

## 8. Would I tell a friend to do this?

**No, not as the income source this brief asks for.** Only if all of these hold:
- they already write ESPHome/DLMS configs;
- they have a ČEZ AMM meter at home to test on;
- they treat Stage 1 as a **≤ €500, about 100 h experiment** that at best pays for its own parts;
- they fund any own hardware from **paid pre-orders**, not from a two-month kit run rate.

Even then, it's best run as a low-hours side module next to a business that can reach €500/month on its own.
