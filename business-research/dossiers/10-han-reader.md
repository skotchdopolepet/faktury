# C10 — "HAN reader CZ": deep-dive dossier

Date: 2026-09-29. FX: 1 € ≈ 25 CZK. The orchestrator's evidence file and 14 WebSearch calls from this session (search snippets only, since WebFetch is blocked) override the hunter's claims. The labels are **[verified: URL]** (a URL-cited search snippet, never read first-hand), **[knowledge]** (unverified background) and **[estimate: reasoning]**.

---

## 1. Verdict in 3 lines
- **Conditional go, and only as a ≤ €900 kit pre-sale test.** Do not become a CE radio-equipment manufacturer until the test shows **≥ 15 paid units/month for 2 consecutive months**. At today's evidence this is a real but small, copyable niche, not an asymmetric bet.
- **Realistic month-12 profit: ≈ €500/month** before income tax and levies (≈ €390 after the 22% set-aside). That assumes about 16 units/month at ≈ €33 net on own hardware. Pessimistic is ≈ €50–100 and optimistic ≈ €1,300.
- **The single biggest risk is that the paying niche is tiny.** The only buyers are Home Assistant or Loxone users who meet all of these conditions:
  - they have a HAN-capable AMM meter;
  - they won't wire a €8 ESP32 + MAX485 themselves;
  - they aren't already served by their inverter's grid meter or the free portal integrations.

  My estimate is 1,000–3,500 buyers nationally over three years, shared with anyone who copies the product.

---

## 2. The exact offer

