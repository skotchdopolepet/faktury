# HUNTER "parts-b2b": obsolete spare parts and B2B physical niches

## Method and evidence limits (read first)
- About 12 web searches ran before the **shared session WebSearch budget (200/200) ran out**. After that the tool refused all further queries.
- **Every WebFetch target was blocked by the egress proxy.** That covers ebay.de, ebay.co.uk, ebay.com, kleinanzeigen.de, bazos.cz, etsy.com, en.wikipedia.org, pcwelt.de, chef-mix.com, caffista.de, nivatechnik.de, lomazoma.com and ost2rad.com. reddit.com was also unreachable.
- As a result, **no eBay "sold" filters and no Kleinanzeigen or Bazoš pages could be read directly.** All facts below come from search-result snippets with their URLs.
- Every number without a URL is labelled **estimate** and shows its reasoning.
- A few rejections rely on background knowledge. Those are marked **"not re-verified this session"**.
- Overall confidence is therefore lower than the ideas may deserve. Each candidate lists the cheap validation step to run next.

### Structural finding for this whole lens
Obsolete-parts businesses are **long-tail**. One SKU typically sells tens of units per year, not per month. For example, a commodity TM31 motor coupling listing on eBay.de shows only 51 sold in total (see candidate 1).

- Profit comes from building **30–100 SKUs around one installed base**, not from one hero product.
- At 10–15 h/week that takes 9–18 months.
- The strongest pattern found is a **forced supply cut**: the OEM stops selling parts while a large installed base is still in use (Thermomix TM31).
- The weakest pattern is "cult vintage brand" parts (Jawa, Babetta, Lada). There, CZ/SK/DE incumbents already exploit the obvious CZ sourcing edge.

---

### 1. Thermomix TM31 end-of-support mechanism parts ("passend für TM31"): lid-lock gear/lever kit plus the parts nobody reproduces
- **What you sell / type (physical|digital|hybrid):** Physical. These are reverse-engineered internal mechanical parts that are no longer sold since Vorwerk ended TM31 parts sales:
  - lid-locking mechanism gears and levers
  - locking-arm parts
  - possibly the control-panel key overlay, which fails with "holes in buttons" and error Er23 (see caffista below)

  Internal gears are produced as SLS/MJF PA12 or in-house engineering-filament prints first, and moved to injection-moulded POM at a CZ moulder once a SKU proves demand. **Food-contact parts (seals, blades, bowl) are deliberately avoided.**
- **Buyer & channel:**
  - B2C: DE/AT/CH TM31 owners via eBay.de (primary), Amazon.de and Kleinanzeigen, later a small Shopify shop with German and Czech listings.
  - B2B: independent Thermomix repair shops that lost their Vorwerk parts source, sold as 5–10 packs. Named examples: caffista.de, planbreparatur.de (Kaarst/Neuss), meinmacher.com, service-center24.de, and repairers listed on kaputt.de.
- **Price (€):** €14.90–24.90 per gear/lever kit plus €4.90 shipping (**estimate**). The anchors:
  - Commodity TM31 parts sit at €7.69–10.99 on eBay.de.
  - Harder-to-get lock parts should command a premium over them.
  - The price of the one comparable "professional" TM5 lock-gear listing could not be read, because eBay was blocked.
- **Unit economics (cost, fees, net per unit):** All figures are **estimates** at a €19.90 item price plus €4.90 shipping (€24.80 gross).

  | Line | Amount | Basis |
  |---|---|---|
  | Part cost | €1.5–4 | SLS PA12 service at batches of 20–50, or ~€0.5 in-house |
  | Packaging and GPSR label | ~€0.5 | |
  | Shipping CZ→DE | ~€4–6 | Packeta or Česká pošta small parcel; rates not verified this session |
  | eBay.de fees | ~€3.0 | ~12% of total incl. shipping, plus a per-order fee |
  | Returns and defect allowance | ~€1 | |
  | **Net per unit** | **≈ €11–14** | before income tax |

  - No VAT is charged while the founder is a CZ non-VAT payer, and EU B2C distance sales stay under €10k/yr.
  - B2B packs sold to repairers run at a lower price but a higher basket, with a similar per-unit net.
