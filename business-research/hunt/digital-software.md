# Hunter: digital-software (software sold as a product, not a service)

Date: 2026-09-29. Lens: micro-SaaS, e-shop platform add-ons (Shoptet/Upgates/Woo/Shopify), HA integrations and hardware kits, game mods and assets, and regulation-driven software gaps.

## How the evidence was gathered (read this first)
- **Tool limits.** The swarm's shared WebSearch budget (200 calls) ran out after about 20 of my searches. WebFetch was blocked by the egress proxy for almost every site I tried: doplnky.shoptet.cz, blog.shoptet.cz, eshopradar.cz, apps.shopify.com, wordpress.org, tebex.io, tindie.com, bazos.cz, flightsim.to, simmarket.com, cezdistribuce.cz, homeassistant-cz.cz, community.home-assistant.io, chromewebstore, wikipedia. Only GitHub and raw.githubusercontent.com were reachable.
- **Primary dataset used.** A public GitHub research repo holds a crawl of the Shoptet and Upgates add-on marketplaces, fetched on 2026-08-21 and 2026-09-01: 394 Shoptet listings and 215 Upgates listings, with rating counts, rating averages, price notes and vendor URLs. The file is https://github.com/mchlkucera/localproblems/blob/main/data/lookup/cz-eshop-addons.jsonl and the crawler is `scripts/fetch_shoptet.sh` in the same repo. All Shoptet rating counts and prices below come from that snapshot. I analysed it but could not re-check it live. **Shoptet does not publish install counts** (per the crawler's notes). I use rating count as a *lower-bound proxy* for paying customers. That assumes only shops that installed an add-on can rate it, which is plausible but unverified.
- A Shoptet add-on *rating* is not a *sale*. Every "installs" or "revenue" figure derived from ratings is labelled **estimate**.
- FX used: **1 € ≈ 25 CZK** (rounded).

### Shared context: the Shoptet add-on channel (applies to candidates 2–5)
- **Shoptet merchant count.** Shoptet reports about 41,000 e-shops in CZ, SK and HU, up about 4,000 year on year. One 2026 guide claims 45,000+. Shoptet's own 2025 revenue was reported as 900M CZK (+25%). Sources are search snippets: https://cc.cz/shoptet-nasel-klic-jak-rychle-rust-i-na-rozebranem-e-commerce-trhu-loni-utrzil-temer-800-milionu/, https://forbes.cz/shoptetu-se-loni-darilo-hlasi-rekordnich-781-milionu-na-trzbach/ and https://www.shopins.cz/blog/shoptet-moduly-pruvodce-2026.
- **Marketplace size.** The sitemap listed 404 add-on pages and 179 vendor pages on 2026-08-21 (crawler notes). Add-ons are paid inside Shoptet, and the search snippet at https://www.sniperdesign.cz/slovnik/shoptet-marketplace says marketplace add-ons are "the only ones with API access on standard rates". Shoptet's marketplace team says new partner add-on proposals arrive "in the lower tens per month" (search snippet, https://blog.shoptet.cz/rozhovor-marketplace-tym/).
- **Pricing norms in the snapshot.** Of the monthly-priced Shoptet add-ons (n=142), the median price is **100 CZK/month** and the median rating count is 8. Of the one-time add-ons excluding templates (n=51), the median price is **290 CZK** and the median rating count is 11. Shoptet's own paid add-ons sit at 100–400 CZK/month.
- **Solo developers win here.** Evidence from the snapshot:
  - jakubtursky.sk: 18 listings, 482 ratings in total.
  - dmartini.cz: 9 listings, 202 ratings.
  - paxio.cz: 10 listings, 201 ratings.
  - honzabartos.cz: one add-on with 88 ratings.
  - "Pohoda by Dominik Prajzler": 36 ratings at 300 CZK/month, plus an optional 18,000 CZK setup.
