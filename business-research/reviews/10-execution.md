# Review 10: "HAN reader CZ", EXECUTION lens (execution, legal and platform risk, CZ)

Reviewer lens: execution, legal load, platform risk, sourcing, skill ramp. Date: 2026-09-29.
Inputs: `00-brief.md`, `dossiers/10-han-reader.md`, `02-main-loop-evidence.md`, `06-verification.md`, `cz-legal-tax-quickstart.md`, `scores/scorer-A/B/C.md`, the longlist C10 block, plus **one** WebSearch this session.
Labels: **[verified: URL]** means a search snippet, never read first-hand. **[knowledge]** means reviewer background, not re-checked. **[estimate]** means reasoning shown.

---

## Verdict: **WEAK, score 3 / 10**

The €900 kit test can actually be run, and the cash at risk is small. That is the dossier's one real strength. Everything that lifts the result above hobby money breaks down once you look at how it would be executed:
- **The €500/month "realistic" case needs Stage 2.** Stage 2 means becoming a radio-equipment manufacturer under RED, EN 18031, EMC, RoHS, GPSR, WEEE and, from 11 Dec 2027, the CRA.
- **Stage 2 can't pay for itself in the window it has.** By the dossier's own timeline, own hardware ships around May–Jun 2027, and its sunk costs are recovered only *after* the CRA's full obligations start. At that point the founder must either take on a multi-year security-support duty or stop selling.
- **The 12-week plan contradicts its own gate.** It spends Stage 2 money (KiCad, prototypes, the EMC pre-scan) in weeks 8–11, before the "≥ 15 paid/month for 2 consecutive months" trigger can even be measured.
- **The plan assumes skills and hardware the brief never gives the founder.** It needs ESPHome, RS485 and DLMS competence, KiCad RF layout, and a HAN-capable AMM meter at home to test on.

What survives is a kit business worth about **€100/month** at month 12. That fits a hobbyist who already runs Home Assistant, not the founder in the brief.

---

## 1. Claims checked

