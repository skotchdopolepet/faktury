# HUNTER: refurb-arbitrage (buy, lightly fix or clean, resell; intra-EU price gaps)

Date: 2026-09-29. FX used: €1 = 24.7 CZK (from the brief: €8,500 ≈ 210,000 CZK).

## Read this first: evidence limits of this hunt

- **The session's shared WebSearch budget ran out (200/200) after 8 searches by this hunter.** Every WebFetch attempt was blocked by the egress proxy: ebay.de (sold listings), kleinanzeigen.de, pc.bazos.cz, pricecharting.com, cardmarket.com, alza.cz, technimax.cz, gigacomputer.cz, svethardware.cz, tomshardware.com, zakonyprolidi.cz and eur-lex.europa.eu. Earlier proxy failures from other agents show that bazos.cz, sbazar.cz, aukro.cz, allegro.pl, vinted.cz, heureka.cz, etsy.com, ebay.com and reddit are blocked too.
- As a result, **the only fetched evidence comes from search-engine result snippets and summaries.** I could not open the pages, so every figure tagged "(search snippet)" should be re-checked on the page itself.
- **[BK] = background knowledge, not verified in this session.** Treat these as hypotheses. Each candidate ends with a short validation test to run before any money is committed.
- Because of this, confidence scores are deliberately conservative. The one theme with solid, recent, multi-source evidence is the **2025–2026 DRAM shortage** (RAM prices up 4–6×). That theme drives the top three candidates.

## The macro fact that shapes this lens: the 2025–2026 "RAMageddon"

