# U.S. Extreme Wet-Bulb Temperatures, 2005–2025

An interactive map of the highest wet-bulb temperatures recorded each year in 56 U.S. cities,
built from hourly NOAA NCEI Local Climatological Data (`FM-15` observations). Hover a city for its
peak, warming trend, and projection toward the empirical 87 °F human-tolerance threshold; click for
year-by-year detail (single hottest hour and the mean of the three hottest days, with fitted trends).

The 87 °F threshold follows the 2022 Penn State study (Vecellio et al., *Journal of Applied
Physiology*), which found the real critical wet-bulb limit for healthy young adults is ~31 °C (≈87 °F),
below the long-assumed 35 °C.

## Hosting

This is a single self-contained `index.html` (city data and U.S. map geometry are inlined; D3 loads
from a CDN). Any static host works — just serve `index.html` at the site root. `.nojekyll` is included
so GitHub Pages serves the file as-is.

## Data notes

- Source: NOAA NCEI LCD, 2005–2025, one primary airport station per city.
- "Highest recorded" = max hourly wet-bulb in the 2005–2025 window (not all-time).
- Trends are OLS slopes of annual maxima vs. year (low R² — illustrative, not forecasts).
- Station substitutions: New York = LaGuardia · Dallas = Dallas–Fort Worth Intl · San Bernardino = Ontario Intl. Denver is missing 2013 (absent from the NCEI archive).
