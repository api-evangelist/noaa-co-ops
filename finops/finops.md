# NOAA CO-OPS API FinOps

## Cost Model

NOAA CO-OPS APIs are **free of charge**. They are funded by the U.S. federal government through NOAA and are provided as a public service under the principles of open government data. There are no usage fees, subscription tiers, per-request charges, or overage costs.

## No Authentication Required

No API key purchase, account registration, or payment is needed to access any CO-OPS API. All three APIs (Data Retrieval, Metadata, Derived Products) are fully open.

## Cost Drivers for Consumers

While NOAA does not charge for API access, organizations integrating CO-OPS data may incur their own infrastructure costs:

| Cost Category | Notes |
|---------------|-------|
| Compute | Costs to run data pipelines, ETL jobs, or applications consuming the API |
| Storage | Costs to cache or archive CO-OPS observational or prediction data |
| Egress | Cloud data transfer costs if the API is called from a cloud-hosted application |
| Engineering | Development and maintenance of integrations |

## Budget Recommendations

- **No budget allocation needed for API access itself.**
- Budget for engineering time to build integrations and handle data range limits (chunking large date ranges into multiple requests).
- Consider bulk data access via NOAA's Amazon S3 or THREDDS/ERDDAP services for very high-volume historical data needs, which may reduce the number of API calls needed.

## Open Data Policy

CO-OPS data is released under the U.S. government open data policy. Data is in the public domain and may be used freely for commercial, research, or personal purposes without licensing fees. Attribution to NOAA CO-OPS is encouraged.

## References

- NOAA Open Data Dissemination: https://www.noaa.gov/information-technology/open-data-dissemination
- NOAA Data Access: https://tidesandcurrents.noaa.gov/web_services_info.html