- Mid-September 2026: the cheapest brand-name 32 GB DDR5 kit costs about **$395**, and tracked kits range from $395 to $610, against **$80–120 a year earlier** (4–6×). A 32 GB DDR4-3200 kit cost **$188** in Aug 2026, and the DDR4 1Gx8 3200 chip hit **$42.50** on 10 Aug 2026. Manufacturers have **cut legacy DDR4 output**. A real decline is expected **late 2027 to 2028**. (Search snippet: https://www.tomshardware.com/pc-components/ram/ram-price-index-2026-lowest-price-on-ddr5-and-ddr4-memory-of-all-capacities , https://tech-insider.org/ddr5-ram-prices-2026-pc-builders/ , https://tech-insider.org/dram-ram-price-crisis-2026/ , https://www.itechguides.com/ram-price-crisis-live-all-the-latest-updates-on-price-surges-global-memory-shortage-expert-advice-and-more/)
- Server RAM: "Why Server RAM Prices Have Doubled" (https://datacenterdisk.com/news/memory-chip-shortage-2026-server-ram-prices, title/snippet).
- CZ retail: DDR4 in Feb 2026 cost about **4.2× Feb 2025**, with "16 GB now costs 4,300 CZK, when a year ago you could buy 64 GB for that" (search snippet, https://svethardware.cz/article/o-kolik-zdrazily-ram-v-cr-priplatite-si-4-6nasobne , https://www.zive.cz/clanky/kdy-se-skutecne-v-roce-2026-stabilizuji-ceny-ram/sc-3-a-239278/default.aspx). RAM and SSD rose **up to 147% in Q1 2026 alone**, and PC makers are stockpiling (https://gamepress.cz/ceny-ram-a-ssd-leti-vzhuru-q1-2026-az-147-zdrazeni/).
- **CZ refurbishers say ex-lease supply now costs more.** Technimax (a CZ refurbisher) writes that a 16 GB DDR5 module went from about 1,000 to about 5,000 CZK, that DDR4 prices have multiplied several times over, and that "when buying from European suppliers, not only new RAM and SSDs but gradually the refurbished PCs and notebooks themselves are significantly more expensive" (search snippet, https://www.technimax.cz/zdrazovani-ram-a-ssd-ovlivnuje-i-ceny-repasovane-techniky). Gigacomputer.cz, another refurbisher, runs a page titled "RAMageddon 2026: Katastrofa pokračuje" (https://www.gigacomputer.cz/jak-vybrat-repas/rammagedon2026.html).
- Used-market liquidity in DE: kleinanzeigen shows a **32 GB DDR4 kit at €159 VB** and **64 GB sets at €180–250 VB**. There are also **wanted ads buying DDR4/DDR5 in bulk "ab 10 Stück" for PC, notebook and server** (search snippet, https://www.kleinanzeigen.de/s-pc-zubehoer-software/arbeitsspeicher/k0c225 , https://www.kleinanzeigen.de/s-pc-zubehoer-software/speicher/64gb-ddr4/k0c225+pc_zubehoer_software.art_s:speicher).

**Why this matters for a solo flipper:** when a commodity component jumps 4× in about 12 months, the whole-device prices that private sellers ask (an "old office PC", "grandpa's laptop") are often anchored to last year's value, while component buyers pay this year's price. That lag between whole-device and parts prices is the asymmetry the brief asks for. It is also **time-limited, with an explicit expected end in late 2027 to 2028**, so the plan must keep inventory turnover fast.

---

## Candidates

### 1. DDR4 RAM and NVMe SSD harvested from under-priced used office PCs and laptops (CZ bazaars, then CZ and DE buyers)
- **What you sell / type (physical|digital|hybrid):** Physical. Tested single DDR4 DIMM and SO-DIMM modules and matched kits (8/16/32 GB), plus NVMe/SATA SSDs that have been securely wiped, all pulled from whole used office machines (Dell OptiPlex, HP EliteDesk/ProDesk, Lenovo ThinkCentre SFF/Tiny) and business laptops. Stripped units are sold on as "barebone, no RAM/SSD" to refurbishers or tinkerers. There is a simple decision rule per unit: part it out or sell it whole, whichever is higher.
- **Buyer & channel:** CZ gamers, upgraders and small IT shops via bazos.cz (free listings [BK]), Aukro and Facebook groups. DE buyers via kleinanzeigen.de and eBay.de, including the bulk "ab 10 Stück" buyers seen on kleinanzeigen. Stripped chassis go as local pickup lots.
- **Price (€):** €30–90 per 8–16 GB module. About €150–160 per 32 GB DDR4 kit (kleinanzeigen ask €159, see above). SSD 256–512 GB about €20–45 (estimate [BK]; SSD prices also rose, per the gamepress.cz link). Barebone SFF chassis €25–60 (estimate [BK]).
- **Unit economics (cost, fees, net per unit):** *Estimate.* Illustrative SFF PC with an 8th–10th gen i5, 2×8 GB DDR4 and a 256 GB NVMe:
  - Buy at 2,000–2,800 CZK (this buy price is the key unverified assumption; see the validation test).
  - Parts resale: 16 GB DDR4 about 2,000 CZK (≈ €80, half of the €159 32 GB kit ask), SSD about 600 CZK, barebone about 1,000 CZK. Total about 3,600 CZK.
  - Costs: Packeta/packaging about 100–150 CZK per shipped part [BK]. eBay.de commercial fees about 11–13% if sold there [BK]. Bazos listings are free [BK].
  - **Net about 700–1,400 CZK (€30–55) per PC**. Labour is about 20–30 min hands-on per PC, plus unattended memtest.
  - **Buy rule:** buy only if ask ≤ (sum of part values) − 800 CZK.
- **Demand evidence (numbers + URLs):** Retail RAM is up 4–6×, with DDR4 at 4.2× y/y in CZ (links in the macro section). Bulk RAM buyers are advertising on kleinanzeigen (link above). Refurbishers report higher input costs (Technimax link). Phones and notebooks are expected to get dearer (https://wave.rozhlas.cz/zdrazi-letos-telefony-a-notebooky-ceny-pameti-ram-raketove-rostou-kvuli-ai-9586430), which pushes buyers toward used hardware and upgrades.
- **Supply gap / asymmetry evidence (numbers + URLs):** The supply side is documented: legacy DDR4 output was cut, and relief is expected no earlier than late 2027 to 2028 (tomshardware/tech-insider snippets). **The asymmetry, meaning private whole-PC asks that lag part values, is NOT verified**, because bazos could not be fetched. One bazos snippet shows single-module sellers already anchoring to the new retail spike (a 32 GB SO-DIMM listing citing "běžná cena 12 000 Kč", https://pc.bazos.cz/inzeraty/sodimm-ddr4-32gb/). The spread therefore has to come from *whole-device* listings and company clear-outs, not from RAM-only listings.
- **Edge for a CZ-based solo founder:** CZ has a dense ex-lease/office-PC bazaar supply and many small-firm clear-outs. Sellers price in CZK against last year's heuristics. There is direct access to both the CZ market and the larger DE market via Packeta. The work is light (open the case, pull the modules, memtest, photograph). No special skill is needed beyond basic PC hardware.
- **Startup cost (€) & hours/week:** €1,000–1,500 rolling inventory (cap unsold RAM stock at €1,500 because of crash risk). About €100 for tools (memtest USB, anti-static mat, SSD enclosure, scale, packaging). 10–12 h/week: about 3 h sourcing and messaging, 3 h pickups, 2 h testing, 3 h listing and shipping.
- **Realistic monthly profit after 12 months (pessimistic / realistic / optimistic, €):** *Estimate:* **€0–100 / €400–700 / €1,500.**
  - Realistic assumes 12–20 PCs a month at €30–55 net.
  - Optimistic assumes 1–2 company lots of 20–50 PCs.
  - Pessimistic assumes bazaar asks have already caught up.
  - Month 12 (Sept 2027) falls near the forecast start of the price decline, so profit is likely to fade after that.
- **CZ/EU legal/regulatory notes:** Trade licence (volná živnost, retail/wholesale) as a side business. See the cross-cutting notes below.
  - **SSDs must be securely erased.** Selling a drive with the previous owner's data creates GDPR and reputational exposure.
  - Keep purchase records and check serials to avoid handling stolen goods (podílnictví).
  - B2C online sales carry a 14-day withdrawal right and 12–24 months liability for defects on used goods.
- **Key risks:**
  1. **Window risk.** DRAM prices fall from late 2027 and stock loses value, so turn inventory within 2–3 weeks.
  2. The bazaar pricing lag may already have closed a year into the shortage.
  3. Test fails and returns on modules.
  4. Fraud from buyers claiming a module was "dead on arrival". Mitigate with serial stickers and photos.
- **Confidence (1–5) and why:** **3.** The demand and scarcity are strongly evidenced from multiple sources, and the shortage is expected to last into 2027–28. Unit work is light and the hours are minimal. The margin depends on an **unverified buy-side lag**, and the opportunity is explicitly temporary.
- **Validation test (2 h, €0):** Log 40 bazos/sbazar listings for "OptiPlex / EliteDesk / ThinkCentre / notebook 16GB". Record ask, RAM, SSD and CPU. Price each part against sold eBay.de and kleinanzeigen prices. Go ahead only if at least 25% of listings clear the buy rule.

### 2. Ex-server DDR4 ECC RDIMM/LRDIMM part-out (decommissioned Dell/HPE/Lenovo servers, then homelab and SMB buyers)
- **What you sell / type:** Physical. Tested 16/32/64 GB DDR4 ECC registered modules, plus server CPUs and PSUs as by-products, harvested from decommissioned 1U/2U servers bought as whole units or small lots.
- **Buyer & channel:** Homelabbers, SMB IT staff and server refurbishers via eBay.de/eBay.com (global), kleinanzeigen (including the bulk "server RAM ab 10 Stück" buyers, link above), bazos and Aukro.
- **Price (€):** *Estimate [BK]:* €50–150 per 32 GB RDIMM. The reasoning: pre-shortage used prices were about €30–40 [BK] and "server RAM prices have doubled" (datacenterdisk link). Verify with eBay sold listings.
- **Unit economics:** *Estimate:* A 2U server such as a Dell R640/R740 or HPE DL380 Gen10 with 8–12 × 32 GB could yield €400–1,000 of RAM alone. Buy price for whole servers is unknown (not verified). Fees are about 11–13% on eBay [BK] and shipping per module is small, about €4–8 [BK]. Hands-on work is about 30–45 min per server, plus memtest.
- **Demand evidence:** "Why Server RAM Prices Have Doubled" (https://datacenterdisk.com/news/memory-chip-shortage-2026-server-ram-prices). Bulk buyers for server RAM on kleinanzeigen (search snippet, https://www.kleinanzeigen.de/s-pc-zubehoer-software/arbeitsspeicher/k0c225). CZ refurbishers actively sell refurbished servers (e.g. https://www.technimax.cz/nejlevnejsi-repasovane-servery/typ-cpu/4x-intel-xeon-16-core), which shows a CZ secondary server market exists.
- **Supply gap / asymmetry evidence:** DRAM makers are prioritising HBM and server memory for AI, which squeezes DDR4 (macro links). CZ SMB decommission lots often sell as "old server, whatever" [BK, not verified].
- **Edge for a CZ-based solo founder:** Access to local company clear-outs and CZ IT asset disposal channels. Global demand makes the RAM itself easy to sell.
- **Startup cost (€) & hours/week:** €1,500–2,500 for 1–3 servers or a small lot, plus a test bench (one cheap compatible server to run memtest). 6–10 h/week.
- **Realistic monthly profit after 12 months (€):** *Estimate:* **€0 / €300–600 / €1,500.** The pessimistic case is that no sourcing channel is found, because servers do not appear on bazaars at the volume that PCs do.
- **CZ/EU legal/regulatory notes:** Business-to-business sales to homelab and SMB buyers are common, and B2B sales carry no withdrawal right. **Wipe or destroy data drives** (or do not buy servers that still hold drives). WEEE rules apply to disposing of the chassis.
- **Key risks:** Sourcing is irregular. Prices will fall as HBM and new fabs ramp up in 2027–28. The servers are heavy and noisy, which is a space problem for a home setup. RAM compatibility disputes (RDIMM vs LRDIMM, rank) cause returns.
- **Confidence:** **2.** The demand side is well evidenced, but sourcing volume and buy prices are completely unverified.
- **Validation test:** Search Aukro, bazos and CZ company-auction sites for "server Dell R640/R740, HPE DL360/380 Gen10" over 2 weeks. Compare the per-server ask with the eBay sold value of the fitted RAM.

### 3. "Plug-and-play" ex-lease 1-litre mini PCs for Home Assistant, Proxmox or home-media use
- **What you sell / type:** Hybrid, physical with a pre-installed free OS image. Lenovo ThinkCentre M7x0q/M9x0q Tiny, Dell OptiPlex Micro or HP EliteDesk Mini units. They are cleaned, repasted, fitted with RAM and SSD, and shipped with Home Assistant OS, Proxmox or Windows 11 Pro from the embedded licence, plus a one-page quick-start card. **This is a product, not support**: the listing says no configuration help.
- **Buyer & channel:** Hobbyists who don't want to build their own and small offices, in DE, AT, NL and CZ. Channels are eBay.de, kleinanzeigen, bazos and Aukro.
- **Price (€):** *Estimate [BK]:* €150–280 depending on CPU, RAM and SSD.
- **Unit economics:** *Estimate:* buy at €80–150 per unit, spend €5 on thermal paste and cleaning, 45–60 min per unit, €8–12 packaging and shipping to DE [BK], about 12% fees on eBay [BK]. **Net about €30–60 per unit.** Because of the RAM shortage, units that already hold 16–32 GB are worth more whole, so the decision between part-out (candidate 1) and whole sale applies here too.
- **Demand evidence:** New PCs are getting dearer because of memory costs (https://wave.rozhlas.cz/zdrazi-letos-telefony-a-notebooky-ceny-pameti-ram-raketove-rostou-kvuli-ai-9586430 , https://gamepress.cz/ceny-ram-a-ssd-leti-vzhuru-q1-2026-az-147-zdrazeni/). **No direct sold-count evidence for mini PCs could be fetched.** The homelab and Home Assistant demand is [BK].
- **Supply gap / asymmetry evidence:** Refurbishers report that European ex-lease supply is getting more expensive (Technimax link). That supports demand for used units but squeezes buy prices. Not verified for mini PCs specifically.
- **Edge for a CZ-based solo founder:** Local ex-lease supply. Pre-configuration is the value-add that turns a commodity box into a ready product. It is a one-off image build, and each unit takes minutes to flash.
- **Startup cost (€) & hours/week:** €1,200–1,500 for 8–10 units, plus €100 for tools. 10–12 h/week.
- **Realistic monthly profit after 12 months (€):** *Estimate:* **€100 / €400–600 / €1,000** (10–20 units a month at €30–60).
- **CZ/EU legal/regulatory notes:** Selling complete electrical devices B2C cross-border into DE may trigger ElektroG/WEEE registration questions (stiftung ear) for the "first placing on the DE market". **Verify before shipping whole devices to DE consumers.** This does not apply to CZ sales or to component sales. Windows only with the device's own embedded OEM licence.
- **Key risks:** Crowded category (DE refurbishers such as https://www.thinkstore24.de/ and https://it-versand.com/). Buyers expect support ("service creep"). WEEE compliance for DE. Rising input prices.
- **Confidence:** **2.** The logic is plausible and the unit work is light, but demand counts and the price gap are unverified, and the competition is visible.
- **Validation test:** Pull 30 eBay.de sold listings for "ThinkCentre Tiny" and "OptiPlex Micro" and 30 bazos asks. Go ahead only if the median sold price minus the median CZ ask is at least €50.

### 4. Modded Game Boy (DMG-01 / Color / Advance) with laminated IPS screen, new shell and USB-C battery
- **What you sell / type:** Physical. Original Nintendo handhelds bought in CZ/SK/PL, cleaned and fitted with an aftermarket IPS kit, a new shell and buttons, and an optional USB-C Li-ion kit. Sold ready to play, one unit at a time.
- **Buyer & channel:** Retro collectors and gift buyers in the EU and US via eBay.de/eBay.com, Etsy and kleinanzeigen.
- **Price (€):** *Estimate [BK]:* €110–220.
- **Unit economics:** *Estimate [BK]:* console €35–70 (CZ bazaar), IPS kit €25–40, shell and buttons €10–15, USB-C battery €10–15. That makes a cost of about €80–130. Fees are about 12–15% (Etsy or eBay) [BK] and shipping about €8–15. **Net about €30–60 per unit** for 1–1.5 h of work (within the brief's 1–2 h limit).
- **Demand evidence:** **Not fetched** (pricecharting, Etsy and eBay were all blocked). Etsy and eBay modded-handheld demand is [BK].
- **Supply gap / asymmetry evidence:** Not verified. The hypothesis is that CZ/PL bazaar prices for original handhelds sit below eBay.de prices.
- **Edge for a CZ-based solo founder:** Cheaper local sourcing (hypothesis). Lower labour cost. Soldering skill can be learned in weeks.
- **Startup cost (€) & hours/week:** €800–1,200: 10 consoles, kits, a soldering station, tri-wing and gamebit drivers. 12–15 h/week.
- **Realistic monthly profit after 12 months (€):** *Estimate:* **€100 / €400–700 / €1,200** (10–15 units a month).
- **CZ/EU legal/regulatory notes:**
  - Lithium batteries: ship them inside the device and check carrier rules.
  - Do not use Nintendo logos in branding, only in the item description.
  - Etsy rules on altered or modified goods: verify.
  - 12-month defect liability for used goods (agreed shortening) and the 14-day withdrawal right.
- **Key risks:**
  - Crowded Etsy niche with many modders [BK].
  - Kit-quality issues, and the DMG IPS mod requires cutting.
  - Collector prices are fad-prone. Check 2025–26 sold prices, not 2021 ones.
- **Confidence:** **2.** The unit economics fit the brief's work limit, but there is zero verified demand or gap evidence from this session.
- **Validation test:** Compare 30 eBay.de sold listings of "Game Boy IPS" (price and sale frequency) against 30 bazos, sbazar and Allegro asks for unmodded consoles.

### 5. Tested vintage manual lenses from Central Europe (Carl Zeiss Jena, Pentacon, Meyer-Optik, Helios, Meopta) with mirrorless adapter
- **What you sell / type:** Physical. M42, Exakta and Praktica lenses bought cheaply in CZ bazaars (often inside old Praktica or Zenit kits). They are cleaned externally, checked for fungus, haze and aperture oil, test-shot on a mirrorless body and sold with a cheap adapter as "ready for Sony E / Fuji X / Nikon Z".
- **Buyer & channel:** Mirrorless and video hobbyists worldwide via eBay.com/eBay.de and Etsy.
- **Price (€):** *Estimate [BK]:* €40–250 per lens.
- **Unit economics:** *Estimate [BK]:* buy €10–60 (or whole kits), adapter €8, fees about 13%, shipping €6–15. **Net about €20–80 per lens** for 30–45 min of work (test shots and photos).
- **Demand evidence:** **Not fetched.** Adapted vintage lens demand is [BK].
- **Supply gap / asymmetry evidence:** Not verified. The hypothesis is that CZ bazaar sellers price whole camera kits as junk while the lenses sell individually abroad.
- **Edge for a CZ-based solo founder:** The region's historic GDR, Soviet and Czech (Meopta) optics stock, Czech-language access to estates and bazaars, and cheap postage via Packeta.
- **Startup cost (€) & hours/week:** €500–800 (initial lenses plus a used mirrorless body for testing). 8–12 h/week.
- **Realistic monthly profit after 12 months (€):** *Estimate:* **€50 / €250–500 / €900.**
- **CZ/EU legal/regulatory notes:** Used goods (see the cross-cutting notes). Disclose optical defects to limit liability claims.
- **Key risks:** Fad cycles (the "Helios swirl" hype may have faded). Hidden fungus or haze leads to returns. It is low value per hour, and volume depends on sourcing luck.
- **Confidence:** **2.** Plausible and cheap to test, but no evidence was fetched.
- **Validation test:** Compare 30 eBay sold listings for "Carl Zeiss Jena Pancolar 50 1.8 / Flektogon 35 / Helios 44-2" against CZ bazaar asks.

---

## Cross-cutting CZ/EU legal notes ([BK]; confirm with a daňový poradce before starting)
- **Trade licence:** a volná živnost (retail/wholesale) can be run as a side business alongside employment. Income tax is 15% on profit. The 60% flat-expense option for trade is usually *worse* than actual costs for resale, because goods cost 60–85% of revenue.
- **VAT:** below the CZ registration threshold (2,000,000 CZK turnover from 2025 [BK]), no CZ VAT is charged. For cross-border B2C "distance sales" the EU-wide €10,000 threshold applies, and above it destination VAT (OSS) is due. Once VAT-registered, used goods bought from private persons can use the **margin scheme (§90 ZDPH, Art. 311–325 VAT Directive)**, which charges VAT only on the margin. Margin-scheme supplies are excluded from the distance-sales rules (Art. 35), so they stay taxed in CZ.
- **Liability for defects:** 24 months for consumer sales in CZ. For **used goods it can be shortened by agreement to at least 12 months** (§2165 OZ). DE allows the same only with express, separate consumer agreement (§476 BGB).
- **Withdrawal right:** online/distance sales to consumers carry a 14-day withdrawal right (§1829 OZ, Directive 2011/83/EU). Personal-pickup sales do not.
- **Platform reporting (DAC7):** marketplaces report sellers above 30 sales or €2,000 a year to tax authorities, so declare everything.
- **Stolen goods:** ex-corporate laptops can carry BIOS supervisor passwords or Computrace/Absolute locks, and iPhones can carry iCloud Activation Lock. Keep a purchase log and check serials, because of the handling-stolen-goods risk (podílnictví, §214 TZ).

---

## Rejected

1. **Generic ex-lease business laptops (ThinkPad, Latitude, EliteBook) bought and resold in CZ.** Evidence-based rejection. CZ refurbishers already sell a *ThinkPad T14 Gen 1 i5/16 GB/512 GB for 9,490 CZK with a 2-year warranty* (https://www.recomp.cz/repasovane-notebooky-lenovo/). Private bazos asks for the newer *T14 Gen 2 are 7,300–9,500 CZK* (https://pc.bazos.cz/inzeraty/thinkpad-t14/ , https://pc.bazos.cz/inzerat/200115896/lenovo-thinkpad-t14-gen-2-prislusenstvi.php). That leaves no spread for a solo buyer who must give at least 12 months of liability.
   - The market is saturated with specialist shops: Počítárna lists 137 Lenovo models (https://www.pocitarna.cz/repasovane-notebooky-lenovo/), and Počítače24 (24-month warranty, https://www.pocitace24.cz/repasovane-notebooky/lenovo-thinkpad-t14-gen-2-2/), ITzoo (https://www.itzoo.eu/collections/repasovane-notebooky-lenovo) and Technimax/Gigacomputer compete too.
   - Wholesale ex-lease input costs are *rising* because of RAM prices (Technimax link).
   - The only viable angle is the RAM-driven part-out or whole-sale decision in candidates 1 and 3.
2. **iPhones and iPads.** [BK] Professional refurbishers on Back Market and refurbed dominate. Apple parts pairing and serialization makes "light" repair (screens, batteries) show non-genuine warnings. iCloud Activation Lock and stolen-device risk are high. Grading disputes and 14-day returns on €300–800 tickets turn a thin spread into losses.
3. **GPUs.** [BK] High ticket (€200–800) in an efficient market where kleinanzeigen and eBay prices are fully arbitraged. Swapped-card and bricked-BIOS scams are frequent. Returns abuse under the withdrawal right is common. Memory-shortage price swings make holding inventory a gamble. There is no CZ-specific edge.
4. **E-bike batteries and parts.** [BK] Regulatory and safety rejection.
   - The EU Battery Regulation (EU) 2023/1542 treats whoever places *repurposed or remanufactured* batteries on the market as the producer, with the obligations that come with it.
   - Lithium packs over 100 Wh ship as dangerous goods (UN3480/3481), and consumer parcel networks restrict or refuse them.
   - Fire liability from a re-celled pack is uninsurable for a hobby seller.
5. **Amazon/retail returns pallets and B-stock lots.** [BK] Negative expected value for small buyers: the manifests are unreliable, the liquidator has already cherry-picked the best items, you inherit WEEE and waste disposal costs, and you need storage space. It is not a repeatable 10–15 h/week business.
6. **TCG cards (Pokémon, Magic).** [BK] Cardmarket is a single EU-wide price book, so there is no CZ-to-DE price gap to exploit. Sealed-product "arbitrage" is really retail-allocation scalping against bots. The 2024–26 Pokémon boom carries clear bubble and reprint risk, and grading adds cost and months of lag.
7. **Designer clothing via Vinted.** [BK] Private sellers on Vinted pay no seller fee, which floods supply and caps prices. A business seller must use Vinted Pro and honour consumer rights (withdrawal, defect liability), which private competitors don't. Counterfeit and authentication risk on designer pieces is high. Per-item profit is €5–30 against 20–40 min of photos, listing and shipping.
8. **LEGO part-out on BrickLink.** [BK] Sorting bulk bought by the kilo takes many hours per kilogram. BrickLink is a globally price-transparent market, so a CZ buy price gives little edge. The effective hourly return is low, and it breaks the brief's "about 1–2 h per unit" spirit because the "unit" is thousands of parts.

### Not assessed (no reachable evidence this session; left open for another pass)
- **Festool/Hilti tools, CZ to DE.** The direction of the price gap is unknown. There is a high stolen-tool risk in the used pro-tool market, and Hilti's fleet-leasing model reduces the private supply.
- **Vintage hi-fi (Tesla, Japanese 1970s–80s receivers).** Bulky, heavy shipping. Capacitor recaps can exceed 2 h per unit.
- **Dyson and robot vacuums.** [BK] New prices are being eroded by Chinese brands, battery wear is heavy and used values fall quickly. It leans toward rejection.