| # | Dossier claim | What I found | Status |
|---|---|---|---|
| 1 | No packaged CZ HAN reader is on sale | My one search (`čtečka HAN elektroměr RS485 RJ12 ESP32 hotová koupit…`) again returned only DIY material: GitHub repos (Tomer27cz, IntExCZ, blesk89), homeassistant-cz.cz threads t=1565 and t=2127 with p=26362, and the EG.D EVA pilot guide. The search summary itself says "no commercial ready-to-buy solution" was found [verified: https://github.com/Tomer27cz/xt211, https://www.homeassistant-cz.cz/viewtopic.php?t=1565, https://www.egd.cz/sites/default/files/2025-07/uzivatelska-prirucka-20250730.pdf]. 06-verification adds that LaskaKit already sells an ESP32 + MAX485 + PoE board, the ESPlan. | **Confirmed, but the gap is thin.** The hardware exists; only the packaging and the guide are missing. |
| 2 | ČEZ: HAN port open, no notification needed | Confirmed by ČEZ Distribuce's own page via 02-evidence. | Confirmed |
| 3 | EG.D works "only on certain meter types"; a sealed cover means requesting unsealing | This comes from the EG.D PDF. **The execution consequence is missing from the dossier.** Every EG.D sale needs a meter-type check before purchase (a photo of the label), and some buyers face a wait for a distributor visit. | Confirmed; it adds pre-sale support time and returns |
| 4 | PRE: customer must request activation, a technician swaps the cover | The dossier admits the exact PRE page is uncertain. Lead time and fee are unknown. The 2 PRE beta kits in week 3 almost certainly **can't report back by week 4**. | Unverified; PRE should be treated as untestable within 12 weeks |
| 5 | Stage 1 kit = founder is a *distributor*, not the manufacturer | **Disputed [knowledge: EU Blue Guide 2022 §3.1 and RED Art. 10–12].** Someone who puts products together under their own name as a new functional product ("HAN-Start kit"), or who changes a product's intended purpose, is treated as its manufacturer. Many ESP32 dev boards are declared as development or evaluation hardware. Turning one into a consumer device for permanent installation, with the seller's firmware and the seller's web installer, is exactly that kind of repurposing. Even a pure distributor must make sure Czech-language instructions and the RED information (band, max power, DoC or simplified DoC) come with the unit. | **Optimistic.** Enforcement risk at 20 units is low, but the framing is legally weak |
| 6 | Stage 1 WEEE: "the distributor is the producer" | That holds only if the seller who invoices the founder is **CZ-established**. TME and Botland, both named in §7, are Polish companies [knowledge]. Under Art. 3(1)(f) of the WEEE Directive, a CZ business that brings EEE in from another member state becomes the CZ producer. | **Partly true.** Buy only from CZ entities (rpishop.cz, GM Electronic, LaskaKit) |
| 7 | Lean CE route: €1,000–2,000 and 30–50 h | Two problems. First, CZ lab invoices carry 21% VAT that a non-payer can't reclaim. Second, EN 18031-1 goes beyond "unique enforced credentials": it also covers secure update (integrity and authenticity of firmware), secure storage and access control [knowledge, moderately confident]. ESPHome's OTA is password-gated but **unsigned by default**, and secure boot and flash encryption aren't standard ESPHome features. For a beginner I estimate **60–120 h, or €1.5–4k with a consultant**, plus 2–6 weeks' booking lead time at the lab [estimate]. | **Optimistic** |
| 8 | CRA: decide by Q3 2027 | The date is right. The dossier doesn't draw the consequence, though: Stage 2 payback (per §10, "~10–12 months" from about month 8) lands **after** 11 Dec 2027. See Fatal flaw F1. | Confirmed; it undermines Stage 2 |
| 9 | Build phase 10–12 h/week for weeks 1–11; run-rate ≈ 3 h/week, 26 min/unit | The build phase is feasible only for someone already fluent in ESPHome. Per unit, the estimate leaves out **pre-sale compatibility questions from non-buyers** (meter photos, pillar-box questions), cable crimping and QC for the kits, re-flashing returns, and firmware maintenance. My estimate is **≈ 45 min per kit sold, all in** [estimate]. | **Optimistic** |
| 10 | Day-30 kill: "< 3 of 8 beta units reading correctly" | This bar is far too low. A product that fails on 5 of 8 meters would generate unmanageable returns and support. | **Wrong threshold** |
| 11 | Realistic path: M6 = 14 kits/month, "Stage 2 triggered at ~15/month" | Under the dossier's **own** gate (≥ 15 for 2 consecutive months), 14/month does **not** trigger Stage 2. The realistic case therefore stays on kits, and at the dossier's own €17/kit that is ≈ **€240** at month 12, not €490. | **Internally inconsistent** |
| 12 | No vázaná (electrical) licence needed | That's true for *making* a 5 V SELV device [knowledge; quickstart §1.2]. **The Long-Line guide "covers conduit (chránička) routing"**, though, which steers laypeople into running cable into a switchboard or boundary pillar box. That is work that under NV 194/2022 Sb. generally belongs to a qualified person [knowledge]. | Partly true; the guide creates liability |

---

## 2. Legal and compliance load (CZ-only, as proposed)

| Regime | Stage 1 (kits) | Stage 2 (own PCB) | Execution note |
|---|---|---|---|
| Živnost (volná) | 800 CZK, 5 working days | same | Fine. If registered in Oct 2026, the 2026 social-insurance threshold drops to 29,375 CZK (quickstart §2.1). That won't be reached in Q4, so no problem |
| VAT / identified person | **Triggered by Meta/Google ads**, and also by **Allegro.cz** (Allegro.pl invoices fees) and **Kaufland.cz** (DE entity) [knowledge]. That means a monthly VAT return by the 25th for every month with such a purchase | same | Avoidable: use organic channels, **Seznam Sklik** (CZ supplier) and Heureka (CZ) only |
| RED 2014/53/EU + DA 2022/30 (EN 18031-1/-2) | Grey zone (claim 5) | **Full manufacturer duty.** Technical file, DoC, EN 18031 self-assessment, and a notified body if any restricted clause is hit | The heaviest item for a beginner. See claim 7 |
| EMC / safety (RED Art. 3.1) | Relies on the module vendor's DoC | Pre-scan plus desk assessment | Lab slots and VAT |
| RoHS | Supplier declarations | Supplier declarations plus a file | Low effort |
| GPSR | Manufacturer or distributor duties: batch number, address, Czech instructions, complaints register | same | Low effort |
| WEEE (542/2020 Sb.) | None, **if** bought from a CZ entity | Collective scheme before the first sale; about €150 in year 1 | CZ-only is correct; exporting to SK/PL would need per-country WEEE |
| Batteries | None (no cell) | None | Good design choice |
| Packaging (EKO-KOM) | Records only | Records only | Trivial |
| **CRA (EU) 2024/2847** | Vulnerability reporting already applies from 11 Sep 2026. The founder's hosted firmware binaries for a paid kit are arguably a commercial product with digital elements [knowledge] | Full duties from **11 Dec 2027**: SBOM, vulnerability handling, security updates over a declared support period (5 years by default unless the product's expected use is shorter) [knowledge] | **The real wall.** See F1. **Also check Annex IV:** "smart meter gateways" are a *critical* category. A customer HAN reader is probably not a "smart meter gateway within a smart metering system" under 2019/944, but a misclassification would mean certification or a notified body [knowledge, uncertain]. Check this before Stage 2 |
| Goods with digital elements (Directive 2019/771 as transposed in the CZ Civil Code) | The seller must supply the updates needed to keep the goods working for the period a consumer can reasonably expect [knowledge] | same | **Missing from the dossier.** If ČEZ or EG.D changes the push list or turns on encryption, the founder owes a firmware update to every past buyer. That is an ongoing maintenance duty of about 1–3 h/month |
| Consumer law | 14-day withdrawal, 24-month warranty, withdrawal button | same | Returns from unsupported meters, sealed covers and PRE activation queues fall **inside** the 14 days |
| GPL / ESPHome name | Publish configs and source; no "ESPHome" branding | same | Fine. **Community norm risk:** selling devices built on volunteer repos without crediting them |
| Hallmarking, AML, margin scheme, US tariffs, Etsy rules | **N/A** | N/A | CZ-only electronics; Etsy's handmade rules would not allow resold modules anyway [knowledge] |

