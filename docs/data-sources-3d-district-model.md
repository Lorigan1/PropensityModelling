# Data Source Register — 3D Phibsborough–Drumcondra District Model

**Project scope:** a navigable, recognisable 3D environment from Griffith Avenue through
the Tolka valley toward Phibsborough, with terrain, buildings, roads, rail, water, trees
and major open spaces in correct X/Y/Z space, each an **individually queryable object
traceable to its underlying source**. Iterations R0 (terrain) → R5 (underground), MVP at
**R2** (urban structure).

**Study area notes:** the corridor lies entirely within the **Dublin City Council (DCC)**
administrative area — Griffith Avenue, Drumcondra, the Tolka valley (Griffith Park),
the Royal Canal cutting, the Maynooth railway line and Phibsborough (Dalymount Park,
Tolka Park). This matters for source selection: local-authority datasets are DCC's, not
Fingal/DLR/SDCC.

This register complements `gsi-dtm-dsm-datasets-dublin.md` (terrain dataset detail).
Compiled September 2026; several portals could not be fetched directly from this
environment (see the verification appendix in the terrain document) — the same caveat
applies to links below marked ⚠.

---

## Traceability model (applies to every object, every release)

The mission statement requires per-object provenance. Recommend every object carries:

| Field | Example (a building in Phibsborough) |
|-------|--------------------------------------|
| `feature_class` | `building` |
| `source_name` | `OpenStreetMap` / `Overture buildings` / `DCC Tree DCC` |
| `source_id` | OSM way ID, Overture **GERS ID**, DCC tree ID, EPA **WFD segment code**, GSI tile ID |
| `source_licence` | `ODbL 1.0` / `CC BY 4.0` |
| `source_vintage` | survey/edit date from the source |
| `retrieval_date` | when the extract was pulled |
| `processing` | e.g. `height = P95(nDSM) within footprint; nDSM = GSI 25cm DSM − OPW 1m DTM` |

Stable upstream IDs exist for almost every class below (OSM element IDs, Overture GERS
IDs, DCC asset IDs, EPA WFD codes) — preserve them rather than minting only internal IDs.

**Licence compatibility:** the stack mixes CC BY 4.0 (Irish government), ODbL (OSM —
**share-alike applies to derived databases**), CDLA-Permissive-2.0 (Overture non-OSM
parts) and EU free-use (Copernicus). Keep source layers separable in the data model so
ODbL share-alike obligations attach only to OSM-derived layers, and emit per-layer
attribution.

---

## R0 — Terrain (ground surface)

| Need | Primary source | Fallback | Access |
|------|---------------|----------|--------|
| Bare-earth DTM | **GSI Open Topographic Data Viewer 1 m DTM** (OPW flood-programme blocks; the Tolka corridor was a flood study area) | OPW Blom 2006–07 **2 m DTM**; Tailte Éireann 10 m DTM | Open (CC BY 4.0) |
| Surface model (input to R1 heights, not for display) | **GSI national 25 cm photogrammetry DSM** | Copernicus GLO-30 (context only) | Open via GSI services ⚠ |

Full detail, ages, and reputation in `gsi-dtm-dsm-datasets-dublin.md`. Trace fields:
GSI/OPW tile ID + survey year. CRS target: ITM (EPSG:2157), Malin Head datum.

## R1 — Urban massing (buildings, roads, water, major land uses)

### Building footprints
- **Primary: OpenStreetMap** — Dublin inner suburbs have essentially complete footprint
  coverage; stable way/relation IDs; ODbL. Extract via Overpass/Geofabrik (Ireland).
