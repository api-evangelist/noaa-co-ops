# NOAA CO-OPS API Rate Limits

## Overview

NOAA CO-OPS protects its APIs and systems under heavy load by throttling the quantity and volume of data queries received from a single client. No hard numeric rate limit (requests per minute or per second) is publicly documented; however, CO-OPS reserves the right to limit requests when a single user is generating excessive load.

## Best Practices

- Include `sleep` statements (pauses) between successive API calls when issuing large batches of requests to avoid triggering throttling.
- Use the `application=` query parameter to identify your application in each request (e.g., `application=MyApp_v1`). This helps CO-OPS staff contact you if your usage pattern causes issues.
- Retrieve the largest allowable date range per request to minimize total request volume.
- Cache responses locally when the same data will be needed multiple times.

## Per-Request Data Range Limits

These are hard caps enforced at the API level per individual request:

| Interval / Product | Maximum Date Range per Request |
|--------------------|-------------------------------|
| 1-minute water level | 4 days |
| 6-minute interval data | 1 month |
| Hourly interval data | 1 year |
| High/Low tide predictions | 1 year |
| Daily mean data | 10 years |
| Monthly mean data | 200 years |

## Authentication

No API key or authentication token is required. The APIs are open and publicly accessible.

## Throttling Behavior

When CO-OPS detects excessive request volume from a single IP or user agent, it may:
- Slow response times for that client
- Return HTTP 429 Too Many Requests or similar error responses
- Temporarily block the client IP

There is no published quota recovery window or hard numeric throttle threshold.

## Contact

If you receive throttling errors or need to discuss high-volume data access needs, contact:
- co-ops.userservices@noaa.gov
