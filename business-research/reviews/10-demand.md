# Review 10, DEMAND lens: "HAN reader CZ" smart-meter reader (C10)

Reviewer lens: demand and competition skeptic. Date: 2026-09-29.
Tags:
- **[verified: URL]**: a web-search snippet (the dossier's, the orchestrator's, or the one search I ran this session). No page was read first-hand.
- **[knowledge]**: my background knowledge, not checked this session.
- **[estimate]**: my own arithmetic, with the reasoning shown.

---

## Verdict: **WEAK, score 3/10**

- **Nobody has paid for this product in CZ, and there is no evidence that anyone would.** Everything the dossier offers as demand is one of two things:
  - an *installed base* (≈1M AMM meters): opportunity, not demand;
  - *DIY interest* (repos, forum threads): demand already served for free by the most capable third of the target market.

  There are no sold counts, waitlists, "where can I buy" threads or CZ price points. The foreign analogues are **asking prices without unit counts**, as the dossier admits in §3.
- **Supply is absent because the prize looks small, not because sellers can't keep up.** A local maker with the hardware, the CE/WEEE set-up and the audience already exists: LaskaKit sells an ESP32 + MAX485 + PoE board [verified: https://www.laskakit.cz/en/laskakit-esplan-esp32-lan8720a-max485-poe/]. It hasn't packaged a HAN kit. That is weak evidence that the people best placed to see this market don't rate it. It is the opposite of the brief's "sellers can't keep up".
- **The substitutes cover most of the job.** The most motivated buyers are PV owners automating surplus and spot prices, and most of them already get real-time grid data from their inverter's grid meter. Free portal integrations cover dashboards. Many target homes have their meter in a boundary pillar box with no power or Wi-Fi.
- **Demand is front-loaded, and the dossier models it as rising.** The launch will serve the forum's pent-up demand. After that the flow depends on new AMM installs among HA users, and those slow once the mandatory rollout phase ends on 1 July 2027, which is before month 12. **The Stage 2 trigger (≥ 15/month for 2 months) would fire on the launch spike and commit about €2.5k of sunk cost just as demand decays.**
- **Corrected realistic month-12 profit: ≈ €150/month, not €500**, from about 8 units/month. The pessimistic case is €0, stopped by day 60–90 with €300–600 lost. The optimistic case is ≈ €750.

---

## 1. Claims checked

