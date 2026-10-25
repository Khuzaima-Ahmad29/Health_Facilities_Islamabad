# Assignment 2 – API-Based Web GIS Application
**Topic:** Healthcare facilities in Islamabad and Rawalpindi
**Name:** Khuzaima Ahmad  |  **Reg. No:** FA23-BRG-030

## 1. API used
I used the **OpenStreetMap Overpass API** (https://overpass-api.de). It is free, needs no API key, and returns OpenStreetMap features as JSON. I queried for features tagged `amenity=hospital`, `clinic` or `pharmacy` inside a bounding box covering Islamabad and Rawalpindi.
As a backup, if the API fails, the site loads a local GeoJSON file of 81 Islamabad hospitals (Pakistan Health Facilities dataset, ALHASAN Systems via HDX, CC0).

## 2. Data fields used
| Field | Meaning |
|---|---|
| `tags.name` | Facility name |
| `tags.amenity` | Type (hospital / clinic / pharmacy) |
| `lat`, `lon` (or `center`) | Location of the facility |
| `addr:*`, `phone`, `opening_hours`, `operator`, `website` | Address and contact details (if available) |

Backup GeoJSON fields: `name`, `category`, `sector` (Government/Private), `lat`, `lng`.

## 3. Steps
1. Created a webpage with HTML, CSS and JavaScript.
2. Added a Leaflet map centred on Islamabad/Rawalpindi with OpenStreetMap tiles.
3. Sent the Overpass query using `fetch()`.
4. Parsed the JSON response and converted each result to a simple object (name, type, lat, lng, extra).
5. Drew a marker for each facility; clicking a marker opens a popup with its details.
6. Added a type dropdown and a name search box that redraw the markers.
7. Added a loading message and error handling (tries a second server, then the backup file).
8. Published the code on GitHub and the demo on GitHub Pages.

## 4. Links
- GitHub repository: _add link_
- Live demo: _add link_

## 5. Attribution
Map data © OpenStreetMap contributors. Backup data: Pakistan Health Facilities (HDX, CC0).
