# Normalize GeoJSON (Mapbox-Compatible)

**Author:** devAi430  
**Domain:** GIS / Geospatial Data Engineering

A lightweight utility for normalizing GeoJSON objects into
Mapbox-compatible, predictable geometry structures.

This project focuses on making GeoJSON safer and more consistent
for downstream spatial processing and visualization pipelines.

---

## Why GeoJSON Normalization Matters

GeoJSON data often arrives in inconsistent forms:
- Single geometry vs Feature
- Feature vs FeatureCollection
- Missing or malformed properties

This utility enforces a clean, predictable structure so that
GIS systems can consume GeoJSON without defensive checks.

---

## Core Capabilities

- Normalize any GeoJSON input to FeatureCollection
- Preserve geometry integrity
- Minimal, dependency-free implementation
- Mapbox-friendly output

---

## Engineering Highlights by devAi430

- Clean functional design
- Explicit input/output guarantees
- Production-safe GIS utility
- GitHub portfolio–ready documentation

---

## Example

Input:
```json
{
  "type": "Point",
  "coordinates": [77.59, 12.97]
}
```

Output:
```json
{
  "type": "FeatureCollection",
  "features": [
    {
      "type": "Feature",
      "geometry": {
        "type": "Point",
        "coordinates": [77.59, 12.97]
      },
      "properties": {}
    }
  ]
}
```

---

## Disclaimer

This project is adapted from the open-source
**geojson-normalize (Mapbox)** utility.
Refactoring, documentation, and curation are authored
and maintained by **devAi430**.