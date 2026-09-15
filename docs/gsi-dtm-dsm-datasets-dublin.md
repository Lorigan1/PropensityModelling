# GSI DTM/DSM Datasets Covering the Dublin Metropolitan Area

**Scope:** Digital Terrain Model (DTM) and Digital Surface Model (DSM) datasets from
Geological Survey Ireland (GSI) — and datasets distributed through GSI infrastructure —
that cover the whole or parts of the Dublin (Ireland) metropolitan area, with a focus on
terrain, elevation and gradient. Complementary non-GSI datasets are listed separately and
clearly labelled. Primary emphasis is on publicly accessible data; restricted/commercial
datasets are flagged as such.

**Compiled:** September 2026. Coverage footprints and service names change over time —
verify current extents in the GSI viewers before relying on them.

**Terminology:** A **DTM** is a bare-earth model (buildings and vegetation removed) —
the correct input for ground elevation and gradient/slope analysis. A **DSM** includes
buildings, tree canopy and other surface features — useful for built-environment height,
viewshed and solar analysis, but it will distort ground-slope calculations in urban areas.

---

## Summary table

| # | Dataset | Provider / host | Type | Resolution | Survey age | Dublin coverage | Access |
|---|---------|-----------------|------|------------|-----------|-----------------|--------|
| 1 | GSI Open Topographic LiDAR Data (Open Topographic Data Viewer) | GSI + partners | DTM + DSM (GeoTIFF), some point cloud | 0.25 m – 2 m (GSI's own tiles: 1 m) | 2015–2021 (GSI acquisitions); partner data varies | Partial — coastal/urban blocks incl. parts of Dublin city and coast | **Open** (CC BY 4.0) |
| 2 | OPW Blom Coastal Survey 2006–2007 LiDAR (hosted by GSI) | OPW, via GSI | DTM + DSM | 2 m (some 5 m) | 2006–2007 (~20 years old) | East-coast strip incl. Dublin coastline and coastal urban areas | **Open** (CC BY 4.0) |
| 3 | OPW Flood Risk Management (CFRAM/ICPSS/FEM-FRAMS) LiDAR | OPW (floodinfo.ie; also via GSI viewer) | DTM + DSM | 0.25 m / 0.5 m / 1 m / 2 m | Various, ~2006 onwards; released as open data from 2021 | Communities and river corridors incl. Dublin-area catchments | **Open** (CC BY 4.0) / some on request |
| 4 | GSI Photogrammetry DSM, 25 cm (national) | GSI (from national aerial imagery) | DSM (+ hillshade) | 0.25 m | Underlying imagery ca. 2017–2023 (Tailte Éireann national programme) | Effectively full national (ROI) coverage incl. all of Dublin | **Open** (view/WMS + TIFF via GSI services) |
| 5 | INFOMAR seabed bathymetry (Dublin Bay) | GSI + Marine Institute | Bathymetric DTM | 2 m (survey legs); 5/10/25 m merged | 1996, 2000–2022, ongoing to 2026 | Dublin Bay, Killiney to Howth | **Open** |
| 6 | 2015 Aerial Laser & Photogrammetry Survey of Dublin City | UCD/NYU (Laefer et al.) — *not GSI* | ALS point cloud + DSM/DTM rasters | ~300+ pts/m²; 1 m rasters | March 2015 | ~2 km² of Dublin city centre only | **Open** (NYU Spatial Data Repository) |
| 7 | Bluesky Ireland national DTM/DSM | Bluesky (commercial) — *not GSI* | DTM + DSM | ~1 m–5 m products | Rolling updates (imagery 2017+) | Full Dublin coverage | **Restricted — commercial licence** |
| 8 | Tailte Éireann (formerly OSi) height data | Tailte Éireann — *not GSI* | DTM (10 m national; finer under licence) | 10 m (±1.5 m vertical) | Periodically updated | Full Dublin coverage | **Restricted — licensed** (INSPIRE view service free to view) |
| 9 | Copernicus DEM GLO-30 / EU-DEM | ESA/EEA — *not GSI* | DSM-like DEM | 25–30 m | TanDEM-X 2011–2015 | Full coverage | **Open** |

---

## 1. GSI Open Topographic LiDAR Data — Open Topographic Data Viewer

- **Source:** [GSI Open Topographic Data Viewer announcement](https://www.gsi.ie/en-ie/events-and-news/news/Pages/Open-Topographic-Data-Viewer.aspx) · [download viewer app](https://dcenr.maps.arcgis.com/apps/webappviewer/index.html?id=b7c4b0e763964070ad69bf8c1572c9f5) · [dataset record on the national open-data hub](https://opendata-geodata-gov-ie.hub.arcgis.com/datasets/ie-gsi-open-topographic-lidar-data-ireland-itm-download-viewer) · [data.gov.ie record](https://data.gov.ie/dataset/open-topographic-lidar-data)
- **What it is:** GSI's central portal (launched 2018) for open Irish LiDAR elevation data.
  It aggregates DTM and DSM rasters (GeoTIFF, Irish Transverse Mercator) from GSI and
  roughly seven partner organisations: the National Monuments Service, National Parks and
  Wildlife Service, The Discovery Programme/Heritage Council, Transport Infrastructure
  Ireland (TII), the OPW and others. GSI's own LiDAR tiles are 1 m grid; partner data
  ranges from 0.25 m to 2 m.
- **Age:** GSI's own LiDAR acquisitions in the viewer were collected between **2015 and
  2021**; partner datasets range from 2006 to the 2020s. Per-tile survey dates are given
  in the viewer's coverage layers (e.g. the
  [LiDAR coverage index layers](https://opendata-geodata-gov-ie.hub.arcgis.com/datasets/ie-gsi-lidar-coverage-gsi-dchg-dp-ireland-roi-itm-view/about)).
- **Dublin coverage:** Partial, not blanket. Coverage is a mosaic of coastal and urban
  survey blocks plus heritage/infrastructure sites; the Dublin area is covered mainly
  through coastal strips, OPW flood-study blocks over the city and its river corridors,
  and TII scheme corridors. Check the coverage layer for the exact current footprint.
- **Suitability:** The 1 m DTM tiles are the best open bare-earth source for elevation
  and gradient work where they exist; matching DSM tiles support building/vegetation
  height analysis.
- **Access:** Free download, no registration, **Creative Commons Attribution 4.0 (CC BY 4.0)**.
- **Reputation:** **Trusted / authoritative source.** GSI, founded 1845, is
  [Ireland's national Earth-science agency](https://www.gov.ie/en/department-of-climate-energy-and-the-environment/policy-information/geological-survey-ireland/),
  a division of the Department of the Environment, Climate and Communications, and a
  registered publisher on the official national open-data portal
  ([data.gov.ie](https://data.gov.ie/organization/geological-survey-of-ireland)).

## 2. OPW Blom Coastal Survey 2006–2007 LiDAR (hosted by GSI)

- **Source:** [Coverage record on the national open-data hub](https://opendata-geodata-gov-ie.hub.arcgis.com/datasets/ie-gsi-lidar-coverage-office-of-public-works-opw-blom-coastal-survey-2006-2007-ireland-roi-itm-view) · [GSI GeoData portal item](https://gsi.geodata.gov.ie/portal/home/item.html?id=abad0663144c44ab896d3e0e9a46d579)
- **What it is:** Airborne LiDAR flown by Blom for the OPW's Irish Coastal Protection
  Strategy Study (ICPSS) and related flood programmes, released openly through the GSI
  Open Topographic Data Viewer. DTM and DSM at **2 m** grid (some areas 5 m).
- **Age:** **2006–2007** — now ~20 years old. Predates substantial Dublin development
  (docklands build-out, new road/rail infrastructure), so treat surface features with
  caution; bare-earth terrain is more stable but coastal morphology has changed in places.
- **Dublin coverage:** The survey covered the main urban areas and much of the east and
  south-east coastline, **including the Dublin coastal strip** (broadly Balbriggan to
  Bray along the coast, extending inland over low-lying flood-relevant land).
- **Suitability:** Usable for coarse terrain/gradient over the coastal metropolitan
  strip; superseded by newer 1 m data where available.
- **Access:** **Open**, CC BY 4.0, via the GSI viewer.
- **Reputation:** Trusted government sources (OPW is the State's lead flood-risk
  management body; distribution via GSI).

## 3. OPW Flood Risk Management LiDAR (CFRAM / FEM-FRAMS / ICPSS programmes)

- **Source:** [OPW press release — LiDAR released as open data](https://www.gov.ie/en/office-of-public-works/press-releases/opw-releases-lidar-captured-as-part-of-flood-risk-management-projects-as-open-data/) (July 2021) · [floodinfo.ie Open Spatial Data Portal](https://www.floodinfo.ie/open-spatial-data-portal/) · [aerial survey data finder](https://www.floodinfo.ie/open-spatial-data-portal/aerial-survey-imagery-data-finder/)
- **What it is:** LiDAR captured for the Catchment Flood Risk Assessment and Management
  (CFRAM) programme and related studies. Primary deliverables include **0.25 m, 0.5 m,
  1 m and 2 m DSMs and DTMs** over "Areas for Further Assessment" — i.e. towns, cities
  and river corridors at flood risk.
- **Age:** Surveys span roughly 2006 onwards (CFRAM surveys largely 2011–2016); released
  as open data from July 2021. Per-block dates are listed in the floodinfo.ie data finder.
- **Dublin coverage:** Dublin city and suburbs were CFRAM study areas (Liffey, Tolka,
  Dodder, Camac and coastal cells), so high-resolution DTM/DSM blocks exist over much of
  the built-up metropolitan area and its river corridors.
- **Suitability:** Purpose-built for terrain/hydraulic modelling — the DTMs are
  well-suited to elevation and gradient analysis in the covered blocks.
- **Access:** **Open** (CC BY 4.0) for the released blocks via floodinfo.ie and the GSI
  viewer; some additional survey areas are supplied **on request** (flood_data@opw.ie) —
  effectively open but not self-service.
- **Reputation:** Trusted government source (OPW), distributed via official State portals.

## 4. GSI National Photogrammetry DSM, 25 cm

- **Source:** [Dataset record: IE GSI Photogrammetry Digital Surface Model (DSM) Hillshade 25cm Ireland (ROI) ITM](https://hub.arcgis.com/datasets/geodata-gov-ie::ie-gsi-photogrammetry-digital-surface-model-dsm-hillshade-25cm-ireland-roi-itm-mh-tiff) · [GSI image service (WMS/REST)](https://gsi.geodata.gov.ie/imagehost/rest/services/Lidar/IE_GSI_Photogrammetry_DSM_HS_GSI_25cm_IE26_ITM_MH_TIFF/ImageServer)
- **What it is:** A **25 cm grid DSM** (with derived hillshade) produced by
  photogrammetry from national aerial imagery, published as GeoTIFF/WMS through GSI's
  GeoData image services. The underlying national imagery programme (Tailte Éireann
  Series 3) was captured **2017–2023**, with 15 cm imagery over the greater Dublin area
  (out to Ashbourne, Naas, Dunshaughlin, Maynooth and Bray) — see
  [Tailte Éireann aerial imagery](https://tailte.ie/map-shop/professional-map-products/aerial-imagery-maps-and-data/).
- **Age:** Recent — a 2020s product; verify per-tile acquisition dates in the service
  metadata.
- **Dublin coverage:** Effectively **complete coverage** of the Dublin metropolitan area
  (national ROI product).
- **Suitability:** Excellent for surface morphology, building heights and fine-grained
  hillshade; as a **DSM** it is *not* bare-earth, so derive ground gradients from a DTM
  instead, or use this only in open unvegetated terrain.
- **Access:** **Open** to view and consume via GSI's public map/image services; bulk
  raster download availability should be confirmed on the GSI GeoData platform.
- **Reputation:** Trusted / authoritative (official GSI publication channel).

## 5. INFOMAR Bathymetric DTMs — Dublin Bay (GSI + Marine Institute)

- **Source:** [INFOMAR data access and download](https://www.infomar.ie/data) · [data.gov.ie record — INFOMAR Seabed Survey Bathymetry (Multibeam & LiDAR)](https://data.gov.ie/dataset/infomar-seabed-survey-bathymetry-multi-beam-and-lidar) · [Dublin Bay Blue Scale map news item](https://infomar.ie/node/574)
- **What it is:** Ireland's national seabed-mapping programme, a joint venture of **GSI
  and the Marine Institute**. Provides bathymetric DTMs: **2 m** resolution survey-leg
  data and **5 m / 10 m / 25 m** merged surfaces, plus backscatter and shaded relief.
  A high-resolution "Blue Scale" map covers **Dublin Bay from Killiney to Howth**.
- **Age:** Data collected 1996 and 2000–2022, with infill mapping continuing to ~2026.
- **Dublin coverage:** Dublin Bay and adjacent coastal waters (the marine side of the
  metropolitan area). Relevant where "terrain" extends below the low-water mark, e.g.
  coastal gradient, flooding and erosion studies.
- **Access:** **Open** download via the INFOMAR/GSI data portals (open standard formats).
- **Reputation:** **Trusted source** — flagship State programme, frequently described as
  one of the world's largest civilian seabed-mapping programmes; data feeds the
  EU EMODnet bathymetry DTM.

## 6. 2015 Aerial Laser and Photogrammetry Survey of Dublin City *(not GSI — academic)*

- **Source:** [NYU Spatial Data Repository collection record](https://geo.nyu.edu/catalog/nyu-2451-38684) · [NYU Faculty Digital Archive](https://archive.nyu.edu/handle/2451/38684) · [DublinCity derivative (V-SENSE, TCD)](https://v-sense.scss.tcd.ie/dublincity/)
- **What it is:** An exceptionally dense urban ALS + photogrammetry dataset over
  **~2 km² of Dublin city centre**, collected in **March 2015** (41 flight paths,
  >1.4 billion points, average density ~250–348 pts/m², flying height 300 m). Includes
  LAZ/LAS point clouds, full-waveform data, orthophotos and oblique imagery; 1 m DSM/DTM
  rasters have been derived from it.
- **Literature citations:**
  - Laefer, D. F., Abuwarda, S., Vo, A.-V., Truong-Hong, L., & Gharibi, H. (2017).
    *2015 Aerial Laser and Photogrammetry Survey of Dublin City Collection Record.*
    NYU Spatial Data Repository / Faculty Digital Archive.
  - Zolanvari, S. M. I., Ruano, S., Rana, A., Cummins, A., da Silva, R. E., Rahbar, M.,
    & Smolic, A. (2019). *DublinCity: Annotated LiDAR Point Cloud and its Applications.*
    BMVC 2019 — an annotated benchmark derived from this survey.
- **Age:** 2015 (city centre has changed since — cranes, docklands construction).
- **Suitability:** Unmatched detail for the covered 2 km²; too small a footprint for
  metropolitan-scale terrain work, but a benchmark for methods development.
- **Access:** **Open** via NYU Spatial Data Repository.
- **Reputation:** Widely cited academic reference dataset (one of the densest urban
  aerial LiDAR datasets ever published); UCD-led, ERC-funded, hosted by NYU Libraries.

## 7. Bluesky Ireland National DTM/DSM *(not GSI — RESTRICTED / commercial)*

- **Source:** [Bluesky Ireland standard height data](https://www.bluesky-world.ie/standard-height-data) · [Bluesky map shop height data](https://ireland.blueskymapshop.com/products/height-data)
- **What it is:** Photogrammetrically derived national DTM and DSM products (roughly
  1–5 m posting depending on product) from Bluesky's rolling aerial survey programme;
  full, regularly refreshed Dublin coverage.
- **Age:** Rolling updates; recent-epoch data available for Dublin.
- **Access:** **RESTRICTED — commercial licence** (academic access sometimes available
  via institutions, e.g. UCD holds licensed Bluesky 1 m DTM/DSM tiles for Dublin).
- **Reputation:** Established commercial aerial-survey supplier; flies the national
  imagery programme used by Tailte Éireann — high quality, but not open.

## 8. Tailte Éireann (formerly Ordnance Survey Ireland) Height Data *(not GSI — RESTRICTED)*

- **Source:** [Tailte Éireann professional map products](https://store.tailte.ie/professional-products/land-and-property.html) · [Tailte Éireann DEM 10m INSPIRE view service](https://inspire-geoportal.ec.europa.eu/srv/api/records/%7B0CD532EA-1AD7-44CE-8AAE-7E5A3F586C16%7D) · [UCD guide to requesting Tailte Éireann data](https://libguides.ucd.ie/gisguide/RequestTailteEireannDigitalData)
- **What it is:** The national mapping agency's height products — a national **10 m DTM
  (vertical accuracy ±1.5 m)**, with finer photogrammetric height data available under
  licence. Full Dublin coverage.
- **Age:** Periodically updated from the national aerial survey (Series 3: 2017–2023).
- **Access:** **RESTRICTED — licensed products** (an INSPIRE-compliant 10 m DEM *view*
  service is freely viewable; free supply to Irish universities via agreement).
- **Reputation:** **Trusted / authoritative** — the State's national mapping authority
  (established 2023 by merger of OSi, PRA and the Valuation Office).

## 9. Copernicus DEM GLO-30 / EU-DEM *(not GSI — open, coarse)*

- European open DEMs (25–30 m, DSM-like, based on TanDEM-X 2011–2015 data) cover all of
  Dublin. Useful only for broad-scale elevation and gradient context; far coarser than
  any of the Irish sources above. Provider: ESA/European Environment Agency (trusted
  institutional source).

---

## Practical notes for terrain / elevation / gradient work in Dublin

1. **Bare-earth first:** For gradient/slope, use DTMs (datasets 1–3, 8); using the 25 cm
   photogrammetry DSM (4) or any DSM in built-up Dublin will contaminate slope rasters
   with building edges.
2. **Best open combination (2026):** GSI Open Topographic Viewer 1 m DTM tiles + OPW
   flood-programme DTM blocks for the urban core and river corridors, gap-filled with the
   OPW 2006–07 coastal 2 m DTM, and Tailte Éireann 10 m DTM (or Copernicus 30 m) for the
   remaining gaps. INFOMAR bathymetry extends the model into Dublin Bay.
3. **Watch the vertical datum and CRS:** Irish open elevation data is generally on the
   Malin Head vertical datum, ITM (EPSG:2157) horizontal; older tiles may differ — check
   per-tile metadata.
4. **Age matters in Dublin:** Between 2006 and 2026 the metropolitan area changed
   substantially. Ground terrain is fairly stable, but land re-profiling, port and
   docklands works, and new road/rail earthworks mean older DTMs (dataset 2 especially)
   should be cross-checked against recent imagery for any site-specific work.
5. **Coverage verification:** GSI's LiDAR holdings are a mosaic, not blanket coverage.
   Always consult the coverage-index layers in the
   [Open Topographic Data Viewer](https://dcenr.maps.arcgis.com/apps/webappviewer/index.html?id=b7c4b0e763964070ad69bf8c1572c9f5)
   for the exact Dublin footprint of each acquisition.

## Source-reputation summary

| Source | Reputation |
|--------|------------|
| Geological Survey Ireland (GSI) | Trusted — national Earth-science agency (est. 1845), division of the Department of the Environment, Climate and Communications; official open-data publisher |
| Office of Public Works (OPW) | Trusted — State lead body for flood risk management |
| INFOMAR (GSI + Marine Institute) | Trusted — flagship national seabed-mapping programme; contributes to EU EMODnet |
| Tailte Éireann | Trusted — national mapping authority (restricted/licensed data) |
| NYU/UCD 2015 Dublin survey (Laefer et al.) | Reputable academic source; widely cited benchmark dataset |
| Bluesky Ireland | Established commercial supplier (restricted/commercial data) |
| ESA/EEA (Copernicus) | Trusted institutional source (coarse resolution) |