| SKU | What it is | Price (CZK / €) | Stage |
|---|---|---|---|
| **HAN-Start kit** | CE-marked ESP32 + RS485 module bought from an EU distributor (e.g. M5Stack Atom Lite + Atomic RS485 Base, or the Waveshare ESP32-S3-RS485 sold at rpishop.cz [verified: https://rpishop.cz/642120/waveshare-prumyslovy-esp32-s3-modul-s-rs485-can/]). It comes with a pre-wired RJ12 cable (pins 3 = A, 4 = B, 6 = GND), a USB-C cable and a Czech guide. The **buyer flashes it** with one click in the browser (ESPHome web installer). Configurations cover ČEZ, EG.D and PRE. | 1,190 / €48 | 1 (test) |
| **HAN Reader Wi-Fi** | Own PCB assembled by JLCPCB: ESP32-C3-MINI-1 (a pre-certified module) + SP3485 + TVS protection + USB-C, in a small ABS box. **Preflashed** with a unique per-device API key and OTA password, and Home Assistant auto-discovers it. Includes a 2 m RJ12 cable and a CE-marked 5 V PSU (−100 CZK without the PSU). | 1,390 / €56 | 2 |
| **HAN Reader Long-Line** | As above, plus 20 m of outdoor twisted-pair cable and an RJ12 coupler, so the reader sits **indoors** while the meter is in a boundary pillar box (RS485 runs hundreds of metres). **No LoRa.** A second radio would mean a second RED test. | 1,890 / €76 | 2 |

- **Buyers:** CZ owners of PV systems, heat pumps or EV chargers on spot or dynamic tariffs who run Home Assistant (primary) or Loxone (secondary). The Loxone crowd is on vodnici.net [verified: https://www.vodnici.net/community/loxone-a-arduino/elektromer-egd-itron-sl7000/].
- **Channels:**
  - homeassistant-cz.cz threads (a page ≈ 20 min of attention);
  - CZ PV and Home Assistant Facebook groups;
  - an own Shoptet or Upgates shop with Zásilkovna shipping;
  - later Heureka and Allegro.cz.
- **CZ only.** WEEE rules apply per destination country (quickstart §4.4), and SK/HU/PL use different meters.

---

## 3. Why it makes money (demand evidence)

**The installed base is forced by regulation and growing right now.**

| Distributor | Status | Source |
|---|---|---|
| ČEZ Distribuce | SmartME project: **>1.02M meters + ~878k relay boxes**; ~350k added in 2026; ~650k by mid-2027 | [verified: https://www.cezdistribuce.cz/cs/dotacni-projekty/cez-distribuce-smartme-inteligentni-mereni, https://www.arecenze.cz/clanky/chytre-elektromery-zdarma-v-roce-2026-statisice-domacnosti-je-uz-maji-mimo-poradnik-vede-placena-cesta/] |
| EG.D | **>290k** installed in early Sep 2026, **+~17k/month**, target 350k by end-2026 | [verified: https://www.byznysnoviny.cz/2026/09/15/energeticky-distributor-eg-d-planuje-mit-letos-instalovano-350-tisic-chytrych-elektromeru/] |
| PREdistribuce | ~50k at end-2025, ~65k by end-2026, ~300k by 2030 | [verified: https://www.tiscali.cz/stovky-tisic-cechu-stale-cekaji-na-chytry-elektromer-kdo-chce-predbehnout-frontu-zaplati-tisice-korun-725021 (search summary)] |
| **Total** | **≈ 0.9–1.0M AMM meters by end-2026, ≈ 1.2M by mid-2027** | [estimate: sum of the rows above] |

**HAN access by distributor**

| | Port | Encryption | Customer action | Source |
|---|---|---|---|---|
| ČEZ | RS485 on the WM-RelayBox (XT211), RJ12, 9,600 bd, push every ~60 s | None observed | **No notification needed** | [verified: https://www.cezdistribuce.cz/cs/pro-zakazniky/potrebuji-vyresit/elektromery-a-odecty/komunikacni-rozhrani-z-elektromeru, https://github.com/Tomer27cz/xt211] |
| EG.D | RS485 DLMS push; **works only on certain meter types** (XT211 "Typ B", AM175 "Typ C"; also ST402D per blesk89) | None observed | If accessible, connect without reporting; if it is behind a sealed cover, **request unsealing** | [verified: https://www.egd.cz/sites/electricity/files/2025-01/ega_2025_komunikacni_rozhrani_rs485.pdf, https://github.com/blesk89/ha-addon-egd-dlms, https://www.homeassistant-cz.cz/viewtopic.php?t=1565] |
| PRE | RJ12 (A = pin 3, B = pin 4, GND = pin 6), 9,600 bd, one-way, 1-minute push | Unclear | **Must request activation** (info@predistribuce.cz); a technician swaps the meter cover for one with a connector; the customer pays for the reading device | [verified: https://www.novemereni.cz/pdf/HAN%20-%20AM175_NAHLED.pdf, https://www.novemereni.cz/pdf/HAN%20-%20E450%203f_NAHLED.pdf (search summary; exact PRE page uncertain)] |

- The MPO customer-interface specification requires DLMS/COSEM security suite 0 capability [verified: https://mpo.gov.cz/assets/cz/energetika/strategicke-a-koncepcni-dokumenty/narodni-akcni-plan-pro-chytre-site/2020/3/Vytah-studie-NAP-SG-rozhrani-na-zakaznika.pdf]. **Encryption can therefore be switched on later.** ESPHome's `dlms_meter` component already takes an AES key, since it was built for encrypted Austrian meters [knowledge], so encryption would add friction but wouldn't kill the product.

**Interest signals, with no paid sales yet**
- There are at least 7 CZ DIY repositories: Tomer27cz/xt211, IntExCZ/Sagemcom_XT211 [verified: https://github.com/IntExCZ/Sagemcom_XT211], blesk89, lhubac/egd-dlms, nero150/CEZ_rele_box, psopso (LoRa) and mstrlc/ha_egd_openapi.
- Several multi-page forum threads exist: t=1565, t=2127 ("Elektroměr PRE"), p=26369 [verified: https://www.homeassistant-cz.cz/viewtopic.php?t=2127], plus a MyPower thread on XT211 four-quadrant behaviour [verified: https://forum.mypower.cz/viewtopic.php?t=15586].
- Root.cz has covered HA spot-selling automation [verified: https://www.root.cz/clanky/home-assistant-prodej-elektriny-na-spotovem-trhu-a-automatizace/].
- Demand drivers [knowledge]: spot and dynamic tariffs, energy sharing through the EDC (sdílení elektřiny), and HDO-tariff automation for boilers and heat pumps. The XT211 + relay-box push includes the tariff and relay state.

**Abroad, plug-and-play readers clearly sell.**
- **NL:** the HomeWizard P1 (€20–43) and SlimmeLezer+ are "the most used" by the Dutch HA community. ESP32 dongles sell at **€55–80** [verified: https://smarthomeduurzaam.nl/kennisbank/p1-meter-vergelijken-home-assistant-2026/, https://www.robbshop.nl/blog/welke-p1-slimme-meter-past-bij-jou-de-ultieme-vergelijking].
- **NO:** Tibber Pulse HAN is sold through mass retail: Clas Ohlson, Elektroimportøren and Onninen [verified: https://www.clasohlson.com/no/Tibber-Pulse-HAN-RJ45-strommaler/p/36-8013, https://www.elektroimportoren.no/tibber-pulse/1405012/Product.html]. amsleser.no sells ESP32 readers, including on Lectronz [verified: https://lectronz.com/products/pow-u-han-port-reader-for-m-bus-meters-esp32].
- **AT:** the meters use encrypted M-Bus, and the customer requests an AES key from the grid operator. The Austrian market stayed DIY-heavy: forum complaints, GitHub readers and M-Bus adapters from Mikroe [verified: https://github.com/tirolerstefan/kaifa, https://www.michaelreitbauer.at/kundenschnittstelle-der-osterreichischen-smart-meter/, https://www.computerbase.de/forum/threads/smartmeter-kundenschnittstelle-aus-der-hoelle.2031259/page-4].
- **HU:** a SlimmeLezer adaptation exists for E.ON meters [verified: https://github.com/amargo/slimmelezer-eon].
- **The lesson.** Where the port is standard, powered and consumer-accessible (NL P1 delivers 5 V), readers became a mass category, then commoditised to **€20–40** from funded firms. Where access is gated by keys (AT), the market stayed hobbyist. CZ sits in between. Its HAN port supplies **no power** (the PRE pinout has only data and ground), PRE needs activation, and EG.D sometimes needs unsealing. No unit-sales figures were found for any analogue.

**Sizing [estimate]**
- ≈ 20–30k CZ Home Assistant installs. This assumes ~1.5–2% of HA analytics installs, scaled up for opt-in.
- × 40–60% with an AMM meter, because HA users skew towards PV and heat pumps, which get priority in the rollout.
- × 10–20% who want real-time HAN data, won't DIY, and find inverter or portal data insufficient.
- The result is **≈ 1,000–3,500 buyers over 2026–2029, ≈ 30–100 units/month for the whole market at peak.** A first mover might take 30–50%.

---

## 4. Supply gap and asymmetry: what is the *real* gap?

The evidence rules out three kinds of gap:
- **Technical:** solved. ESPHome `dlms_meter` supports the XT211, and the frame formats are public.
- **Legal:** the port is open. ČEZ needs no notification.
- **Knowledge:** the forum threads already cover it.

**The real gap is the last metre for the non-soldering HA user.** No packaged reader turned up in 5 separate searches (CZ e-shops, Bazoš, Tindie, Energomonitor, Wattrouter, Loxone and HW-server retailers). That is still not proof [verified: search results above]. The pieces that user can't easily get are:
- a tested device in a box with the correct RJ12 pinout;
- per-distributor OBIS configurations;
- a power and cable solution for meter cabinets and boundary pillar boxes;
- Czech instructions for PRE activation and EG.D unsealing;
- a person who answers questions in Czech.

This is worth roughly €25–35 of margin per buyer.

**Substitutes that shrink it**
- **Free portal integrations** (the ČEZ PND HACS integration, EG.D OpenAPI [verified: https://github.com/mstrlc/ha_egd_openapi]) provide 15-minute data with a delay. That is enough for dashboards but not for real-time surplus automation.
- **PV owners' hybrid inverters** already measure the grid in real time [knowledge]. For them, the HAN reader adds only the billing-grade values, the four-quadrant summed values and the HDO state.
- **EG.D piloted "EVA"**: a free sensor + gateway + app, with devices sent to participants and the pilot running until Mar 2026 [verified: https://www.egd.cz/pilot-eva, https://www.egd.cz/sites/default/files/2025-07/uzivatelska-prirucka-20250730.pdf]. **A distributor-supplied reader is plausible**, although EVA is app-only and not Home Assistant.

**Durability: 12–24 months.** Any CZ hobby-electronics maker (LaskaKit, Pájeníčko, HWKitchen [knowledge, unverified]) or forum member can clone the product in weeks. The EU Cyber Resilience Act's main obligations start on **11 Dec 2027** [verified: https://developer.espressif.com/blog/2026/03/esp32-cra-compliance/], which puts an ongoing security-support cost on anything still being placed on the market after that date. The foreign giants would need a new RS485 SKU for a ~1M-meter market, so they are unlikely to arrive before 2028 [estimate].

---

## 5. Competitor map

| Competitor / substitute | Price | Positioning |
|---|---|---|
| DIY: ESP32 + MAX485 + ESPHome (forum, 7 GitHub repos) | ~€8 in parts [knowledge] | Free code; the forum crowd *is* the target market's most capable third |
| USB–RS485 dongle + HA add-on (blesk89) | €5–15 [knowledge] | Needs the HA host near the meter |
| RS485→Wi-Fi/Ethernet gateways (Elfin EW11, PUSR) | €15–30 [knowledge] | Generic, and the user must configure the decoding |
| Waveshare ESP32-S3-RS485-CAN (rpishop.cz) | Price not captured | A component, not a product; also a possible Stage 1 input |
| Portal integrations (ČEZ PND HACS, EG.D OpenAPI) | Free | Not real-time |
| Inverter meters (DTSU666 etc.), Shelly Pro 3EM | €100–150 + electrician [knowledge] | Real-time, in the panel |
| EG.D EVA pilot device | Free (pilot) | App-only; possible future substitute |
| HomeWizard P1 / SlimmeLezer / Tibber Pulse / amsleser Pow | €20–110 | **Not CZ-compatible** (P1 or M-Bus), but they anchor price expectations |

---

## 6. Unit economics (per unit, €)
Assumptions:
- The buyer pays Zásilkovna shipping (79–89 CZK), and the seller subsidises €0.5.
- Payment gateway (Comgate/GoPay): 1.5% + €0.10 [knowledge].
- Returns allowance: 5% of price.
- Ads: €4 × 1.21, because Meta ads make the seller an identified person who pays 21% VAT on them.
- Non-payer of VAT: no output VAT.

| Line | HAN-Start kit | HAN Reader Wi-Fi | Long-Line |
|---|---|---|---|
| Price | 48.0 | 56.0 | 76.0 |
| Hardware | 19.0 (CE module from an EU distributor) [estimate] | 6.5 (PCBA incl. freight + import VAT) [estimate] | 6.5 |
| Enclosure, RJ12 cable, USB cable | 2.5 | 3.5 | 3.5 + 13.5 (20 m outdoor FTP + coupler) |
| CE-marked 5 V PSU | 0 (buyer's own) | 3.5 | 3.5 |
| Box, label, printed guide | 1.0 | 1.0 | 1.0 |
| Payment fee | 0.8 | 0.9 | 1.2 |
| Packaging + shipping subsidy | 0.5 | 0.5 | 1.5 |
| Returns allowance (5%) | 2.4 | 2.8 | 3.8 |
| Ads (incl. 21% VAT) | 4.8 | 4.8 | 4.8 |
| WEEE / EPR fees | 0 (the distributor is the producer) | 0.2 | 0.3 |
| **Net per unit** | **≈ 17** | **≈ 32–33** | **≈ 34** |
| Less CE amortisation (€1,600 over ~380 units) | – | ≈ −4 | ≈ −4 |

The founder's time is excluded here and covered in §8.

---

## 7. Sourcing and production plan
- **Stage 1 (kits).** Buy CE-marked modules from **EU or CZ distributors** (rpishop.cz, botland.cz, TME), so the founder is a *distributor*, not the manufacturer or WEEE producer. RJ12 6P6C cable and crimps come from TME or GM Electronic.
- **Stage 2 (own PCB).**
  - Design in KiCad: ESP32-C3-MINI-1 using the module maker's antenna keep-out, SP3485, SM712 TVS, USB-C 5 V and a THT RJ12.
  - Have JLCPCB or PCBWay build batches of 100.
  - Estimated cost at 100 pcs, landed [estimate: typical LCSC part prices + JLC setup/stencil/extended-part fees + DHL + 21% import VAT, which a non-payer can't reclaim]:
    - LCSC components ≈ $3.5–4.5/unit;
    - PCB + assembly ≈ $1.5–2/unit;
    - DHL ≈ $25 per batch.
  - Lead time is 7–10 days to build plus 4–7 days shipping.
  - Enclosure: a Kradex Z-series ABS box from TME (~20–30 CZK) with a printed label.
  - PSU: a CE-marked 5 V 1 A adapter from a CZ distributor.
- **Batch and volume.** 100 units (≈ €1,300 all-in) covers ~5 months at the realistic rate. One evening can process 15–20 units, so a realistic 4–5 units/week is ~1.5 h.

---

## 8. Time model (Stage 2, per unit)

| Step | Minutes |
|---|---|
| Sourcing and reorders (amortised) | 2 |
| Flash + generate unique keys + print label (scripted) | 3 |
| Functional test (replay a captured DLMS frame through a USB-RS485 adapter, check auto-discovery) | 3 |
| Assembly (box, cable, QC) | 4 |
| Photos / listing (one-off ~6 h) | ~0 |
| Pack + Zásilkovna label | 4 |
| Messages and setup support (early average; the kit needs ~20) | 10 |
| **Total** | **≈ 26 min** |

At 16 units/month that is ≈ 7 h, plus community posting 4 h and admin 2 h: **≈ 13 h/month (~3 h/week)**. The build phase in weeks 1–11 takes **10–12 h/week**.

---

## 9. Staged budget (total ≤ €6,500 of the €8,500)

**Stage 1: kit pre-sale test, ≤ €900**

| Item | € |
|---|---|
| 3 candidate boards, USB-RS485 dongle, RJ12 crimp tool and cables | 120 |
| 8 beta kits for forum volunteers (3 ČEZ, 3 EG.D, 2 PRE) | 200 |
| First 20 sale kits | 450 |
| Trade licence (800 CZK), T&C template, domain | 80 |
| Reserve | 50 |

- **Pass:** by day 45, all of the following:
  - **≥ 15 paid kits at ≥ 1,190 CZK**, or ≥ 40 reservations for the preflashed version;
  - working on ≥ 2 of 3 distributors;
  - failure or return rate < 10%.
- **Fail:** < 8 paid kits. Stop and sell the leftovers at cost on the forum.

**Stage 2: own CE-marked hardware, only if ≥ 15 paid/month for 2 consecutive months (or ≥ 40 preflash reservations), ≈ €4,300**
- PCB design and 2 prototype rounds: €300.
- EMC pre-scan at a CZ lab (ITC Zlín, UNIS Testlab, TU Liberec, ELKO EP [verified: https://www.itczlin.cz/laboratore/zkusebna-elektro-vyrobky-emc-lvd, https://www.unis-testlab.cz/cs/zkousky-emc]) plus one retest: €1,200 [estimate: €600–1,000/day, typical CZ lab rates, knowledge].
- EN 18031 self-assessment with Espressif's RED-DA tool plus optional expert review: €400.
- WEEE collective scheme (REMA, ASEKOL or ELEKTROWIN), first year: €150.
- 100 PCBA + enclosures, cables and PSUs: €1,500.
- Shop for a year: €250.
- Ads: €300.
- Labels: €200.

**Reserve: ≈ €1,300** for a full accredited RED test (€3–6k [estimate]) *only* if the pre-scan is marginal or a retailer demands it.

**What getting CE right costs a solo seller (the answer to the brief's question)**

| Route | Cash | Founder time | Notes |
|---|---|---|---|
| **Lean but defensible** | **€1,000–2,000** | 30–50 h | Module A self-declaration: the pre-certified module's radio reports (EN 300 328) + an EMC pre-scan of the final product (EN 301 489-1/-17) + a desk assessment for EN 62368-1 and EN 62479 + an **EN 18031-1/-2 self-assessment** (-2 because household consumption data is personal data [knowledge]). Add RoHS supplier declarations, a DoC and a technical file. |
| Belt and braces | €3,000–6,000 | 20–30 h | Full accredited test report |
| **Trap** | €5–15k+ | – | A **notified body** becomes mandatory if the design falls into an EN 18031 "restricted" clause, e.g. letting the user skip setting a password [verified: https://developer.espressif.com/blog/2025/04/esp32-red-da-en18031-compliance-guide/, https://iterasec.com/blog/en-18031-red-cybersecurity/]. **ESPHome's defaults (open fallback AP, optional OTA password) fall into this trap, so ship unique enforced credentials.** |

---

## 10. Projections (operating profit per month before levies; fixed costs ≈ €40/month)

| | Month 3 | Month 6 | Month 12 |
|---|---|---|---|
| Pessimistic | 4 kits × €17 − 30 = **€40** | 5 × €17 − 30 = **€55** | 6 kits × €17 − 30 = **€70** (Stage 2 never triggered) |
| Realistic | 10 kits × €17 − 30 = **€140** | 14 kits × €17 − 30 = **€210** (Stage 2 triggered at ~15/month) | 16 × €33 − 40 = **€490 ≈ €500** (own hardware from ~month 8) |
| Optimistic | 20 kits × €17 − 30 = **€310** | 30 × €32 − 40 = **€920** | 40 × €34 − 60 = **€1,300** |

- In the realistic case, Stage 2 is **marginal**. About €2.5k of the €4.3k is sunk (design, pre-scan, EN 18031, WEEE, shop); the rest is recoverable inventory. The sunk part pays back in ~10–12 months from the ~€15/unit uplift over kits.
- The optimistic case needs the first-mover share of a 60–100/month national market and no clone.
- Set aside 22% of profit for levies while staying under the social-insurance threshold (117,521 CZK/yr). The realistic case (~€6k/yr ≈ 150k CZK) **crosses that cliff**, so budget ~38%, or time expenses (quickstart §2.1).

---

## 11. CZ/EU legal checklist (product-specific)
- **Živnost:** volná, with the fields "Výroba elektronických součástek, elektrických zařízení…" and "Velkoobchod a maloobchod" (800 CZK online). The device is 5 V SELV, so no vázaná electrical licence is needed. **The guide must forbid breaking seals.** Customers use only the accessible port and request unsealing or activation (EG.D, PRE) from the distributor.
- **VAT:**
  - As a non-payer, sell without VAT in CZ.
  - Meta or Google ads and any non-EU SaaS make the founder an **identified person**: register within 15 days, file a monthly return by the 25th, and pay 21%.
  - JLCPCB and LCSC are *goods*, so import VAT is paid at customs and is not reclaimable. That isn't an identified-person trigger.
  - **Never give an EU parts supplier your DIČ.**
- **Margin scheme:** not applicable.
- **CE:**
  - Stage 2: **RED 2014/53/EU**, which covers the safety and EMC essential requirements, plus Delegated Reg. 2022/30 → **EN 18031-1 and -2**. Also **RoHS**, a signed DoC, the CE mark, and a technical file kept for 10 years.
  - Stage 1 kits (distributor model): check that each module has a CE mark and a DoC, and keep copies.
- **CRA (EU) 2024/2847:** vulnerability-reporting duties from 11 Sep 2026 and full obligations from **11 Dec 2027**, including a declared security-support period, an SBOM and an update process [knowledge; dates per the Espressif CRA blog above]. Decide by Q3 2027 whether to comply or stop placing new units.
- **GPSR:** type, batch number and manufacturer name and address on the product; Czech instructions and warnings; the same data in the online listing; a complaints register.
- **WEEE (542/2020 Sb.):** in Stage 2, register as a producer through a collective scheme *before* the first sale, mark the crossed-out bin, and publish take-back information. The kit stage buys from a CZ distributor, which is the producer. **No battery in the design**, so no battery EPR.
- **Packaging:** keep EKO-KOM records; the business stays under the ~300 kg relief.
- **Consumer law:** 24-month warranty (new goods), 14-day withdrawal right, the withdrawal button from 19 Jun 2026, and the ČOI ADR clause.
- **IP / licences:**
  - ESPHome's C++ runtime is GPLv3, so publish the firmware config and source [knowledge].
  - Don't use the "ESPHome" name as a brand without the "Made for ESPHome" program [knowledge].
  - Mention ČEZ, EG.D and PRE only descriptively ("kompatibilní s…"), with no logos.
- **Not relevant:** hallmarking and the margin scheme.

---

## 12. Risks and mitigations

| Risk | Likelihood | Mitigation |
|---|---|---|
| Niche too small (scorers A, B and C) | High | The Stage 1 pre-sale is the test. Add Loxone and standalone web-UI/MQTT users to widen the niche. |
| Pillar-box meters with no socket or Wi-Fi (B, C) | Medium–high | Long-Line SKU: the RS485 cable runs to the house. The guide covers conduit (chránička) routing. Measure the share among beta buyers. |
| PV owners already get data from the inverter (B, C) | High | Sell billing-grade four-quadrant values, the HDO/relay state and non-PV heat-pump households; don't pitch surplus control alone. |
| Clones on Bazoš or from a CZ maker (B) | High | Speed, documentation and support; accept 12–24 months of durability. The open firmware makes clones inevitable. |
| Compliance cost vs. volume (A, C) | Medium | Stay on the kit model until ≥ 15/month for 2 months; take the lean CE route; design out the EN 18031 restricted clauses. |
| A distributor ships its own device (EG.D EVA) or enables encryption | Low–medium | ESPHome supports keys. Watch EVA news. |
| PRE activation and EG.D unsealing friction slows sales | Medium | Email templates in the guide. Lead with ČEZ, the largest base with no notification needed. |
| CRA from Dec 2027 | Certain | Plan a support period, or exit or transfer the design by then. |

---

## 13. Kill criteria
- **Day 30:** < 25 interest sign-ups from forum and FB posts, **or** < 3 of 8 beta units reading correctly → stop, with ~€350 lost.
- **Day 60:** < 12 paid kits cumulative, **or** returns or failures > 10% → stop and sell the remaining stock at cost.
- **Day 90:** run-rate < 12 paid/month → **no Stage 2**; keep kits as a hobby or exit. 12–14/month → hold on kits for another 60 days. ≥ 15/month for 2 consecutive months → Stage 2.

---

## 14. 12-week launch plan
1. Register the živnost online. Order 3 candidate boards, a USB-RS485 dongle and RJ12 tools. Post an interest thread on homeassistant-cz.cz asking for beta testers per meter type.
2. Write ESPHome configs for XT211, AM175, ST402D and E450. Bench-replay the DLMS frames published in the GitHub repos. Build the web-installer page on GitHub Pages.
3. Ship 8 beta kits (3 ČEZ, 3 EG.D, 2 PRE). Draft the Czech guide, including the PRE activation email and EG.D unsealing.
4. Collect beta results and fix issues. Open a reservation form showing both prices (1,190 kit / 1,390 preflashed).
5. Open paid kit sales (Shoptet trial or bank transfer + Zásilkovna). Order 20 kits.
6. Publish a forum tutorial and FB group posts, and pitch a root.cz or MyPower write-up. Track conversions.
7. Day-45 checkpoint against the Stage 1 pass/fail rule.
8. If passed, start the KiCad design with the EN 18031 choices: unique enforced credentials, no open AP, authenticated OTA.
9. Order a JLCPCB prototype (5–10 pcs). Get pre-scan quotes from 2 CZ EMC labs and quotes from WEEE schemes.
10. Test the prototypes on the beta meters and a 20 m Long-Line setup.
11. Run the EMC pre-scan. Write the technical file, the EN 18031 self-assessment (Espressif tool), the GPSR risk analysis and the DoC.
12. Day-90 decision. If ≥ 15/month for 2 months, join WEEE and order 100 PCBA after the pre-scan passes; otherwise stay on kits or stop.

---

## 15. Critical claims to verify (ready-to-run searches)
1. `"HAN" čtečka elektroměru ESP32 hotová prodej Kč ČEZ EG.D PRE e-shop 2026` (does a packaged CZ reader already exist?)
2. `LaskaKit OR Pájeníčko OR HWKitchen HAN elektroměr RS485 DLMS modul` (is a CZ maker about to clone or already selling?)
3. `Home Assistant analytics installations by country Czech Republic 2026` (is the buyer pool really 20–30k installs?)
4. `EG.D EVA aplikace senzor gateway ostrý provoz 2026 zákazníci` (will a distributor give a device away?)
5. `ČEZ WM-RelayBox HAN RJ12 přístupný zaplombovaný pilíř elektroměr zásuvka` (can customers physically reach and power it?)
6. `PREdistribuce aktivace HAN rozhraní výměna krytu poplatek lhůta` (how much does PRE's activation friction cost the buyer?)
