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
| 10 | FABDEM v1.2 | Univ. of Bristol / Fathom — *not GSI* | Bare-earth DTM (corrected GLO-30) | 30 m | Based on 2011–2015 TanDEM-X | Full coverage | **Open, non-commercial only** (CC BY-NC-SA 4.0) |
| 11 | SRTM 1-arcsec / NASADEM | NASA/USGS — *not GSI* | DSM-like DEM | ~30 m | February 2000 | Full coverage | **Open** (public domain) |
| 12 | ALOS World 3D (AW3D30) / ASTER GDEM v3 | JAXA / NASA-METI — *not GSI* | DSM | ~30 m | Imagery 2006–2011 / 2000–2013 | Full coverage | **Open** (attribution) |
| 13 | MERIT DEM | Yamazaki Lab, Univ. of Tokyo — *not GSI* | Error-corrected DTM-like DEM | ~90 m | Based on SRTM (2000) | Full coverage | **Open, non-commercial** (registration) |
| 14 | DeltaDTM v1.1 | Deltares / TU Delft — *not GSI* | Coastal bare-earth DTM | ~30 m (1 arcsec) | Published 2024 (ICESat-2 era) | Coastal lowlands of Dublin | **Open** (CC BY 4.0) |
| 15 | CoastalDEM | Climate Central — *not GSI* | Coastal DTM (ML-corrected SRTM) | 30 m (1 arcsec) | Based on SRTM (2000) | Coastal lowlands of Dublin | **Restricted** — free for non-commercial research via licence request |
| 16 | EMODnet Bathymetry DTM / GEBCO | EMODnet consortium / GEBCO — *not GSI* | Bathymetric DTM | ~115 m / ~450 m | Compilations, updated to 2020s | Dublin Bay and Irish Sea | **Open** |
| 17 | ICESat-2 ATL08/ATL03 | NASA — *not GSI* | Spaceborne laser altimetry (profiles, not a raster) | ~100 m segments along track | 2018–present, ongoing | Sparse tracks across Dublin | **Open** |
| 18 | WorldDEM Neo / Bluesky MetroVista | Airbus / Bluesky — *not GSI* | DSM+DTM / 3D mesh & LiDAR city model | 5 m / ~10 cm-class | Neo: 2017+ radar; MetroVista: recent urban flights | Full / Dublin city | **Restricted — commercial** |

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

## 10. FABDEM v1.2 — Forest And Buildings removed Copernicus DEM *(not GSI — open, non-commercial)*