| # | Dossier claim | What I found | Status |
|---|---|---|---|
| 1 | ≈ 0.9–1.0M AMM meters by end-2026 and ≈ 1.2M by mid-2027 | The distributor figures are cited. But the ČEZ row mixes ">1.02M meters" (a project figure) with "~650k by mid-2027" (installed). Summed on the installed figures (650k + ~350k EG.D + ~65k PRE), mid-2027 is **≈ 1.05–1.1M, not 1.2M** [estimate]. It doesn't change the verdict, because the base was never the constraint. **Only part of the base is HAN-usable.** EG.D works only on certain meter types, PRE needs activation plus a cover swap the customer pays for, and many detached-house meters sit in pillar boxes [verified: dossier's egd.cz, novemereni.cz sources; share of pillar boxes unmeasured]. | Holds as opportunity; overstated as demand |
| 2 | "No packaged CZ reader is on sale" | **Confirmed again this session.** A Czech-language search for a finished device with a CZK price returned only DIY repos (blesk89, IntExCZ, Tomer27cz), forum threads and a Facebook how-to question. The search summary says "most users build their own solutions" [verified: https://github.com/blesk89/ha-addon-egd-dlms, https://github.com/IntExCZ/Sagemcom_XT211, https://github.com/Tomer27cz/xt211, https://www.homeassistant-cz.cz/viewtopic.php?p=26379]. **The hardware already exists at CZ retail**, though: LaskaKit ESPlan, the Waveshare ESP32-S3-RS485 at rpishop.cz, M5Stack Atom + RS485 base [verified: laskakit.cz, rpishop.cz links above]. IntExCZ's integration uses a generic RS485-to-Ethernet converter. **The gap is only a pre-crimped cable, a config and a Czech guide.** | Holds, but the gap is very thin |
| 3 | Interest signals: 7 CZ repos, multi-page forum threads, root.cz coverage | True, but all are **DIY or interest signals**. The main HA-CZ thread I found is on page 2 (p=26379), which is small. The one Facebook hit is "does anyone have working readout of data from the smart meter from…", a how-to question, not a request to buy [verified: facebook.com/groups/2232679967058877/posts/4043520129308176/, snippet only]. No waitlist, pre-order, Bazoš "koupím" or "where can I buy" evidence was cited or found. | **No paying-demand evidence** |
| 4 | "Abroad, plug-and-play readers clearly sell" | Every figure is an **asking price**. There are no unit counts for HomeWizard, SlimmeLezer, amsleser or Tibber [dossier §3]. **The analogues don't transfer:** <br>• NL: P1 is a standardised port on nearly every meter and **supplies 5 V**, across ~8M meters [knowledge]. <br>• NO: Tibber Pulse is a customer-acquisition device for an electricity supplier, in a market where hourly pricing is universal and the HAN port is powered [knowledge]. <br>• AT: the closest analogue in access friction, and it **stayed DIY** [verified: dossier's AT sources]. <br>CZ has an **unpowered** port, gated access at PRE and EG.D, and pillar-box meters. For most households it looks like AT, not NL. | **Refuted as evidence for CZ** |
| 5 | ≈ 20–30k CZ Home Assistant installs | **Unverified.** The orchestrator's check returned NOT FOUND (06-verification.md). Plausible, but I'd widen it to 15–30k [estimate]. | Unverified |
| 6 | 10–20% of HA+AMM households want real-time HAN data, won't DIY, and find inverter or portal data insufficient | **The load-bearing number, and it has no source.** Every term in it cuts downwards (see §3). | Unsupported |
| 7 | "A first mover might take 30–50%" | Nothing about the product is defensible. The firmware is GPL and has to be published. The hardware is off-the-shelf. The guide leaks the moment the first buyer posts it. I'd use **20–45% in year 1, falling** [estimate]. | Optimistic |
| 8 | Durability 12–24 months; foreign giants not before 2028 | I agree about the foreign giants. **The local threat is faster.** LaskaKit already sells the board, has an e-shop and an audience, and is already the CE and WEEE producer. A HAN guide or kit from them is weeks of work [estimate]. The dossier's own Stage 1 design leaks as well: a public web installer lets any buyer flash a €15–20 board bought directly, skipping the €25–30 kit markup. **Expect the gap to start closing 3–9 months after visible traction, not 12–24.** | Too long |
| 9 | Realistic trajectory: 10 → 14 → 16 units/month at M3/M6/M12 | **Wrong shape.** At launch the founder sells to a *stock* of HA households that already have AMM (≈ 75% of the end-2027 base is installed by Oct 2026 [estimate from row 1]). After that he sells to a *flow* that shrinks once the mandatory phase ends on 1 Jul 2027 [verified: hunt/digital-software.md, zakonyprolidi.cz/cs/2020-359]. The meters installed after that go to lower-consumption households, where HA users are rarer [estimate]. **The expected shape is a spike in months 2–6, then decay.** | **Refuted** |
| 10 | Demand drivers: spot and dynamic tariffs, energy sharing (EDC), HDO automation | Only one of these needs HAN data. <br>• Energy sharing is settled from 15-minute data held by the EDC, not the customer's HAN reader [knowledge]. <br>• HDO schedules are published, and free HACS integrations read them [knowledge]. <br>• The share of CZ households on spot or dynamic tariffs is small, though I have no figure [knowledge]. <br>• Negative-price curtailment is done through the inverter's export control, which uses the inverter's own meter. <br>What's left is real-time import/export for households **without** an inverter grid meter, mostly heat-pump or EV homes without PV. | Mostly doesn't need HAN |
| 11 | PV owners' hybrid inverters already meter the grid | I agree, and it matters more than the dossier allows. Subsidy-era hybrid installs almost always include a grid-point meter (DTSU666, Chint or similar) for export limiting [knowledge]. **The most HA-dense segment is the one best served already.** | Holds; strengthens the substitution |
| 12 | The "last metre" gap is "worth roughly €25–35 of margin per buyer" | Only until the first clone or published BOM. The forum will price the kit against ~€20 of visible parts. | Holds briefly |

