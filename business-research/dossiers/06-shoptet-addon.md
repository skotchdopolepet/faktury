# Dossier C05: Shoptet add-on (promo mechanics, and which Shoptet niche to pick instead)

Date: 2026-09-29. FX: 25 CZK = €1 (the hunter's rounding). Labels: **[verified: URL]** means a web-search snippet this session or the orchestrator's evidence (no page was opened). **[crawl]** means the hunter's 2026-08-21 marketplace crawl (https://github.com/mchlkucera/localproblems/blob/main/data/lookup/cz-eshop-addons.jsonl). **[knowledge]** and **[estimate]** are as defined in the brief.

## 1. Verdict in 3 lines
- **No-go on promo mechanics as specified.** It is crowded, a third party cannot own the cart price, and it competes with Shoptet's own paid add-ons, which Shoptet itself approves or rejects. **Weak conditional-go** on the better Shoptet niche, a **Shoptet → iDoklad invoice connector (C13 re-scoped)**, but only if the founder passes a coding gate and two free gates: no live iDoklad listing, and Shoptet approves the proposal.
- **Realistic month-12 profit: about €125/month** (18 paying shops). It could reach about €400/month by month 24. The idea compounds slowly and will not beat the resale candidates in year 1.
- **Biggest risk:** spending 150–200 evening hours on something an existing connector (Shoptet's own iDoklad add-on, GoodEshop, Dativery) or a rejected proposal makes worthless. Both gates are checked before building.

## 2. The exact offer
| SKU | Spec | Price | Buyer / channel |
|---|---|---|---|
| **"Faktury do iDokladu" Basic** (working name) | Paid Shoptet order → iDoklad invoice. Cancellation or return → credit note. Payment status synced back. VAT-rate, shipping, payment-fee and discount mapping. Sync log with one-click retry. Setup wizard with a dry-run preview of the last 5 orders | 290 CZK/month up to 300 orders/month; 2,900 CZK/year | CZ (then SK) Shoptet merchants who keep invoicing in iDoklad: OSVČ sole traders and small s.r.o. companies, 20–500 orders/month. Sold on doplnky.shoptet.cz (30-day trial), iDoklad's integrations page, Shoptet merchant Facebook groups, and the authors of partneri.shoptet.cz demand posts |
| **Basic → Plus** | Unlimited orders, OSS and foreign currencies, several shops into one iDoklad account | 490 CZK/month | Same buyers, larger shops |
| *Comparison only: promo add-on* | Gift tiers, quantity-break display, free-gift progress bar | 290 CZK/month | Not recommended (§4–5) |

Pricing sits under the incumbent accounting connectors: Pohoda by Prajzler at 300 CZK and Money S3 by Napojse at 400 CZK **[crawl]**.

## 3. Why it makes money (demand evidence)
- **The Shoptet base** is about 41,000 shops in CZ, SK and HU **[verified: https://cc.cz/shoptet-nasel-klic-jak-rychle-rust-i-na-rozebranem-e-commerce-trhu-loni-utrzil-temer-800-milionu/]**. Merchants buy add-ons inside the Shoptet admin, usually for "hundreds of CZK a month" **[verified: https://blog.shoptet.cz/rozhovor-marketplace-tym/]**.
- **Accounting connectors are a proven, paid, sticky category [crawl]:**

  | Connector | Ratings / average | Price |
  |---|---|---|
  | Pohoda by Dominik Prajzler (solo developer) | 36 / 5.0 | 300 CZK/month + optional 18,000 CZK setup |
  | Napojse Money S3 | 15 | 400 CZK/month |
  | SuperFaktura | 15 | 100 CZK/month |
  | Fakturoid by Kulhánek | 7 | 300 CZK/month |
  | Shoptet's own Pohoda add-on | 9 / 3.2 | 200 CZK/month |
- **Merchants ask for exactly this:** there is a public "Shoptet/iDoklad" demand post **[verified: https://partneri.shoptet.cz/poptavka/shoptet-idoklad-2/]**.
- **Promo demand is larger but already served:**
  - Shoptet's native Dárky has 49 ratings, Množstevní slevy 41, Slevové kupóny 58 and X+Y 17, at 100–300 CZK/month **[crawl]**.
  - Third-party AOV tools have 69–88 ratings **[crawl]**.
  - There is a demand post for a quantity-discount add-on **[verified: https://partneri.shoptet.cz/poptavka/doplnek-mnozstevni-sleva/]**.
- **Ratings are not installs.** Shoptet publishes no install counts. I assume paying installs are **3–10× the rating count** **[estimate: typical app-store review rates of 5–20%, unverified for Shoptet]**. On that assumption:
  - The **median monthly add-on** (8 ratings, 100 CZK **[crawl]**) earns about 25–80 installs, or **€100–320/month gross**.
  - The **Fakturoid connector** (7 ratings × 3–10 × 300 CZK) grosses about **€250–840/month** after years on the market.
  - **Pohoda by Prajzler** grosses about **€1.3k–4.3k/month** plus setup fees.

  This is the realistic ceiling band for a niche connector.

## 4. Supply gap and asymmetry: an honest reassessment
**Promo mechanics: the gap is mostly gone.**
- **Native Shoptet covers the core.** Množstevní slevy, Objemové slevy (order-value tiers, shown on the product or in the cart **[verified: https://doplnky.shoptet.cz/objemove-slevy]**), Slevy X+Y, Dárky, Věrnostní slevy and Slevové kupóny.
- **Third parties cover the display layer:**
  - "Pro dopravu/dárek zdarma zbývá" (orchestrator)
  - "Rozbalené dárky v košíku" **[crawl]**
  - "Dynamické akce a slevy" **[verified: https://doplnky.shoptet.cz/dynamicke-akce-a-slevy]**
  - "Cena po zadání slevového kódu" **[verified: https://doplnky.shoptet.cz/cena-po-zadani-slevoveho-kodu]**
  - "Bonusový systém" **[verified: https://doplnky.shoptet.cz/bonusovy-system]**
  - "Upsell a cross sell"; "Doplňkový prodej v košíku" **[crawl]**

  The hunter's claim that no third-party alternative exists is false (scorer A is right).
- **Technical ceiling.** The API exposes discount-coupon generation **[verified: https://developers.shoptet.com/insert-discount-coupons-via-api/]**, quantity discounts **[verified: https://api.docs.shoptet.com/shoptet-api/openapi/quantity-discounts]**, price lists **[verified: https://api.docs.shoptet.com/shoptet-api/openapi/price-lists]**, and order items of type "discount-coupon" **[verified: https://api.docs.shoptet.com/shoptet-api/openapi/order-items]**.
  - I know of **no hook that lets an add-on compute cart prices at checkout** **[knowledge: the Shoptet API is an admin API; cart totals come from Shoptet's own price lists, native discount modules and coupons]**.
  - A third-party "promo engine" can therefore only emulate mechanics:
    - auto-applying coupons through injected storefront JS;
    - writing the native modules' settings;
    - adding 0-CZK gift products by JS, which customers can abuse;
    - editing orders after checkout, which the customer never sees.
  - Storefront JS breaks when Shoptet ships frontend changes, which it announces regularly **[verified: https://developers.shoptet.com/frontend-news-from-july-21-2026/, https://developers.shoptet.com/frontend-news-from-september-09-2026/]**.
- **Approval conflict.** Shoptet assesses every proposal *before* development for "fit, benefit to the customer and pricing policy", and replies within 4 weeks **[verified: https://doplnky.shoptet.cz/chcete-delat-vlastni-doplnky]**. A clone of Shoptet's own paid promo add-ons is the proposal most likely to be refused **[estimate]**.
- **What is left is a quality gap.** The native promo add-ons average 3.0–3.2 **[crawl]**. Shoptet can close that in one sprint.

**iDoklad connector: a thinner but more defensible gap.**
- **What already exists:**
  - Shoptet announced its own "napojení na iDoklad" add-on at doplnky.shoptet.cz/idoklad, years ago **[verified: https://m.facebook.com/shoptet/photos/m%C3%A1me-pro-v%C3%A1s-druh%C3%BD-dopln%C4%9Bk-shoptet-api-je-to-n%C4%9Bco-co-jste-cht%C4%9Bli-u%C5%BE-dlouho-napoj/10156297268950266/]**. It was **absent from the Aug-2026 crawl** of 394 listings **[crawl]**, so it may have been retired. **Its current status is the #1 check.**
  - Off-marketplace, GoodEshop sells a Shoptet–iDoklad integration **[verified: https://goodeshop.cz/integration/shoptet-idoklad]**, and Dativery integrates Shoptet with accounting systems **[verified: https://www.dativery.com/cs/s-type/full-connection-shoptet-with-accounting/]**.
  - Scorer B's "off-marketplace integrators exist" is confirmed.
- **Why it is still the better niche:**
  - **Merchants search the marketplace first.** An in-marketplace connector with a trial beats an integrator site **[knowledge]**.
  - **It runs only on the back end**, through the API and webhooks. That means no template fragility, and the code is deterministic and testable, which suits AI-assisted development.
  - **Churn is low.** Switching connectors means re-mapping VAT, so merchants stay.
  - **Low conflict with Shoptet's own add-ons**, if Shoptet has retired its own.
- **Durability:** the gap is 1–3 years. Trexify, who builds these connectors for Upgates, could port them **[crawl]**, and iDoklad (Solitea) could ship its own connector.

**Other Shoptet niches checked:**
- **Back-in-stock:** the native Hlídací pes already covers restock, promo and price-below alerts **[verified: https://podpora.shoptet.cz/hlidaci-pes/]**. Rejected.
- **Repeat-purchase reminders:** exist (Incomaker, Repetiv) **[verified: https://doplnky.shoptet.cz/incomaker]**. Rejected.
- **True recurring-payment subscriptions:** there are repeated demand posts **[verified: https://partneri.shoptet.cz/poptavka/predplatne-pro-produkty-2/, https://partneri.shoptet.cz/poptavka/opakovana-objednavka-opakovana-platba/]**. But card tokenisation through the payment gateway plus money-movement bugs is too hard and too urgent for a non-senior evening developer. Rejected.
- **B2B suite:** a valid second product (native Velkoobchod rated 3.2 at 400 CZK **[crawl]**), but it needs storefront JS. Keep it for later.

**Asymmetry:** cash at risk is under €1k, and a won shop pays monthly for years. The real stake is **founder time**, and it is not scarcity-driven. Base rate: about 70% of micro-SaaS stay under $1k MRR, and part-timers grow 2.2× slower (longlist traps).

## 5. Competitor map
| Space | Competitor | Price | Position |
|---|---|---|---|
| iDoklad | Shoptet "iDoklad" add-on | ? (status unknown) | Native, old; possibly retired |
| iDoklad | GoodEshop | ? | Off-marketplace integrator |
| Accounting | Dativery | Custom | Integrator, Pohoda-focused, service-like |
| Accounting | Pohoda by Prajzler | 300/month + 18k setup | Solo developer, 5.0, the benchmark |
| Accounting | Napojse Money S3 / Seyfor Money S3 | 400/month / ? | Seyfor rated 1.0 |
| Accounting | Fakturoid by Kulhánek; SuperFaktura; iÚčto | 300 / 100 / ? | Small |
| Promo | Native Dárky / Množstevní / X+Y / Objemové / Věrnostní / Kupóny | 100–300/month | Rated 3.0–3.2, high volume |
| Promo | Pro dopravu/dárek zdarma zbývá, Rozbalené dárky (490 one-time, 3.9), Dynamické akce, Cena po zadání kódu, Bonusový systém | 100–500 | Display and automation layer |

Prices are in CZK **[crawl / verified URLs above]**.

## 6. Unit economics (per shop per month)
Assumptions:
- **Shoptet commission: 25%.** It is **not public** and is set in the partner contract **[verified: https://partneri.shoptet.cz/api-partneri/ names a commissions contact; no rate is published]**. The sensitivity case uses 30%.
- **Billing:** Shoptet bills the merchant and pays the partner, so there is no card fee **[knowledge; verify in contract]**.

| CZK/month | Basic 290 | Plus 490 | Promo 290 (comparison) | Back-in-stock 190 |
|---|---|---|---|---|
| Shoptet commission (25%) | −72 | −122 | −72 | −48 |
| Payment fee | 0 | 0 | 0 | 0 |
| Hosting per shop (VPS €6 ÷ ~15 shops) | −10 | −15 | −10 | −15 (incl. e-mail) |
| Churn/refund allowance (3%; promo and alerts 5%) | −7 | −11 | −11 | −8 |
| Ads | 0 | 0 | 0 | 0 |
| **Net per shop** | **≈201 (€8.0)** | **≈342 (€13.7)** | **≈197 (€7.9)** | **≈119 (€4.8)** |
| Net at 30% commission | ≈187 (€7.5) | ≈317 (€12.7) | ≈182 | ≈110 |

Levies:
- Use the 60% flat-rate expenses (paušál).
- While under the social-insurance threshold, set aside about 8.7% of revenue (quickstart §2.4).
- **€500/month net needs about 60 Basic shops.** That is month 24–36, not month 12 (scorers A and B).

## 7. Build plan (the software counterpart of "sourcing")
- **Stack:** Laravel/PHP 8 with MySQL on one small VPS.
  - Shoptet's PHP SDK exists (it exposes a webhook-event enum) **[verified: https://api.docs.shoptet.com/shoptet-api/openapi/section/code-lists/system-webhooks]**.
  - There is a community add-on skeleton (pajaeu/shoptet-addon-skeleton) **[hunter, GitHub]**.
  - iDoklad has a public REST API with OAuth2 **[knowledge; check which iDoklad plan includes API access]**.
- **Hosting:**
  - A Czech VPS (e.g. Wedos) at about 150–300 CZK/month **[knowledge]**. This avoids the identified-person trigger.
  - Alternative: Hetzner (DE), about €5–8/month **[knowledge]**, which is a foreign service and so a trigger.
  - Domain about 300 CZK/year; off-site backups about €2/month.
- **Shoptet access:** partners get an unlimited free test shop after the contract **[verified: https://doplnky.shoptet.cz/chcete-delat-vlastni-doplnky]**.
- **Build estimate (about 150 h)** **[estimate]**:

  | Component | Hours |
  |---|---|
  | OAuth install and settings | 15 |
  | Webhooks and order fetch | 15 |
  | iDoklad client and VAT/shipping/discount mapping | 35 |
  | Credit notes and cancellations | 15 |
  | Payment back-sync | 10 |
  | Sync log and retry UI | 12 |
  | 50-case fixture test suite | 20 |
  | Deploy and monitoring | 8 |
  | Czech listing and 15 KB articles | 12 |
  | Shoptet review fixes | 8 |

  For comparison, the promo add-on needs about 130 h plus 2–4 h/month of template upkeep.
- **Skill requirement (non-senior plus AI tools):**
  - The founder must be able to read REST docs, run OAuth2 and verify webhooks, write queued, idempotent jobs, deploy Linux with HTTPS, and debug production logs alone at 22:00.
  - AI tools write most of the code; they do not replace debugging judgement.
  - Nothing in the founder's workspace (a folder of invoice images) shows coding experience.
  - **Gate in week 1:** build and deploy a toy app that receives a webhook and writes it to a database over HTTPS, in 8 hours or less. If that fails, stop; the build would take 2–3× longer.
- **Weekly volume:** 3–5 new paying shops per month after launch is realistic for a niche connector **[estimate: marketplace "new" placement plus category search; no install data]**.

## 8. Time model
| Activity | Per new shop | Recurring |
|---|---|---|
| Onboarding | 0 min (self-serve wizard) | — |
| First-month questions | 20–30 min (falls to about 10 with the KB) | — |
| Ongoing support | — | 5–10 min/shop/month |
| API and maintenance upkeep | — | 2–4 h/month |
| Marketing (listing, Facebook groups, iDoklad partner page) | — | 2–4 h/month |

- **Build phase:** 12 h/week for about 13 weeks.
- **At 18–25 shops:** about **2–3 h/week**.
- **Keeping it a product and not a service:**
  - E-mail-only support with a stated 1-business-day SLA; no phone.
  - No paid setup (unlike Prajzler's 18k CZK) and no custom mappings.
  - A published "not supported" list (Money, Pohoda, zálohové faktury in v1).
  - Plain-Czech error messages with a retry button.
  - Automatic alerts to the merchant, sent before they notice.
  - A reminder on the 20th to review failed syncs before the kontrolní hlášení control statement is due on the 25th (answers scorer C's point about deadline urgency).

## 9. Staged budget
| Stage | Items | € |
|---|---|---|
| **1 (weeks 1–12)** | Trade licence 32 · tax advisor 1 h 80 · VPS 3 months 20 · domain 12 · iDoklad plan 3 months ~30 · AI coding tool 3 months 60 (if not owned) · one-off accountant review of VAT mapping 150 · T&C + DPA template 100 | **≈ 484 (cap 1,000)** |
| Stage 1 pass rule | By day 90: Shoptet approved and technical review submitted; ≥3 beta shops synced ≥50 real orders with 0 unrecovered errors; support ≤1 h/week | |
| **2 (months 4–12)** | Hosting and tools 300 · listing graphics and short video 150 · Czech copy edit 100 · contingency 400 | **≈ 950** |
| **Total** | | **≈ 1,450** (far under €8,500) |

Do not buy ads. They trigger identified-person status, and at €8/shop/month a €50–150 customer-acquisition cost takes 6–19 months to pay back **[estimate]**.

## 10. Projections (net CZK → €, pre-tax, all [estimate])
Timeline assumptions:
- Proposal decision by week 4; build weeks 4–13; Shoptet technical review 2–4 weeks; public launch in month 4–5.
- The 30-day trial pushes the first revenue to month 5–6.
- Fixed costs are about €25/month.

| Month | Pessimistic | Realistic | Optimistic |
|---|---|---|---|
| 3 | −€40 (in build) | −€40 | −€40 |
| 6 | 0 shops → −€25 | 3 shops → ≈ €0 | 8 shops → +€40 |
| 12 | 5 shops → +€15 | 16 Basic + 2 Plus → **≈ +€125** | 45 Basic + 10 Plus → ≈ +€470 |

- **Month 24, realistic:** 45–60 shops, about €350–480/month.
- **Promo variant:** similar numbers, with higher churn and template upkeep, and €0 if Shoptet refuses it.
- **Longlist comparison:** the €350–450 month-12 figures in the longlist ignore the 4–5-month approval, build and review lag.

## 11. CZ/EU legal checklist
- **Trade licence (živnost):** volná, field "Poskytování software, poradenství v oblasti informačních technologií, zpracování dat, hostingové a související činnosti a webové portály"; 800 CZK online (quickstart §1.1).
  - Register once Shoptet approves, because the partner contract needs an IČO **[knowledge]**.
  - Check § 304 of the Labour Code if the employer works in software or e-commerce.
- **Income tax and insurance:** use the 60% paušál. At the projected revenue, profit stays far below the 117,521 CZK social-insurance threshold. Levies are about 8.7% of revenue.
- **VAT:** the founder is a non-payer (neplátce).
  - If Shoptet s.r.o. is the counterparty, sales are a domestic B2B supply with no VAT **[knowledge; confirm billing flow]**.
  - Billing SK/HU merchants directly would be a cross-border B2B service. That makes the founder an identified person and requires an EC Sales List (souhrnné hlášení) **[B]**.
  - **Scorer C missed a trap.** Buying AI coding tools, Hetzner, GitHub or AWS for the business also triggers identified-person status: register within 15 days, then file a monthly VAT return in each month with such purchases (quickstart §3.3). Prefer Czech hosting, and ask the tax advisor about the AI subscription.
- **GDPR:** the founder is a **processor** of buyer names, addresses and IČO numbers.
  - Put a DPA (zpracovatelská smlouva) in the T&C and keep Art. 30 records.
  - Host in the EU, encrypt tokens, keep logs for at most 90 days, list sub-processors, and have a breach procedure.
- **T&C and privacy policy** must meet the minimums in the Shoptet cooperation agreement **[verified: snippet, https://doplnky.shoptet.cz/chcete-delat-vlastni-doplnky]**.
  - Include a liability cap and a "not accounting advice" disclaimer. The merchant stays responsible for invoice content (§ 29 ZDPH).
- **IP:** own code; check the Laravel (MIT) and SDK licences. Name it descriptively, without implying endorsement by Shoptet or Solitea.
- **Promo variant only:** Omnibus 30-day lowest-price display (§ 12a, zákon 634/1992 Sb.).
- **Not applicable:** GPSR, EPR/packaging, WEEE, hallmarking, the margin scheme.

## 12. Risks and mitigations
| Risk | Mitigation |
|---|---|
| A live iDoklad connector already exists, or GoodEshop is good enough | Gate 0: check the live catalog and GoodEshop's price; interview 30 merchants |
| Shoptet rejects the proposal (overlap, "no benefit") | Submit in week 1 before coding the Shoptet side; if refused, pick the backup cloud-invoicing tool once, then stop |
| Commission is 30% or more | Price is tested at 30% (net €7.5); walk away if it is above 35% |
| Skill gap, so the build overruns | Week-1 toy-app gate; 80 h cap by day 60 |
| Urgent accounting bugs around the 25th | Idempotent sync, dry-run preview, 20th-of-month alert, manual fallback in iDoklad |
| iDoklad or Shoptet API changes | Contract tests in CI; follow Shoptet "Addon News" **[verified: https://developers.shoptet.com/addon-news-from-september-7-2026/]** |
| Small segment (Fakturoid connector has only 7 ratings) | Add a second adapter only when Basic reaches 15 shops |

## 13. Kill criteria
- **Day 30:**
  - The Shoptet proposal is not approved, or an iDoklad connector is live on the marketplace with ≥4.0 rating.
  - Or fewer than **5 of 30** iDoklad-using merchants say they would pay 290 CZK and fewer than **2** commit to a beta.
  - → Stop.
- **Day 60:**
  - Order → invoice → credit-note sync on the test shop does not pass **≥45 of 50** fixture cases.
  - Or more than **80 h** have been spent.
  - → Stop.
- **Day 90:**
  - Fewer than **3** beta shops are syncing.
  - Or any data-loss incident.
  - Or support is above **1 h/week**.
  - → Stop.
- **Month 8 (post-launch check):** fewer than **8 paying shops** → maintenance mode only, with no new features.

## 14. 12-week launch plan
1. Week-1 coding gate; check the live catalog for iDoklad, Vyfakturuj and Fakturoid connectors; read every 1–3★ review of the accounting and promo add-ons; submit the Shoptet proposal form.
2. 15 merchant interviews (Facebook groups, demand-post authors); open an iDoklad API sandbox; 1-hour tax-advisor session (billing flow, identified-person triggers).
3. Raise interviews to 30; build the iDoklad client and mapping engine against fixtures.
4. **Day-30 gate.** Register the trade licence; sign the Shoptet contract; set up the test shop.
5. OAuth install flow and webhook ingestion.
6. End-to-end order → invoice sync; idempotency; retry queue.
7. Credit notes and cancellations; payment status back-sync.
8. Setup wizard with dry-run preview; sync log; Czech error texts. **Day-60 gate.**
9. Complete the 50-case test suite; one-off accountant review of the VAT mapping.
10. Production deploy (backups, uptime alerts); T&C and DPA; 15 KB articles.
11. Submit for Shoptet technical review; onboard 3 free beta shops.
12. Fix review findings; measure the beta. **Day-90 gate.** Set the launch price and annual plan.

## 15. Critical claims to verify
1. `"iDoklad" site:doplnky.shoptet.cz doplněk napojení 2026`: is Shoptet's iDoklad add-on still live, and what are its rating and price?
2. `Shoptet API partner smlouva provize Shoptetu z ceny doplňku procenta vyplácení partnerům`: the revenue share and billing flow.
3. `GoodEshop Shoptet iDoklad integrace cena měsíčně recenze`: the strength and price of the off-marketplace competitor.
4. `Shoptet doplněk návrh zamítnut duplicitní funkce nativní doplněk schvalování partner marketplace`: does Shoptet reject proposals that overlap its own add-ons?
5. `iDoklad API v3 přístup tarif cena počet uživatelů iDoklad e-shop 2026`: API access per plan, and the size of the iDoklad segment.
6. `Shoptet API košík změna ceny doplněk checkout hook developers.shoptet.com cart`: confirms or refutes that no third-party cart-pricing hook exists (relevant only if promo is reconsidered).
