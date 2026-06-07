# Joint Health and Education Service Desert Mapping

**Country:** Ghana
**CRS:** EPSG:25000 - Leigon / Ghana Metre Grid
**Project file:** `Joint-Health-Edu-Desert.qgz`

---

## Overview

This project identifies settlements in Ghana that are simultaneously beyond the service reach of both health facilities and education facilities. Individual 5 km catchment buffers are generated for each sector, and settlements outside both coverage zones are classified as joint service deserts. This dual-sector desert classification represents the most underserved communities where neither health nor education infrastructure is proximally accessible.

---

## Objectives

- Generate 5 km service catchment buffers around health facilities.
- Generate 5 km service catchment buffers around education facilities.
- Identify settlements outside both catchment zones as joint service deserts.
- Tag all settlements with their combined service coverage status.

## Methodology

1. Health facilities reprojected to EPSG:25000; 5 km buffers generated and dissolved: `health_facilities_5km_buffer.gpkg`.
2. Education facilities reprojected to EPSG:25000; 5 km buffers generated and dissolved: `education_facilities_5km_buffer.gpkg`.
3. Settlements tagged with health coverage and education coverage flags individually.
4. Settlements outside both coverage zones identified as joint service deserts: `service_desert_settlements.gpkg`.
5. All settlements tagged with combined service status: `settlements_service_tagged.gpkg`.

## Output Layers

| File | Description |
|------|-------------|
| `health_facilities_5km_buffer.gpkg` | Dissolved 5 km service catchment around health facilities |
| `education_facilities_5km_buffer.gpkg` | Dissolved 5 km service catchment around education facilities |
| `service_desert_settlements.gpkg` | Settlements outside both health and education catchment zones |
| `settlements_service_tagged.gpkg` | All settlements tagged with health and education coverage status |

## Key Findings

- Joint service deserts are concentrated in the Savannah, Northern East, Bono East, and parts of Oti regions, confirming that the same spatial clusters that lack road connectivity also lack both health and education infrastructure.
- The dual-desert classification is a stronger prioritisation signal than single-sector gap analysis alone, pointing to communities with compounded deprivation.
- These settlements represent high-priority targets for integrated rural development programmes and off-grid social infrastructure investment.

## Deliverables

| File | Type |
|------|------|
| `Joint-Health-Edu-Desert.qgz` | QGIS project |

## Notes

- No `reference_layout.png` or PDF export is present in this folder.
- All layers use EPSG:25000 (Leigon / Ghana Metre Grid).
- The 5 km catchment threshold is commonly used in humanitarian and development planning standards for rural service accessibility.