---

## 2. The demand-lens questions

**Does demand exceed supply?** It can't be shown, and probably not. Packaged supply is zero and paying demand is also unmeasured. The brief's pattern is sold-outs, waitlists, long processing times and resale above retail, and none of those is present. What exists is an **unserved convenience niche inside a DIY community**, which is the classic "sounds clever, doesn't sell" setup the founder has been burned by.

**Sold prices or asking prices?** Asking prices only, and all of them foreign: HomeWizard P1 €20–43, NL ESP32 dongles €55–80, Tibber Pulse at retail, amsleser on Lectronz. **There isn't one CZ price point, and not one sold count anywhere.** The two CZ anchors a buyer actually sees are:
- about €20 of parts plus free YAML (the DIY floor);
- a Shelly Pro 3EM for about €100–150 plus an electrician (the premium substitute) [knowledge].

At 1,190 CZK the kit sits close to the DIY floor in the one venue where the founder can sell, a forum that knows the BOM.

**How many competitors, and do they cover the gap?** Nobody sells the packaged product, but **eleven substitutes** cover the job for most buyers:
1. DIY ESP32 + MAX485 with ESPHome `dlms_meter` or the Tomer27cz component;
2. LaskaKit ESPlan;
3. the Waveshare and M5Stack RS485 boards;
4. RS485 gateways such as the EW11, which many PV+HA users already own for inverter Modbus [knowledge];
5. a USB-RS485 dongle with the blesk89 add-on;
6. the ČEZ PND HACS integration;
7. the EG.D OpenAPI integration;
8. inverter grid meters;
9. Shelly and other CT meters;
10. the EG.D EVA pilot device [verified: egd.cz/pilot-eva];
11. any supplier or aggregator that later bundles a reader [knowledge, speculative].

The gap is covered for the capable, the PV-equipped and the dashboard-only. What remains is non-DIY HA users without an inverter meter, whose meter is physically reachable.

**Does the gap close within 6–12 months once others notice?** Yes, probably faster. There is no IP, no exclusive supply and no switching cost, and the product is one-off with no repeat. A forum member can publish a "buy this board, use this installer" post for free. LaskaKit can list a kit. The founder has to advertise in public forums to sell, and that same advertising reveals the recipe and the demand to his competitors.

**Is the trend rising or fading?**
- **Rising:** the meter base grows through mid-2027, and HA adoption keeps growing [knowledge].
- **Fading:** the urgency and the inflow of new motivated owners. The residential PV boom of 2022–23 has cooled, energy prices are less salient than in 2022, and the mandatory rollout phase ends 1 Jul 2027 [knowledge; the date is verified].
- **Hard wall:** the CRA's full obligations from 11 Dec 2027 [verified: developer.espressif.com CRA blog] cap the placing-on-market window at about 15 months unless compliance is funded.
- **Net for this specific pain:** it peaks in 2026–H1 2027 and flattens after.

**Are new entrants succeeding?** There are no CZ entrants to observe, so there's no evidence either way. Abroad, small makers (SlimmeLezer, amsleser) found buyers where the port is standard and powered. In NL the category then **commoditised to €20–43 under funded firms**, and in AT it never left DIY. Neither outcome favours a solo seller at €48–76.

---

## 3. My rebuilt demand funnel [estimate throughout]

This covers buyers reachable in the window Oct 2026 to Dec 2027 (the CRA wall).

