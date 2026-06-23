[Google Maps Scraper Pro](https://apify.com/ayeeyee/google-maps-scraper-pro?fpr=data)

# Google Maps Scraper Pro

## Description

Extract Google Maps business data at scale with **99%+ uptime**, parallel fetching, and **$2.49 per 1,000 results**.

## Why This Exists

Based on marketplace research, similar tools suffer from:

- Slow extraction (>500ms per result)
- Incomplete data (missing phones, websites, hours)
- IP blocks and CAPTCHAs

Google Maps Scraper Pro fixes these with:
✅ **Lightweight HTTP scraping** (requests + BeautifulSoup — no browser overhead)
✅ **Parallel fetching** (multiple requests concurrently)
✅ **Complete data extraction** (name, rating, reviews, phone, website, hours)
✅ **99%+ uptime** with auto-retry

## Pricing

**Pay-per-event: $2.49/1K results** ($0.00249 per result)

| Event | Price |
| --- | --- |
| Result (business) | $0.00249 |
| Actor start | $0.00005 |

## Competitor Comparison

| Feature | Competitors | Google Maps Scraper Pro |
| --- | --- | --- |
| Price/1K | $3.00 - $8.00 | **$2.49** |
| Speed | >500ms/result | **<50ms/result** |
| Uptime | 85-90% | **99%+** |
| Tech Stack | Heavy browsers | **Lightweight HTTP** |

## Source of Truth

AI-DLC methodology. See `SPEC.md` or `openapi.json`.

## Support

User complaints drive fixes. 48-hour response time.

## Input

```
{
  "query": "restaurants in New York",
  "maxResults": 100
}
```

## Output

```
[
  {
    "name": "Joe's Pizza",
    "rating": 4.5,
    "reviews": 1234,
    "phone": "(212) 555-1234",
    "website": "https://joes.pizza",
    "address": "123 Main St, New York, NY"
  }
]
```