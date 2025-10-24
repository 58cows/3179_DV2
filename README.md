# Malaysia’s Income & Poverty

State-level poverty, income, and population across Malaysia.

**Live site:** _add your GitHub Pages link here_

---

## Files
- **index.html** — main page (Vega-Lite embeds + explanations)
- **css/style.css** — layout & typography
- **js/main.js** — `vegaEmbed` calls (with cache-buster)
- **specs/** — Vega-Lite specifications  
  `map_poverty_latest.json`, `bar_rank_poverty.json`,  
  `scatter_income_vs_poverty.json`, `lollipop_income_gap.json`,  
  `popshare_100_stacked.json`
- **data/** — CSV/TopoJSON (kept small)
  - `hh_poverty_state.csv`, `hh_income_state.csv`, `population_state.csv`
  - `malaysia_map.json` (ADM1), `ne_110m_ocean.json`, `ne_110m_graticules_5.json`

---

## Visualisations
1. **Where is poverty highest?** Choropleth map of latest **poverty rate (%)** by state.  
   _Color:_ sequential **Blues** (darker = higher). Tooltip shows state, % and year.
2. **Poverty by State (ranked).** Horizontal bars sorted by latest poverty rate; **dashed rule** = national average.  
   _Color:_ above average **#4f46e5**, below average **#cbd5e1**.
3. **Income vs. Poverty (bubble size = population).**  
   **X:** median income (RM), **Y:** poverty rate (%), **Size:** population.  
   _Style:_ violet fill **#7c8cf8** with purple outline **#4f46e5**.
4. **Income Gap from National Median (lollipop).**  
   **Gap (RM) = state median − national median.** Right of 0 = above; left = below.  
   _Color:_ **green #10b981** (≥ 0) vs **red #ef4444** (< 0).
5. **Population Exposure by Poverty Tier (100% stacked).**  
   Share of national population per state by tier (**Very Low → Very High**).  
   _Palette:_ `#d1fae5`, `#86efac`, `#fde68a`, `#f59e0b`, `#ef4444`.

---

## Sources & Attribution
- DOSM OpenDOSM:  
  Population — https://open.dosm.gov.my/data-catalogue/population_state  
  Household Poverty — https://open.dosm.gov.my/data-catalogue/hh_poverty_state  
  Household Income — https://open.dosm.gov.my/data-catalogue/hh_income_state
- Boundaries (ADM1): geoBoundaries via HDX  
  https://data.humdata.org/dataset/geoboundaries-admin-boundaries-for-malaysia
- Basemap assets: Natural Earth (ocean & graticules)
- Geometry simplification/export: https://mapshaper.org/

**Author:** Aisha Zafar • **Updated:** _YYYY-MM-DD_  
All assistance acknowledged.