| Step | Range | Reasoning |
|---|---|---|
| CZ HA households | 15–30k | Dossier's 20–30k, unverified; widened at the low end |
| × have AMM by end-2027 | 35–55% → 5–16k | AMM ≈ 1.1M of ~6M metering points ≈ 18% nationally [knowledge: ~6M points]; HA/PV skew raises it 2–3× |
| × port physically usable (ČEZ or an accessible EG.D type, PRE activation accepted, and power and Wi-Fi at the meter, or willing to run a cable from the pillar box) | 40–60% → 2–10k | Pillar-box share unmeasured; the dossier itself rates it "medium–high" |
| × real need not met by an inverter meter, portal or Shelly | 30–50% → 0.6–5k | Most PV hybrid owners already meter the grid |
| × won't DIY even with a no-solder €20 board and a free installer | 25–40% → 150–2,000 | HA users self-select for tinkering |
| × buy from the founder rather than a clone, LaskaKit or a forum recipe | 30–60% → **≈ 50–1,200 units** | No moat |

- **Midpoint ≈ 250–300 units over about 15 months.** Roughly 60% of that is stock at launch and 40% is flow.
- **Shape:** about 15–25 units/month in months 2–6, decaying to **≈ 6–10 units/month by month 12**.
- The uncertainty is about ±3×. The *shape* is the robust finding; the level is not.
- The dossier's optimistic case needs 40 units/month at month 12. That is above my *entire* estimated market flow at that point.

---

## 4. Fatal flaws (demand lens)

1. **Zero paying-demand evidence against a brief that awards points only for proven paying demand.** The dossier has installed-base and interest signals only, and the orchestrator verification did not change that.
2. **The segment is hollow in the middle.**
   - The most motivated HA users can DIY it for €20.
   - The richest sub-segment (PV owners) already has real-time grid data.
   - A large share of the rest have meters in pillar boxes or stairwells, where a €56 Wi-Fi dongle doesn't work without extra cabling or an electrician.
3. **No moat, and a capable local incumbent one step away.** Taken together with the GPL firmware and the public forum channel, the first sign of traction is also the signal that invites the clone.
4. **The Stage 2 gate measures the wrong thing.** Two months at ≥ 15 units will almost certainly be the pent-up launch spike. Investing about €4.3k (about €2.5k of it sunk) on that signal would be investing into decay, with a CRA wall 6–12 months later. On my numbers the ~€15/unit uplift over kits at 8 units/month repays the €2.5k in about 21 months, after the CRA deadline.

None of these is a legal or technical impossibility. Together they mean this is **not an asymmetric bet**. At best it is a small hobby business with a short window.

---

## 5. Fixable issues and the fix

| Issue | Fix |
|---|---|
| The day-30 test counts "interest sign-ups", the cheap signal that burned the founder before | Replace it with **prepaid deposits**: one forum post plus two FB groups, a 300 CZK refundable deposit, a 21-day window. **Kill if fewer than 15 deposits.** Drop the "≥ 40 reservations" alternative from the Stage 1 pass rule. |
| €450 of sale kits and €200 of beta kits are bought before any money comes in | Buy boards **after** payment; CZ distributors ship in 1–3 days. Cut beta kits to 3–4 (2 ČEZ, 1–2 EG.D). **This takes money at risk from ~€900 to ~€250.** |
| The funnel percentages are guesses | Put 6 questions on the deposit form: distributor, meter type, meter location (indoor / facade / pillar box / stairwell), existing inverter grid meter y/n, HA / Loxone / none, "would you build it yourself from a parts list?". Within 3 weeks this replaces §3's guesses with data. |
| The Stage 2 trigger fires on the launch spike | Require **≥ 15 paid units/month in months 4 and 5 after launch** (after the forum backlog clears). Also require the Stage 2 sunk cost to be repaid before **Dec 2027** at the observed run-rate. On my numbers, both fail. |
| The price is untested against a visible ~€20 BOM | Split-test 990 vs 1,190 CZK on the deposit page. Lead with what is hard to copy: a pre-crimped, tested cable, per-distributor configs and Czech support. |
| The buyer pool is only HA hobbyists | Test two wider channels before any hardware work: (a) **B2B packs for PV installers and HA/Loxone integrators**, who already open pillar boxes with an electrician and can add a DIN-rail PSU; (b) a SK variant, if Slovak meters match (unverified). |
| LaskaKit could clone this | Consider pitching the configs, the cable spec and the guide to LaskaKit as a co-branded kit on a per-unit fee. Upside is small, but it turns the biggest clone threat into a channel at almost no risk. This is optional. |

