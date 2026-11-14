# MARSCOPE

**Intelligent Mars Exploration System** for the NASA Space Apps Challenge 2026.
Challenge: *Interplanetary Survival Guide: Martian Map*.
Team: **Mars explorer** (Nauyryz Inzhu, Nauyryz Aray).

Live app: https://inzhunauyryz.github.io/marscope/

## What it does

MARSCOPE combines data from four NASA Mars missions into one interactive, phone-friendly map to help plan safer Marswalks.

- Four switchable layers: Viking imagery, MOLA elevation, THEMIS thermal infrared, CTX 5 m imagery.
- Route planning: tap two points or pick a science target or NASA landing site.
- Hazard screening against mapped canyons, volcano slopes, deep basins and polar regions, with a LOW / MODERATE / HIGH rating.
- A suggested safer detour when one exists.
- Marswalk estimate for routes under 50 km: round-trip time at an assumed 3 km/h compared with an assumed 8 h EVA window.
- One tap to open CTX imagery and inspect local terrain.

## NASA data (via NASA Mars Trek, trek.nasa.gov)

| Layer | Mission | Resolution |
|---|---|---|
| Imagery | Viking MDIM 2.1 colorized mosaic (NASA/USGS) | 232 m/px |
| Elevation | Mars Global Surveyor, MOLA colorized shaded relief | 463 m/px |
| Thermal IR | Mars Odyssey, THEMIS IR Day mosaic | 100 m/px |
| High-res | Mars Reconnaissance Orbiter, CTX global mosaic (Caltech/NASA) | 5 m/px |

## How the screening works

- The route is sampled at 100 points along a straight line, using Mars radius 3,389.5 km for distances.
- Hazard zones are approximate regional boxes drawn by the team from public NASA and USGS Mars information. They are not slope measurements.
- The rating uses the share of the route inside each zone, weighted by severity.
- The safer detour searches a grid of one waypoint and minimizes distance multiplied by a hazard penalty.

## Limitations

- Regional screening only: no walking-scale slope or rock data yet.
- Zone boundaries, landing site positions, walking speed and EVA window are approximate or assumed.
- Next steps: HiRISE terrain models, slope maps, radiation and thermal data.

## Built with

- Leaflet 1.9.4 (BSD 2-Clause), loaded from the unpkg CDN
- GitHub Pages hosting, single `index.html`

## AI assistance

The team chose the challenge, data layers and features, and tested the app on a phone. Claude (Anthropic) assisted with writing the code and the English text.

## Credits

NASA Mars Trek, NASA/USGS, MGS MOLA, Mars Odyssey THEMIS, MRO CTX (Caltech), NASA Science Mars pages, USGS Astrogeology Science Center.
