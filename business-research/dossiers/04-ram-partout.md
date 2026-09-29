# C12 dossier: DDR4/SSD part-out arbitrage from used PCs, mini PCs and servers (CZ)

Date: 2026-09-29. FX: €1 = 24.5 CZK (quickstart §2.4). Evidence tags: **[verified: URL]** means a WebSearch result snippet from this session or the orchestrator file (no page was opened, and Bazoš snippets carry no date). **[knowledge]** means background knowledge not checked this session. **[estimate]** means my own arithmetic, with the reasoning shown.

---

## 1. Verdict in 3 lines

- **NO-GO as a business. CONDITIONAL-GO only as a trade of at most €1,000 over 90 days in "RAM-heavy" hardware (servers and workstations), and only if the €0 listing test passes.** Fresh Bazoš data shows that the longlist's core SKU loses money: parting out ordinary 8–16 GB office PCs yields less than selling them whole.
- **Realistic month-12 profit is about €150/month** (range €0–600), before about 22% in levies. The longlist's €400–700 is not supported.
- **Biggest risk:** the buy-side spread is already gone, and DDR4 prices are topping out. Czech sellers price RAM at *used* value, which is about ⅓ of new retail. So the likely outcome is 6–8 h/week at about €8–10/h, with stock exposed to a price turn.

## 2. The exact offer

| Lane | SKU | Price (CZ / DE) | Buyer & channel |
|---|---|---|---|
| **A (core)** | Tested DDR4 ECC RDIMM, 16/32/64 GB, pulled from decommissioned Dell R630/R730/R640, HPE DL360/380 Gen9–10, HP Z440/Z640/Z840 and Precision T5810/7820 | 32 GB: 1,800–2,000 Kč on Bazoš/Aukro [estimate]; **€80–85 delivered** on eBay.de [estimate, anchored below the €90 Kleinanzeigen ask] | Homelabbers, people building local-LLM machines on Xeon/EPYC [knowledge], and small IT firms. CZ first, then DE |
| **B** | DDR4 SO-DIMM/UDIMM, 16 GB singles and 2×16 GB kits, from 32–64 GB laptops, workstations and gaming PCs | 16 GB: 1,300–1,400 Kč; 2×16 GB: 2,400–2,500 Kč | CZ upgraders via Bazoš, Aukro and Facebook Marketplace. **CZ only** |
| **C (residual and exit lane)** | Stripped servers sold whole for local pickup. Configured 1-litre mini PCs (M720q/M920q, i5-8500T/16 GB/256 GB/W11 Pro on its embedded licence) | Mini PC **4,590–4,790 Kč**, undercutting Počítárna's "from 4,990 Kč" | Bazoš, **CZ only** (because of WEEE) |
| By-product | SSDs wiped to NIST "purge" level, sold with a SMART screenshot | 256 GB NVMe 350–450 Kč; 512 GB 600–800 Kč [estimate] | Bazoš |

**Dropped:** ordinary office-PC part-out (see §6, row D), laptops with soldered RAM, and DDR3.

## 3. Why it makes money (demand evidence)

