# Boots-on-the-Ground Fieldwork Plan — Phibsborough–Drumcondra 3D Model

**Constraint set:** all work executable by **1–2 people**, in a **non-professional
capacity**, with **basic equipment** (smartphone, optionally an action camera, a €30
laser distance measure, and optionally a sub-250 g camera drone). Tasks are ranked by
model impact per unit of effort and mapped to the R0–R5 roadmap.

**Why fieldwork matters for this model:** the open-data stack (see
`data-sources-3d-district-model.md`) delivers geometry, but three things it cannot
deliver are exactly what the mission statement asks for — **recognisability** (the model
looking like the place), **currency** (the corridor changes; open data lags), and
**per-object ground truth** (validating that queryable objects match reality).

---

## Ranked task list

### 1. Street-level imagery sweep — highest impact per hour *(serves R1–R4)*

Walk or cycle every public street and path in the corridor with a smartphone or action
camera capturing sequenced, geotagged images, uploaded to **Mapillary** or
**Panoramax** (open licences, free hosting, automatic face/plate blurring).

- **Why:** one sweep produces a reusable evidence base for nearly every later task —
  digitising kerbs, crossings, signals and furniture (R3), roof forms, façades and
  entrances (R4), validating building footprints and land use (R1), and QA of the whole
  model. It converts every desk session thereafter into "look it up" instead of "go
  back out".
- **Effort:** the corridor holds roughly 25–35 km of streets and paths; 2–4 half-day
  outings on foot/bike for one person. Repeat annually or after visible change.
- **Equipment:** phone on a chest/bike mount; an action camera (~€250–350) improves
  quality but is optional.
- **Traceability:** each derived object cites the image sequence ID + capture date.

### 2. OSM completion and enrichment survey *(serves R1–R3)*

Targeted OpenStreetMap editing in the corridor using **StreetComplete** and **Every
Door** (phone apps built for exactly this kind of non-professional survey):
building **storey counts** (`building:levels`) and **roof shapes**, missing paths and
steps, bridge details, surface types, crossings, and park internals (Griffith Park
paths, pitch outlines).

- **Why:** OSM is the model's primary geometry source, so every improvement flows
  directly into the pipeline with a timestamped changeset ID — provenance for free. The
  single most valuable tag campaign is **storey counts**, which calibrate and gap-fill
  the nDSM-derived building heights (the weakest link in R1). Because the corridor is
  dominated by repeating typologies (Victorian/Edwardian terraces, 1930s semis), one
  observation often covers a whole terrace run — survey by street segment, not by
  building.
- **Effort:** 3–6 half-days for the corridor's main streets; gamified apps make this
  genuinely one-person work.
- **Caution:** edits must reflect ground truth (OSM rules), which is fine — ground
  truth is precisely what's wanted.

### 3. DTM/height validation with simple checkpoints *(serves R0–R1)*

Collect ~30–50 validation observations: averaged phone-GNSS positions plus relative
levels at photo-identifiable places — pitch surfaces in Griffith Park, the canal
towpath (a near-level line by construction, ideal for detecting DTM tilt/noise), bridge
decks, and street corners. Measure bridge soffit-to-water and wall heights with the
laser measure.

- **Why:** cheap ground truth turns "we think the terrain is right" into a stated
  accuracy figure per release — and the Royal Canal's level pound is a free, kilometres-
  long reference line through the heart of the corridor.
- **Accuracy honesty:** phone GNSS is 3–5 m horizontal; averaging and photo-identified
  features get useful checks at 1 m-DTM scale, but this validates, it does not survey.
  A budget RTK receiver (~€300–600) is the one optional upgrade that changes the game
  (centimetre positions), and is stretch-goal, not required.
- **Effort:** 1–2 days total, combinable with task 1.

### 4. Tree gap-fill survey *(serves R2 — MVP)*

The DCC tree dataset covers council-managed street trees. Survey what it misses:
**Griffith Park and canal-bank trees, and prominent private/garden trees visible from
public land**. Record position (averaged phone GNSS + offset note), species (app-
assisted, e.g. PlantNet — record confidence), height class (clinometer app or
comparison to adjacent known-height buildings), and crown spread (paced).

- **Why:** trees are an MVP (R2) feature class, and the Tolka valley's and Griffith
  Avenue's character *is* its tree lines — this is a direct recognisability win.
- **Effort:** 2–3 half-days for the park and main avenues. Two people work well here
  (one measures, one records).
- **Traceability:** `source = field survey`, observer, date, method, species
  confidence — fits the register schema directly.

### 5. Landmark capture by ground photogrammetry *(serves R2/R4 recognisability)*

Photograph-walk key landmarks with a phone (60–80% overlapping stills, two heights,
full circuit where accessible) and reconstruct with **WebODM** (open source) or a phone
photogrammetry app: St Peter's Church Phibsborough (the corridor's dominant spire),
Drumcondra church and bridge, the Cross Guns Bridge/canal lock area, Tolka bridges,
Dalymount Park's street-facing stands, Brendan Behan Park features.