- **Alternative: [Overture Maps buildings](https://gee-community-catalog.org/projects/overture_buildings/)** —
  merges OSM + Microsoft/Google ML footprints, adds **GERS IDs** (stable global IDs
  designed exactly for the queryable-object requirement) and `height`/`num_floors`
  attributes where known. Height coverage in Dublin is sparse, so treat heights as
  opportunistic, not primary.
- **Authoritative but RESTRICTED: Tailte Éireann Prime2** (national topographic object
  database — building polygons with authoritative geometry and IDs) and **GeoDirectory**
  (An Post/Tailte — building use, address matching, Eircodes). Licensed products; free
  academic routes exist via university agreements. Label clearly if used.

### Building heights (the Z in "correct X/Y/Z")
- **Primary (open, recommended): derive an nDSM** = GSI 25 cm photogrammetry DSM − R0
  DTM, then assign each footprint a height statistic (e.g. 95th percentile within the
  polygon). All inputs CC BY 4.0; the method is standard and fully traceable in the
  `processing` field.
- **Fallback: [Copernicus Urban Atlas Building Height 2012](https://sdi.eea.europa.eu/catalogue/srv/api/records/14c85db6-ac28-4a91-ad9c-e4356733976d)** —
  10 m raster over Dublin's core, reference year 2012; coarse and dated, adequate only
  for sanity-checking massing.
- **Literature:** a national ML building-height map of Ireland was produced from open
  data — see [*Using machine learning to produce a cost-effective national building
  height map of Ireland to categorise local climate zones*](https://asr.copernicus.org/articles/19/13/2022/)
  (Advances in Science and Research, 19, 13–27, 2022) — useful methodological reference
  for exactly this step.

### Roads
- **Primary: OSM** highway network (centrelines, names, classes, one-way, bridges) —
  Dublin coverage is excellent; ODbL. **Overture transportation** offers the same with
  GERS IDs if you standardise on Overture. Authoritative alternative: Tailte Prime2
  road casings (RESTRICTED).

### Water
- **Primary: EPA/OSi WFD river network** — 1:50,000 river and lake segments with WFD
  segment codes (the Tolka's segments are individually coded), free download from the
  [EPA Geoportal](https://gis.epa.ie/GetData) ⚠. This gives authoritative, traceable
  hydrology objects.
- **Geometry supplement: OSM** water polygons (riverbanks, the Royal Canal, weirs) for
  visual width where the EPA centreline is too abstract.
- **Optional context: OPW flood extents** (floodinfo.ie) for the Tolka floodplain.

### Major land uses
- **Primary: [Copernicus Urban Atlas 2018](https://land.copernicus.eu/en/products/urban-atlas/urban-atlas-2018)** —
  vector land-use polygons for the whole Dublin functional urban area (open, EU);
  classes map well to "major land uses" at massing level.
- **Supplement: OSM** `landuse`/`leisure` polygons; **DCC Development Plan zoning**
  layers via [Smart Dublin / Dublinked](https://data.smartdublin.ie/) ⚠ for the
  statutory view.

## R2 — Urban structure (trees, paths, bridges, railway, parks, pitches)

### Trees
- **Primary: DCC "Tree DCC" dataset** on
  [data.smartdublin.ie](https://data.smartdublin.ie/dataset/tree-dcc) ⚠ — individual
  public/street trees with ID, species, age, condition, stem diameter, spread and
  height: exactly the per-object, source-traceable record the mission requires.
  (The [Trees DLR 2019](https://data.smartdublin.ie/dataset/trees-dlr-2019) equivalent
  is the wrong council for this corridor — noted only for future districts.)
  Verify vintage and whether park trees (Griffith Park) are included.
- **Gap-fill:** private/garden and park canopy from the R1 **nDSM** (local-maxima
  detection on vegetated areas), and the **Urban Atlas Street Tree Layer** (2018) for
  street-canopy polygons. OSM `natural=tree` is sparse but has IDs where present.

### Paths, bridges, railway
- **Primary: OSM** — footways/cycleways (Royal Canal towpath, Tolka riverside paths),
  `bridge=*` objects (Drumcondra Road bridge over the Tolka, canal and rail
  overbridges), and the railway layer (Maynooth/Sligo line through Drumcondra station,
  cuttings and embankments tagged). No open authoritative alternative exists at this
  granularity; Prime2 (RESTRICTED) is the licensed upgrade path.

### Parks and pitches
- **Primary: OSM** `leisure=park` / `leisure=pitch` (Griffith Park, Dalymount Park,
  Tolka Park, school pitches are all mapped as individual objects).
- **Cross-check: DCC parks/green-space datasets** on Smart Dublin ⚠ and Urban Atlas
  green-urban-area polygons.

## R3 — Street structure (beyond MVP — forward notes)

- **DCC open datasets** (Smart Dublin): traffic-signal locations, parking, and related
  street assets are published intermittently — inventory what exists at build time ⚠.
- **OSM**: crossings, traffic signals, street furniture where mapped (variable
  completeness at this level — expect gaps).
- **Street-level imagery for digitising:** Mapillary / KartaView (crowdsourced, open
  licences) along the corridor; Google Street View is **RESTRICTED** (no extraction
  under its terms).

## R4 — Architectural detail (forward notes)

- **Tailte Éireann 15 cm Dublin aerial imagery** (RESTRICTED, licensed) — the corridor
  is inside the 15 cm greater-Dublin block; best orthophoto base for roof forms.
- **Bluesky MetroVista** (RESTRICTED, commercial) — urban mesh/oblique LiDAR if Dublin
  coverage confirms; the open **GSI 25 cm DSM** supports basic roof-form extraction
  (ridge/hip detection) without licence cost.
- The 2015 NYU/UCD city-centre ALS survey **does not reach this corridor** — don't plan
  around it.
- Own capture (drone photogrammetry) is the realistic open path for façades; note IAA
  drone rules in a residential area.

## R5 — Underground / infrastructure (forward notes)

- **Uisce Éireann (Irish Water) networks** — RESTRICTED; access via infrastructure
  enquiries/dig-request processes, typically NDA'd, not republishable.
- **DCC drainage** (Greater Dublin Strategic Drainage Study legacy data) — on request
  to DCC; treat as restricted.
- **GSI open subsurface data** — geotechnical borehole database, groundwater layers and
  Dublin urban geology mapping are open via GSI viewers ⚠ and give legitimate,
  publishable underground context (made ground depth, bedrock, water table) even where
  utility networks stay closed.

---

## Summary: MVP (R0–R2) source stack

| Feature class | Primary source | Licence | Object ID for traceability |
|---------------|---------------|---------|---------------------------|
| Terrain | GSI/OPW 1 m DTM | CC BY 4.0 | GSI tile ID + survey year |
| Building footprints | OSM (or Overture) | ODbL (CDLA for non-OSM Overture parts) | OSM way ID / GERS ID |
| Building heights | nDSM: GSI 25 cm DSM − DTM | CC BY 4.0 | derived — record method + input tiles |
| Roads, paths, bridges, rail | OSM | ODbL | OSM way/node IDs |
| Water | EPA/OSi WFD river network + OSM banks | CC BY 4.0 / ODbL | WFD segment code / OSM ID |
| Land use | Copernicus Urban Atlas 2018 | EU free use | UA polygon ID |
| Trees (public) | DCC Tree dataset (Smart Dublin) | DCC open data (CC BY — verify) | DCC tree ID |
| Trees (canopy gap-fill) | nDSM local maxima + UA Street Tree Layer | CC BY 4.0 / EU | derived — record method |
| Parks, pitches | OSM + DCC parks data | ODbL / CC BY | OSM ID / DCC asset ID |

**The whole MVP is achievable with open data.** Restricted sources (Prime2,
GeoDirectory, Tailte imagery, MetroVista, Uisce Éireann) only become necessary at
R3–R5 or for authoritative-grade geometry, and are labelled RESTRICTED above.

### New links to verify manually (extends the terrain document's appendix)

| Source | Link | Verify |
|--------|------|--------|
| DCC Tree dataset | https://data.smartdublin.ie/dataset/tree-dcc | Vintage, spatial coverage (street vs park trees), licence |
| Smart Dublin portal (parks, zoning, signals) | https://data.smartdublin.ie/ | Current DCC datasets relevant to R2–R3 |
| EPA Geoportal — WFD river network | https://gis.epa.ie/GetData | Tolka segment geometry + codes, licence |
| Urban Atlas 2018 (Dublin FUA) + Street Tree Layer + Building Height 2012 | https://land.copernicus.eu/en/products/urban-atlas | Registration requirements, Dublin tile contents |
| Overture buildings (Dublin extract) | https://overturemaps.org/ | GERS IDs, height attribute coverage in the corridor |
| GSI geotechnical/urban geology viewers | https://www.gsi.ie/en-ie/data-and-maps/ | Borehole density in the corridor (for R5) |
