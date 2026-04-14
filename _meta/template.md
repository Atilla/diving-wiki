# Destination File Template

Every destination file in the diving report follows this structure. Sections that don't apply should be omitted entirely (not left empty).

## Required frontmatter fields

```yaml
---
destination: {Full destination name}
region: {Red Sea | Indo-Pacific | Caribbean | Eastern Pacific | Pacific | Indian Ocean | Other}
sub_region: {e.g., Indonesia, Egypt — omit if not applicable}
status: {STATUS LABEL — brief description}
tier: {1-5, matching ranking-table.md}
coral_rating: {Excellent | Good | Moderate | Poor | N/A} with optional qualifier
marine_life_rating: {World-class | Excellent | Very Good | Good | Moderate}
best_season: {e.g., Oct-Apr}
peak_months: [Mon, Mon, Mon]
access: {Brief access description}
liveaboard: {true | false}
liveaboard_season: {e.g., Oct-Apr — omit if liveaboard: false}
water_temp_range: {e.g., 27-30C}
visibility_range: {e.g., 15-30m}
experience_level: {Beginner | Intermediate | Advanced | Expert} with optional detail
last_verified: {YYYY-MM}
bleaching_resilience: {low | moderate | high}
highlights:
  - {highlight 1}
  - {highlight 2}
  - {highlight 3}
---
```

## Section structure

```markdown
# {Destination Name}

## Status
(1-3 paragraphs: current coral/reef condition, bleaching history, recovery trajectory)

## Key Dive Sites
(### per site cluster, #### per individual site. Format: name, depth range, description, what to expect)

## Marine Life
(species encounters, reliability, seasonal patterns)

## Dive Conditions
- **Visibility**: ...
- **Temperature**: ...
- **Currents**: ...
- **Experience level**: ...

## Season
(month-by-month or season-by-season breakdown, best windows)

## Practical Info
- **Access**: ...
- **Operators**: ...
- **Itineraries**: ...
- **Costs**: ...
- **Recompression**: ...

## Conservation
(MPA status, restoration, threats — include if content exists in original)

## Trip Reports
(firsthand accounts with dates — include if content exists in original)

## Related Destinations
(bulleted list with relative markdown links to related destinations — geographic neighbors, similar experiences, biological corridors, alternatives. See CLAUDE.md section 5 for conventions.)
```

## Heading level rules

- `#` — destination name (one per file)
- `##` — main sections (Status, Key Dive Sites, Marine Life, etc.)
- `###` — site clusters or sub-areas (e.g., "North and Central Atolls", "Fury Shoals")
- `####` — individual dive sites (e.g., "Shark Reef & Yolanda Reef")
