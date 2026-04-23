# SAR-Plotter

Plot common aerial search patterns using the Google Maps JavaScript API.

## Current setup

This project originally targeted Google Maps JavaScript API v2, which Google shut down on May 26, 2021.
The HTML has been updated to the current v3-style API, but you still need to provide a modern Google Maps API key before the map will load.

Set `GOOGLE_MAPS_API_KEY` near the top of [html/sarplotter.html](html/sarplotter.html).

## OpenStreetMap version

The Leaflet/OpenStreetMap version is [html/sarplotter_osm.html](html/sarplotter_osm.html).

If you open that file directly from disk with a `file://` URL, OpenStreetMap tiles may fail with a `403` error saying a `Referer` header is required. That is expected with current OSM tile policy.

Serve the project over local HTTP instead, for example from the repo root:

```powershell
python -m http.server 8000
```

Then open:

```text
http://localhost:8000/html/sarplotter_osm.html
```
