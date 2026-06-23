[Google Maps Scraper Pro](https://apify.com/knotless_cadence/google-maps-scraper-pro?fpr=data)

# Google Maps Scraper

Extract business data from Google Maps at scale — names, ratings, reviews, phone numbers, addresses, and 10+ more fields. No coding required, just enter your search query and get structured results.

## Features

- **13+ data fields per place** — name, rating, review count, address, phone, website, category, hours, price level, coordinates, place ID, photos count, and more
- **Bulk search** — process multiple search queries in a single run
- **Review extraction** — optionally scrape individual reviews with author, text, rating, and date
- **Geo-coordinates** — extract latitude/longitude for every place
- **Auto-scrolling** — automatically loads up to 100+ results per search query
- **Multi-language support** — scrape in any language supported by Google Maps
- **Export to JSON, CSV, Excel** — download results in any format via Apify

## Output Example

```
{
  "name": "Joe's Pizza",
  "rating": 4.6,
  "reviewCount": 12847,
  "address": "7 Carmine St, New York, NY 10014",
  "phone": "+1 212-366-1182",
  "website": "joespizzanyc.com",
  "category": "Pizza restaurant",
  "hours": "Open 24 hours",
  "priceLevel": "$$",
  "latitude": 40.7306,
  "longitude": -74.0021,
  "placeId": "ChIJLfySpTOlRIcR...",
  "photosCount": 3420,
  "url": "https://www.google.com/maps/place/...",
  "scrapedAt": "2026-03-18T12:00:00.000Z"
}
```

## Use Cases

- **Lead generation** — build targeted lists of businesses in any city or niche (restaurants, dentists, gyms, agencies)
- **Competitive analysis** — compare ratings, review counts, and pricing across competitors in a market
- **Market research** — discover business density and saturation in specific geographic areas
- **Local SEO monitoring** — track your own and competitor ratings and review volumes over time
- **Real estate analysis** — map nearby amenities (schools, hospitals, shops) for property valuations

## Input Parameters

| Parameter | Type | Default | Description |
| --- | --- | --- | --- |
| `searchQueries` | Array | `["restaurants in New York"]` | List of Google Maps search queries to process |
| `maxResults` | Number | `100` | Maximum number of places to extract per query |
| `language` | String | `"en"` | Language code for results (en, es, fr, de, etc.) |
| `includeReviews` | Boolean | `false` | Whether to extract individual reviews per place |
| `maxReviewsPerPlace` | Number | `5` | Maximum reviews to extract per place |

## Cost Estimation

- ~$1.50 per 100 places (with Apify Playwright compute)
- ~$3.00 per 100 places with reviews included
- Free tier: up to 30 results with Apify free plan

## FAQ

**Q: How many places can I scrape in one run?**
A: You can extract up to 100+ places per search query, and run multiple queries simultaneously. A typical run of 500 places takes 15-20 minutes.

**Q: Does it work for any country?**
A: Yes. Google Maps Scraper works globally — just enter your search query in any language or set the `language` parameter. Supports 50+ countries.

**Q: Can I get review text and ratings?**
A: Yes. Set `includeReviews` to `true` and configure `maxReviewsPerPlace`. Each review includes author name, text, star rating, and date.

> **Need a custom scraper built in 48 hours?** Pilot rate: $100/project. 78 published Apify actors, 348+ runs on our flagship Trustpilot scraper. Email **[spinov001@gmail.com](mailto:spinov001@gmail.com)** or Telegram **@scraping_ai** — reply by Friday for priority slot.