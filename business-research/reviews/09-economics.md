# Review 09: A2 exam prep pack, ECONOMICS lens (unit economics and time)

Reviewer lens: unit economics and time skeptic. Dossier: `dossiers/09-a2-exam-prep.md` (C08).
Tags: **[verified: URL]** means a claim carried over from the dossier, `02-main-loop-evidence.md` or `06-verification.md` search snippets. **[knowledge]** means my background knowledge, not checked this session. **[estimate]** means my own arithmetic, with the reasoning shown. I ran one WebSearch, for the CzechReady premium price; it returned no price. Exchange rate: 24.5 CZK/€.

---

## Verdict: **WEAK, 4/10**

The dossier's arithmetic is internally consistent. Its inputs are optimistic in the three places that matter:
- **Paid CAC.** The 300 Kč figure is a best case. At a more likely 400–600 Kč including VAT, paid search loses money at 590 Kč.
- **Market share.** The realistic case assumes 2.5% of all candidates buy from a brand-new entrant within 12 months. My estimate is 1–1.5%.
- **Hours.** The build is about 300 h, not 155 h. The run phase is about 9–10 h/week, not 5–6 h/week.

Corrected:
- **Month-12 profit:** about **€300/month before levies (≈ €260 after)**.
- **Run-phase pay:** about **€7/hour**.
- **Year 1 in cash terms:** negative, about −€1,500 to −€2,000. Break-even comes around month 18.

The structural ceiling is about €1,000–1,500/month even as the category leader.

What keeps this from a KILL: the downside is small and well fenced. Stage 1 costs ≤ €1,000 plus about 60 h, it holds no inventory, and the kill gates are well designed. It is a cheap experiment with a low ceiling, not an asymmetric bet.

---

## 1. Claims checked

