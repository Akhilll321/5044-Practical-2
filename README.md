# CS5044 Practical 2 — Exploring Global Trends in Continued Breastfeeding Rates

An interactive dashboard visualising continued breastfeeding rates worldwide
(UNICEF SOWC 2025) with three linked views: a world map, a radar chart of
structural factors, and a faceted bar chart comparing the poorest and
richest 20%.

---

## File structure

```
5044-Practical-2/
├── index.html            # Main dashboard — open this one
├── map_country.html      # Choropleth / bubble / pictogram world map
├── radar_chart.html      # Radar chart of structural factors
├── facetedbar.html       # Faceted bar chart (poorest vs richest 20%)
├── data/
│   └── final_new3.csv    # Cleaned dataset used by all three views
└── README.md
```

`map_country.html`, `radar_chart.html` and `facetedbar.html` are embedded
into `index.html` via `<iframe>` and communicate through custom events
so that selecting a country on the map filters the other two views.

---

## How to run

The dashboard loads `data/final_new3.csv` at runtime via `d3.csv(...)`,
so it must be served over HTTP (opening `index.html` directly through
`file://` will be blocked by the browser's cross-origin policy and the
views will be empty).

Follow the same workflow shown in the lectures:

1. Open the `5044-Practical-2` folder in **VS Code**.
2. Open `index.html`.
3. Click **"Go Live"** in the bottom-right status bar (VS Code
   **Live Server** extension by Ritwick Dey).
4. A browser tab will open at a local address.

Tested on the latest **Chrome**. An internet connection
is required on first load so that D3 v7, topojson-client v3 and
world-atlas v2 can be fetched from the jsDelivr CDN.

---

## How to interact

Interaction instructions are provided in two places:

- **Inside the dashboard itself** — see the *"How to interact"* and
  *"Glossary of Attributes"* panels below the charts on `index.html`.
- **Accompanying demo video** — included with the submission.