- **Why:** a handful of well-modelled landmarks does more for "recognisable" than a
  thousand extruded footprints, and ground capture needs **no permissions** from public
  footpaths. This is also the drone fallback (see task 7).
- **Effort:** ~half a day per landmark including processing; pick 5–8 landmarks.

### 6. Recognisability QA viewpoints *(serves every release)*

Define 15–20 fixed viewpoints along the mission route (Griffith Avenue → Tolka valley →
Phibsborough), photograph each from a marked spot, and re-photograph after each model
release. Compare photo vs render side by side as the project's standing acceptance
test for "recognisable".

- **Why:** it operationalises the mission statement's key adjective, catches
  regressions, and doubles as progress material for stakeholders.
- **Effort:** half a day to establish; an hour per release thereafter.

### 7. Drone capture — valuable but conditional *(serves R4; some R1 QA)*

A sub-250 g camera drone (e.g. DJI Mini class, ~€300) flying grid/orbit patterns over
selected blocks yields oblique imagery and photogrammetric meshes (via WebODM) far
beyond anything open data provides: roof forms, rear-of-terrace massing, accurate
ridge heights, and textured landmark models.

**Regulatory reality for this corridor (Ireland/EASA rules — check before planning):**

- Any camera drone, including sub-250 g, requires **IAA operator registration**
  (~€41/2 years) and the free online A1/A3 training via the IAA MySRS platform.
- North Dublin airspace is complex: **Dublin Airport's restricted zones, hospital
  helipads (the Mater is just south of the corridor), Phoenix Park and other geozones
  overlap the city**. The corridor sits near the edge of the airport's restriction
  radius — whether a given street is flyable must be checked on the **official IAA
  geozone map** per location, and some or all of it may require authorisation or be
  effectively off-limits to hobby flight.
- **DCC parks require permission** for drone take-off/landing under park byelaws —
  Griffith Park is not a free launch site.
- A1 rules for <250 g allow flight over uninvolved people but **not assemblies**;
  residential privacy matters — plan lines over streets/landmarks, not gardens, and
  don't publish raw imagery of private space.

**Recommendation:** treat drone work as an *enhancement pass* for specific landmark
sites where the geozone map and permissions allow — not as a load-bearing pipeline
step. Tasks 1–6 must not depend on it; task 5 is its designed fallback. If most of the
corridor proves unflyable, nothing in the MVP is lost.

### 8. Micro-structure and street-furniture pass *(serves R3 — post-MVP)*

Fold into tasks 1–2 rather than a separate outing: while sweeping imagery, tag
crossings, signals, post boxes, bus stops, kerb build-outs and parking arrangements in
StreetComplete/Every Door. Defer any dedicated R3 fieldwork until after MVP.

### 9. Tolka channel observations *(serves R0 edge-case + future R5)*

The DTM stops at the water surface. From banks and bridges (no wading): photograph bank
conditions, laser-measure bridge soffit heights and bank-top-to-water distances, and
log observation time against the nearest **OPW hydrometric gauge** reading so water
levels can be tied to datum later.

- **Effort:** one afternoon, combinable with tasks 1/3.

---

## What one or two people should NOT attempt

- **Utility/underground survey (R5):** genuinely requires operators' records and
  professional access — no amateur substitute exists.
- **Authoritative-grade GNSS control networks:** validation yes (task 3); establishing
  survey control, no.
- **Anything requiring private-property access:** rear gardens, rooftops, private
  grounds — the model must be built from public-vantage observation only.
- **Wading/instream work in the Tolka:** safety and permissions both say no.

## Equipment summary

| Item | Cost | Needed for |
|------|------|-----------|
| Smartphone (GNSS + camera) | assumed owned | everything |
| Phone chest/bike mount | ~€20 | task 1 |
| Laser distance measure | ~€30 | tasks 3, 9 |
| Clinometer app (free) + measuring tape | ~€10 | task 4 |
| Action camera | ~€250–350 (optional) | task 1 quality |
| Sub-250 g camera drone | ~€300 (optional, conditional) | task 7 |
| Budget RTK GNSS receiver | ~€300–600 (stretch) | upgrades task 3 |
| Hi-vis vests | ~€10 | roadside credibility and safety |

## Suggested sequencing against releases

| When | Fieldwork |
|------|-----------|
| During R0 | Task 3 (DTM validation), task 6 (establish viewpoints) |
| During R1 | Task 1 (imagery sweep), task 2 (storey-count campaign) |
| During R2 (MVP) | Task 4 (trees), task 5 (first landmarks), task 9 (Tolka) |
| Post-MVP | Task 7 (drone, where legal), task 8 (R3 tagging), repeat 1 & 6 |

Every field observation enters the project through the same traceability schema as
desk data: `source_name = field survey`, observer, date, method, and the photo/track
evidence retained — so ground-truthed objects remain exactly as queryable and traceable
as everything else.
