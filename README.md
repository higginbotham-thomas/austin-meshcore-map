# Austin MeshCore RF Network Map

Interactive map of the [Austin MeshCore](https://austinmesh.org) LoRa mesh radio network with Fresnel zone RF path analysis.

**Live map:** https://higginbotham-thomas.github.io/austin-meshcore-map/

---

## What's on the map

- All repeaters in the Austin metro MeshCore network with routing table paths
- **Fresnel zone clearance** for every path — CLEAR, MARGINAL, OBSTRUCTED, or BLOCKED
- **Terrain obstacle markers (▲)** at the worst obstruction point along each blocked path
- **Antenna height sensitivity table** in each repeater popup — shows how much clearance improves per meter of antenna height
- **Link budget margin** for every path (FSPL vs. 154 dB LoRa budget)
- **Bearing** (cardinal + degrees, reciprocal) for antenna alignment

## RF Analysis

- **Frequency:** 915 MHz ISM (LoRa)
- **Clearance rule:** 60% first Fresnel zone radius
- **Earth curvature:** 4/3 effective Earth radius model
- **Terrain data:** USGS 3DEP 1/3 arc-second (~10m resolution), 6-tile merge covering 29–32°N, 96–100°W
- **Link budget:** +20 dBm TX, 2 dBi antennas, −130 dBm sensitivity = 154 dB total

### Status definitions

| Status | Meaning |
|---|---|
| **CLEAR** | ≥60% first Fresnel zone clearance |
| **MARGINAL** | Clear, but <5m margin |
| **OBSTRUCTED** | Sub-Fresnel clearance — LoRa typically still works via diffraction |
| **BLOCKED** | Geometrically impossible as direct LoRa; likely routing table propagation |

> OBSTRUCTED ≠ non-functional. LoRa SF12 with ~40 dB diffraction margin above FSPL handles most sub-Fresnel paths.

## Data sources

- Node positions and routing paths: MeshMapper AUS region export (June 2026)
- Infrastructure heights: [AustinMesh.org infrastructure page](https://austinmesh.org/about/infrastructure/)
- Terrain: [USGS 3DEP 1/3 arc-second DEM](https://www.usgs.gov/programs/national-geospatial-program/national-map)

## Operator

Map maintained by **tgh0831** — Oak Hill repeater operator and MeshMapper admin for the Austin region.

- MeshMapper AUS: https://aus.meshmapper.net
- Austin Mesh: https://austinmesh.org
