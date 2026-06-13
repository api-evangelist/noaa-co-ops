# NOAA CO-OPS

NOAA Center for Operational Oceanographic Products and Services (CO-OPS) provides free, open REST APIs for accessing tides and currents predictions, observed water levels, meteorological data, and oceanographic products from monitoring stations across the United States coastline and Great Lakes.

## APIs

### CO-OPS Data Retrieval API
Base URL: `https://api.tidesandcurrents.noaa.gov/api/prod/`

Retrieves real-time and historical observational and prediction data. Products include:
- Water levels (6-minute, hourly, daily, monthly means)
- Tidal predictions (high/low, hourly)
- Currents observations and predictions
- Meteorological: wind, air pressure, air temperature, water temperature, humidity, conductivity, salinity, visibility

### CO-OPS Metadata API
Base URL: `https://api.tidesandcurrents.noaa.gov/mdapi/prod/`

Station metadata including locations, sensor configurations, harmonic constituents, datums, benchmarks, and flood level thresholds.

### CO-OPS Derived Product API
Base URL: `https://api.tidesandcurrents.noaa.gov/dpapi/prod/`

Derived products including sea level trends, sea level rise projections, high tide flooding statistics and decadal projections, and extreme water level analysis.

## Access

- **Cost**: Free, no registration or API key required
- **Formats**: JSON, XML, CSV, KML, NetCDF
- **Portal**: https://tidesandcurrents.noaa.gov/
- **Documentation**: https://tidesandcurrents.noaa.gov/web_services_info.html

## Contents

- `apis.yml` — APIs.json 0.19 provider profile
- `plans/free.md` — Plan details (free public access)
- `rate-limits/rate-limits.md` — Rate limiting and data range constraints
- `finops/finops.md` — Cost model (free government open data)
