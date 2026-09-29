# Orchestrator verification of the dossiers' "critical claims"

Each dossier listed the claims that would most change its verdict. The orchestrator ran web searches on them. The results are search-result summaries only; pages could not be opened.

## Dossier 06: Shoptet add-on (C05/C13)
- **Claim: "no iDoklad connector exists on the Shoptet marketplace." REFUTED.** Shoptet itself launched an iDoklad add-on ("the second Shoptet API add-on", doplnky.shoptet.cz/idoklad) back around 2018. It sends orders and tax documents to iDoklad and syncs stock across e-shops. Integroid.cz also sells an iDoklad + Shoptet integration, and iÚčto has its own marketplace add-on.
  - Sources: https://m.facebook.com/shoptet/photos/m%C3%A1me-pro-v%C3%A1s-druh%C3%BD-dopln%C4%9Bk-shoptet-api-je-to-n%C4%9Bco-co-jste-cht%C4%9Bli-u%C5%BE-dlouho-napoj/10156297268950266/, https://www.integroid.cz/stranka/idoklad-shoptet, https://doplnky.shoptet.cz/iucto, https://partneri.shoptet.cz/poptavka/propojeni-shoptet-a-idoklad/
- **Claim: "Shoptet's partner commission is not public." CONFIRMED.** A search found no published revenue-share figure. Shoptet decides with each developer whether an add-on is offered to all plans or only to Premium.
  - Sources: https://doplnky.shoptet.cz/chcete-delat-vlastni-doplnky, https://www.sniperdesign.cz/a/shoptet-doplnky-velky-pruvodce-2026
- **Orchestrator decision: KILL.** Both Shoptet niches the swarm found (promo mechanics and the iDoklad connector) are already served, the dossier itself forecast only about €125/month at month 12, and the founder's coding ability is unknown. **Adversarial reviewers were not spent on this dossier**; the effort went to the live candidates instead.

## Dossier 08: breast-milk keepsake jewelry (C04)
- **Claim: "MILKIES (Szczecin) is a large incumbent with a patented DIY kit." CONFIRMED.** MILKIES reports 50,000+ completed orders and "trusted by over 100,000 moms" in 50+ countries. It holds a US patent (US12049027B2) and a European patent (EP3804554A1) on liquid breast-milk preservation, and sells DIY sets in DE and CH.
  - Sources: https://milkies-diy.ch/, https://milkies-diy.de/faq/, https://www.milkies.eu/sets/
- Together with the Czech competitors listed in 02-main-loop-evidence.md (6+ CZ makers with 8–12 week queues), this confirms the dossier's no-go on durable asymmetry.
- **Orchestrator decision: KILL as a main bet.** The dossier's own verdict is no-go, and verification strengthens it. It goes to the steelman reviewer (see below) rather than a 3-reviewer panel.

## Dossier 10: HAN smart-meter reader (C10)
- **Claim: "no packaged CZ HAN reader is on sale." PARTLY CONFIRMED.** Searches found only DIY routes: forum threads on homeassistant-cz.cz and a free GitHub HA add-on for EG.D DLMS over RS485 (blesk89/ha-addon-egd-dlms). LaskaKit sells a generic **ESPlan ESP32 + RS485 + PoE board** that hobbyists can use for this, so the "hardware" already exists as a board and only the packaged, preconfigured product is missing.
  - Sources: https://github.com/blesk89/ha-addon-egd-dlms, https://www.laskakit.cz/en/laskakit-esplan-esp32-lan8720a-max485-poe/, https://www.homeassistant-cz.cz/viewtopic.php?t=1565, https://www.homeassistant-cz.cz/viewtopic.php?t=2127
- **Claim: the number of Home Assistant installations in CZ.** NOT FOUND. analytics.home-assistant.io has per-country data, but it can't be fetched here.
- **Implication:** the gap is thin. A local maker such as LaskaKit could ship a "HAN kit" with a guide at any time.

## Dossier 09: A2 exam prep (C08)
- **Market size CONFIRMED:** more than 12,000 people passed the A2 exam in 2024 (MŠMT, Oct 2025), and the number of applicants is rising. In 2023 there were 8,819 candidates with an 86.2% pass rate. Writing is the weakest skill at 65.9%.
  - Sources: https://msmt.gov.cz/zajem-o-zkousku-z-cestiny-pro-trvaly-pobyt-roste-stat-jiz, https://epale.ec.europa.eu/cs/resource-centre/content/zkouska-z-ceskeho-jazyka-pro-trvaly-pobyt-statisticky-prehled
- **Competition is CONFIRMED and crowded:**
  - **CzechReady**: free reading and listening, with writing, speaking and mocks in a premium tier
  - **ExamOnline.cz**: an A2 course
  - **studyfun.cz**
  - **ICJ**: a 40 h course for 5,400 CZK, marketing the "new format 2026"
  - **UJOP**: 1,580 CZK consultation
  - **languageatelier.eu** and **EduJoy**
  - the free official preparation page on cestina-pro-cizince.cz
  - Sources: https://czechready.cz/, https://examonline.cz/en/courses/cestina-trvaly-pobyt/, https://icj.cz/en/preparation-for-the-a2-exam-for-permanent-residence-new-format-2026/, https://ujop.cuni.cz/UJOPEN-74.html?ujopcmsid=68:individual-preparation-for-the-exam-for-permanent-residence-applicants, https://studyfun.cz/cz/courses/czech/czech-preparation-course-for-permanent-residence-a2-language-test
- **Implication:** demand is real (roughly 14,000 candidates a year) and so is the supply. With an 86% pass rate, most candidates don't feel desperate. The niche is contested and asymmetry is weak; the remaining angle is native-language (UA/VI) writing and speaking drills.