**Bottom line on legal load.** Stage 1 is legally light in practice: nobody enforces against 20 kits sold on a forum. It is not as clean as the dossier claims, and the fixes cost almost nothing (see fixes 2 and 3). Stage 2 is disproportionate: roughly 60–150 h of compliance work plus a 2027 CRA decision, for a product selling perhaps 15–25 units a month.

---

## 3. Platform, channel and sourcing risk

- **The channel depends on community goodwill, not on a platform.** The sales funnel is homeassistant-cz.cz threads and CZ PV and HA Facebook groups. Hobby forums and FB groups usually confine commercial posts to a marketplace section or ban them outright [knowledge, unverified for this forum].
  - The audience is also the most DIY-capable in the country. A post selling a 1,190 CZK kit that wraps the free code of forum members like Tomer27cz and blesk89 invites "just build it for €8" replies.
  - **The repo authors themselves are the most likely clones.** They already have the code, the credibility and the audience.
- **The clone threat is concrete, not hypothetical.** LaskaKit already sells the ESP32 + MAX485 board and publishes ESPHome material [verified via 06: https://www.laskakit.cz/en/laskakit-esplan-esp32-lan8720a-max485-poe/]. It already holds CE and WEEE and has shop traffic. A public launch thread is exactly what would prompt it to ship a "HAN kit + návod" within weeks. The dossier's 12–24-month durability looks like **6–12 months** from a public launch [estimate].
- **Distributor substitute.** EG.D's EVA pilot shipped a free "Senzor a Gateway" to participants [verified: EG.D PDF above]. If it rolls out, the EG.D segment (≈ 290k meters) goes to zero overnight.
- **Sourcing, Stage 1.** It depends on one specific dev board staying in stock at a CZ-established seller (the M5Stack Atom + RS485 Base, or the Waveshare ESP32-S3-RS485-CAN). Board revisions change pins and break configs. The Waveshare price wasn't even captured. The €19 hardware line is probably €19–25 once CZ retail margin and non-reclaimable VAT are included [estimate].
- **Sourcing, Stage 2.** JLCPCB and LCSC are reliable, and the ESP32-C3-MINI-1 is abundant [knowledge]. The fragility sits in firmware, not parts: third-party ESPHome components maintained by hobbyists, monthly ESPHome releases, and occasional breaking changes. Pin versions and own the update channel.
- **Physical install reality: the hidden killer.**
  - Many CZ family houses, which are the PV and heat-pump segment, have the meter in a **boundary pillar box** with no socket and weak Wi-Fi [knowledge; scorers B and C].
  - Indoor meter cabinets are often **steel**, which kills a PCB antenna.
  - The Long-Line SKU moves the problem to "run 20 m of cable from the fence into the house". For many buyers that means an electrician visit (≈ 1,000–2,500 CZK [estimate]) or a conduit that doesn't exist.
  - Each such prospect costs 10–20 min of pre-sale Q&A, and many don't convert.

---

## 4. Skill ramp and time to first sale

| Founder profile | Kit stage (weeks 1–7) | First paid sale | Stage 2 feasible? |
|---|---|---|---|
| Already runs HA + ESPHome, owns an XT211/relay box, has soldered RS485 before | 40–60 h | **Week 6–8** (mid–late Nov 2026). Beta volunteers take 1–3 weeks to install and report, so week 4 is optimistic | Yes, but 100–200 h for KiCad RF layout, EN 18031 and the tech file. At 10–12 h/week that is **4–5 months**, not 5 weeks |
| Competent generalist (codes a little, no embedded experience) | 80–120 h | Week 10–14 | Not without a paid consultant (€2–4k), which breaks the budget logic |
| Beginner, the brief's default | Not credible within 12 weeks | > 3 months, if ever | No |

The brief gives the founder **no** stated electronics or firmware skill, and the orchestrator already flagged "the founder's coding ability is unknown" for the software dossier. The plan also quietly assumes the founder has a HAN-accessible AMM meter at home. Without one, every test runs through forum volunteers, which is slow and depends on their goodwill. Bench replay of captured frames checks decoding but not the physical layer: polarity, termination, cable length, relay-box behaviour.

---

## 5. Fatal flaws (fatal to the dossier's €500 case, not to a €900 hobby test)

**F1. Stage 2 runs into the CRA before it pays back.**
- By the dossier's timeline, own hardware ships from about month 8 (May–Jun 2027). The Stage 2 sunk cost of ≈ €2.5k pays back over "~10–12 months", which means around Q1–Q2 2028.
- CRA full obligations begin **11 Dec 2027**. That leaves ~6–7 months of selling own hardware, about one 100-unit batch at the realistic rate.
- After that, the founder either commits to CRA manufacturer duties (a multi-year security-update commitment, vulnerability handling and an SBOM, all for a side-business gadget) or stops placing new units with the sunk cost unrecovered.
- The dossier notices the date but never runs the payback against it.

**F2. The realistic €500 fails the dossier's own gate.**
- Realistic M6 is 14 kits/month, and the trigger is ≥ 15 for 2 consecutive months. So the realistic path never reaches Stage 2, and M12 is a kit business.
- At €15–17/kit that is **≈ €100–240/month**, and less once clones arrive.

**F3. The 12-week plan spends Stage 2 money before the gate.**
- Weeks 8–11 are KiCad, a JLCPCB prototype, lab quotes and the **EMC pre-scan (≈ €1,200)**. Week 12 is the "day-90 decision".
- Paid sales open in week 5, so "2 consecutive months ≥ 15" can't be observed before about week 13–14 (early Jan 2027).
- As written, the founder would sink ≈ €1.5k of Stage 2 cost on the strength of 3–7 weeks of kit sales.

**F4. The execution prerequisites aren't in the brief.**
- The plan is feasible only for an existing ESPHome hobbyist who owns a HAN meter.
- For the brief's founder (skills unknown, already burned by clever ideas), time to first sale goes past 3 months, and Stage 2 isn't executable at 10–15 h/week.

---

## 6. Fixable issues and the fix

| # | Issue | Fix |
|---|---|---|
| 1 | Plan/gate inconsistency (F3) | Measure the gate over Nov and Dec 2026. Start KiCad work **no earlier than Jan 2027** and spend nothing on the lab before the gate passes. Raise the Stage 2 trigger to **≥ 25/month for 2 months**, because that is the volume at which Stage 2 pays back before 11 Dec 2027 [estimate: €2.5k ÷ €15 uplift ≈ 170 units in ≤ 7 months ≈ 25/month] |
| 2 | Stage 1 "distributor" framing (claim 5) | Sell the **unmodified CE module as a resold item**, with the manufacturer's DoC on file and a Czech RED info sheet, plus a **passive RJ12 cable** as your own accessory and the guide and configs free on GitHub Pages. No own-brand "kit" on the radio device. Get the DoC in writing *before* buying stock, and reject boards declared "for evaluation/professional use only" |
| 3 | WEEE producer status via Polish suppliers (claim 6) | Buy EEE only from CZ-established sellers. Check who issues the invoice, not the site's TLD |
| 4 | Identified-person admin | Drop Meta and Google ads and don't list on Allegro or Kaufland. Use organic forum and FB posts, Sklik and Heureka. This saves ≈ €4.8/unit and 12 VAT returns a year |
| 5 | Returns from unsupported or unreachable meters | Add a mandatory **compatibility check before payment**: meter label photo, distributor, meter location (indoor, pillar box or steel cabinet). Refuse unsupported types. Publish an "EG.D Typ A = not supported" table |
| 6 | Beta pass bar (claim 10) | Pass only if **≥ 7 of 8** units work, with ≥ 2 working units per supported distributor. Launch **ČEZ-only**; add EG.D once proven and PRE once one real activation has gone end to end |
| 7 | Long-Line install liability (claim 12) | Don't sell cable routing as DIY. State that a cable into a switchboard or pillar box is a job for an electrician. Alternatively, offer a **no-radio variant** (a resold CE USB-RS485 adapter plus a long cable to the HA host, with the free blesk89-style add-on). That removes RED and EN 18031 entirely |
| 8 | Stage 2 compliance weight | If Stage 2 ever happens, make it **wired (Ethernet/USB), not Wi-Fi**: no RED and no EN 18031, leaving only EMC, RoHS, GPSR and WEEE (and CRA from Dec 2027). Or **license** the configs and guide to LaskaKit or a repo author for a per-unit royalty, so they carry CE and WEEE. That turns the most likely clone into the manufacturer |
| 9 | CRA classification | Before any Stage 2 spend, confirm in writing (ČTÚ or a consultant) that a customer-side HAN reader is not an Annex IV "smart meter gateway" |
| 10 | Firmware maintenance duty | Budget 1–3 h/month. Pin ESPHome versions and keep an OTA or web-installer update channel for every past buyer |
| 11 | Community backlash | Credit and contribute upstream, ask the forum moderators before selling, and post in the commercial section |

---

## 7. What kills this in the first 6 months (ranked)

1. **Interest doesn't convert to payment.** The forum crowd builds its own or waits for LaskaKit, and the day-60 count comes in under 12 paid kits. Likelihood: high.
2. **Compatibility and installation failures** (EG.D meter types, sealed covers, PRE queues, pillar boxes, steel cabinets) push returns above 10% and swamp evenings with support. Likelihood: medium–high.
3. **A clone from LaskaKit or a repo author** within weeks of the public launch, cheaper and with existing traffic and CE. Likelihood: medium–high within 6–12 months.
4. **Founder time and skill.** Remote debugging through volunteers, plus the sustained 10–12 h/week build phase, slips the plan by 1–3 months. Likelihood: medium (high for a non-ESPHome founder).
5. **Distributor action.** EG.D rolls out EVA free, or a distributor turns on encryption; the latter is survivable with a firmware update but adds friction. Likelihood: low–medium.

**Can a normal employed person run the 12-week plan?** Weeks 1–7 (the kit test): yes, but only if they are already an ESPHome and HA hobbyist with a ČEZ meter. Weeks 8–12 (the Stage 2 build): no. That work is realistically 4–5 months at 10–12 h/week, and in the plan it comes before the gate anyway.

---

## 8. Corrected estimates

The kit unit economics are corrected as follows [estimate]:
- price €48;
- hardware €21 (CZ retail incl. non-reclaimable VAT);
- cables €2.5, box and guide €1, payment €0.8, packaging €0.5;
- returns €2.4 (10% return rate × shipping refund + reflash, plus about 3% unsellable);
- ads €2 (Sklik only).

That gives **≈ €16–18 net per kit**, or about €13 if Meta ads are kept.

| Month-12 case | Assumption | Profit/month before levies | Hours/month | €/hour |
|---|---|---|---|---|
| **Pessimistic** | Day-60 kill (< 12 paid). One-off loss ≈ €400–700 after leftovers are sold on at cost | **€0** | 0 | n/a (year 1 ≈ −€5/h over ~100 h) |
| **Realistic** | Kits only, never passing a CRA-aware gate. **8/month × €16 − €30 fixed** (shop, domain, payment gateway), with LaskaKit-style clone pressure capping volume | **≈ €100** (≈ €78 after the 22% set-aside) | ≈ 12 (8 × 45 min + 3 h community + 2 h admin + 1 h firmware) | **≈ €8/h** at run-rate; **≈ €2–3/h** for year 1 including the 120–150 h build |
| **Optimistic** | Gate passed by month 5; wired or lean Stage 2 from month 8 at 25–30/month × €30 − €60; no clone yet | **≈ €750** | ≈ 20 | ≈ €37/h. The window closes at the 11 Dec 2027 CRA decision |

Compared with the dossier (€50–100 / €500 / €1,300 and an implied ≈ €38/h), **the realistic case falls about 5× once the dossier's own gate and the CRA timing are applied.**

---

## 9. Would you tell a friend to do this?

**Only if** all of these hold:
- they already run Home Assistant and ESPHome;
- they have a ČEZ XT211 with a relay box they can physically reach at home;
- they treat it as a **€900, 60-day, ČEZ-only kit experiment**, sold as a resold CE module plus their own cable, with no paid Meta ads;
- they accept that ~€100/month is the likely ceiling.

Tell them **not** to start own-PCB Stage 2 unless kits sell ≥ 25/month for 2 months **and** they have a written CRA plan (support period or exit) before spending on the lab. For the founder in the brief, whose skills aren't stated and who wants a reliable €500+/month: **no.**

---

### Sources used this session
- https://github.com/Tomer27cz/xt211
- https://github.com/IntExCZ/Sagemcom_XT211
- https://github.com/blesk89/ha-addon-egd-dlms
- https://www.homeassistant-cz.cz/viewtopic.php?t=1565
- https://www.homeassistant-cz.cz/viewtopic.php?t=2127
- https://www.homeassistant-cz.cz/viewtopic.php?p=26362
- https://forum.mypower.cz/viewtopic.php?t=15586
- https://www.egd.cz/sites/default/files/2025-07/uzivatelska-prirucka-20250730.pdf
- From 06-verification: https://www.laskakit.cz/en/laskakit-esplan-esp32-lan8720a-max485-poe/