---

## 6. Corrected month-12 estimate (operating profit before income tax and levies)

| Case | Units/month at M12 | Net/unit | Fixed | **M12 €/month** | Notes |
|---|---|---|---|---|---|
| Pessimistic | 0 (stopped at day 60–90) | – | – | **€0** | €300–600 lost one-off; ~€150–250 with the deposit-first fix |
| **Realistic** | ≈ 8 | €16 (kit) or ≈ €29 (own HW after CE amortisation) | €30–40 | **≈ €100–190, point ≈ €150** | Kit-only ≈ €100. Stage 2 triggered on the spike ≈ €190/month at run-rate, but with ≈ €2.5k sunk and ~60 of 100 PCBA units still unsold at M12 |
| Optimistic | ≈ 25 | ≈ €32 | €50 | **≈ €750** | Needs a root.cz feature, no LaskaKit or forum clone, and a B2B installer channel that works |

**€/hour:**
- **Realistic month-12 run-rate: ≈ €15/h.** That is ≈ €150 over ≈ 9–10 h/month: 8 units × 26–40 min, plus ≈ 3 h community posting and ≈ 2 h admin.
- **Year 1 all-in, including the ~60–120 h build and launch phase and the sunk costs: ≈ €1–9/h.** That's ≈ €9/h if the founder stays on kits and ≈ €1/h if Stage 2 is triggered on the spike [estimate].
- The dossier's realistic €500/month is about 3–4× too high on demand grounds alone.

---

## 7. Would you tell a friend to do this?

**No, not as a way to make money.** I'd say yes only if the friend is a Home Assistant hobbyist who would enjoy building it anyway and accepts all of these conditions:
- they cap the money at risk at ~€250 using the deposit-first test;
- they stop at fewer than 15 prepaid deposits;
- they never enter Stage 2 on launch-spike numbers.

Even then the ceiling is a few hundred euros a month for about 15 months, after which the CRA and clones close the window.

---

## Sources used this session
- Search (1 call): https://github.com/blesk89/ha-addon-egd-dlms, https://github.com/IntExCZ/Sagemcom_XT211, https://github.com/Tomer27cz/xt211, https://www.homeassistant-cz.cz/viewtopic.php?p=26379, https://www.vodnici.net/community/technologicke-vybaveni-domu/vycitani-dat-z-han-portu-elektromeru/, https://github.com/Antrac1t/HomeAssistant-EGDdistribuce/issues/8, https://www.facebook.com/groups/2232679967058877/posts/4043520129308176/
- From 06-verification.md: https://www.laskakit.cz/en/laskakit-esplan-esp32-lan8720a-max485-poe/
- From 02-main-loop-evidence.md: https://www.cezdistribuce.cz/cs/pro-zakazniky/potrebuji-vyresit/elektromery-a-odecty/komunikacni-rozhrani-z-elektromeru, https://github.com/konikvranik/hacs_cez_distribuce
- From the dossier and the hunt file (not re-checked): the egd.cz, novemereni.cz, byznysnoviny.cz, zakonyprolidi.cz, smarthomeduurzaam.nl, clasohlson.com, egd.cz/pilot-eva and developer.espressif.com URLs as cited there.

---

**Return line:** `WEAK|3|€150|~€15/h at M12 run-rate (≈€1–9/h all-in year 1)|Zero paying-demand evidence: the gap is a thin convenience layer over free DIY, inverter meters and off-the-shelf CZ boards (LaskaKit ESPlan) that any local maker can clone within months, and demand is a front-loaded launch spike that decays as the mandatory AMM rollout ends in mid-2027.`
