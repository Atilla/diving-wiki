# CLAUDE.md — Wiki Schema & Maintenance Guide

This file governs how this wiki is structured, updated, and maintained. It is the authoritative reference for any LLM or human contributor working on this project.

## 1. Purpose & Scope

This is a **Global Coral Bleaching Report for Dive Trip Planning (2026)**. It provides honest, destination-by-destination assessments of diving destinations in the context of the 4th Global Mass Coral Bleaching Event (2023-2025).

**Audience:** Divers planning dive trips — liveaboard, resort-based, shore diving, or day-boat.

**In scope:**

- Diving destinations worldwide (liveaboard, resort-based, day-boat, shore diving)
- Coral/reef condition with scientific grounding (NOAA, peer-reviewed research)
- Marine life encounters and reliability
- Practical logistics (access, operators, costs, seasons, safety)
- Conservation context and MPA status

**Out of scope:**

- General travel advice (hotels, restaurants, non-diving activities)
- Marine biology database (species taxonomy, phylogenetics)
- Dive training or certification guidance
- Equipment reviews

## 2. File Structure & Naming

```text
diving-wiki/
├── CLAUDE.md                 ← this file (wiki schema & rules)
├── README.md                 ← main index with destination links
├── _meta/                    ← cross-cutting content
│   ├── template.md           ← YAML frontmatter + section template
│   ├── ranking-table.md      ← tier 1-5 master ranking
│   ├── strategic-takeaways.md← 15 cross-cutting insights
│   ├── sources.md            ← bibliography
├── red-sea/                  ← region folders
├── indo-pacific/
│   └── indonesia/            ← sub-region folder (only Indonesia currently)
├── caribbean/
├── eastern-pacific/
├── pacific/
├── indian-ocean/
└── other/
```

**Naming conventions:**

- One markdown file per destination
- Filenames: lowercase, hyphenated, descriptive (e.g., `thailand-andaman-north.md`, not `thailand-1.md`)
- Region folders match the `region` frontmatter field (see mapping below)
- Indonesia has its own sub-folder under `indo-pacific/` due to the number of destinations (10)
- The `hammerhead-triangle.md` in `eastern-pacific/` is the only "concept" file — a cross-cutting grouping spanning multiple destinations (Galapagos, Cocos, Malpelo)

**Region folder mapping:**
| Folder | `region` value |
|---|---|
| `red-sea/` | Red Sea |
| `indo-pacific/` | Indo-Pacific |
| `caribbean/` | Caribbean |
| `eastern-pacific/` | Eastern Pacific |
| `pacific/` | Pacific |
| `indian-ocean/` | Indian Ocean |
| `other/` | Other |

## 3. YAML Frontmatter Schema

Every destination file begins with YAML frontmatter. Fields:

| Field | Type | Values / Format | Notes |
|---|---|---|---|
| `destination` | string | Full destination name | Must match the `#` heading |
| `region` | enum | Red Sea, Indo-Pacific, Caribbean, Eastern Pacific, Pacific, Indian Ocean, Other | Exactly 7 values |
| `sub_region` | string | e.g., "Indonesia", "Egypt" | Omit if not applicable |
| `status` | string | "LABEL — brief description" | Free-form; uppercase label + dash + narrative |
| `tier` | integer | 1-5 | Must match `_meta/ranking-table.md`. Use `~` for inaccessible destinations |
| `coral_rating` | string | Base: Excellent, Good, Moderate, Poor, Very Poor, N/A | Parenthetical qualifiers allowed, e.g., "Good (recovering)". N/A requires explanation, e.g., "N/A (wreck destination)". Compound forms allowed: "Poor-Moderate", "Good-VG" |
| `marine_life_rating` | string | World-class, Extraordinary, Exceptional, Excellent, Very Good, Good, Moderate | Qualifiers allowed, e.g., "World-class macro", "Excellent sharks" |
| `best_season` | string | e.g., "Oct-Apr" | Month range |
| `peak_months` | list | e.g., [Nov, Dec, Jan] | 3-letter month abbreviations |
| `access` | string | Brief access description | e.g., "Fly Sorong via Jakarta" |
| `liveaboard` | boolean | true / false | |
| `liveaboard_season` | string | e.g., "Oct-Apr" | Use `~` if `liveaboard: false` |
| `water_temp_range` | string | e.g., "27-30C" | |
| `visibility_range` | string | e.g., "15-30m" | |
| `experience_level` | string | Free-form | e.g., "Advanced Open Water, 50+ logged dives", "Open Water (inner) to Advanced (walls)" |
| `last_verified` | string | YYYY-MM | When this file's content was last checked against current sources |
| `bleaching_resilience` | enum | low, moderate, high | Use `~` if not applicable or unknown |
| `highlights` | list | 3 items typical | Key selling points |

**Null values:** Use `~` (YAML null) when data is unavailable, not applicable, or the destination is inaccessible.

## 4. Section Template & Heading Rules

See `_meta/template.md` for the full template. Heading hierarchy:

- `#` — destination name (one per file, must match frontmatter `destination`)
- `##` — main sections: Status, Key Dive Sites, Marine Life, Dive Conditions, Season, Practical Info, Conservation, Trip Reports, Related Destinations
- `###` — site clusters or sub-areas (e.g., "Dampier Strait", "Fury Shoals")
- `####` — individual dive sites (e.g., "Cape Kri", "Shark Reef & Yolanda Reef")

**Rules:**

- Omit sections that don't apply — don't leave empty sections
- Status section always leads with a bold one-line summary matching the frontmatter `status` field
- Individual dive sites follow the format: Name — depth range. Description. What to expect.
- Related Destinations is always the last section

