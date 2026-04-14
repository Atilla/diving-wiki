# Global Coral Bleaching Report for Liveaboard Trip Planning (2026)

## Context

The 4th Global Mass Coral Bleaching Event (2023-2025) — the worst in recorded history — has affected **84.4% of the world's coral reef area** across 83+ countries. NOAA had to add three new alert levels (3-5) because the existing scale was insufficient. This report synthesizes scientific data, NOAA monitoring, conservation reports, and firsthand diver accounts from ScubaBoard/blogs/magazines to give an honest, destination-by-destination assessment for liveaboard trip planning.

**Critical near-term concern:** NOAA forecasts 72-80% probability of El Nino emerging by late 2026, which could trigger another severe bleaching wave on reefs that have had minimal recovery time.

---

## How to use this report

Each destination has its own file with:
- **YAML frontmatter** — structured metadata (status, tier, coral rating, season, etc.) for quick querying
- **Standardised sections** — Status, Key Dive Sites, Marine Life, Dive Conditions, Season, Practical Info, Conservation, Trip Reports

Cross-cutting content lives in `_meta/`:
- [Ranking Table](_meta/ranking-table.md) — Tier 1-5 master ranking with one-line summaries
- [Strategic Takeaways](_meta/strategic-takeaways.md) — 15 cross-cutting insights
- [Sources](_meta/sources.md) — Bibliography
- [Template](_meta/template.md) — Section template for new/updated destinations

## How to update

See [CLAUDE.md](CLAUDE.md) for the complete wiki maintenance guide, including ingest workflows, cross-referencing conventions, and contradiction handling.

Quick reference:
1. Edit the individual destination file
2. Update the `last_verified` field in frontmatter
3. If the tier or status changed, update `_meta/ranking-table.md` to match

---

## Destinations by Region

### Red Sea
- [Northern Egypt](red-sea/northern-egypt.md) — Gulf of Aqaba, Sharm, Hurghada, Ras Mohammed, Dahab
- [BDE Circuit](red-sea/bde-circuit.md) — Brothers, Daedalus, Elphinstone
- [Southern Egypt](red-sea/southern-egypt.md) — Marsa Alam, Fury Shoals, St. Johns, Deep South
- [Sudan](red-sea/sudan.md) — Inaccessible (civil war)
- [Djibouti](red-sea/djibouti.md) — Seven Brothers, Gulf of Tadjoura
- [Saudi Arabia](red-sea/saudi-arabia.md) — Yanbu, Jeddah, NEOM

### Indo-Pacific
- [Maldives](indo-pacific/maldives.md) — Central/North degraded, South resilient, Fuvahmulah
- [Thailand — Gulf](indo-pacific/thailand-gulf.md) — Koh Tao, Sail Rock, Chumphon
- [Thailand — Andaman North](indo-pacific/thailand-andaman-north.md) — Similans, Richelieu Rock, Surin
- [Thailand — Andaman South](indo-pacific/thailand-andaman-south.md) — Koh Haa, Hin Daeng, Phi Phi
- [Myanmar — Mergui](indo-pacific/myanmar-mergui.md) — Mergui Archipelago
- [Philippines](indo-pacific/philippines.md) — Tubbataha, Apo Reef, Visayas
- [Malaysia](indo-pacific/malaysia.md) — Sipadan, Mabul, Layang-Layang, Peninsular
- [Great Barrier Reef](indo-pacific/great-barrier-reef.md) — Severely degraded, minke whales
- [Papua New Guinea](indo-pacific/png.md) — Kimbe Bay, Milne Bay
- [Palau](indo-pacific/palau.md) — Blue Corner, Jellyfish Lake
- [Fiji](indo-pacific/fiji.md) — Soft coral capital, Namena, Beqa