- **Unknown.** The commission Shoptet takes from partners could not be verified. The models below **assume 20%**. Confirm this in the partner agreement before committing.
- **Build stack.** Shoptet publishes add-on tooling (https://github.com/shoptet/shoptet-bender), and community Laravel skeletons exist (https://github.com/pajaeu/shoptet-addon-skeleton). The work is PHP/JS plus a small hosted backend (OAuth install and webhooks), which is feasible with AI assistance for a non-senior developer. Support is in Czech or Slovak, B2B, over e-mail.

---

### 1. "HAN reader CZ": plug-and-play smart-meter reader for Czech AMM meters (ESP32 + ESPHome, Home Assistant ready)
- **What you sell / type:** Hybrid (a physical kit plus firmware). The device is:
  - an ESP32-C3 with an isolated RS485 transceiver in a small enclosure;
  - an RJ12 cable for the meter's HAN port;
  - a 5 V USB PSU;
  - preflashed ESPHome that uses the official `dlms_meter` component, which lists the **Sagemcom XT211** (the ČEZ meter) as tested.

  It works with Home Assistant out of the box (auto-discovery) and has a Czech manual with configs for ČEZ, EG.D and PRE. Planned variants are Wi-Fi now, and later a long-cable RS485 or LoRa pair for outdoor meter boxes (pilíř).
- **Buyer & channel:**
  - Czech homeowners with PV, heat pumps or EV chargers who now have a smart meter. They want real-time grid import/export for surplus automation and spot-price tariffs.
  - Channels: own small Shoptet or Upgates shop, homeassistant-cz.cz, Czech PV and HA Facebook groups, Heureka, and later Etsy/Tindie for the SK/HU/PL variants.
- **Price (€):** 1,290–1,490 CZK (≈ €52–60) for the Wi-Fi unit. The LoRa or long-cable variant would be about 2,190 CZK (≈ €88). Both are estimates, since I found no CZ competitor price to anchor against.
- **Unit economics (all figures are estimates from typical LCSC/AliExpress component prices, not verified this session):**
  - BOM: ESP32-C3 board ~€3–4, RS485 module ~€1–2, RJ12 cable ~€1.5, printed enclosure ~€1, CE-marked USB PSU ~€3–4, box and printed manual ~€1.5. Total **≈ €11–14**.
  - Payment fee about 1.5%. Shipping via Zásilkovna is charged to the buyer.
  - Returns reserve for the 14-day withdrawal right: about 5% of revenue.
  - Labour: flash, test and pack takes about 20–30 min per unit.
  - **Net ≈ €33–40 per unit** before the founder's time and income tax. No VAT is charged while under the 2M CZK VAT threshold.
- **Demand evidence:**
  - **Regulation-forced installed base.** Vyhláška 359/2020 Sb. requires the rollout of smart meters (AMM) for customers using more than 6 MWh/year, among others, from July 2024 to 1 July 2027. The target is **about 850,000 metering points by mid-2027**. EG.D alone plans to replace meters at about 560,000 points. Sources: https://www.zakonyprolidi.cz/cs/2020-359, https://mpo.gov.cz/assets/cz/energetika/strategicke-a-koncepcni-dokumenty/narodni-akcni-plan-pro-chytre-site/2021/1/Prezentace-MPO-vyhlaska-o-mereni-elektriny.pdf and https://www.egd.cz/clanek/od-pristiho-leta-musi-distributori-zacit-s-instalaci-chytrych-elektromeru.
  - **The port is meant for customers.** ČEZ Distribuce says the HAN interface (RS485, DLMS/COSEM) is prescribed for AMM meters in categories C1–C3, and that **using HAN needs no notification to ČEZ**, unlike the other interfaces (search snippet of https://www.cezdistribuce.cz/cs/pro-zakazniky/potrebuji-vyresit/elektromery-a-odecty/komunikacni-rozhrani-z-elektromeru).
  - **The data is unencrypted and pushed every ~60 s.** For the XT211, the HAN port sits on the WM-RelayBox, is an isolated RJ12 at 9600 bps, and has no key mentioned (https://github.com/Tomer27cz/xt211 and https://github.com/nero150/CEZ_rele_box). EG.D meters (ZPA AM175, Meter&Control ST402D, Sagemcom XT211) push on HAN at 9600 baud (https://github.com/blesk89/ha-addon-egd-dlms). The ESPHome docs list XT211 as tested and say most standard meters need no key (https://github.com/esphome/esphome.io/blob/current/src/content/docs/components/sensor/dlms_meter.mdx).
  - **DIY demand is visible.** At least five Czech open-source projects appeared in 2025–26, created by people who could not buy a ready device:
    - Tomer27cz/xt211 (created 2025-11);
    - psopso/esp32_xt211_mqtt_lora (2026-04);
    - blesk89/ha-addon-egd-dlms;
    - lhubac/egd-dlms;
    - nero150/CEZ_rele_box.

    Multi-page Czech forum threads show the same interest: "Data z elektroměru přes ESP" (https://www.homeassistant-cz.cz/viewtopic.php?p=26369), the ČEZ PND integration thread with 5+ pages (https://www.homeassistant-cz.cz/viewtopic.php?t=1237), and https://www.vodnici.net/community/technologicke-vybaveni-domu/vycitani-dat-z-han-portu-elektromeru/.
  - **Paying demand in analogous markets.** In Norway, amsleser.no sells ready HAN readers for the amsreader firmware (465★ on GitHub; the README says "have a look at our shop at amsleser.no", https://github.com/UtilitechAS/amsreader-firmware). In the Netherlands, Zuidwijk's commercial SlimmeLezer is recommended over DIY (https://github.com/mweimerskirch/smarty_dsmr_proxy), and a Hungarian adaptation of SlimmeLezer for E.ON meters exists (https://github.com/amargo/slimmelezer-eon). **I have no unit sales numbers for any of these.**
- **Supply gap / asymmetry evidence:**
  - Every Czech project I found is DIY-only, with no mention of selling devices (READMEs above).
  - The current alternatives are USB-RS485 dongles wired by hand, RS485-TCP gateways (PUSR USR-DR134) or CT-clamp meters such as Shelly, which need an electrician inside the switchboard.
  - **Not verified:** I could not scan bazos.cz, Heureka or Alza for an existing Czech ready-made HAN reader because they were egress-blocked. This is the first check to make.
- **Edge for a CZ-based solo founder:**
  - Czech language and knowledge of each distributor (ČEZ, EG.D and PRE differ in meter models and relay boxes).
  - Local shipping via Zásilkovna within 1–2 days.
  - Ability to test on real Czech meters.
  - Firmware is already solved upstream (the ESPHome `dlms_meter` component), so the product is integration, packaging and documentation, not R&D.
- **Startup cost (€) & hours/week:**
  - About **€1,500–3,500 in total**: prototypes ~€100, a first batch of 50 units ~€700, a 3D printer if none is owned ~€400, an optional EMC pre-scan at a lab ~€500–1,500, WEEE collective-scheme membership, and a simple e-shop. All figures are estimates.
  - Time: about 10 h/week for 2 months to productise, then 3–6 h/week for fulfilment and support.
- **Realistic monthly profit after 12 months (all estimates):**
  - Pessimistic: 5 units/month ≈ **€150**.
  - Realistic: 25 units/month ≈ **€850**.
  - Optimistic: 80 units/month across CZ, SK and HU variants ≈ **€2,800**, which would need about 40 h/month of assembly or outsourced PCBA.
- **CZ/EU legal/regulatory notes:**
  - The founder becomes the *manufacturer*: CE under RED 2014/53/EU (use a pre-certified ESP32 module), EMC, and RoHS.
  - Since 1 Aug 2025 the RED cybersecurity delegated act (EU) 2022/30 applies to internet-connected radio devices, via EN 18031-1. That means no default passwords and a way to update firmware (https://eur-lex.europa.eu/eli/reg_del/2022/30/oj). This is stated from prior knowledge and was not re-fetched.
  - Register as an electrical-equipment producer and join a collective take-back scheme under zákon 542/2020 Sb.
  - GPSR product-safety information and a manufacturer address on the product.
  - Ship a CE-marked PSU and do not make the device mains-powered, which avoids LVD work.
  - ESPHome's C++ runtime is GPL-licensed, so publish the firmware config and source. This is normal for "Made for ESPHome" products; verify it.
  - Trading licence: volná živnost (výroba, obchod a služby).
- **Key risks:**
  - Many meters sit in outdoor boxes (pilíř) with no socket and weak Wi-Fi. The existence of psopso's LoRa project hints at this, and it may force a pricier two-part variant.
  - Distributors could change the HAN configuration or start encrypting (Austria does).
  - A Czech seller may already exist (unverified).
  - Shelly and other brands could add HAN support.
  - Hardware returns and CE paperwork.
  - The buyer pool is the HA/DIY niche, not all 850k meters.
- **Confidence: 3/5.** The regulation-driven installed base, the unencrypted and no-notification port, the free upstream firmware and the paying analogs in NO/NL/HU are all solid. The CZ competitor scan and direct paying-demand numbers are missing because of tool limits.

### 2. "Dárky a množstevní slevy+": better promo mechanics add-on for Shoptet (gift-with-purchase, tiered/quantity discounts, X+Y, free-gift progress bar)
- **What you sell / type:** Digital, a Shoptet marketplace add-on on a monthly subscription. One admin screen for gift tiers by cart value, quantity-break pricing display, 1+1 and 2+1 rules, and a cart progress bar ("do dárku zbývá 230 Kč").
- **Buyer & channel:** Small and mid Shoptet merchants in CZ, SK and HU, sold through doplnky.shoptet.cz with its 30-day free trial and "doplněk" category placement.
- **Price (€):** 290 CZK/month (≈ €11.6), or 3,190 CZK/year.
- **Unit economics:** 290 CZK, minus the assumed 20% Shoptet commission (unverified), gives 232 CZK. Hosting runs about €10–20/month across all shops. **Net ≈ €9 per shop per month.** No VAT is charged under the threshold.
- **Demand evidence (snapshot of 2026-08-21, https://github.com/mchlkucera/localproblems/blob/main/data/lookup/cz-eshop-addons.jsonl):**
  - Shoptet's own *paid* promo add-ons have many raters:
    - "Dárky k objednávce a produktům": **49 ratings**, 100 CZK/month (https://doplnky.shoptet.cz/darky-k-objednavce-a-produktum).
    - "Množstevní slevy": **41 ratings**, 100 CZK/month (https://doplnky.shoptet.cz/mnozstevni-slevy).
    - "Slevy X+Y": 17 ratings, 300 CZK/month (https://doplnky.shoptet.cz/slevy-x-y).
    - "Slevové kupóny": 58 ratings, 200 CZK/month.
  - Third-party cart add-ons prove that merchants pay outsiders for AOV tools:
    - "Upsell a cross sell" (honzabartos.cz): **88 ratings, 5.0** (https://doplnky.shoptet.cz/upsell-a-cross-sell).
    - "Doplňkový prodej v košíku" (iGlass/fv-studio): **69 ratings**, 200 CZK/month (https://doplnky.shoptet.cz/doplnkovy-prodej-v-kosiku).
- **Supply gap / asymmetry evidence:** The native promo add-ons are **the worst-rated high-volume listings in the marketplace**: Dárky averages **3.0**, Množstevní slevy **3.2** and Slevy X+Y **3.2**. Merchants pay for them but are unhappy with them. The only third-party gift add-on, "Rozbalené dárky v košíku", has 16 ratings and a 3.9 average at 490 CZK one-time. No third-party quantity-discount or X+Y add-on appears among the 394 Shoptet listings.
- **Edge for a CZ-based solo founder:** Czech-language support and marketplace listing, the local platform, and knowledge of Czech promo habits (dárek k objednávce is a very Czech convention). Global Shopify promo-app companies are not on Shoptet.
- **Startup cost (€) & hours/week:** About €200–500 (hosting, domain, trade licence, a test shop). Estimate 100–150 hours to build, i.e. 2–3 months at 12 h/week, then 2–4 h/week for support and Shoptet template-change fixes.
- **Realistic monthly profit after 12 months:** Estimate, assuming rating counts understate paying shops and benchmarking against incumbents with 41–88 ratings:
  - Pessimistic: 10 shops ≈ **€80**.
  - Realistic: 50 shops ≈ **€450**.
  - Optimistic: 150 shops ≈ **€1,350**.
- **CZ/EU legal/regulatory notes:**
  - Displayed discounts must respect the 30-day lowest-price rule (Omnibus, zákon 634/1992 Sb.). Build that in as a feature.
  - GDPR processing is minimal (cart data only).
  - B2B sale; the trade licence covers it.
- **Key risks:**
  - **Technical feasibility is the #1 unknown.** I have not confirmed whether a third-party add-on can alter cart prices through the Shoptet API or JS. Incumbents show partial ability: the upsell add-on applies "různé výše slev u doplňkových produktů". Verify with Shoptet partner documentation before building.
  - Platform risk: Shoptet can improve its native add-ons at any time.
  - Low ticket size.
- **Confidence: 3/5.** Paying demand plus visible dissatisfaction is well evidenced. Feasibility and the commission rate are unverified.

### 3. Shoptet ↔ iDoklad (then Vyfakturuj) invoice and order sync add-on
- **What you sell / type:** Digital, a Shoptet add-on subscription. It pushes paid orders to iDoklad as invoices and credit notes, syncs payment status back, and maps VAT rates, OSS and currencies.
- **Buyer & channel:** Small Shoptet merchants (OSVČ and small s.r.o.) who keep their books in iDoklad or Vyfakturuj. Sold on doplnky.shoptet.cz; later co-marketed with iDoklad's and Vyfakturuj's integration pages.
- **Price (€):** 250–300 CZK/month (≈ €10–12), plus optional paid onboarding of about 1,500 CZK. The incumbent Pohoda connector charges 300 CZK/month plus 18,000 CZK for expert setup.
- **Unit economics:** 300 CZK, minus the assumed 20% commission, gives 240 CZK. **Net ≈ €9 per shop per month.** API costs are none known; iDoklad has a public API (not re-verified). Hosting €10–20/month in total.
- **Demand evidence (snapshot):** Accounting connectors are a proven *paid, sticky* category on Shoptet:
  - "Pohoda by Dominik Prajzler" (a solo developer): **36 ratings, 5.0, 300 CZK/month + 18,000 CZK optional setup**.
  - Napojse "Napojení na účetnictví MS3": 15 ratings, **400 CZK/month** (https://doplnky.shoptet.cz/money-s3).
  - SuperFaktura: 15 ratings, 100 CZK/month (https://doplnky.shoptet.cz/superfaktura).
  - "Fakturoid by Kulhánek": 7 ratings, 300 CZK/month (https://doplnky.shoptet.cz/fakturoid-by-kulhanek).
  - Shoptet's own Pohoda add-on: 9 ratings, 3.2 average, 200 CZK/month.
- **Supply gap / asymmetry evidence:** In the 394-listing Shoptet snapshot, **no iDoklad or Vyfakturuj.cz connector exists**. Both exist on the smaller Upgates marketplace, built by Trexify s.r.o., which shows a vendor already sells them on a rival platform. Existing Money S3 options are weak: Seyfor's own "Money S3 by Seyfor" is rated **1.0**. Second target: a better Money S3 connector.
- **Edge for a CZ-based solo founder:** Czech accounting and VAT specifics (DPH, kontrolní hlášení fields, OSS, rounding, ISDOC export) are a moat against foreign developers. Czech-language support also matters for a B2B accounting tool.
- **Startup cost (€) & hours/week:** About €200–500. Estimate 120–200 hours to build, because the invoice edge cases are long-tail. Afterwards 3–5 h/week of support, which is *heavier* than candidate 2 because accounting errors are urgent for customers.
- **Realistic monthly profit after 12 months (estimates):**
  - Pessimistic: 8 shops ≈ **€70**.
  - Realistic: 40 shops ≈ **€350**.
  - Optimistic: 120 shops, adding Money S3 ≈ **€1,100**.
- **CZ/EU legal/regulatory notes:**
  - The founder becomes a GDPR *processor* of customer invoice data, so a DPA (zpracovatelská smlouva) template is needed.
  - Not accounting advice; include clear disclaimers.
  - No licence required.
- **Key risks:**
  - **Unverified:** iDoklad (or Shoptet) may already offer a native import outside the marketplace. Check the iDoklad integrations page and search the Shoptet marketplace before building.
  - The support load is higher than for front-end add-ons.
  - Trexify could port its Upgates connectors to Shoptet.
  - iDoklad API changes.
- **Confidence: 3/5.** The category's paying demand is evidenced and the gap is visible in the snapshot. Whether iDoklad users on Shoptet are numerous enough is not verified.

### 4. "B2B objednávky+": wholesale ordering toolkit for Shoptet
- **What you sell / type:** Digital, a Shoptet add-on subscription layered on Shoptet's customer groups. Features:
  - prices hidden until login, per group;
  - minimum order quantity and order-in-multiples;
  - a quick-order grid or CSV re-order for B2B customers;
  - "request a quote" instead of the cart, with PDF quotes.
- **Buyer & channel:** Shoptet merchants who also sell wholesale (manufacturers, distributors, craft producers), sold on doplnky.shoptet.cz.
- **Price (€):** 390 CZK/month (≈ €15.6).
- **Unit economics:** 390 CZK, minus the assumed 20% commission, gives 312 CZK. **Net ≈ €12 per shop per month.**
- **Demand evidence (snapshot):** Merchants already buy these features piecemeal:
  - Shoptet "Velkoobchod": **19 ratings at 400 CZK/month** (https://doplnky.shoptet.cz/velkoobchod).
  - "Cena po přihlášení" (jakubtursky.sk): 18 ratings, 490 CZK one-time (https://doplnky.shoptet.cz/cena-po-prihlaseni).
  - "Objednávání po násobcích" (dmartini.cz): 13 ratings, 50 CZK/month (https://doplnky.shoptet.cz/objednavani-po-nasobcich).
  - "Cena na dotaz": 8 ratings, 100 CZK/month.
  - Techka's "Cena produktu na dotaz": 200 CZK/month.
  - "Tisk cenové nabídky" (Ryvenia): 100 CZK/month.
- **Supply gap / asymmetry evidence:** The native wholesale add-on is poorly rated (**3.2 average**), and the rest of the B2B job is split across 5+ micro add-ons from different vendors. "Tisk cenové nabídky" has a single 1.0 rating. No bundled B2B suite exists in the snapshot.
- **Edge for a CZ-based solo founder:** Czech and Slovak B2B conventions (IČO/DIČ, ARES lookup, proforma invoices). Local language.
- **Startup cost (€) & hours/week:** About €200–500. Estimate 120–180 hours to build, then 2–4 h/week.
- **Realistic monthly profit after 12 months (estimates):**
  - Pessimistic: 5 shops ≈ **€60**.
  - Realistic: 25 shops ≈ **€300**.
  - Optimistic: 80 shops ≈ **€1,000**.
- **CZ/EU legal/regulatory notes:** B2B only, so the consumer rules and withdrawal button do not apply to the B2B flow. GDPR processing is minor.
- **Key risks:**
  - A smaller buyer pool than candidate 2 (only merchants with a wholesale side).
  - It depends on Shoptet's customer-group API.
  - Shoptet could upgrade Velkoobchod.
- **Confidence: 2/5.** The piecemeal paying demand is real, but each piece has small rating counts and the combined-suite premium is untested.

### 5. "Hlídací pes+": back-in-stock and price-drop alerts for Shoptet (e-mail and SMS, with merchant demand analytics)
- **What you sell / type:** Digital, a Shoptet add-on subscription. It covers customer sign-ups for restock and price-drop alerts, automatic e-mails (optional SMS through a Czech gateway), and a "most-wanted out-of-stock products" report for purchasing.
- **Buyer & channel:** Shoptet merchants with frequent stock-outs (fashion, cosmetics, hobby, spare parts), sold on doplnky.shoptet.cz.
- **Price (€):** 190 CZK/month (≈ €7.6); SMS passed through at cost plus margin.
- **Unit economics:** 190 CZK, minus the assumed 20% commission, gives 152 CZK. **Net ≈ €5.5 per shop per month** after e-mail sending costs (Amazon SES-type pricing, pennies).
- **Demand evidence (snapshot):** Shoptet's native "Hlídací pes" has **24 ratings at 100 CZK/month** (https://doplnky.shoptet.cz/hlidaci-pes). "Opuštěný košík" (the native abandoned cart add-on, a related retention tool) has 15 ratings at 200 CZK/month. On Shopify, back-in-stock apps are a large category. That is prior knowledge and was not re-verified this session.
- **Supply gap / asymmetry evidence:** The native add-on averages **3.7**. The only third-party stock add-on (Napojse "Hlídání skladu", 2 ratings) is merchant-side stock monitoring, not customer alerts. The snapshot shows no third-party customer-alert add-on.
- **Edge for a CZ-based solo founder:** Czech copy and SMS gateways (e.g., Czech providers), and local support.
- **Startup cost (€) & hours/week:** About €200–400. Estimate 60–100 hours to build (the simplest candidate here), then 1–3 h/week.
- **Realistic monthly profit after 12 months (estimates):**
  - Pessimistic: 10 shops ≈ **€50**.
  - Realistic: 40 shops ≈ **€220**.
  - Optimistic: 120 shops ≈ **€650**.
- **CZ/EU legal/regulatory notes:** The add-on stores shoppers' e-mails and phone numbers for alerts, so the founder is a GDPR processor. It needs consent wording and a DPA. Alert e-mails are transactional, not marketing, which avoids zákon 480/2004 Sb. consent issues if worded correctly.
- **Key risks:**
  - Low ticket size.
  - Shoptet can fix its native watchdog.
  - E-mail marketing tools (Ecomail, SmartEmailing, Leadhub: 49, 23 and 86 ratings in the snapshot) may bundle back-in-stock flows.
- **Confidence: 2/5.** The demand is modest (24 ratings) but clear. Best treated as a second add-on after candidate 2, reusing the same codebase and customers.

---

## Rejected

1. **Slovak Peppol e-invoicing connector (mandate from 1 Jan 2027, Act 385/2025 Z.z.): price collapse and platform build-out.**
   - A comparison site already lists **34 invoicing systems** (https://www.epostari.sk/fakturacne-systemy/).
   - The access point Fakturix sells plans **from €0.99/month** with ready plugins for WooCommerce, PrestaShop, Shopify and Shoptet (https://fakturix.sk/).
   - Fakturovo is free (https://www.epostari.sk/digitalni-postari/fakturovo/), and Verteco charges from €2/month per IČO (https://peppol.verteco.digital/cennik).
   - Shoptet itself is piloting a Peppol connector, with plugins from July 2026 (search snippet, https://epostak.sk/blog/e-faktura-pre-eshopy).
   - Becoming a Peppol access point is not solo-feasible.
2. **German XRechnung/ZUGFeRD e-invoice app or plugin (B2B issuing duty 2027/2028): saturated, including free options.**
   - Shopify already has Clever Invoice, InvoPass, E-Docs, Sufio and a **free** "E-Rechnung" app (https://apps.shopify.com/e-invoice-1, https://apps.shopify.com/invopass, https://apps.shopify.com/e-rechnung).
   - WooCommerce has Germanized Pro, weLaunch, E-Invoicing for WooCommerce and **free** RechnungsPilot (https://moduldeck.de/, https://www.welaunch.io/en/knowledge-base/faq/woocommerce-xrechnung-zugferd-factur-x-integration/).
   - No CZ edge.
3. **Polish KSeF plugin (mandatory Feb/Apr 2026): free and native incumbents.**
   - There is a **free** KSeF integration for WooCommerce (https://www.wpdesk.pl/blog/krajowy-system-e-faktur-ksef-dla-woocommerce/).
   - Shoper, IdoSell and Sky-Shop implemented KSeF natively (https://kluczesoft.pl/ksef-a-sklep-internetowy-allegro-shopify-prestashop-integracja-2026.htm).
   - The window closed in April 2026.
4. **Shoptet regulatory-feature add-ons (GPSR fields; the "Odstoupit od smlouvy" withdrawal button under Act 159/2026 Sb., effective 1 Jan 2027): the platform and incumbents give them away.**
   - Shoptet added GPSR manufacturer-contact fields natively (search snippets, https://blog.shoptet.cz/gpsr-e-shopy/ and https://blog.shoptet.cz/shoptet-novinky-jaro-2025/).
   - For the withdrawal button, Shoptet provides a native order-detail withdrawal page (https://podpora.shoptet.cz/nova-pravidla-odstoupeni-od-smlouvy-od-roku-2026/).
   - Retino, used by 2,000+ e-shops, offers the button **free** on the Shoptet store (https://doplnky.shoptet.cz/retino, as analysed in https://github.com/mchlkucera/localproblems/blob/main/data/problems/cz/p-0028-eshop-consumer-law-compliance.md).
   - Regulation-forced demand exists, but nothing is left to charge for.
5. **ČOI legal-compliance scanner or legal-texts add-on for e-shops: weak willingness to pay.**
   - Enforcement is real: ČOI found violations in 639 of 751 inspected e-shops in 2025, with ~13M CZK in fines (https://www.sos-msk.cz/z-751-kontrol-e-shopu-porusilo-zakon-85-z-nich-padly-pokuty-za-temer-13-milionu-korun/).
   - Yet the paid compliance add-ons have tiny traction: "Hlídač Slev" has **5 ratings (3.4)** and "Slevy správně" **4 ratings (4.0)**, against 40–90 for sales-lifting add-ons.
   - The register that analysed the idea scored it money 1/5 and gap 1/5: "most shops live with the risk of a fine rather than pay to remove it" (same p-0028 file).
6. **EAA accessibility widget or audit add-on for CZ e-shops: no enforcement pull.**
   - Zákon 424/2023 Sb. has applied since 28 Jun 2025, but micro-enterprises are exempt.
   - **ČOI's 2026 market-surveillance plan contains no accessibility project**, and no fines were found.
   - Global overlay incumbents (accessiBe, AudioEye) already own the "widget" answer.
   - Source: https://github.com/mchlkucera/localproblems/blob/main/data/problems/cz/p-0020-eshop-accessibility-enforcement.md, citing https://coi.gov.cz/pro-podnikatele/pristupnost-vyrobku-a-sluzeb-pro-podnikatele/.
   - (Prior knowledge, not re-verified: the US FTC's 2025 order against accessiBe damaged the overlay category's credibility.)
7. **Shoptet premium templates and cosmetic one-time micro add-ons: winner-take-most and low ticket.**
   - Templates: "Šablona Apollo" (4,990 CZK) holds **281 of the 407 template ratings (69%)**. The 11 templates from techka average about 5 ratings each. Templates also carry heavy support, because merchants want customisation.
   - Cosmetic add-ons (back-to-top arrow, sticky header, "show full description") sell for 150–390 CZK *one-time*. At 41 ratings × 190 CZK, "Back to Top šipka" implies a lower bound of only about 7,800 CZK lifetime gross.
   - Three solo developers (jakubtursky.sk, paxio.cz, dmartini.cz) already cover this shelf.
   - Source: snapshot analysis of cz-eshop-addons.jsonl.
8. **FiveM/RedM scripts on Tebex: saturated with scaled studios, heavy support, unverifiable economics.**
   - Incumbents are large: RTX Development claims "10,000+ servers" and 500+ five-star reviews (https://rtx.tebex.io/), and JG Scripts is a Tebex Top Partner (https://www.tebex.io/resources/tebex-creator-spotlight-jg-scripts-2).
   - Tebex publishes no per-creator revenue, and my searches found none (https://fivemx.com/blog/tebex-alternatives-fivem-2026).
   - Buyers expect Discord support across ESX, QBCore and QBox frameworks.
   - Script leaking is endemic, and the platform (Cfx.re) is owned by Rockstar/Take-Two.
   - It requires Lua plus NUI (JS) skill, and there is no CZ edge.

**Not assessed because of tool limits (no verdict):** MSFS/X-Plane Czech scenery and liveries, Roblox UGC, Unity/Fab asset packs, Figma plugins, Chrome extensions (for example Vinted seller tools), Excel add-ins and Farming Simulator mods. I gathered no paying-demand data for these. Another pass with web access is needed before anyone scores them.