## 5. Cross-Referencing

Use relative markdown links between files.

**Link syntax:** `[Destination Name](../region/filename.md)` or `[Name](filename.md)` for files in the same folder.

**Where cross-references appear:**

1. **Inline in prose** — when the text naturally mentions another destination (e.g., "see [Triton Bay / Cenderawasih](triton-bay-cenderawasih.md) for near-guaranteed whale shark encounters")
2. **`## Related Destinations` section** — bulleted list at the bottom of each file

**Relationship categories for Related Destinations:**

- **Geographic neighbor** — destinations commonly combined in one trip
- **Similar experience** — comparable diving style (e.g., muck diving, wreck diving)
- **Biological corridor** — connected ecosystems or migration routes
- **Alternative to** — when one destination is degraded or unavailable, link to a similar option

**Example Related Destinations section:**

```markdown
## Related Destinations
- [Komodo](komodo.md) — combine in a single Indonesia liveaboard trip
- [Triton Bay / Cenderawasih](triton-bay-cenderawasih.md) — nearby; near-guaranteed whale sharks
- [Banda Sea](banda-sea.md) — common transit route extension
- [Wakatobi](wakatobi.md) — premium coral alternative within Indonesia
```

**Cross-references in `_meta/` files** use paths relative to the repo root (e.g., `[Socorro](eastern-pacific/socorro.md)`).

## 6. Ingest Workflow

When incorporating new information, follow the workflow for the relevant source type:

### Trip reports (ScubaBoard posts, blogs, dive magazines)

1. Extract: date, destination, coral observations, marine life encounters, conditions, operator info
2. Compare against existing file content — note agreements and contradictions
3. Update relevant sections (Status, Marine Life, Dive Conditions, Practical Info)
4. Add entry to `## Trip Reports` with a date and a one-line observation summary. No source names or origin labels — just what was seen and when.

### Scientific / monitoring data (NOAA Coral Reef Watch, GCRMN, peer-reviewed studies)

1. Update `## Status` section with new findings
2. Assess whether `coral_rating`, `bleaching_resilience`, or `tier` should change
3. Add source to `_meta/sources.md`

### Geopolitical / access changes (travel advisories, conflicts, visa changes, operator closures)

1. Update `## Status` and `## Practical Info` immediately
2. If destination becomes inaccessible: move to "Not Currently Viable" in `_meta/ranking-table.md`, set relevant frontmatter fields to `~`
3. Geopolitical safety changes override all other considerations

### After any ingest

- Update `last_verified` in frontmatter to current YYYY-MM
- If `tier` or `status` changed, update `_meta/ranking-table.md` to match
- Check if any insight in `_meta/strategic-takeaways.md` needs revision
- Check if Related Destinations links need updating

## 7. Contradiction Handling

When new information contradicts existing content:

1. **Do not silently overwrite.** Add the new information alongside the old with dates.
2. **Clear winner:** If the new info is clearly more recent and credible, update the main claim and note the change with a date (e.g., "Previously rated X; as of [date], now Y").
3. **Ambiguous:** If the contradiction can't be resolved (e.g., one trip report says coral recovering, another says still degraded), present both observations with dates and let the reader judge.
4. **Safety override:** Geopolitical and safety information always takes precedence immediately — don't wait for corroboration.

## 8. Currency & Confidence

This wiki uses a lightweight approach to confidence tracking:

- **`last_verified`** in frontmatter is the primary currency signal. Files older than 6 months should be flagged for review.
- **`## Trip Reports`** serves as the evidence trail — each entry must include a date and source type.
- **Hedging language** for uncertain claims: use "reportedly", "operators claim", "a single 2025 report suggests", "unconfirmed but" when a claim rests on a single source or is otherwise uncertain.
- **No source attribution in destination files.** Do not name sources, publications, organisations, or language communities anywhere in destination file prose or Trip Report entries — not inline ("per IFRECOR…"), not as trailing notes ("Source: SUBAQUA"), not as origin labels ("French monitoring data", "German dive press"). The git log records which ingest pass introduced a change; `_meta/sources.md` records the bibliography. That is sufficient. Destination files contain only facts, observations, and hedged claims — never the name of what they came from.

## 9. Maintenance Checks

Periodic tasks to keep the wiki consistent:

- [ ] **Stale files:** Flag any destination where `last_verified` is older than 6 months
- [ ] **Tier consistency:** Verify that `tier` in each destination file matches `_meta/ranking-table.md`
- [ ] **Status consistency:** Verify that the `status` frontmatter matches the bold lead line in `## Status`
- [ ] **Strategic takeaways:** Review `_meta/strategic-takeaways.md` for any insights invalidated by per-destination updates
- [ ] **Cross-reference completeness:** Check for destination names mentioned in prose but not linked
- [ ] **Ranking table completeness:** Ensure all destinations appear in `_meta/ranking-table.md`
- [ ] **NOAA check:** Review NOAA Coral Reef Watch (coralreefwatch.noaa.gov) for new alerts affecting tracked destinations

## Design Decisions

**No raw sources folder.** Sources are external (NOAA, ScubaBoard, research papers). The wiki links to them. Trip Reports sections and `_meta/sources.md` serve as the provenance layer. Storing copies would bloat the repo and create copyright issues.

**No per-claim confidence scores.** The `last_verified` field plus hedging language is sufficient for this wiki's scope (~67 destinations, ~5,000 lines of content).

**No tags beyond frontmatter.** The structured YAML fields already capture the relevant taxonomy. Adding inline tags would duplicate what frontmatter conveys.

**One file per destination.** Files range from ~30 to ~160 lines. This granularity is right — no need to split into sub-files or merge into monolithic documents.
