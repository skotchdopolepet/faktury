# Review 05: flash-modded iPod Classic (C01), EXECUTION lens

Date: 2026-09-29. Reviewer lens: execution, legal and platform risk for a Czech employed founder (10–15 h/week, ≤ €8,5k, product not service).

Inputs: `00-brief.md`, `dossiers/05-modded-ipod.md`, `02-main-loop-evidence.md`, `06-verification.md`, `cz-legal-tax-quickstart.md` (§1–6), `scores/scorer-A/B/C.md`, plus the hunter entry in `hunt/demand-signals.md` and `01-longlist.md` for context. I did not read the other reviewers' files.

Tags: **[verified: URL]** is a search-result snippet seen this session; **[file]** is a claim taken from the inputs above; **[knowledge]** is my own background knowledge, unverified here; **[estimate]** is my arithmetic, with the reasoning shown. I used one WebSearch.

---

## 1. Verdict

**VIABLE, but only as a small CZ-only side income. Score: 5/10.**

- **The good news:** it is one of the more executable plans in the swarm. The test costs ≈ €900, most of which is recoverable by parting out. The legal load is manageable as long as sales stay in CZ. The 12-week plan has real kill gates, and the skill is learnable.
- **Why only 5:** three things cap it, and none of them is legal.
  - **Donor flow.** Realistic volume needs most of the dossier's own estimate of the national supply of broken donors.
  - **CZ demand.** Post-Christmas demand at ~5,000 Kč is unproven: there are no sold prices and no CZ volume data.
  - **No export path.** The DE/Etsy expansion window is structurally empty (§5). Scaling beyond CZ therefore doesn't pay.
- **The dossier's compliance mitigations contain two internal contradictions** (§3.1 and §3.2). Both are fixable, but the dossier doesn't notice them.

---

## 2. Claims checked