- **Demand evidence (numbers + URLs):**
  - **Forced cut:** Vorwerk ended TM31 support in Dec 2024 and stopped selling individual parts from Jan 2025. Stock depends on the remaining inventory. Sources: https://www.pcwelt.de/article/2548531/supportende-bei-thermomix-tm31-was-tun-bei-defekten.html, https://www.pcwelt.de/article/2339688/thermomix-tm31-support-aus-faq-vorwerk.html, https://www.zaubertopf-club.de/artikel/keine-ersatzteile-tm31-thermomix.html, https://www.netzwelt.de/news/235081-achtung-diesen-thermomix-gibt-bald-keinen-support-mehr.html
  - **Which part fails:** a repairer calls the locking unit "one of the most common defects of all" ("einer der häufigsten Defekte überhaupt"): https://meinmacher.com/thermomix/blog/verriegelung-defekt-am-thermomix
  - Lid-mechanism gears and locks break when the lid is not detected, and the device then won't start or turn the blade (PC-Welt snippet above).
  - Control-panel holes cause error Er23: https://caffista.de/thermomix-blogs/bedienfeld-tauschen-er23-reparatur/
  - **Money changing hands:**
    - A TM31 motor coupling sells at €10.99 with volume tiers down to €7.69 and **51 sold**. This is one of the listings returned for the query, and the exact item ID could not be isolated because eBay is blocked. Candidates: https://www.ebay.de/itm/283637234408, https://ebay.de/itm/331947579452, https://www.ebay.de/itm/283514391658
    - The same part is also sold as EUROPART 10027093 for €10.49: https://www.ebay.de/p/1376985022
    - eBay.de runs a dedicated "Tm 31 Ersatzteile" browse node: https://www.ebay.de/b/Tm-31-Ersatzteile/20673/bn_7005483125
    - Used TM31 units trade actively on eBay.de, which means a live installed base and cheap donor units. Examples: https://www.ebay.de/itm/226962658749, https://www.ebay.de/itm/397194022347
  - **Installed-base size:** Vorwerk sells about 1.4–1.5M Thermomix units a year across all models (https://www.handelsblatt.com/unternehmen/handel-konsumgueter/vorwerk-verkauft-weniger-geraete-vom-thermomix-macht-aber-mehr-gewinn/100034597.html). No TM31-only figure was found. TM31 was sold 2004–2014 (https://www.zaubertopf.de/thermomix-tm31-tm5-tm6-unterschiede/), so it is safely a multi-million-unit installed base (**estimate**).
- **Supply gap / asymmetry evidence (numbers + URLs):**
  - **Commodity TM31 parts are already served:** couplings, measuring cups, blade covers and similar. Sellers include https://ersatzteil-check.de/product-category/kuche/kuechenmaschine/vorwerk-thermomix/thermomix-tm31/, https://chef-mix.com/produkt-kategorie/thermomix-tm31/, https://www.staubsaugerladen.de/geeignet-fuer-vorwerk-thermomix-tm31 and Europart. Do NOT compete there.
  - **The gap is in the lock-mechanism internals and the panel overlay.** No search result showed a third-party source for these, but that absence is **unverified**, because eBay listings couldn't be browsed.
  - Buyers are told to search eBay and Kleinanzeigen for used stock ("kompatible Alternativen sind jetzt besonders gefragt", per the pcwelt snippet). That is the classic supply-gap signal.
- **Edge for a CZ-based solo founder:**
  - Cheap CZ/CEE injection moulders and SLS services.
  - A non-VAT-payer price advantage below the thresholds.
  - Thermomix is also big in CZ/PL, which gives a local test market (not verified this session).
  - It is a precision-fit engineering job that casual 3D-print hobbyists do badly. A review snippet contrasted "professionally manufactured, precisely fitting" gears with "simple 3D prints" (search result for the TM5 gear, see candidate 2).
- **Startup cost (€) & hours/week:**
  - €900–1,800 (**estimate**):
    - 2 defective TM31 donor units: €50–150 each
    - FDM printer for engineering filament: ~€600, optional if SLS is outsourced
    - SLS prototypes: €100–200
    - First batches: €200–400
    - Packaging and labels: €50
    - DE packaging registration (LUCID plus a dual-system licence): ~€50–100/yr
  - An injection mould later costs €2–4k per SKU (**estimate**), and only once a SKU sells more than 30/month.
  - Hours: 10–15 h/week for the first 3 months (teardown, CAD, fit tests), then 4–6 h/week (packing, listings, new SKUs).
- **Realistic monthly profit after 12 months (pessimistic / realistic / optimistic, €):** €50 / €350 / €1,200 (**estimate**). The pessimistic case is ~5 units/mo; the realistic case is 25–35 units/mo across 5–8 SKUs at ~€12 net; the optimistic case adds B2B repairer packs and 100+ units/mo.
- **CZ/EU legal/regulatory notes:**
  - **Trademark:** use "passend für Vorwerk Thermomix TM31" only as a referential indication of purpose. This is allowed under Art. 14(1)(c) of Regulation (EU) 2017/1001 when honest. Use no logos and no "original".
  - **Design:** internal parts that are not visible in normal use are not protectable designs. The Design Directive (EU) 2024/2823 also adds a repair clause for visible parts.
  - **Patents:** TM31-era patents from about 2003–2004 are likely expired (20-year term; not verified).
  - **GPSR (EU) 2023/988**, applicable since 13 Dec 2024, requires manufacturer or importer identification, a product ID, safety information and a simple risk file.
  - **Food contact:** avoid parts that touch food. Otherwise Reg. (EC) 1935/2004 and a declaration of compliance apply.
  - DE VerpackG/LUCID registration is needed for B2C parcels.
  - Trade licence: volná živnost.
- **Key risks:**
  - The volume per SKU may be tiny (the coupling shows 51 sold).
  - Vorwerk legal pressure.
  - Donor-harvested used parts compete on price.
  - The installed base shrinks every year.
  - A fit or safety failure could lead to a liability claim, because a lid lock is a safety interlock. Mitigate with a strict fit test and clear instructions, and consider not selling interlock-critical parts.
- **Confidence (1–5) and why:** **3.** The OEM-forced supply cut is documented by several independent sources, the failure mode is repeatedly named by repairers, and money demonstrably changes hands for TM31 parts. However, the specific "nobody sells the lock internals" gap could not be confirmed on eBay (it was blocked). **Next validation (1 evening):** check eBay.de sold results for "TM31 Verriegelung" and "TM31 Zahnrad", and email 5 repairers asking which parts they cannot get.

### 2. Thermomix TM5 lock-drive gear ("C153" pinion or spur gear) in wear-resistant engineered plastic
- **What you sell / type (physical|digital|hybrid):** Physical. This is a single replacement gear for the TM5 lid-lock motor drive, which fails often (see evidence). It is sold as a gear alone rather than as the full lock assembly, in POM or PA-CF with a fitting guide.
- **Buyer & channel:** DE/FR/IT/ES/PL/CZ TM5 owners who don't want an expensive Vorwerk repair, plus independent repairers. Channels: eBay.de, Amazon.de and Kleinanzeigen.
- **Price (€):** €14.90–19.90 plus shipping (**estimate**). It must beat the existing pro seller, whose price could not be read.
- **Unit economics (cost, fees, net per unit):** Similar to candidate 1 (**estimate**). Part cost is €0.5–3 and net is about €9–12 per unit after eBay ~12%, shipping ~€4–6 and packaging.
- **Demand evidence (numbers + URLs):**
  - A professional seller lists this exact part, "Ritzel Zahnrad passend Vorwerk Thermomix TM 5 Motor Antrieb Verriegelung C 153": https://www.ebay.de/itm/405464852480
  - The same part appears on Kleinanzeigen: https://www.kleinanzeigen.de/s-anzeige/c153-vorwerk-motor-zahnrad-thermomix-tm-5-antrieb-verriegelung/2765860536-176-8836
  - A free STL for the same gear is on Cults3D, "Thermomix TM5 Stirnrad Zahnrad Verriegelung Motor Austausch Ersatzteil": https://cults3d.com/en/3d-model/home/thermomix-tm5-stirnrad-zahnrad-verriegelung-motor-austausch-ersatzteil
  - Three independent makers targeting one gear is a strong signal of a recurring failure. Sold counts could not be read.
- **Supply gap / asymmetry evidence (numbers + URLs):**
  - Supply is thin: 1 pro eBay seller, 1 Kleinanzeigen seller, and 1 free STL for owners who have printers.
  - Vorwerk presumably still services the TM5, which was sold 2014–2019, but it sells assemblies or repairs rather than the gear alone (not verified).
  - **The asymmetry is weaker than for the TM31**, because an established seller and a free STL already exist.
- **Edge for a CZ-based solo founder:** The same tooling, CAD workflow and shop as candidate 1, so this is an incremental SKU at near-zero extra fixed cost. A CZ moulder can make POM parts at a cost well below hobby 3D prints once volume justifies it.
- **Startup cost (€) & hours/week:** €150–400 on top of candidate 1 (a donor gear or unit plus prototypes, **estimate**). About 1–2 h/week once it is listed.
- **Realistic monthly profit after 12 months (pessimistic / realistic / optimistic, €):** €0 / €150 / €600 (**estimate**: 0, ~15 or ~60 units/mo at ~€10 net).
- **CZ/EU legal/regulatory notes:**
  - As candidate 1.
  - TM5 patents may still be in force, so run a quick Espacenet check on Vorwerk lid-lock patents before selling.
  - The gear is not visible, so it has no design protection.
- **Key risks:**
  - The existing seller has a head start and reviews.
  - The free STL caps the price.
  - Vorwerk could redesign the part or run a goodwill program.
  - Patent risk on a recent model.
- **Confidence (1–5) and why:** **2.** Recurring demand is proven by three independent suppliers, but supply already exists and neither prices nor sold counts could be read. The gear is only worth doing as an add-on SKU to candidate 1.

### 3. CZ-made new Jawa 350 / ČZ / Babetta reproduction parts listed on eBay.com, eBay.co.uk and eBay.de (marketplace arbitrage from CZ producers, plus own bundled kits)
- **What you sell / type (physical|digital|hybrid):** Physical. The offer has two parts:
  - Resale of new parts from small Czech producers and wholesalers: rubber parts, gaskets, cables, chrome wheels, ignition parts and manuals.
  - Own bundled kits sold as one listing, such as a "Jawa 634/638 complete gasket + cable restoration set" or a "Babetta 210 engine rebuild kit".

  Everything is branded "fits Jawa/ČZ" and uses no logo decals.
- **Buyer & channel:**
  - UK and NL Jawa/ČZ owners' clubs (the Dutch Jawa scene is documented at https://oud.jawa.nl/import_en_dealers_jawa.htm).
  - US/CA vintage two-stroke owners.
  - Channels: eBay.com, eBay.co.uk and eBay.de listings with English and German titles. These buyers search eBay rather than Czech webshops.
- **Price (€):** €8–150 per part. Kits run €35–90 (**estimate**).
- **Unit economics (cost, fees, net per unit):** **Estimate** for a €45 average order:
  - COGS ~€25 (CZ wholesale or bulk price, assumed ~20–30% under CZ retail; no supplier quotes were obtained)
  - eBay fees ~13% ≈ €6
  - Packaging €1
  - International shipping mostly paid by the buyer, with a ~€2 subsidy
  - **Net ≈ €10–12 per order.**
- **Demand evidence (numbers + URLs):**
  - The eBay.com Jawa/CZ 350 parts category showed **~1,671 listings, of which only ~37 ship from the Czech Republic**: https://www.ebay.com/b/Motorcycle-Parts-for-Jawa-CZ-350/10063/bn_22398995
  - At least one listing showed **16 sold**: "NEW CHROME WHEEL 18" JAWA 350 + ČZ", https://www.ebay.com/itm/122745488628, per the search snippet.
  - A seller of a "Czech made original" ignition coil has feedback citing "super fast delivery and good quality parts" (same search).
  - eBay UK has an active "Jawa CZ" shop page: https://www.ebay.co.uk/shop/jawa-cz?_nkw=jawa+cz
- **Supply gap / asymmetry evidence (numbers + URLs):**
  - **Weak.** CZ/SK web shops already export worldwide:
    - JAWAPARTS.COM, Zlín, with >9,000 parts: https://www.jawaparts.com/
    - https://www.4jawa.com/category/68/motorcycle-parts
    - https://www.jawashop.com/
    - https://mz-b.net/jawa-en
    - https://www.jawamarkt.cz/en/jawa-babetta-2/
    - DE's https://www.ost2rad.com/JAWA-CZ/
  - The only asymmetry is **channel presence**: few CZ sellers are on eBay (37/1,671), where overseas buyers actually search.
- **Edge for a CZ-based solo founder:**
  - Czech language and physical access to small CZ producers and swap meets such as the Moto veterán burzy (not verified this session).
  - CZ cost base.
  - Fast EU shipping.
- **Startup cost (€) & hours/week:** €1,500–3,000 of inventory for ~60–100 SKUs, plus a photo setup (**estimate**). 8–12 h/week for listing creation, packing and customer questions in English.
- **Realistic monthly profit after 12 months (pessimistic / realistic / optimistic, €):** €0 / €250 / €800 (**estimate**: 0, ~25 or ~70 orders/mo at ~€11 net).
- **CZ/EU legal/regulatory notes:**
  - **JAWA** is a live trademark (JAWA Moto), and **ČZ** is used by Česká zbrojovka. Use only "fits/passend für" and never reproduce logos or tank badges.
  - Brake and lighting parts need type approval for road use, so only resell parts that already carry it.
  - GPSR traceability applies.
  - For UK orders up to £135, eBay collects the UK VAT.
  - The US ended the $800 de minimis for all countries in Aug 2025 (background knowledge, verify), so US buyers now face duties and paperwork. That hurts the US channel.
- **Key risks:**
  - Incumbents list on eBay too and undercut.
  - Thin margins on resale.
  - Customs friction for UK/US orders.
  - The aging owner base.
  - Inventory tied up in slow SKUs.
- **Confidence (1–5) and why:** **2.** Money visibly changes hands on eBay, but the CZ-sourcing edge is already exploited by at least six dedicated exporters. The opportunity is only a channel gap, and no supplier pricing was verified.

### 4. Reproduction mechanical parts for vintage tape decks NOT covered by Revox/Studer specialists (NAB hub adapters, drive gears, idler/tension rollers for Grundig, Akai GX, Tandberg and Tesla decks)
- **What you sell / type (physical|digital|hybrid):** Physical. The range covers:
  - CNC-turned aluminium NAB hub adapters, machined by a CZ job shop
  - injection-moulded or precision-machined replacement gears for specific cassette decks and radio-cassettes
  - rubber-covered tension and idler rollers for Akai GX models

  Each SKU targets one model family.
- **Buyer & channel:** DE/NL/UK/US reel-to-reel and cassette hobbyists. Channels: eBay.de, eBay.com, Etsy, and the tapeheads/audiokarma/analog-forum.de communities.
- **Price (€):** NAB adapter pair €25–45. Gears €12–20. Rollers €20–40 (**estimate**, from background knowledge of typical listings; not verified this session).
- **Unit economics (cost, fees, net per unit):** **Estimate** for a €35 NAB pair:
  - CZ CNC cost €8–15 per pair at a batch of 50 (needs a quote)
  - Anodising ~€2
  - eBay fee ~€4.5
  - Packaging €1
  - Shipping mostly buyer-paid
  - **Net ≈ €13–19.**

  For a €15 gear: part cost €1–3, fees ~€2, **net ≈ €8–10**.
- **Demand evidence (numbers + URLs):**
  - An eBay.de store specialises in NAB hubs for reel-to-reel ("nabhubreeltoreel"): https://www.ebay.de/str/nabhubreeltoreel
  - A replacement gear for GRUNDIG CF 5500 / MCF 500 / MCF 600 is sold new and explicitly marketed as "NEU Nicht 3D Druck" (new, not 3D printed). Sellers differentiate on manufacturing quality: https://www.ebay.de/itm/164238357736
  - Revox pinch rollers sell on eBay.de: https://www.ebay.de/itm/355706840904
  - Akai and Revox reel-to-reel machines trade in dedicated eBay.de categories: https://www.ebay.de/b/AKAI-Tonbandgerate/116868/bn_469128, https://www.ebay.de/b/Revox-Tonbandgerate-und-Spulentonbandgerate/116868/bn_470436
  - Tension-arm rollers for the AKAI GX series appear on eBay.at/.de: https://www.ebay.at/sch/i.html?_sacat=60092&_nkw=akai+tonbandger%C3%A4t&_frs=1
- **Supply gap / asymmetry evidence (numbers + URLs):**
  - **Revox and Studer are saturated**: https://www.revox-online.de/andruckrolle, https://www.analogfan.de/andruckrollen.html, Premium-Hifi, and eBay sellers.
  - The gap for Akai, Grundig, Tandberg and Tesla parts is **unverified**. The existence of "not 3D printed" marketing suggests buyers get burned by poor prints, which means quality pays.
- **Edge for a CZ-based solo founder:**
  - CEE CNC and anodising job shops are cheap (no quotes obtained).
  - Czech Tesla decks (B-series reel-to-reel) have a local owner base and no Western supplier (background knowledge, not verified).
- **Startup cost (€) & hours/week:** €1,000–2,000: a donor deck or part, measurement tools, CAD, and first CNC batches of 30–50 (**estimate**). 8–10 h/week initially, then 3–5 h/week.
- **Realistic monthly profit after 12 months (pessimistic / realistic / optimistic, €):** €50 / €250 / €800 (**estimate**: ~20 units/mo across 6–10 SKUs at €10–15 net for the realistic case).
- **CZ/EU legal/regulatory notes:**
  - Purely mechanical, non-electrical parts fall outside WEEE/RoHS.
  - "Fits Akai GX-…" is referential use only.
  - GPSR identification applies.
  - Low regulatory risk overall.
- **Key risks:**
  - Very fragmented demand, where each model is a micro-market.
  - Existing US and Chinese sellers of NAB adapters. Chinese NAB adapters are known to exist cheaply (background knowledge, not verified).
  - Hobbyist expectations for "perfect" tolerances.
- **Confidence (1–5) and why:** **2.** Demand is real (active categories, specialist stores, quality-differentiated gear listings), but no sold counts could be read, and the saturated Revox segment shows that incumbents move in once a part is known to sell.

### 5. Babetta (Jawa 207/210) restoration and engine kits for the US moped scene
- **What you sell / type (physical|digital|hybrid):** Physical. Curated kits of new CZ-made parts, for example a "Babetta 210 engine gasket + seal + bearing + clutch set" or a "cable + rubber set". Each kit comes with an English photo guide, which could also be sold as a PDF, making this hybrid.
- **Buyer & channel:** US and Canadian moped hobbyists (the Moped Army/Treatland crowd), plus NL/DE. Channels: eBay.com, Etsy, and possibly wholesale to US moped shops.
- **Price (€):** Kits $40–90 (**estimate**).
- **Unit economics (cost, fees, net per unit):** **Estimate** for a $65 kit:
  - Parts cost ~€25 from CZ suppliers
  - Fees ~13% (~€7.5)
  - US shipping ~€15–20, largely buyer-paid but depressing conversion
  - Duties now apply because the US ended de minimis in Aug 2025 (background knowledge, verify)
  - **Net ≈ €12–18 per kit.**
- **Demand evidence (numbers + URLs):**
  - Treatland, which describes itself as the largest in-stock US vintage moped parts store, surfaced only a Babetta 210 **manual** in search: https://www.treatland.tv/jawa-babetta-typ-210-spare-parts-MANUAL-p/jawa-210-manual-yellow.htm
  - A Slovak brand, bbttagroup, sells Babetta tuning and parts for the 206/207/210/215/225 with EU shipping, which shows a paying enthusiast niche: https://bbttagroup.com/, https://bbttagroup.com/collections/engine_and_drivetrain
  - An eBay listing exists: https://www.ebay.com/itm/322625702902
  - No sold counts were obtained.
- **Supply gap / asymmetry evidence (numbers + URLs):**
  - Possibly thin **US in-stock** supply of Babetta parts, based on Treatland's snippet. This is weak evidence.
  - CZ/SK exporters exist: https://www.jawashop.com/by-type_k11/jawa_k17/jawa-50-babetta_k19/jawa-50-type-210-babetta_k20/, https://www.jawaparts.com/babetta-207-210-225, https://mz-b.net/babetta-en
  - NL coverage exists via https://moto.autodoc.nl/motorfiets-onderdelen/jawa-motorcycles/babetta
- **Edge for a CZ-based solo founder:** Direct access to Czech Babetta part producers and swap meets, with kits curated in Czech and sold in English.
- **Startup cost (€) & hours/week:** €800–1,500 of inventory for 10–15 kit SKUs (**estimate**). 5–8 h/week.
- **Realistic monthly profit after 12 months (pessimistic / realistic / optimistic, €):** €0 / €100 / €400 (**estimate**).
- **CZ/EU legal/regulatory notes:**
  - Do not use the "JAWA" or "Babetta" marks beyond "fits" (JAWA Moto trademarks).
  - Handle US customs and duties.
  - GPSR applies for EU sales.
- **Key risks:**
  - A tiny US market.
  - The loss of US de minimis kills small-parcel economics.
  - bbttagroup and jawashop could simply list on eBay.com.
- **Confidence (1–5) and why:** **1.** This is a hypothesis with thin evidence. It is included only because it is the most plausible under-served geography in the Jawa family. Validate by asking Treatland or another US moped shop whether they would wholesale Babetta kits, before buying any stock.

---

## Rejected
- **Generic Jawa/ČZ/Babetta/Pionýr parts webshop (the "CZ source" angle):** saturated by CZ/SK exporters that already ship worldwide:
  - JAWAPARTS.COM, Zlín, >9,000 parts: https://www.jawaparts.com/
  - https://www.4jawa.com/
  - https://www.jawashop.com/
  - https://mz-b.net/jawa-en
  - https://www.jawamarkt.cz/
  - bbttagroup (SK)
  - DE's https://www.ost2rad.com/JAWA-CZ/
  - Even AUTODOC NL lists Babetta parts: https://moto.autodoc.nl/motorfiets-onderdelen/jawa-motorcycles/babetta

  The CZ edge is already priced in. Only the eBay channel sliver (candidate 3) remains.
- **Lada Niva parts for Germany after the importer collapse:** tempting, because the importer effectively stopped by end-2025 and closed in March 2026, and more than 20,000 Nivas were registered in DE on 1 Jan 2022 (5,438 Lada 4x4 + 13,809 Niva + 6,179 not type-approved). Sources: https://www.nivatechnik.de/viewtopic.php?t=22355 (search snippet), https://www.auto-motor-und-sport.de/verkehr/keine-ladas-mehr-fuer-deutschland-deutscher-lade-importeur-pleite/. It is rejected for these reasons:
  - Supply is still broad through at least 7 DE shops: https://www.aet-autoteile.de/LADA-Parts, https://www.lada.shop/de/lada-niva/, https://niva-power.de/ersatzteile/, https://www.autodoc.de/ersatzteile/lada/niva, https://www.teilehaber.de/autoteile-shop/ersatzteile/lada-niva-(2121-2123)-tm1176.html (2,483 parts), https://www.carsundparts-shop.de/c/ersatzteile-fuer-lada-niva, https://www.autoteileprofi.de/lada-niva-ersatzteile
  - Russian-origin goods carry sanctions and origin-compliance risk that is unsuitable for a solo side business.
  - The installed base is shrinking.
  - There is no CZ edge.
- **Revox/Studer pinch rollers and vintage audio belts:** Revox/Studer rollers are served by at least 3 German specialists (https://www.revox-online.de/andruckrolle, https://www.analogfan.de/andruckrollen.html, Premium-Hifi) plus eBay sellers. Drive belts are a commodity with many sellers (background knowledge, not re-verified this session). Re-rubbering idlers is a repair service, which the brief excludes.
- **Commodity TM31 parts (motor coupling, measuring cup, blade cover, seals):** the price has already collapsed to €7.69–10.99 with volume tiers (eBay.de listings above). EUROPART sells the coupling at €10.49 (https://www.ebay.de/p/1376985022), and it is carried by chef-mix, ersatzteil-check and staubsaugerladen. Seals and blades also trigger food-contact rules (Reg. (EC) 1935/2004).
- **KitchenAid worm gears and service parts:** a commodity sold by many Amazon/eBay sellers at a low price, and the brand still supplies parts (background knowledge, **not re-verified this session**). There is no supply gap.
- **Game Boy / retro console shells and IPS screen kits:** the market is flooded by Chinese aftermarket makers (FunnyPlaying, Hispeedido and many AliExpress clones), and prices have compressed to near cost. A CZ seller has no edge (background knowledge, **not re-verified this session**).
- **Simson reproduction parts for Germany:** the market is huge but served by large DE specialists with deep catalogues and in-house repro production (e.g. AKF, MZA, ZT-Tuning, Ost2Rad). The CZ labour-cost edge doesn't beat their scale and German-language community ties (background knowledge, **not re-verified this session**).
- **B2B consumables for barbers and tattoo studios:**
  - Barber consumables (neck strips, blades, capes) are a commodity dominated by distributors and direct Chinese imports on Amazon, with no CZ edge.
  - Tattoo inks are regulated under the REACH restriction Reg. (EU) 2020/2081 (applied from 4 Jan 2022), which is too heavy a compliance burden for a solo founder. Needles and grips are a commodity.

  This is background knowledge, **not re-verified this session**.