#### Indonesia
- [Raja Ampat](indo-pacific/indonesia/raja-ampat.md) — World's best coral triangle
- [Komodo](indo-pacific/indonesia/komodo.md) — Upwelling-protected reefs
- [Banda Sea](indo-pacific/indonesia/banda-sea.md) — Pristine & remote
- [Wakatobi](indo-pacific/indonesia/wakatobi.md) — Premium coral + macro
- [Lembeh Strait](indo-pacific/indonesia/lembeh.md) — World's #1 muck diving
- [Triton Bay / Cenderawasih](indo-pacific/indonesia/triton-bay-cenderawasih.md) — Soft coral walls + whale sharks
- [Nusa Penida](indo-pacific/indonesia/nusa-penida.md) — Mola mola + mantas
- [Alor](indo-pacific/indonesia/alor.md) — Muck + pelagic combo
- [Derawan / Kakaban](indo-pacific/indonesia/derawan-kakaban.md) — Jellyfish lake + mantas
- [Halmahera](indo-pacific/indonesia/halmahera.md) — Last Coral Triangle frontier

### Caribbean & Atlantic
- [Jardines de la Reina, Cuba](caribbean/jardines-cuba.md) — Inaccessible 2026-2027
- [Belize](caribbean/belize.md) — Lighthouse Reef, Blue Hole
- [Bonaire / Saba / Curacao](caribbean/bonaire-saba-curacao.md) — Shore diving capital
- [Bahamas](caribbean/bahamas.md) — Tiger Beach, Bimini
- [Turks & Caicos](caribbean/turks-caicos.md) — Wall diving + whales
- [Roatan](caribbean/roatan.md) — Bay Islands, Honduras
- [Cozumel & Playa del Carmen](caribbean/cozumel-playa-del-carmen.md) — Drift diving, cenotes, bull sharks
- [Fernando de Noronha](caribbean/fernando-de-noronha.md) — Spinner dolphins, Brazil

### Eastern Pacific
- [Galapagos](eastern-pacific/galapagos.md) — Megafauna paradise
- [Socorro](eastern-pacific/socorro.md) — Giant mantas & sharks
- [Cocos Island](eastern-pacific/cocos-island.md) — Hammerhead schools
- [Malpelo](eastern-pacific/malpelo.md) — Largest hammerhead schools on Earth
- [Hammerhead Triangle](eastern-pacific/hammerhead-triangle.md) — Eastern Tropical Pacific corridor

### Pacific
- [French Polynesia — Tuamotus](pacific/french-polynesia-tuamotus.md) — 700+ grey reef sharks
- [Solomon Islands](pacific/solomon-islands.md) — WWII wrecks + pristine reefs
- [Chuuk Lagoon](pacific/chuuk-lagoon.md) — World's #1 wreck diving
- [Vanuatu](pacific/vanuatu.md) — President Coolidge wreck
- [Tonga](pacific/tonga.md) — Humpback whale swimming
- [Niue](pacific/niue.md) — Legendary visibility

### Indian Ocean
- [Mozambique](indian-ocean/mozambique.md) — Dugongs, shark diving
- [Seychelles](indian-ocean/seychelles.md) — Outer atolls, adaptation evidence
- [Oman](indian-ocean/oman.md) — Upwelling-protected (not viable Apr 2026)
- [Tanzania](indian-ocean/tanzania.md) — Zanzibar, Mafia, Pemba
- [Madagascar](indian-ocean/madagascar.md) — Nosy Be, whale sharks
- [Mauritius](indian-ocean/mauritius.md) — Holiday + diving
- [Reunion](indian-ocean/reunion.md) — Volcanic topography + whales
- [Christmas Island](indian-ocean/christmas-island.md) — Whale sharks + red crabs
- [Andaman & Nicobar](indian-ocean/andaman-nicobar.md) — Barren Island volcano
- [Timor-Leste](indian-ocean/timor-leste.md) — World-record fish biodiversity

### Other
- [Sao Tome & Principe](other/sao-tome-principe.md) — Eastern Atlantic biogeography
- [Azores](other/azores.md) — Blue sharks + mobula rays
- [Malta & Gozo](other/malta-gozo.md) — Mediterranean wreck diving
- [Scapa Flow](other/scapa-flow.md) — WWI dreadnoughts
- [Narvik](other/narvik.md) — WWII Arctic destroyers
- [Cape Verde](other/cape-verde.md) — Whale sharks + European access
