# Option 3 · Hereford Express near Sherbrooke · original vs our edit

**Dates:** Mon–Tue Sep 21–22 2026 (overnight)  
**Camp:** Camping Villette preferred  
**Guide:** https://bikepacking.com/routes/hereford-express/  
**Shareable brief:** `site/option3-compare.html` (also `site/index.html`) · live Pages: https://pietro-betakick.github.io/bike-hereford-gravel-sep2026/

Nothing in this folder books lodging or invents private shortcuts.

---

## Original (RWGPS / BIKEPACKING.com)

| Field | Value |
|-------|-------|
| Source file | `gpx/official-hereford-express.gpx` (from RWGPS **40540319**, 4,515 track points) |
| Recomputed distance | **~164.9 km** |
| Recomputed ascent | **~1,833 m** raw · **~1,658 m** filtered (3 m threshold) |
| Elev max on GPX | **~722 m** (summit approach; published guide also cites 824 m summit high point) |
| Character | Pre–Oct 2024 **gravel** alignment: clockwise over **Chemin Lépine → Sam’s Turnpike** and Eaton–Beloin forest connectors. The live BIKEPACKING.com page later rewrote the massif crossing onto **~15 km Circuits Frontières singletrack** (difficulty 4/10 → 7/10) and flipped the loop counterclockwise. |

Published page stats for context: **166 km / ~1,830 m**.

---

## Our edit (public roads only · Day 2 scrubbed Sep 2026)

| Field | Value |
|-------|-------|
| Source | `gpx/routes.json` (Day 1 + Day 2 Leaflet coords + meta) |
| **Total** | **~132.4 km / ~1,187 m** |
| Day 1 | **~74.0 km / ~876 m** · Sherbrooke → North Hatley → Hatley → Coaticook → Camping Villette |
| Day 2 (rebuilt) | **~58.4 km / ~311 m** · Villette → St-Herménégilde → Ste-Edwidge → Martinville → Waterville → Sherbrooke |
| Direction | Counterclockwise overnight |
| Summit | **Mount Hereford SKIPPED** (45.0888, −71.5962) |
| Private OSM hits after scrub | **0** |

Day 1 largely follows the classic public gravel/paved corridor into camp. **Day 2 is the redesign**, rebuilt so geometry uses only named municipal / numbered public roads (and public cycleways). BRouter `trekking` + nogo circles around known private driveways/tracks.

---

## What we created (Day 2 bypass)

1. **Chemin Lebel** (St-Herménégilde) — start at public road by Camping Villette  
2. **Chemin Saint-Denis**  
3. **Chemin Saint-Jacques** → **Route 251** / Rue Principale  
4. North on **QC-251** toward **Sainte-Edwidge-de-Clifton** (skip Scalabrini `highway=track` spur)  
5. Farm / municipal links → **Martinville** (Rue Principale)  
6. **Chemin Orr** (Milby / Waterville)  
7. **Rue Winder** → **Rue Queen (QC-143)** into Lennoxville (avoid private driveway shortcuts)  
8. Public streets / cycleways → **Sherbrooke**

**Intentionally out:** Mount Hereford summit; Circuits Frontières singletrack; disputed **Lépine / Sam’s Turnpike / Eaton–Beloin** forest connectors; OSM `access=private` tracks/driveways previously clipped by the older Day 2 line.

### Trespass stance / verification

- **Designed for public roads only.**  
- **Verification:** (1) unique-geometry distance to known `access=private` OSM ways = **0 hits**; (2) OSM map-bbox nearest-highway snap on ~30 samples = **0** `access=private/no`.  
- **Field caveat:** Québec backroads can still show unmapped “chemin privé / interdit” signs. If one appears, use the next numbered public road (QC-141 / 147 / 251 / 253) and do not trespass.

---

## Access and camp

- **Camp:** Camping Villette preferred (season window covers Sep 21 2026; call to confirm; do not book from this doc). Plan B: Parc de la Gorge de Coaticook.  
- **Access:** car usually preferred Outremont → Sherbrooke (~2h15). REM is available as a rule when it fits, but car is usual for this start.

---

## Tradeoffs (short)

| | Original GPX | Our edit |
|--|--------------|----------|
| Distance | ~164.9 km | ~132.4 km |
| Ascent | ~1,833 m | ~1,187 m |
| Summit / singletrack | Yes (or later Circuits Frontières) | No |
| Bike fit | Mountain / mixed | True ~32 mm+ gravel overnight |
| Access ethics | Uses disputed forest connectors (old GPX) or paid singletrack (Oct 2024) | Public roads only · **0** OSM private hits after scrub |

---

## Files

- `site/option3-compare.html` / `site/index.html` — Leaflet + **embedded static SVG** comparison brief  
- `site/option3-map.svg` — static overlay (original / Day 1 / Day 2)  
- `gpx/official-hereford-express.gpx` — original track  
- `gpx/routes.json` — our edit coords + km/ascent  
- `gpx/day2.gpx` — rebuilt Day 2  
- `gpx/waypoints.json` — towns, camp, skipped summit  
- `research.md` — full redesign notes  

**Map script order (Leaflet grey-map fix):** `setView` → add tiles → add polylines → `fitBounds` → `bringToFront` → `invalidateSize`. jsDelivr Leaflet + Esri (CARTO fallback).