- **Source:** [FABDEM v1.2 at the University of Bristol data repository](https://research-information.bris.ac.uk/en/datasets/fabdem-v1-2/) · [commercial successor FABDEM+ (Fathom)](https://www.fathom.global/product/global-terrain-data-fabdem/)
- **What it is:** A global **30 m bare-earth DTM** created by machine-learning removal of
  forest and building bias from Copernicus GLO-30. Validation shows mean absolute
  vertical error reduced from 1.61 m to 1.12 m in built-up areas and from 5.15 m to
  2.88 m in forests versus GLO-30 — a significant improvement for terrain/gradient work
  at metropolitan scale in a built environment like Dublin.
- **Literature citation:** Hawker, L., Uhe, P., Paulo, L., Sosa, J., Savage, J.,
  Sampson, C., & Neal, J. (2022). *A 30 m global map of elevation with forests and
  buildings removed.* Environmental Research Letters, 17(2), 024016.
- **Age:** Derived from TanDEM-X data acquired 2011–2015; v1.2 released 2023.
- **Access:** **Open for non-commercial use only** (CC BY-NC-SA 4.0); commercial use
  requires the licensed Fathom product (FABDEM+).
- **Reputation:** Reputable academic source (University of Bristol hydrology group /
  Fathom); peer-reviewed and independently validated; widely adopted in flood modelling.

## 11. SRTM 1-arcsecond / NASADEM *(not GSI — open)*

- **Source:** [USGS EarthExplorer](https://earthexplorer.usgs.gov/) / NASA Earthdata.
- **What it is:** The February **2000** Shuttle Radar Topography Mission DEM (~30 m,
  DSM-like radar surface), and its 2020 reprocessing **NASADEM**. Public domain, full
  Dublin coverage.
- **Literature citation:** Farr, T. G., et al. (2007). *The Shuttle Radar Topography
  Mission.* Reviews of Geophysics, 45, RG2004.
- **Suitability/age:** A quarter-century old and coarse; superseded by Copernicus
  GLO-30/FABDEM for most purposes, but remains a common baseline in literature.
- **Reputation:** Trusted (NASA/USGS); one of the most-cited elevation datasets in the
  scientific literature.

## 12. ALOS World 3D (AW3D30) and ASTER GDEM v3 *(not GSI — open)*

- **Source:** [JAXA AW3D30 portal](https://www.eorc.jaxa.jp/ALOS/en/dataset/aw3d30/aw3d30_e.htm) · NASA/METI ASTER GDEM v3 via Earthdata.
- **What they are:** ~30 m global photogrammetric **DSMs**: AW3D30 from ALOS PRISM
  stereo imagery (2006–2011, v3.x), ASTER GDEM v3 from ASTER stereo (2000–2013 imagery,
  released 2019). Both fully cover Dublin; both are surface models with building/canopy
  bias in urban areas.
- **Reputation:** Trusted space-agency sources (JAXA; NASA/METI). AW3D30 generally
  validates better than ASTER GDEM and is widely used where Copernicus DEM licensing or
  artefacts are a concern.

## 13. MERIT DEM *(not GSI — open, non-commercial)*

- **Source:** [MERIT DEM, Yamazaki Lab, University of Tokyo](http://hydro.iis.u-tokyo.ac.jp/~yamadai/MERIT_DEM/)
- **What it is:** A ~90 m error-corrected DEM (stripe noise, speckle, tree-height bias
  removed from SRTM/AW3D), designed for hydrography and terrain analysis.
- **Literature citation:** Yamazaki, D., et al. (2017). *A high-accuracy map of global
  terrain elevations.* Geophysical Research Letters, 44, 5844–5853.
- **Access:** Free for research/education after registration; **non-commercial**.
- **Suitability:** Too coarse for intra-urban Dublin work; relevant mainly as the basis
  of global hydrological products (MERIT Hydro flow directions and river networks).

## 14. DeltaDTM v1.1 — global coastal DTM *(not GSI — open)*

- **Source:** [DeltaDTM paper (open access)](https://www.ncbi.nlm.nih.gov/pmc/articles/PMC10917791/); data distributed openly by Deltares (also mirrored on cloud platforms).
- **What it is:** A 1-arcsecond (~30 m) **bare-earth DTM of global coastal lowlands**
  (terrain below ~10 m elevation), built from Copernicus DEM corrected with ICESat-2 and
  GEDI spaceborne LiDAR. Covers Dublin's low-lying coastal strip — the zone most relevant
  to coastal flood exposure work.
- **Literature citation:** Pronk, M., Hooijer, A., Eilander, D., Haag, A., de Jong, T.,
  Vousdoukas, M., Vernimmen, R., Ledoux, H., & Eleveld, M. (2024). *DeltaDTM: A global
  coastal digital terrain model.* Scientific Data, 11, 273.
- **Access:** **Open** (CC BY 4.0).
- **Reputation:** Reputable applied-research institute (Deltares, with TU Delft);
  peer-reviewed in Scientific Data.

## 15. CoastalDEM *(not GSI — RESTRICTED for commercial use)*

- **Source:** [Climate Central CoastalDEM](https://www.climatecentral.org/coastaldem)
- **What it is:** A 30 m coastal DTM produced by neural-network correction of SRTM,
  widely used in sea-level-rise exposure studies (including headlines about Dublin's
  coastal flood exposure).
- **Literature citation:** Kulp, S. A., & Strauss, B. H. (2018). *CoastalDEM: A global
  coastal digital elevation model improved from SRTM using a neural network.* Remote
  Sensing of Environment, 206, 231–239.
- **Access:** **Restricted** — free licence for non-commercial research on request;
  commercial use licensed. Based on 2000-era SRTM, so ageing.
- **Reputation:** Reputable non-profit research organisation; peer-reviewed method, though
  later products (FABDEM, DeltaDTM) generally validate better.

## 16. EMODnet Bathymetry DTM and GEBCO *(not GSI — open, marine)*

- **Source:** [EMODnet Bathymetry portal](https://emodnet.ec.europa.eu/en/bathymetry) · [GEBCO gridded bathymetry](https://www.gebco.net/data_and_products/gridded_bathymetry_data/)
- **What they are:** Harmonised European seabed DTM (~1/16 arc-minute, ~115 m; INFOMAR is
  a principal contributor for Irish waters) and the ~15 arcsecond global GEBCO grid.
  Both cover Dublin Bay and the Irish Sea; use INFOMAR (dataset 5) where available, as it
  is the higher-resolution source these compilations draw on.
- **Access:** **Open**.
- **Reputation:** Trusted — EU-funded consortium (EMODnet) and the IHO/IOC-backed GEBCO
  programme.

## 17. ICESat-2 laser altimetry (ATL03/ATL08) *(not GSI — open, validation)*

- **Source:** [NASA ICESat-2 data at NSIDC](https://nsidc.org/data/icesat-2)
- **What it is:** Spaceborne photon-counting laser altimetry (2018–present) providing
  sparse but very accurate ground-elevation profiles along satellite tracks crossing the
  Dublin area. Not a raster DEM — its role is **independent validation/bias correction**
  of the DTM/DSM rasters above (this is how FABDEM and DeltaDTM were built). Note that
  GEDI, the other spaceborne LiDAR, does *not* cover Dublin (coverage limited to ±51.6°
  latitude).
- **Access:** **Open** (NASA Earthdata).
- **Reputation:** Trusted (NASA).

## 18. Commercial high-resolution alternatives *(not GSI — RESTRICTED)*

- **Airbus WorldDEM Neo** — 5 m global DSM/DTM from TanDEM-X radar (2017 onwards);
  full Dublin coverage; commercial licence. ([Airbus intelligence](https://intelligence.airbus.com/imagery/reference-layers/worlddem-neo/))
- **Bluesky MetroVista** — aircraft-flown urban 3D mesh and high-density LiDAR programme
  covering major cities in Britain and Ireland, including Dublin city; ~10 cm-class
  detail; commercial licence. ([Bluesky MetroVista](https://www.bluesky-world.com/metrovista))
- **Maxar Precision3D and similar** — satellite-photogrammetry DSM/DTM (~0.5 m) available
  on order; commercial licence.
- **Reputation:** Established commercial suppliers; quality is high but data is closed —
  label any derived outputs accordingly.

## 19. Dublinked / Smart Dublin regional open-data portal *(not GSI — open, no primary DEMs)*

- **Source:** [Dublinked / Smart Dublin](https://www.dublincity.ie/business/economic-development-and-enterprise/smart-cities/dublinked)
- **What it is:** The open-data platform of the four Dublin local authorities (~300
  datasets). It does **not** currently host a primary DTM/DSM — Dublin local-authority
  elevation data reaches the public through the GSI viewer and OPW portals instead — but
  it is worth monitoring for derived terrain products (e.g. flood, drainage and
  building-height layers) and for context data used alongside elevation modelling.
- **Reputation:** Trusted — official local-government open-data initiative.

---

## Practical notes for terrain / elevation / gradient work in Dublin

1. **Bare-earth first:** For gradient/slope, use DTMs (datasets 1–3, 8); using the 25 cm
   photogrammetry DSM (4) or any DSM in built-up Dublin will contaminate slope rasters
   with building edges.
2. **Best open combination (2026):** GSI Open Topographic Viewer 1 m DTM tiles + OPW
   flood-programme DTM blocks for the urban core and river corridors, gap-filled with the
   OPW 2006–07 coastal 2 m DTM, and Tailte Éireann 10 m DTM (or Copernicus 30 m) for the
   remaining gaps. INFOMAR bathymetry extends the model into Dublin Bay. For
   metropolitan-scale gradient work in a single consistent raster, **FABDEM (30 m,
   non-commercial)** is the best open bare-earth compromise; use **DeltaDTM** on the
   coastal strip and **ICESat-2** profiles to validate whichever mosaic you build.
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

## Appendix: links requiring manual verification

This document was compiled in a sandboxed environment whose network proxy **blocked
direct access to several source sites** (notably `data.gov.ie`, `gsi.geodata.gov.ie`,
`opendata-geodata-gov-ie.hub.arcgis.com`, `libguides.ucd.ie` and `geo.nyu.edu`). Details
for those sources were corroborated from search-result content only. The links below
should be opened manually to confirm the stated coverage, survey dates, licence terms
and download availability.

### Confirmed blocked in this session (highest priority to verify)

| Dataset | Link | What to verify |
|---------|------|----------------|
| GSI Open Topographic LiDAR Data (data.gov.ie record) | https://data.gov.ie/dataset/open-topographic-lidar-data | Current resolutions, survey-year range, licence, last-updated date |
| GSI Open Topographic LiDAR download viewer (open-data hub record) | https://opendata-geodata-gov-ie.hub.arcgis.com/datasets/ie-gsi-open-topographic-lidar-data-ireland-itm-download-viewer | Exact Dublin tile footprint; contributing organisations |
| GSI LiDAR coverage index layer | https://opendata-geodata-gov-ie.hub.arcgis.com/datasets/ie-gsi-lidar-coverage-gsi-dchg-dp-ireland-roi-itm-view/about | Per-block survey dates over the Dublin area |
| OPW Blom Coastal Survey 2006–07 coverage layer | https://opendata-geodata-gov-ie.hub.arcgis.com/datasets/ie-gsi-lidar-coverage-office-of-public-works-opw-blom-coastal-survey-2006-2007-ireland-roi-itm-view | Dublin coastal extent; 2 m vs 5 m cell areas |
| GSI 25 cm photogrammetry DSM — service metadata | https://gsi.geodata.gov.ie/imagehost/rest/services/Lidar/IE_GSI_Photogrammetry_DSM_HS_GSI_25cm_IE26_ITM_MH_TIFF/ImageServer/info/metadata | Acquisition dates, lineage (source imagery), licence, whether raw DSM (not just hillshade) is downloadable |
| GSI 25 cm photogrammetry DSM — hub record | https://hub.arcgis.com/datasets/geodata-gov-ie::ie-gsi-photogrammetry-digital-surface-model-dsm-hillshade-25cm-ireland-roi-itm-mh-tiff | Same as above |
| 2015 Dublin City ALS survey (NYU Spatial Data Repository) | https://geo.nyu.edu/catalog/nyu-2451-38684 | Licence wording, DOI, exact deliverables (DSM/DTM rasters vs point cloud only) |
| 2015 Dublin City ALS survey (NYU archive mirror) | https://archive.nyu.edu/handle/2451/38684 | Same as above |
| UCD LibGuide — LiDAR & remote sensing for Ireland | https://libguides.ucd.ie/gisguide/LiDAR | Institutional Bluesky 1 m DTM/DSM holdings for Dublin; access conditions |

### Not fetched directly — verified via search snippets only

| Dataset | Link | What to verify |
|---------|------|----------------|
| GSI Open Topographic Data Viewer (announcement) | https://www.gsi.ie/en-ie/events-and-news/news/Pages/Open-Topographic-Data-Viewer.aspx | Programme description, partner list |
| GSI Open Topographic Data Viewer (application) | https://dcenr.maps.arcgis.com/apps/webappviewer/index.html?id=b7c4b0e763964070ad69bf8c1572c9f5 | Interactive check of Dublin coverage and per-tile metadata |
| OPW open-data LiDAR press release (July 2021) | https://www.gov.ie/en/office-of-public-works/press-releases/opw-releases-lidar-captured-as-part-of-flood-risk-management-projects-as-open-data/ | Which survey blocks were released; licence |
| OPW floodinfo.ie Open Spatial Data Portal | https://www.floodinfo.ie/open-spatial-data-portal/ | Dublin-area LiDAR blocks, resolutions, request procedure |
| OPW aerial survey data finder | https://www.floodinfo.ie/open-spatial-data-portal/aerial-survey-imagery-data-finder/ | Per-survey dates and deliverables (0.25/0.5/1/2 m DSM+DTM) |
| INFOMAR data download portal | https://www.infomar.ie/data | Dublin Bay bathymetry resolutions and survey years |
| INFOMAR bathymetry record (data.gov.ie) | https://data.gov.ie/dataset/infomar-seabed-survey-bathymetry-multi-beam-and-lidar | Licence (CC BY?), formats |
| Tailte Éireann aerial imagery / height products | https://tailte.ie/map-shop/professional-map-products/aerial-imagery-maps-and-data/ | Series 3 capture years (2017–2023), 15 cm Dublin extent |
| Tailte Éireann 10 m DEM INSPIRE view service | https://inspire-geoportal.ec.europa.eu/srv/api/records/%7B0CD532EA-1AD7-44CE-8AAE-7E5A3F586C16%7D | Service status, licence, accuracy statement |
| Bluesky Ireland height data | https://www.bluesky-world.ie/standard-height-data | Product resolutions, update epochs, Dublin coverage |
| Bluesky MetroVista | https://www.bluesky-world.com/metrovista | Whether Dublin city is in the current MetroVista programme |
| FABDEM v1.2 repository | https://research-information.bris.ac.uk/en/datasets/fabdem-v1-2/ | Licence (CC BY-NC-SA 4.0), version, tile download |
| MERIT DEM | http://hydro.iis.u-tokyo.ac.jp/~yamadai/MERIT_DEM/ | Registration and licence terms |
| DeltaDTM paper / data | https://www.ncbi.nlm.nih.gov/pmc/articles/PMC10917791/ | Data-repository link and licence in the paper's Data Availability section |
| CoastalDEM | https://www.climatecentral.org/coastaldem | Current licence request process |
| EMODnet Bathymetry | https://emodnet.ec.europa.eu/en/bathymetry | Current DTM release and resolution |
| Dublinked / Smart Dublin | https://www.dublincity.ie/business/economic-development-and-enterprise/smart-cities/dublinked | Whether any terrain-derived datasets have since been published |

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
| NASA / USGS (SRTM, NASADEM, ICESat-2) | Trusted space/science agencies; SRTM among the most-cited elevation datasets |
| JAXA / NASA-METI (AW3D30, ASTER GDEM) | Trusted space agencies (open DSMs) |
| University of Bristol / Fathom (FABDEM) | Reputable academic source; peer-reviewed (Hawker et al. 2022), independently validated; non-commercial licence |
| Yamazaki Lab, Univ. of Tokyo (MERIT) | Reputable academic source; peer-reviewed (Yamazaki et al. 2017); non-commercial |
| Deltares / TU Delft (DeltaDTM) | Reputable applied-research institute; peer-reviewed (Pronk et al. 2024) |
| Climate Central (CoastalDEM) | Reputable non-profit; peer-reviewed (Kulp & Strauss 2018); restricted licence |
| EMODnet / GEBCO | Trusted EU consortium and IHO/IOC programme (marine) |
| Airbus / Maxar | Established commercial suppliers (restricted data) |
| Dublinked / Smart Dublin | Trusted local-government open-data initiative (no primary DEMs) |