| # | Dossier claim | What I found | Status |
|---|---|---|---|
| 1 | Donors are cheap in CZ (€15–25 purchase, €30 effective) | Aukro "nefunkční / na díly" units run from a few Kč to ~700 Kč, some at 240–1,580 Kč [file: 06-verification]. The **price** is confirmed. The **volume** isn't: the dossier's own estimate is 5–20 broken Classic/Video donors a month nationally, contested by other flippers [file: dossier §7, unverified]. | Price OK; volume unproven |
| 2 | "Buy batteries from an EU/CZ distributor with a CE declaration, so they are the battery producer, not you" (§7, §11) | This conflicts with the spec. S1 uses a **2,000 mAh** cell, S2/S3 a **3,000 mAh** cell, and the unit economics price the cell at EOE (Canada). My one search for these upgrade cells returned only US/international sellers (Amazon, eBay, DCG iPod, resalefirm, moonlit.market, iFlash.xyz) and no CZ distributor [verified: https://www.amazon.com/3000mAh-Battery-Replacement-Classic-Generation/dp/B088RJYTXZ, https://dcg-ipod.affinityco.net/products/3000mah-repalcement-battery, https://www.iflash.xyz/3rd-party-extended-battery-guide/]. The search skews to the US, so this is absence of evidence, not proof. CZ repair-parts shops typically stock OEM-capacity cells [knowledge]. | **Mitigation probably not executable with the stated spec** |
| 3 | CZ WEEE: you are a distributor, not a producer, if "CZ stock is sourced in CZ" (§11) | The same dossier recommends eBay.at/.de "defekt" donors to fill volume (§7), which contradicts it. It also claims **GPSR manufacturer** status for the substantial modification, which weakens the "mere distributor" argument under Act 542/2020 [knowledge]. | Internally inconsistent |
| 4 | Volná živnost is enough; no vázaná electrical licence | Correct. The device is USB-powered at 5 V. It stays correct only if you **don't bundle a mains charger** (see fix 9). The quickstart flags mains refurbishment as a grey zone (§1.2). | OK with a caveat |
| 5 | Etsy: only 5G/5.5G meet the 20-year vintage rule | Correct on dates [knowledge]: 5G Oct 2005, 5.5G Sep 2006, 6G Sep 2007, 7G Sep 2009. However, a 5.5G *manufactured* in 2007 is not yet 20. A unit with new storage, a new battery and possibly a new shell may not count as "vintage" at all under Etsy's rules. Etsy listings for 6G/7G builds exist, e.g. the $358 7G [file], so enforcement is loose. That is not the same as allowed, and a shop suspension hits a new seller hardest. | Confirmed, and riskier than stated |
| 6 | eBay.de needs DE WEEE + battery registration, and Abmahnung risk exists | Consistent with the quickstart §4.3–4.4 and scorer C: German marketplaces must check WEEE registration since ElektroG3 [file; knowledge]. | Confirmed |
| 7 | Vinted CZ (Pro) as a CZ channel | **Vinted Pro availability in CZ is unverified** in the dossier and here. Without it, business sales on Vinted breach the terms. DAC7 reporting flags a private account after 30 sales or €2,000 [file: quickstart §5.1], i.e. after about 10 iPods. Vinted CZ also trades with HR/HU/RO/SI [verified in dossier], which would trigger EPR duties there. | Channel may not exist |
| 8 | Registering in Oct 2026 is safe for the social-insurance threshold (29,375 CZK in 2026) | Correct. Q4 will be close to a loss after the ≈ €900 stage-1 spend [estimate]. | OK |
| 9 | Realistic M12 €500/month; "set aside ~38%" | €500/month (€6,000/yr ≈ 147k CZK) sits **exactly in the social-insurance dead zone**. Crossing 117,521 CZK costs ≈ 18,900 CZK at once [file: quickstart §2.1]. Take-home is no higher than at ≈ €400/month until profit reaches ≈ €505/month. Reasoning: net at the threshold is 117,521 × 0.7825 ≈ 91,960 CZK, and 91,960 / 0.622 ≈ 147,800 CZK/yr ≈ €503/month. | The realistic figure is the worst place to land |
| 10 | Stage 3 DE/Etsy adds profit | It adds almost nothing (see §5). | **Refuted** |
| 11 | "Back plate replaced if needed" in S1 at €8 | Cheap AliExpress 6G/7G back plates mostly carry the Apple logo and "iPod" engraving [knowledge]. The dossier itself bans logo-bearing aftermarket shells as counterfeit (§11). So in practice S1 can only use original back plates taken from donors, or verified logo-free ones. | Contradiction in practice |
| 12 | 12-week plan: list in week 5 | This only works if adapters are ordered in week 1. AliExpress lead time is 2–4 weeks [knowledge]. From 1 Jul 2026 an EU €3 duty applies per low-value item [file: quickstart §5.7], so expect extra customs handling. Genuine iFlash comes from the UK, which means import VAT a non-payer can't reclaim, plus a customs handling fee [knowledge]. | Feasible only with resequencing |

---

## 3. Legal load, item by item (CZ founder)

| Area | Load | Comment |
|---|---|---|
| **Živnost** | Low | Volná, 800 CZK online, ≤ 5 working days. Tick *Velkoobchod a maloobchod* and the electronics production/repair field [file]. Check the §304 ZP clause, which matters only if the employer is in electronics retail or repair. |
| **Income tax / levies** | Low–medium | See fix 10 (method choice) and fix 11 (the dead zone). **Pay private donor sellers by bank transfer and keep a one-line purchase note.** Otherwise donor costs are hard to evidence under actual expenses. |
| **VAT / identified person** | Low if CZ-only | Bazoš and Aukro are Czech platforms, so no reverse charge applies. **Any** Meta/TikTok ads, Etsy fee or Vinted boost triggers identified-person status: a monthly return by the 25th and 21% on the fee [file: quickstart §3.3]. The dossier's CZ-direct column assumes €1 of ads, so stay organic. |
| **OSS / €10k** | Only if exporting | This is what kills the DE window (§5). |
| **Margin scheme** | N/A | Non-payer. The dossier is right to ignore it. |
| **GPSR** | Medium, one-off | A 1-page risk sheet, a serial per unit, name, address and email, and CS warnings. Your **home address goes on every unit and listing**; a virtual address that actually receives mail avoids that [knowledge]. |
| **CE (EMC/RoHS)** | **Grey zone, not in the dossier** | The dossier asserts "substantial modification → you are the manufacturer" for GPSR. Under the Blue Guide logic, a modification that changes the *original performance* can make the product a "new product" that must meet CE rules again (EMC, RoHS for EEE) [knowledge]. A hobbyist can't evidence EMC or RoHS for AliExpress clone adapters. Enforcement risk at 5–10 Bazoš sales a month is low [estimate], but the risk is latent. Keep the position "repair with functionally equivalent replacement parts" and don't add USB-C or Bluetooth mods. |
| **WEEE (CZ)** | Low, but resolve it | Either keep donors strictly CZ-sourced and document "distributor" status, or simply join a CZ collective scheme (ASEKOL, REMA or ELEKTROWIN) as a small producer [knowledge]. My estimate is tens to low hundreds of € a year, based on small-client tariffs; get a quote. The second option removes the ambiguity and allows eBay.at/.de donors. |
| **Batteries (Reg. 2023/1542)** | **Medium, the real trap** | If you import upgrade cells yourself (EOE Canada, iFlash UK, AliExpress), you are the **importer and producer** of batteries in CZ. You then need EPR registration **and** cells that carry CE and conformity documentation, which most unbranded upgrade cells lack [knowledge]. Registration alone doesn't fix that: the cell must be compliant. See fix 1. |
| **Packaging EPR** | Low | EKO-KOM small-quantity relief; keep a weight log [file]. |
| **Warranty / withdrawal** | Medium, and it grows | 12 months for used goods only if the T&Cs say so. Presumption of defect is 1 year; claims must be settled within 30 days [file: quickstart §5.3]. **The warranty load grows with the installed base.** At 8–12% incidents a year [dossier estimate], 70 units sold in year 1 means 6–8 bench repairs spread over year 2 [estimate]. |
| **Li-ion shipping** | Low | Cells inside equipment by road with Packeta are fine [knowledge]. Never ship swollen cells. Do burn-in charging in a fire-safe box, and check whether your home insurance covers business activity [knowledge]. |
| **Trademark** | Low | Descriptive use of "iPod"; disclose "modified, not affiliated with Apple". The logo-free S3 shell is fine. Logo-bearing aftermarket plates are not (claim 11). |
| **Puncovnictví, AML, US tariffs** | N/A | No precious metals, no US shipping. The dossier correctly avoids the US. |
| **EET** | Watch | If EET returns (announced, status unverified [file: quickstart §5.3]), cash payment at handover could fall under it. Use QR bank transfer at handover. |

**Bottom line on legal:** CZ-only is clean and cheap once the battery source and the WEEE position are settled. Every step outside CZ, including Vinted cross-border, SK and Etsy, adds a per-country WEEE + battery + packaging registration.

### 3.1 The battery contradiction in more detail
- The product's selling point on eBay and Etsy is "2,000/3,000 mAh".
- The dossier's compliance escape is "buy from a CZ distributor", and I found no CZ distributor for those cells.
- The founder therefore faces a choice:
  - (a) Use standard-capacity cells from a CZ distributor. Flash storage draws far less than the HDD did, so runtime still improves a lot [knowledge]. Market the runtime, not the mAh figure.
  - (b) Register as a CZ battery producer **and** source upgrade cells that come with an EU declaration of conformity.
  - (c) Import unbranded cells and hope. That is the path the unit economics currently assume, and it breaks the dossier's own rule.

### 3.2 The WEEE contradiction
- "Keep CZ stock sourced in CZ" (§11) cannot coexist with "supplement with eBay.at/.de defekt units" (§7).
- Claiming GPSR-manufacturer status also undercuts the "distributor" framing.
- The cheap fix is to register with a CZ scheme.

---

## 4. Platform risk

| Channel | Risk | Notes |
|---|---|---|
| **Bazoš** | Low platform risk, high friction | Free, and there is no account to lose. The friction is scam buyers (fake "Zásilkovna/payment link" phishing aimed at sellers), haggling and no-shows [knowledge; scorer C]. You must disclose that you are a trader (IČO), or it is an unfair practice [file]. **Plus:** a handover in person is not a distance contract, so the 14-day withdrawal right doesn't apply [knowledge]. |
| **Aukro** | Low–medium | Czech company, so no reverse charge. **The dossier's CZ-direct column omits Aukro's commission**, ≈ 7–10% in electronics [knowledge, unverified]. Aukro has raised fees before [knowledge]. |
| **Vinted CZ** | **High until Vinted Pro is confirmed** | See claim 7. You also can't sell to HR/HU/RO/SI buyers without EPR there. If cross-border visibility can't be switched off, don't use Vinted. |
| **Etsy** | High | 5G/5.5G only, with a doubtful vintage status for modified units. Identified-person status from the first fee. Per-country EPR. New-shop payment reserves [knowledge]. One policy strike and the shop is gone. 6G units become eligible only from Sep 2027. |
| **eBay.de** | High | WEEE and battery numbers are checked. It also needs an Impressum, 24-month used-goods warranty in practice, and exposure to competitor Abmahnungen [file]. |
| **Instagram / TikTok (organic)** | Low | Free reach. Paid ads trigger identified-person status. |
| **Own Shoptet** | Low but premature | Adds a fixed cost, T&Cs and GDPR/cookie work, and the withdrawal button required since 19 Jun 2026 [file]. Not worth it below ~10 units a month. |

Channel concentration is low (classifieds and Aukro), which is good. The flip side is that none of these channels give you any buyer demand you can build on: every sale is a cold classified ad.

---

## 5. Why the DE/Etsy stage should be dropped: the window is empty

Assumptions, all from the dossier: the extra DE compliance fixed cost is ≈ €100–140/month (the dossier's own €130 vs €30); DE net before per-unit compliance allocation is ≈ €49 at €219 and ≈ €75 at €249 [estimate: the dossier's €34 + €15 allocation, plus the price step minus ~12% extra fees]; the OSS cap is €10k/yr across all EU cross-border B2C.

| DE price | Break-even units/month | Max units before OSS (€10k/yr) | Best possible monthly contribution |
|---|---|---|---|
| €219 | 2.0–2.9 | 3.8 | ≈ €45–85 |
| €249 | 1.3–1.9 | 3.3 | ≈ €110–150 |

- **Above the cap, 19% DE VAT via OSS takes ≈ €35/unit** [file], so the net goes to about zero.
- The best case is ≈ €150/month, in exchange for:
  - three registrations: WEEE and battery via a Bevollmächtigter, plus LUCID and a dual system;
  - monthly identified-person returns;
  - Abmahnung exposure;
  - 24-month warranties on DE sales.
- **Don't request DE quotes in week 8 either.** It is wasted effort.

---

## 6. Sourcing fragility and skill ramp

**Sourcing is the binding constraint, not hours.**
- 8–12 sellable units a month at 25–30% duds needs **11–17 donors a month**. That is at or above the dossier's own estimate of **5–20 broken donors a month nationally**, and other flippers and repair shops compete for them.
- The fallback, "working but tired" units at 1,500–2,500 Kč (€61–102), costs **€30–70 more per unit** than a €30 donor. The net falls to ≈ €30–60.
- My estimate: ≈ 5–6 good-margin donors a month is sustainable for one person. Volume above that comes at roughly half the margin.

**Parts:**
- Clone adapters vary and some are dead on arrival [file].
- Card prices are up ~124% [file: dossier, Tom's Hardware].
- Genuine iFlash comes via the UK, with import VAT and handling [knowledge].
- A torn headphone-jack/hold-switch flex, a common beginner accident on 6G/7G [knowledge], is a €5–15 part with a 2–4 week wait from China. Without spares on hand, one slip parks a unit for a month.

**Skill ramp (beginner, units 1–10):**
- The dossier's 4.5 h/unit is fair.
- Model quirks catch beginners [knowledge]:
  - 30 GB 5G/5.5G boards have half the RAM, so large libraries make the database struggle. Cap those boards at 128 GB.
  - The thin vs thick back plate decides which batteries fit.
  - The stock firmware and sync behaviour need explaining.
- Start with the 5G, as the dossier says. Expect 1–2 of the first 6 builds to need a second part order [estimate].

**Buyer-side ramp:**
- Gen-Z buyers usually stream. Spotify and Apple Music downloads can't go on an iPod Classic [knowledge].
- A buyer without MP3 files and a computer running Finder, Apple Devices or iTunes becomes a withdrawal. I'd set the withdrawal rate at 5–10%, not the dossier's 3–5% [estimate].
- The CS sync sheet is necessary, but the listing itself must pre-qualify buyers.

---

## 7. Time to first sale and the 12-week plan

- **Realistic first sale: week 6–8.** The živnost takes ≤ 5 working days, adapters take 2–4 weeks, and builds 1–2 take a week, so listing in week 5–6 is possible. The dossier's week-5 listing works only if adapters are ordered in week 1.
- **Weekly load:** weeks 1–5 run at ≈ 10–14 h: 6 builds × 4.5 h, plus the risk sheet, T&Cs, the CS/DE/EN leaflet, photos and watchdogs. That is feasible for an employed person, but tight in the build weeks.
- **Calendar effect.** Starting on 1 Oct 2026 puts week 10 in early December, right in the gift season (Packeta's Christmas cut-off is around 18–20 Dec [knowledge]). That helps sales, but it **flatters the day-90 gate**. Day 90 lands around New Year, before the January withdrawals, warranty claims and the Q1 slump.
- **Verdict on the plan:** a normal employed person can execute it with four changes:
  1. Order adapters and spares in week 1.
  2. Delete the DE quote step.
  3. Settle the battery source and WEEE position in week 1–2.
  4. Add a day-120 gate on the Jan–Feb run-rate.

---

## 8. What kills it in the first 6 months (ranked)

1. **Thin post-Christmas CZ demand at ~5,000 Kč.**
   - All price evidence is asking prices.
   - There is no CZ sold data.
   - 5,290 Kč is ~14% of a Czech monthly net wage [knowledge], steep for students.
   - A Jan–Mar run-rate under 5 a month is my single most likely failure [estimate].
2. **Donor starvation.** Fewer than 8 good donors a month at ≤ €30 effective forces a choice: stall the volume, or halve the margin with "working" units.
3. **Quality incidents.** Clone-adapter dropouts, beginner flex damage and failing cells can easily produce 2 incidents in the first 6 sales. That trips the dossier's own day-60 gate and dents Aukro/Bazoš reputation.
4. **Sync/DRM withdrawals** from streaming-native buyers.
5. **Scope creep** into DE/Etsy/Vinted-cross-border compliance: admin hours and €1,200–1,700 a year for ≤ €150/month (§5).

Legal and platform problems are **not** the likely killer if the founder stays CZ-only.

---

## 9. Fatal flaws

- **None for a CZ-only test.** It is cheap, reversible (dud donors and stock can be parted out) and legally clean once fixes 1–2 are done.
- **Fatal for the EU-expansion thesis:** the DE/Etsy window can't be worth more than ≈ €150/month (§5). With CZ as the only channel, the ceiling is set by CZ demand and CZ donor flow, roughly €500–750/month. That is not the asymmetric upside the brief asks for; the asymmetry is only on the downside (a cheap test).

---

## 10. Fixable issues and fixes

1. **Battery source vs spec.**
   - Before buying stock, find an EU-established seller of 2,000/3,000 mAh cells that has a declaration of conformity and is registered in CZ.
   - If there is none, either fit standard-capacity cells from a CZ distributor and advertise tested runtime, or register as a CZ battery producer and buy only CE-documented upgrade cells.
   - Drop EOE, AliExpress and unbranded cells.
2. **WEEE position.** Get a small-producer quote from ASEKOL, REMA or ELEKTROWIN in week 1. Joining costs little and permits foreign donors. Otherwise, source CZ-only and keep the purchase records.
3. **CE grey zone.**
   - Document the unit as a repair with like-function replacement parts.
   - Skip USB-C, Bluetooth and other mods that change the interface or performance class.
   - Use a genuine iFlash for premium units.
   - Put this question in the paid advisory hour. It needs a product-compliance adviser, not only a tax adviser.
4. **Back plates.** Only reuse original Apple plates harvested from dud donors (they are a free supply) or verified logo-free plates. Never use logo-bearing aftermarket plates.
5. **Drop stage 3 (DE/Etsy).** Put the €1,200–1,700 and the admin hours into CZ stock and spares instead.
6. **Vinted.** Don't list until Vinted Pro is confirmed in CZ **and** cross-border buyers can be excluded. Use Bazoš, Aukro and organic Instagram/TikTok.
7. **Parts sequencing.** In week 1, order clone adapters, spare headphone-jack/hold-switch flexes, battery connectors, clips and a spudger kit. Add ≈ €60 to stage 1.
8. **Withdrawals.**
   - Pre-qualify in the listing: "needs a computer and your own music files; streaming apps don't work".
   - Push in-person handover with a demo in Prague or Brno; an in-person sale has no 14-day withdrawal right.
   - Take payment by QR bank transfer.
9. **No chargers in the box.** A bundled mains USB charger would put you on the market for a mains device, with CE and WEEE duties. Ship with a cable only.
10. **Tax method.**
    - Keep full records and choose at filing between actual expenses and the 60% paušál.
    - At the dossier's €94 net on €216 (56% costs), the paušál is slightly better.
    - At my corrected ≈ €57 on €204 (≈ 72% costs), actual expenses win, and they keep the realistic profit under the social-insurance cliff.
11. **Social-insurance dead zone.** Plan to stay at ≤ ≈ €400/month profit or clear ≈ €505/month. Nothing in between improves take-home (claim 9).
12. **Gates.**
    - Keep the day-30 and day-60 gates.
    - Add a **day-120 gate**: Jan–Feb run-rate ≥ 5 a month at ≥ 4,790 Kč, with ≤ 10% withdrawals or claims.
    - Don't let December sales pass the business.
13. **Safety and insurance.** Charge and burn in inside a metal box or fire bag. Get product-liability quotes (2–4k CZK a year, dossier estimate) before the first sale. Check whether your home insurance excludes business use.
14. **Aukro fees.** Add ≈ 8% to the CZ-direct column for units sold on Aukro.

---

## 11. Corrected month-12 estimate (profit before income tax and levies)

Per-unit correction for CZ direct at M12 [estimate], starting from the dossier's €94 at 5,290 Kč:

| Adjustment | € per unit |
|---|---|
| Price compression to ~4,990 Kč (dossier's own 12–24-month compression call) | −12 |
| Blended donor cost €40, including "working" fill-ins (dossier forecasts €35–40) | −10 |
| About ⅓ of sales on Aukro at ~8% | −5 |
| Higher withdrawal/warranty reserve (sync, clone adapters) | −5 |
| Breakage spares, COD non-pickups and no-shows | −5 |
| **Corrected net per unit** | **≈ €57** |

Fixed costs: ≈ €45/month for insurance, a CZ WEEE/battery scheme, the accounting app and Bazoš bumps. Part-out income from dud donors adds ≈ €20–30/month.

| Scenario | Units/month | Net/unit | M12 profit/month | Notes |
|---|---|---|---|---|
| Pessimistic | 3 | €45 | **≈ €100** (in practice killed at day 90–120, with ≈ €200–400 lost after part-out) | Thin CZ demand after Christmas |
| **Realistic** | 6 | €57 | **≈ €300** | Donor-capped, CZ only |
| Optimistic | 10 | €75 | **≈ €750** | Strong CZ demand, a steady donor pipeline, some S3 units |

Dossier figures for comparison: €250 / €500 / €1,100.

**Hours at the realistic level:**
- Build and sell: 6 units × ≈ 2.3 h all-in = 13.8 h. That is the dossier's 1.9 h plus real pickup, dud and after-sales time.
- Admin: ≈ 4 h.
- Warranty bench work on the installed base: ≈ 1.5 h.
- Organic content: ≈ 2 h.
- **Total ≈ 21 h/month (≈ 5 h/week).**

**Effective rate: ≈ €14/h before levies.** The realistic profit (€3,600/yr ≈ 88k CZK) stays under the social cliff, so levies are ≈ 21.75%. That leaves **≈ €235/month take-home, ≈ €11/h**.

---

## 12. Would you tell a friend to do this?

**Only if** all of these hold:
- they already enjoy fiddly electronics;
- they stay CZ-only;
- they treat the ≈ €900 stage 1 as the entire commitment until **January–February** sell-through is proven;
- they fix the battery source before buying stock;
- they accept that this is a €200–700/month hobby-plus income that will fade with the fad, not a scalable business.

For a founder who has been burned by clever-sounding ideas, the redeeming feature is the downside: it is cheap to test, quick to read and easy to exit. Just don't expect it to grow.

---

Sources used this session (one search): https://www.amazon.com/3000mAh-Battery-Replacement-Classic-Generation/dp/B088RJYTXZ, https://www.ebay.com/itm/127790690794, https://dcg-ipod.affinityco.net/products/3000mah-repalcement-battery, https://resalefirm.com/products/2000mah-battery-for-ipod-classic-video-30-60-80-120-160gb-5th-6th-7th-square, https://moonlit.market/products/battery, https://www.iflash.xyz/3rd-party-extended-battery-guide/. All other citations come from the input files.