| # | Dossier claim | What I found | Effect |
|---|---|---|---|
| 1 | 14,000–18,000 candidates a year (≈ 1,250/month) | Consistent with 12,000+ passes in 2024 and an 86% pass rate [verified: https://msmt.gov.cz/zajem-o-zkousku-z-cestiny-pro-trvaly-pobyt-roste-stat-jiz; 06-verification]. The head-count is fine. The hidden assumption is **conversion**. | Neutral |
| 2 | Realistic month 12 = 32 A2 sales/month ≈ 2.5% of all candidates | For a new entrant in year 1 with no brand, this is too high. It competes with free NPI mocks, freemium CzechReady, free cestinaexam.cz, ExamOnline (1,900 Kč), Patreon, YouTube and paid courses. Base-rate reasoning [estimate]: perhaps 8–12% of candidates pay for *any* self-study product (most payers buy courses; most others use free material). That is ≈ 1,200–1,800 buyers a year across all vendors. A new entrant winning 15–25% of that in year 1 sells **15–35 a month**, centred near 18. | Volume roughly halved |
| 3 | Paid search CAC 300 Kč + 21% reverse-charge VAT = 363 Kč | CAC = CPC ÷ conversion rate. For CZ/UA/VI long-tail exam keywords, I'd expect a CPC of about 5–20 Kč [knowledge/estimate]. A cold landing page for a €24 digital product converts at about 1–3% [knowledge]. That gives a range of **170–1,000 Kč, centred at 400–500 Kč**. The free official site ranks first for the same queries. At a 450 Kč CAC (545 Kč with VAT), **a paid-only A2 sale at 590 Kč nets ≈ 9 Kč (€0.40)**: 590 − 18 fee − 18 refunds − 545 ads. | Paid search is break-even at best, so it isn't a scalable channel at this price |
| 4 | Payment fee ≈ 2% + 6 Kč; 3% refund and chargeback allowance | Reasonable. Stripe charges 1.5% + €0.25 for EEA cards; Czech gateways (GoPay/Comgate) are similar [knowledge]. Digital content with an express waiver keeps withdrawals low. Keep 3%, because a pack that is "off-level" or has errata errors will draw goodwill refunds. | OK |
| 5 | Income levies ≈ 8.7% of revenue (60% paušál) | Correct arithmetic under the 60% paušál [quickstart §2.4 example B]. Two caveats: **(a)** whether selling access to your own authored content is §7(1)(b) živnost income (60%) or a copyright licence under §7(2)(a) (40%) is a known grey zone in CZ practice [knowledge, uncertain]. At 40% the levies are ≈ 13% of revenue. **(b)** In year 1, real costs (builds, voices, translators, ads) will probably exceed 60% of revenue, so **actual expenses beat the paušál in the build year**: roughly €0 of tax instead of ≈ €350–400. | Small; fixable (see below) |
| 6 | Fixed costs €45–60/month | Itemised [estimate]: checkout/member SaaS (FAPI/SimpleShop class) €25–50, email tool with automation €15–30, hosting and domain €5, invoicing and bookkeeping tool €5–8. **€55–90/month**; I use €70. | Minor |
| 7 | Build = 155 h A2 + 50 h B1 | Too low. See the time model below: **≈ 300 h for A2 + 70–100 h for B1**. Item writing (7 h per full mock of about 50 items plus writing and speaking tasks), explanations (14 h for about 400 items in total) and the web app (20 h for auth, auto-scoring, streamed audio, in-browser recording, watermarking and a 5-language UI) are each understated by 1.5–3×. | Full pack ships around month 6–7, not week 8–12 |
| 8 | Run phase ≈ 5–6 h/week at 30–40 sales/month | The dossier's own risk section says ads don't work and distribution is community work. Community presence, ambassador management, 5-language SEO, pre-sale questions from non-native speakers, errata, a monthly identified-person VAT return and contractor admin add up to **≈ 9–10 h/week at about 20 sales/month**. | €/hour roughly halved |
| 9 | Stage-2 budget €2,600 (cumulative €3,600) | Under-budgeted by about €1,000–1,300 [estimate]. Explanations for 8 mocks plus the template bank and UI come to about 18–22k words per language, ≈ 70–80 normostran at about 200 Kč, ≈ **€600 per language, €1,800 for UA/RU/VI**, against the €935 budgeted. Teacher review at 8 × 3 h × 600 Kč ≈ €590, against €350 budgeted. Voices at 8–10 h of sessions × 2–3 voices × 700 Kč ≈ €550–700, against €500. **Realistic cumulative spend: €4,500–5,000.** | Longer payback |
| 10 | Optimistic month 12 = €2,300 (75 A2 + 25 B1 sales/month) | 75 A2 sales is ≈ 6% of every candidate in the country each month, from a first-year entrant. Not credible inside 12 months. | Optimistic cut to ≈ €1,000 |
| 11 | B2B 10-seat licence, ≈ €200/month in the optimistic case | NGOs and integration centres run grant-funded free courses and already have free NPI material [knowledge]. Their sales cycles are slow and hour-heavy. Year-1 B2B ≈ €0–100/month. | Minor |
| 12 | Hidden admin: paying voices, translators and reviewers | If they aren't OSVČ, you either pay them through a DPP, which since 2025 means monthly reporting to ČSSZ [knowledge], or take a licence agreement with 15% withholding tax plus the annual withholding report [knowledge]. Each option adds 3–6 h of setup and a recurring filing. | Hours and admin risk |

---

## 2. Rebuilt unit economics (per sale, Kč)

Assumptions [estimate]:
- **Realised price.** The A2 mix is 60% A (590) and 40% B (890), which averages 710 Kč. After coupon codes for community posts, affiliate buyer discounts and launch promos (≈ 10%), the realised price is **640 Kč**. B1 is sold mostly as a discounted cross-sell at **670 Kč**.
- **Channel mix.** 30% paid at a 450 Kč CAC plus 21% VAT = 545 Kč per paid sale. 20% through affiliates at 25%. The rest is organic or community.

| Line | A2 blended | B1 cross-sell | A2, paid-only (stress) | Dossier A2 blended (for comparison) |
|---|---|---|---|---|
| Realised price | 640 | 670 | 590 | 590 / 890 |
| Payment fee | −19 | −19 | −18 | −18 / −24 |
| Refund/chargeback 3% | −19 | −20 | −18 | −18 / −27 |
| Affiliate (blended 5%) | −32 | −34 | 0 | −30 / −45 |
| Ads (blended, incl. VAT) | −164 | −55 | −545 | −145 |
| **Contribution** | **406 (€16.6)** | **542 (€22.1)** | **9 (€0.4)** | 379–649 (€15.5–26.5) |
| Levies at 8.7% of revenue (13% if the 40% paušál applies) | −56 (−83) | −58 | −51 | −51 / −77 |
| **After levies** | **350 (€14.3)** | **484 (€19.8)** | **≈ −42** | €13.4–23.3 |

**Takeaways:**
- Per-unit contribution is roughly what the dossier says (€16–17 blended, against its ≈ €19).
- **The damage is in volume and hours, not in the per-unit line.**
- Paid search at the current prices is a loss-leader, so growth depends entirely on the founder's unpaid community hours.
- There is no inventory, shipping, packaging, breakage, GPSR or EPR cost; this is correct for pure digital.
- Warranty exposure is limited to digital-content conformity: answer-key errors lead to errata and refunds, which the 3% allowance covers.
- Insurance is negligible.

---

## 3. Realistic time model

### Build [estimate]

| Step | Dossier | My estimate | Why |
|---|---|---|---|
| Spec study, benchmarking | 8 h | 10–12 h | Includes working through NPI mocks 1–2, CzechReady and ExamOnline |
| 8 mocks: original texts, ~50 items each, distractors, keys, pictures, revisions after teacher review | 56 h | 80–110 h | 10–14 h per mock for a non-professional item writer calibrating to A2 |
| Audio: scripting, scheduling voices, recording, retakes, editing, loudness | 32 h | 40–48 h | 5–6 h per mock |
| Writing templates + fail/pass/strong answers + rubric | 10 h | 15–20 h | |
| Speaking drills + phonetics audio | 8 h | 12–15 h | |
| Item explanations (~400 items) + briefing and QA of 3 translators | 14 h | 40–50 h | About 5 min per item, plus translation coordination |
| Platform: checkout, member area, auto-scored quizzes with audio, record-and-compare, watermarking, 5-language UI | 20 h | 50–70 h | Assumes a non-developer on WordPress + FAPI/SimpleShop + a quiz plugin; record-and-compare is custom JS |
| Anki deck + date-driven email plan | not itemised | 10–15 h | |
| Lead magnet + landing pages in 4–5 languages | 6 h | 12–15 h | |
| T&Cs, GDPR notice, withdrawal-waiver flow, contracts with voices and translators | 0 h | 6–10 h | |
| **Total, A2 Complete** | **155 h** | **≈ 275–365 h (use 300)** | |
| B1 + reálie pack | 50 h | 70–100 h | |

At a realistic 12 effective h/week, the full A2 pack ships around **month 6–7**. The B1 pack, if the gates are passed, lands around **month 9–10**. Months 1–7 are therefore build-dominated, and sales run on a partial product.

### Run phase at ≈ 20 sales/month [estimate]

| Task | h/month |
|---|---|
| Support, including pre-sale questions from non-native speakers (≈ 10 min per sale + 5 min per enquiry) | 5 |
| Community posting, ambassador and admin relations, lead-magnet distribution | 17 |
| SEO articles and short videos in several languages | 8–9 |
| Ads management and pruning | 4 |
| Errata, updates, format tweaks | 4 |
| Admin: identified-person VAT return (monthly), bookkeeping, affiliate payouts, contractor filings | 2 |
| **Total** | **≈ 41 h/month ≈ 9.5 h/week** |

**Hours per unit:** about 41 h ÷ 22 sales ≈ **1.9 h of founder time per sale** at month 12, before counting any amortised build. At about €16 contribution per sale, the "product" behaves like time-for-money at about **€8/hour**.

---

## 4. Cash, sell-through and payback (realistic branch, continuing past the gates) [estimate]

- **Inventory:** none. Cash at risk is the build spend.
  - Stage 1 non-ad, non-fixed spend ≈ €670.
  - Stage 2 corrected ≈ €2,850.
  - Total one-off ≈ **€3,500**.
- **Sales ramp:**
  - Month 2: about 20 pre-sales at 390 Kč.
  - Months 3–12: 8 → 20 A2 sales per month, about 136 in total.
  - B1 from month 9: 2 → 4 per month, about 13 in total.
- **Year-1 cash:**
  - Contribution after ads ≈ €2,450–2,700. The lower end reflects months 3–7, when only the 590 Kč 4-mock product exists.
  - Fixed costs ≈ €840.
  - One-off build ≈ €3,500.
  - **Year-1 net ≈ −€1,650 to −€1,900.**
  - Maximum drawdown is about €2,500–3,000, around month 7–8.
- **Break-even:** around month 18, at a run-rate of about €300/month.
- **Year-1 €/hour:** negative. About 600 h in total (≈ 300 h build + ≈ 300 h run and marketing) for about −€1,650 to −€1,900.
- **Lifetime (to about 2029–30, when the format next changes):**
  - Assumes maintenance mode at 4–6 h/week earning €200–350/month.
  - That works out to roughly **€3–6/hour** over the product's life.
  - The ZDP-driven Ukrainian cohort (2028–30) could lift it, but that falls outside the 12-month window.

---

## 5. Fatal (structural) flaws

1. **The only scalable channel does not pay at this price point.**
   - At a realistic 400–600 Kč CAC including VAT, paid search is break-even on a 590 Kč pack.
   - All profitable volume must come from the founder's own community and affiliate work.
   - That turns a "digital product" into roughly 2 hours of founder labour per sale. This is exactly the service-like profile the brief tries to avoid, just without an invoice.
2. **The ceiling is low.**
   - The addressable pool of *self-study buyers* is about 1,200–1,800 a year across all vendors [estimate].
   - A category leader with 40% share sells about 40–60 A2 packs a month. That is ≈ **€1,000–1,500/month** before levies, even with B1.
   - It cannot become meaningfully larger without turning into an AI-graded SaaS, which means competing with CzechReady.
3. **Free substitutes erode willingness to pay over time.**
   - The substitutes are two official new-format mocks, CzechReady's free tier, and general-purpose LLMs that will generate A2 practice and grade a letter for free [knowledge].
   - The dossier's durability argument ("sellable to 2030") covers the *content*, not the *price*.

None of these kills the stage-1 test, which is cheap. Together, they make it very unlikely that the month-12 business pays more than about €8–10/hour.

---

## 6. Fixable issues and fixes

| Issue | Fix |
|---|---|
| Underpricing kills the paid channel | The anchors are ExamOnline at 1,900 Kč and the exam fee at 3,200 Kč. **Test 790 / 1,190 Kč** (A / Complete) against 590 / 890 in the pre-sale, using two landing variants. At 1,190 Kč a paid sale nets ≈ 550 Kč even at a 545 Kč CAC, which roughly doubles blended contribution. Position B, "Complete", as the default. |
| Build scope and translation budget are too large before evidence | Ship **4 mocks, not 8**, before day 90. Launch in **UA + EN only**. Add VI only if a Vietnamese channel is proven, and make RU optional. This cuts translation spend from about €1,800 to about €600 and saves about 60–80 h. Defer the Anki deck, the date-driven email plan and record-and-compare. |
| Weak pre-sale signal (390 Kč from friendly communities) | The gate should require **≥ 10 sales at full price** from strangers, and should count **founder hours per sale**. |
| Kill gates measure sales, not €/hour | Add a day-90 gate of **contribution ÷ hours ≥ €12/h**. Otherwise freeze to passive mode on a zero-fixed-cost merchant-of-record host (Lemon Squeezy/Gumroad-style, ≈ 5–10% per sale) so a frozen product costs nothing monthly. |
| Paying levies on a loss year | Use **actual expenses (daňová evidence) in year 1**, then switch to the paušál in year 2. Confirm the 60% vs 40% paušál question with a tax advisor before relying on 8.7%. If the founder also runs another side business, remember that deemed profits combine against the 117,521 Kč social-insurance threshold. |
| Identified-person admin for small ad spend | If ads stay marginal, test **Sklik (Seznam, a domestic supplier with no reverse charge)** first. Avoid foreign SaaS so the monthly VAT return isn't triggered for €50 of Google Ads. Otherwise accept about 25 min/month of admin. |
| Contractor admin | Hire voices, translators and reviewers who **invoice as OSVČ**, with a licence assignment in the contract. Avoid DPP payroll reporting and royalty withholding. |
| Target segment too broad | Focus the message on **re-sit candidates** (≈ 14% fail, ≈ 170/month) and on **writing**, the weakest skill at 65.9%. These buyers have the highest willingness to pay. |

---

## 7. Corrected month-12 estimate

Profit is after ads and fixed costs; "net" is after income levies.

| Scenario | Month-12 sales | Before levies | After levies | Founder hours | €/hour (run phase) |
|---|---|---|---|---|---|
| Pessimistic (≈ 50% probability: fails the day-30 or day-90 gate, frozen on a zero-fixed-cost host) | 0–5 passive | **€0–50** | €0–45 | ≈ 0–1 h/week | n/a (sunk cost ≈ €700–1,000 + 60–100 h) |
| **Realistic** (continues at modest scale) | 18 A2 + 4 B1 | **≈ €300** (18 × €16.6 + 4 × €22 − €70 fixed ≈ €320) | **≈ €260** | ≈ 9.5 h/week | **≈ €7** (≈ €6 after levies; ≈ €0 or negative over year 1 including the build) |
| Optimistic (a strong UA community partner, price raised) | 45 A2 + 12 B1 + small B2B | **≈ €1,000** | ≈ €900 | 12–15 h/week | ≈ €16–19 |

The dossier's claim of **€700/month at 5–6 h/week (≈ €26/h) is not credible**. It needs roughly 2× my realistic volume at roughly half my hours. Even using the whole 10–15 h/week budget, the realistic month-12 figure is about €300–450, because months 1–7 are consumed by the build.

The probability-weighted month-12 result is ≈ 0.5 × €25 + 0.4 × €320 + 0.1 × €1,000 ≈ **€240/month**.

---

## 8. Would I tell a friend to do this?

**Only if** all three hold:
- They are a native Czech speaker with real experience teaching Czech as a foreign language, so item writing is fast and credible.
- They already have a trusted foothold in a Ukrainian or Vietnamese community (group admin, ambassador, or partner school), so CAC is near zero.
- They cap it at ≈ €1,000 and ≈ 60 h, with the day-30 gate enforced and full-price sales counted.

Otherwise, **no**. The realistic outcome is about €7/hour after a year of evenings, with a ceiling around €1,000–1,500/month. The founder's scarce 10–15 h/week earns more in almost any of the physical-goods candidates, or even in a plain DPP side job.