- **DDR4 is at record prices.** The chip hit $42.50 in Aug 2026. A 32 GB DDR4 kit cost $60–90 in Oct 2025 and $150–180 in Jan 2026 [verified: https://www.tomshardware.com/pc-components/ram/ram-price-index-2026-lowest-price-on-ddr5-and-ddr4-memory-of-all-capacities, https://www.techpowerup.com/345717/ddr4-prices-skyrocketing-amid-dram-shortage-crunch]. **DDR4 1Gx8 spot was $46.04 on 22 Sep 2026, above the August "record"** [verified: https://www.trendforce.com/news/2026/09/23/insights-memory-spot-price-update-dram-spot-prices-hold-cautious-tone-ddr4-2gx8-drops-3-6/].
- **Czech retail:** a new 16 GB module cost 4,300 Kč in Feb 2026, 4.2× the year before [verified: https://svethardware.cz/article/o-kolik-zdrazily-ram-v-cr-priplatite-si-4-6nasobne].
- **Liquidity is real.** Kleinanzeigen has wanted ads buying DDR4 in bulk ("ab 10 Stück"). There is a 32 GB kit at €159 VB, and a **32 GB RDIMM PC4-2400 asked at €90** [verified: https://www.kleinanzeigen.de/s-pc-zubehoer-software/arbeitsspeicher/k0c225, https://www.kleinanzeigen.de/s-pc-zubehoer-software/ddr4-server-ram/k0c225]. On eBay US, used 32 GB DDR4 ECC is asked at **$175–189** [verified: https://www.ebay.com/b/32GB-ECC-Network-Server-Memory-DDR4-SDRAM/11210/bn_120449283].
- **Gap:** every one of these is an *ask* or an index. No sold count was seen. RAM demand is certain; demand **at the assumed price** is not.

## 4. Supply gap, asymmetry and durability

### Have Czech used-PC sellers already repriced to include the RAM value? Mostly yes.

| Item (Bazoš unless noted) | Ask | ≈ € |
|---|---|---|
| 8 GB DDR4, used (SO-DIMM/DIMM) | 450–990 Kč | 18–40 |
| 16 GB DDR4 SO-DIMM, used | 1,300–1,500 Kč | 53–61 |
| 2×16 GB SO-DIMM kit | 2,500 Kč | 102 |
| OptiPlex 7070 SFF, i5-9500/8 GB/128 GB/W11P | 3,599 Kč | 147 |
| OptiPlex 7070, i5-8500/8 GB/250 GB | 2,500 Kč | 102 |
| Same seller, 8 GB vs 16 GB version | 4,700 vs 5,400 Kč | +€29 per extra 8 GB |
| Počítárna M720q Tiny, refurbished with warranty | from 4,990 Kč; "16 GB +600 Kč" | 204 |
| Dell R640 with 32 / 64 / 128 GB RDIMM | 16,000 / 17,000 / 19,000 Kč | **≈ €41 per extra 32 GB** |

Sources: [verified: https://pc.bazos.cz/inzeraty/ddr4-8gb/, https://pc.bazos.cz/inzeraty/sodimm-ddr4-16gb/, https://pc.bazos.cz/inzeraty/16gb-sodimm/, https://pc.bazos.cz/inzerat/213770031/dell-optiplex-7070-sff-i5-9th.php, https://pc.bazos.cz/inzerat/210379445/kompaktni-pc-dell-optiplex-7070.php, https://www.pocitarna.cz/pocitace/lenovo-thinkcentre-m720q-tiny/, https://pc.bazos.cz/inzeraty/thinkcentre-m720q/, https://pc.bazos.cz/inzeraty/server-poweredge/].

**How to read this table:**
1. The Czech used-RAM market does **not** price at the new-retail spike. A used 16 GB module asks about 1,400 Kč against 4,300 Kč new. The longlist valued RAM at spike prices; that was the mistake.
2. Dealers price RAM increments consistently with used-module asks (+700 Kč per extra 8 GB), so there is no lag at the dealer level.
3. For an office PC, the sum of the parts is **below** the whole-unit price (§6, row D). The "whole-device lag" hypothesis fails for the common case.
4. **One gap of 2× or more survives.** Czech dealers bundle RDIMM at about €41 per 32 GB inside servers, while asks are €90 in DE and $175+ in the US. This is a cross-border RDIMM gap, but it compares asks with asks.

### Supply side
Legacy DDR4 output was cut, and the major makers are prioritising HBM and DDR5 (orchestrator). Refurbishers report dearer ex-lease input, so fewer cheap units are coming through [verified: https://www.technimax.cz/zdrazovani-ram-a-ssd-ovlivnuje-i-ceny-repasovane-techniky].

### How long is the window?
The market is already showing signs of a top:
- 2Gx8 DDR4 spot fell 3.6% in one week, and "module houses loosened quotes" [verified: TrendForce URL above, https://www.trendforce.com/news/2026/09/16/insights-memory-spot-price-update-dram-spot-cools-as-ddr5-inquiries-slow-2gx8-ddr4-prices-retreat].
- Q3 contract growth is moderating to +13–18% QoQ as consumer demand weakens [verified: https://www.trendforce.com/presscenter/news/20260703-13134.html].
- Manufacturers still say the market is undersupplied into 2027 [verified search summary: https://capitalandcompute.net/blog/when-will-ram-prices-drop/].

**[estimate]** Prices will plateau from Q4 2026 to Q1/Q2 2027, decline in H2 2027 and normalise in 2028. That leaves a **usable trading window of about 6–9 months**, and month 12 (Sep 2027) probably falls in the decline. When DRAM has turned in the past, prices fell 30–60% over 2–4 quarters (2019, and 2022–23) [knowledge].

### What happens to inventory in a crash
RAM stays liquid; you lose the markdown, not the stock. Assume a RAM cap of €1,000 at cost, turnover within 3 weeks, and a downturn of about 7–10% per month [estimate]. That costs about €70–100 per month. The worst case, a 25% gap-down with full stock, costs about €250. Servers and chassis are less liquid, so they are capped separately (§9).

### Scorer objections, answered
- **A** ("the lag is unverified and eroding"): the new data confirms it has eroded for office PCs.
- **B** ("trade it, don't build a business on it"): agreed. This dossier recommends a capped trade with a stop-loss.
- **C** ("small transactions eat the hours; selling CZ components avoids WEEE and the identified-person registration"): agreed. The plan is CZ-first, uses multi-quantity listings, and adds eBay.de only for RDIMM.

## 5. Competitor map

| Competitor | Where | Price / positioning |
|---|---|---|
| Počítárna.cz | CZ refurbisher | M720q Tiny from 4,990 Kč, upgrades, warranty [verified above] |
| Technimax, Gigacomputer ("RAMageddon 2026" page), Recomp, Počítače24, ITzoo | CZ refurbishers | Buy the same ex-lease lots at volume. Recomp sells a ThinkPad T14 at 9,490 Kč with a 2-year warranty [verified: longlist] |
| Private and semi-pro Bazoš sellers | CZ | 8 GB 450–990 Kč; 16 GB 1,300–1,500 Kč; R640 16–19k Kč. Some single-module asks anchor to "běžná cena 12 000 Kč" [verified: https://pc.bazos.cz/inzeraty/sodimm-ddr4-32gb/] |
| Kleinanzeigen sellers and bulk buyers | DE | 32 GB kit €159 VB; 64 GB €180–250; 32 GB RDIMM €90 [verified above] |
| DE server-parts dealers (servershop24.de, it-market.com) | DE | Warranty and volume [knowledge] |
| thinkstore24.de, it-versand.com | DE mini PCs | Crowded [verified: longlist] |

## 6. Unit economics

Assumptions:
- eBay.de commercial fee is about 11% plus €0.35 per order [knowledge; verify the category rate].
- Packeta from CZ to DE home delivery costs about €7 (quickstart range 150–300 Kč).
- Bazoš listings are free, and the buyer pays Zásilkovna shipping [knowledge].
- 21% identified-person VAT is due on eBay fees.

| € per unit | **A: 32 GB RDIMM → eBay.de** | **B: 16 GB SO-DIMM → Bazoš** | **C: configured M720q → Bazoš** | **D: OptiPlex 7070 part-out (longlist core)** |
|---|---|---|---|---|
| Sale price | 85 (shipping included) | 55 (1,350 Kč) | 191 (4,690 Kč) | 113 total for 4 parts: RAM 29, SSD 10, i5-9500 41, barebone 33 [estimate] |
| Buy cost | 42 (≈ the Czech dealer's implied €41 per 32 GB) | 33 (bought as part of a whole machine priced at ≤ 0.65 × part value) | 115 unit + 20 RAM + 15 NVMe + 2 paste | 135 (3,300 Kč, negotiated down from 3,599) |
| Platform fee | 9.7 | 0 | 0 | 0 |
| VAT on fees (identified person) | 2.0 | 0 | 0 | 0 |
| Payment / COD fee | incl. | 1.0 | 1.0 | 3.0 |
| Shipping | 7.0 | buyer pays | buyer pays / pickup | buyer pays |
| Packaging | 0.8 | 0.5 | 2.0 | 1.5 |
| Returns and warranty allowance | 3.4 (4%) | 1.7 (3%) | 11.5 (6%) | 3.0 |
| Ads | 0 | 0 | 0 | 0 |
| **Net per unit** | **≈ €20** | **≈ €19** | **≈ €24** | **≈ −€30** |

In Lane A, selling a 32 GB RDIMM **inside CZ** at about 1,900 Kč would net about €32, if Czech demand exists at that price (unverified). Company-lot purchases carry 21% VAT that a non-payer cannot reclaim, so the buy rule must use gross prices.

**Buy rule:** conservative net part value × 0.65 ≥ asking price, **and** RAM must be at least 50% of the part value.

## 7. Sourcing plan in CZ

- **Bazoš (pc.bazos.cz):** search "server", "PowerEdge", "ProLiant", "Z640/Z840", "Precision", "workstation", "64GB", "128GB", "256GB", "na díly", "vyřazené", "likvidace firmy". R640s at 16–19k Kč prove that listings exist [verified above].
- **Aukro:** ended auctions show *realised* prices, which is the best free sold-data source in CZ.
- **Sbazar and Facebook Marketplace.**
- **Insolvency and public auctions** (trustee asset sales, e-auction portals) and **ÚZSVM state surplus** [knowledge; verify which portals list IT lots].
- **Direct outreach:** 10 emails a month to MSPs, small IT firms and schools: "vykoupím vyřazené servery/pracovní stanice, bez disků nebo s protokolem o výmazu". This is a purchase condition, not a paid service.
- **Realistic volume** [estimate]: about 1 server plus 3 RAM-heavy workstations or laptops plus 2 mini PCs a month, or **16–24 modules a month**. A company lot is upside, not the base case.

## 8. Time model (active minutes; memtest runs unattended overnight)

| Step | Server (8 modules) | Workstation/laptop (3 modules) | Mini PC |
|---|---|---|---|
| Sourcing and negotiating | 45 | 30 | 20 |
| Pickup and travel | 90 | 45 | 30 |
| Strip, clean, test set-up | 40 | 20 | 30 |
| Drive wipe and log | 15 | 10 | 10 |
| Photos and multi-quantity listing | 30 | 15 | 15 |
| Messages | 40 | 15 | 15 |
| Packing and drop-off | 55 | 20 | 10 |
| Residual chassis sale | 45 | 20 | – |
| **Total** | **≈ 6 h (45 min per module)** | **≈ 2.9 h** | **≈ 2.2 h** |

Month at target volume: 1 server + 3 workstations + 2 mini PCs + 4 h of listing scans + 2 h of admin ≈ **25 h/month (about 6 h/week)**. Net ≈ €250, so **about €10/h**.

## 9. Staged budget (total committed ≤ €2,500; the remaining ~€6,000 stays free for a lasting business)

| Stage | When | Spend | Content | Pass / fail |
|---|---|---|---|---|
| **0** | Weeks 1–2 | €0 | Log 60 listings in 3 buckets (office PCs, RAM-heavy workstations and laptops, servers). Pull eBay.de *sold* comps by hand. Re-check after 7 days which listings disappeared | **Pass:** ≥25% of the RAM-heavy and server listings clear the buy rule, **and** the eBay.de sold median for a 32 GB RDIMM is ≥ €65 with ≥20 sales in 30 days |
| **1** | Weeks 3–7 | ≤ €1,000 | Živnost €33, 1-hour tax advisor €80, tools €105 (ESD mat, NVMe/SATA enclosure, USB sticks, clamshells, mailers, serial labels, scale), inventory ≤ €750 (one server ≤ €400 plus 2–3 RAM-heavy units) | **By day 45:** ≥70% of modules sold within 21 days, average net ≥ €12 per module, batch ROI ≥ 25%, ≤1 return per 20 modules |
| **2** | Week 8+ | +€1,500 max | Rolling cap: RAM ≤ €1,000 at cost, residual units ≤ €500. RDIMM test bench (a used Z440, about €120). eBay.de business account plus LUCID/dual system (about €50 a year) | Every month: net ≥ €200 and no exit trigger hit |

Capital is not the bottleneck; sourcing is. More money only adds exposure to a price turn.

## 10. Projections (monthly net before income tax and levies)

| Scenario | Assumptions | M3 (Dec 26) | M6 (Mar 27) | M12 (Sep 27) |
|---|---|---|---|---|
| Pessimistic | Stage 0 fails, or the first batch sells slowly. Stop by day 45 with a loss of ≤ €150 | 0 | 0 | 0 |
| **Realistic** | 16–24 modules a month at €15–18 (€10 by M12 as prices soften), 2–3 whole units at €20–25, minus €50–90 for fuel, fixed costs and markdowns | **150** | **250** | **150** (or 0 if exited on a trigger) |
| Optimistic | One company or insolvency lot a month plus 1 server: 40–50 modules at €18 and 6–10 units at €25; prices hold to Q3 2027 | 400 | 900 | 600 |

Q4 2026 profit (realistic €300–450, about 7–11k Kč) stays under the reduced 2026 social-insurance threshold of 29,375 Kč, so **registering in October is fine**.

## 11. CZ/EU legal checklist

| Topic | What applies | Action |
|---|---|---|
| Živnost | Volná, field "Velkoobchod a maloobchod". Swapping modules is not vázaná electrical work (don't open PSUs) [knowledge] | JRF online, 800 Kč. Check employer consent under § 304 ZP if you work in IT hardware |
| Income tax method | Goods plus fees ≈ 65–75% of revenue, so **actual expenses** beat the 60% paušál [estimate] | Compare at year end |
| VAT | Non-payer; turnover far below 2M Kč. VAT on company-lot purchases is not reclaimable | Use gross prices in the buy rule |
| Identified person | **eBay.de fees trigger it**. Bazoš and Aukro (CZ firms) do not [knowledge + quickstart §3.3] | Stay CZ-only until RDIMM sales in CZ stall. Then register within 15 days and file a monthly return by the 25th |
| OSS €10k | DE B2C RAM sales count; that is about 117 RDIMM at €85 | Track the running total monthly |
| Margin scheme | Not applicable to a non-payer | Revisit only if you register for VAT |
| GPSR | Used goods are in scope; you are a distributor [knowledge] | Listing shows the manufacturer's name and address plus the part number. Mini PCs ship with the maker's Czech safety sheet |
| Packaging EPR | CZ: records only, under 300 kg. DE: LUCID plus dual system **before the first DE consumer parcel** | Weight log; register in LUCID at Stage 2 |
| **WEEE** | Components that are not finished devices are generally out of scope [verified snippet: https://www.elektrogesetz.de/themen/passive-geraete/, https://stiftung-ear.de/de/themen/elektrog/hersteller-bv/anwendungsbereich/abgrenzungsbeispiele]. **Internal SSDs need checking.** Whole devices sent to DE are first placed on the German market, so you would need stiftung ear registration via an authorised representative, with fines up to €100k [verified: https://www.it-recht-kanzlei.de/registrierung-dritter-elektrog.html, https://www.provimedia.de/blog/elektrog-weee]. Laptops and mini PCs also contain batteries, which brings battery EPR abroad. In CZ you are a distributor of equipment already placed on the CZ market (Act 542/2020) [knowledge] | **Whole units: CZ only.** Give collection-point information on listings. Scrap goes to ASEKOL/REMA/Elektrowin points or licensed buyers, with receipts kept |
| Data (GDPR) | Personal data on bought drives is your problem once you hold them | Prefer "bez disků". Otherwise do an NIST 800-88 purge (nvme format with crypto erase, hdparm secure-erase, or nwipe/ShredOS) **without browsing the data**. Log serial, method and date. Physically destroy drives that fail. Reset iDRAC/iLO, BIOS and TPM |
| Licences | The Windows OEM licence is embedded in the motherboard and stays with it. Corporate KMS/MAK Enterprise images belong to the company. Server OS licences and CALs do not transfer [knowledge] | Reinstall from Microsoft media. Never sell keys on their own. Barebones go without Windows |
| Stolen goods | § 214 TZ, plus negligent receiving under § 215 [knowledge] | Keep a purchase log with ID, a signed kupní smlouva or invoice, and serials. Refuse BIOS-locked or Computrace units |
| Consumer law | 14-day withdrawal for online sales. **24-month liability, shortened to 12 months for used goods if agreed**; defects are presumed to have existed at delivery for 1 year; complaints must be settled within 30 days. DE requires a separately agreed shortening (§ 476 BGB) | 12-month clause in the T&Cs and every listing. Budget 3–6% for returns. Exclude liability for B2B (IČO) buyers. Keep a pool of spare parts for warranty repairs |
| DAC7 / IP / hallmarking | Aukro and eBay report sellers. Brand names are descriptive only. No hallmarking | Declare everything |

## 12. Risks and mitigations

| Risk | Likelihood | Mitigation |
|---|---|---|
| The spread has already closed | **High** | Run the €0 bucket test first. Buy only when the rule clears |
| DDR4 price turn | Medium–high | RAM cap €1,000; no module held more than 21 days; weekly TrendForce check; exit triggers (§13) |
| Too little sourcing volume | High | Use several channels. Better still, bolt this onto a C02/C07 picker as opportunistic buys |
| Haggling and small transactions creep | Medium | Fixed prices, multi-quantity listings, batched drop-offs |
| RDIMM/LRDIMM/3DS compatibility returns | Medium | Exact part number and rank in the title; photo of the label |
| DOA swap fraud | Low–medium | Serial stickers plus a photo log |
| Unwiped data | Low probability, severe impact | Wipe protocol; destroy drives that fail |
| WEEE breach on whole units abroad | Medium if ignored | Whole units CZ only |
| Server weight, noise, illiquid residuals | Medium | RAM must cover ≥60% of the price; pickup-only sales of residuals |
| Poor hourly return (about €10/h) | High | Time-box to 90 days |

## 13. Kill criteria and exit plan

- **Day 30:** Stage 0 fails → stop with €0 spent. If Stage 1 has started and less than 50% of the first batch has sold → stop buying.
- **Day 60:** stop and liquidate if any of these hold:
  - cumulative net < €100;
  - average net < €10 per module;
  - ≥2 returns per 20 modules;
  - **DDR4 1Gx8 spot < $37** (−20% from $46).
- **Day 90:** wind down if any of these hold:
  - month-3 net < €200;
  - < €8/h;
  - own 30-day sold median down ≥15% from the day-30 baseline.

**Exit and pivot, once prices normalise.** Triggers: any kill criterion, or 2 weekly declines in a row of more than 3% in 1Gx8 spot.
- **Days 0–21 after a trigger:**
  - stop buying the same day;
  - reprice all RAM at −10%, then −20% after 14 days;
  - bulk-sell the remainder to DE "ab 10 Stück" buyers or CZ component buyers;
  - sell residual units whole in CZ, or as scrap.
- **Keep:** the test bench, the parts pool, the živnost, Packeta and the bookkeeping setup. The sunk cost of exiting is about €150.
- **Pivot options:**
  1. Fold the sourcing and testing loop into **C07/C02** as opportunistic buys.
  2. **CZ-only configured mini PCs.** This lane does not depend on the window and gets *better* when RAM is cheap again (32–64 GB homelab boxes), at €20–30 per unit.
  3. **C01** (iPod mods) reuses the bench.

## 14. 12-week launch plan

1. Log 60 listings in 3 buckets; pull eBay.de sold comps; build the price sheet.
2. Do the 7-day disappearance check and the **Stage 0 decision**. Book the tax-advisor hour. If Stage 0 passes, file the JRF.
3. Once the IČO arrives: open the bank account, set up Fakturoid, write T&Cs with the 12-month used-goods clause, buy tools, set up Packeta.
4. First buy: one RAM-heavy server or workstation lot ≤ €400. Strip it, run memtest, wipe and log.
5. List on Bazoš and Aukro in batches. Sell the residual chassis locally. Make the second buy.
6. Measure sell-through. If CZ RDIMM demand is thin, do the identified-person registration and LUCID, then open eBay.de.
7. **Day-45 Stage 1 gate.**
8. If it passes: source once a week; email 10 MSPs; check insolvency auctions.
9. Test 2 configured mini PCs, CZ only.
10. Run the weekly price watch (TrendForce spot plus own sold data) and adjust the buy rule.
11. Mark down any stock older than 21 days; day-75 check.
12. **Day-90 decision:** continue capped, wind down, or pivot. Check Q4 profit against the 29,375 Kč threshold.

## 15. Critical claims to verify

1. `ebay.de verkauft 32GB DDR4 ECC REG RDIMM 2666 PC4 Preis 2026`
2. `bazos.cz 32GB DDR4 ECC REG RDIMM cena Kč 2026`
3. `pc.bazos.cz PowerEdge R730 OR R630 256GB RAM cena Kč`
4. `TrendForce 4Q26 DRAM contract price forecast DDR4 legacy decline 2027`
5. `stiftung ear Abgrenzungsbeispiele Arbeitsspeicher interne SSD Festplatte Bauteil Anwendungsbereich`
6. `stiftung ear gebrauchte Elektrogeräte aus EU-Ausland Fernabsatz Registrierungspflicht erstmaliges Inverkehrbringen`
