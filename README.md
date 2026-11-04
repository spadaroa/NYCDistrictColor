# NYC District Color Map

A single-page map of the 32 NYC community school districts. Select whole districts, color them, label the colors, add
citywide boxes (D75, D79, or your own), adjust number, line and background styling, and download a PNG or SVG with a
title and legend. Colors are saved in the viewer's browser and can be copied/pasted as settings.

A personal project; not affiliated with NYC Public Schools. 

## Files

- `index.html`: the whole site (self-contained; district shapes are embedded). Deploy as a static site with no build step.
- `build/template.html`: the page source, with a placeholder where the map data goes.
- `build/make_map.py`: rebuilds `index.html` from the template and the district shapes.

## Rebuilding

District lines come from NYC Open Data, School Districts (8ugf-3d8u). Download the GeoJSON, then:

```
pip install shapely
python3 build/make_map.py path/to/districts.geojson
```

## Hosting (Cloudflare Pages)

Framework preset: None. Build command: none (or `exit 0`). Build output directory: `/`.
