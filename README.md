[Google Maps Scraper Pro](https://apify.com/red.cars/google-maps-scraper-pro?fpr=data)

[![Apify Actor](https://img.shields.io/badge/Apify-Actor-blue?logo=apify)](https://apify.com/red.cars/google-maps-scraper-pro)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)

[![Pay-Per-Event](https://img.shields.io/badge/Pricing-Pay%20Per%20Event-green?logo=usd)](https://apify.com/red.cars/google-maps-scraper-pro#pricing)

> Market Density Score: Professional Google Maps intelligence for OpenClaw agents

## Description

Market Density Score: Professional Google Maps intelligence for OpenClaw agents. Identify competitor clusters, extract verified local business leads, and calculate market expansion opportunities without an API key.

## Features

📌 Status
🧠 Context
[2026-03-12] — outputSchema description added (spec-005)

## How It Works

This actor uses intelligent extraction with Apify's proxy infrastructure to gather public data from Google Maps Scraper Pro - Business Intelligence WITHOUT API Key. It handles authentication, pagination, and error recovery automatically.

## Quick Start

```
# Run via Apify API
apify run -a red.cars/google-maps-scraper-pro

# Or configure input and click Run on:
# https://apify.com/red.cars/google-maps-scraper-pro
```

### Using as an MCP Tool

### Running on Apify Platform

Set `API_KEY` in your Apify Console secrets, configure input via the Actor input schema UI, and click **Run**.

## Input Schema

| Parameter | Type | Description | Default |
| --- | --- | --- | --- |
| `searchQuery` | string | What businesses are you looking for? (e.g., 'restaurants', 'dentists', 'coffee shops') | restaurants |
| `location` | string | City, state, or address to search in (leave empty for no location filter) | - |
| `maxResults` | integer | Number of businesses to extract | 5 |
| `proxyType` | string | Choose your preferred balance of cost vs reliability. You control proxy costs from your Apify plan. Options: `DATACENTER`, `RESIDENTIAL` | RESIDENTIAL |
| `debugMode` | boolean | Enable minimal extraction for health checks and testing. Guarantees success within 300s. | false |
| `includeReviews` | boolean | Extract customer reviews and ratings for deeper business intelligence | true |
| `includePhotos` | boolean | Extract photo URLs from business listings (increases processing time) | false |
| `includeContactInfo` | boolean | Extract phone numbers, websites, and contact details for lead generation | true |
| `enableIntelligence` | boolean | Calculate proprietary Market Density and Opportunity Scores. Identifies competitor clusters and business gaps in the area. | false |
| `intelligenceRadius` | integer | The distance in kilometers to search for competitors when calculating Market Density. | 5 |
| `searchQueryFile` | string | Upload a CSV or JSON file containing business search queries for bulk processing. File should contain search terms, business types, or categories to extract. | - |
| `locationListFile` | string | Upload a CSV or JSON file containing locations for bulk Google Maps analysis. File should contain cities, addresses, or geographic areas to search. | - |
| `businessListFile` | string | Upload a CSV or JSON file containing specific business names or Google Maps URLs for targeted extraction. File should contain business names or Google Maps links. | - |
| `exportFormat` | string | Choose output format for your lead generation. Use 'markdown' for token-efficient LLM-ready business cards. Options: `json`, `csv`, `markdown` | json |
| `checkOnly` | boolean | When true, returns immediately with capability metadata without scraping. Used by AI agents to verify availability before committing to a paid run. Free, <5 seconds. | false |

## Output Schema

| Field | Type | Description |
| --- | --- | --- |
| `results` | string | Google Maps business listings with market intelligence scoring. Each result contains: title, category, address, coordinates, phone, website, rating (0-5), reviewsCount, priceLevel, openingHours, marketDensityScore (competitor count), opportunityScore (0-100). Use for lead gen, franchise site selection, competitive intelligence, local market analysis. AI agents: query business type + city for instant lead list. |

## Example Output

```
{
  "results": [
    {
      "url": "https://example.com/profile",
      "username": "example_user",
      "fullName": "Example User",
      "followersCount": 10000,
      "followingCount": 500,
      "postsCount": 250,
      "isVerified": false,
      "biography": "Example bio text",
      "latestPosts": [],
      "scrapedAt": "2026-03-23T13:24:14.468Z"
    }
  ]
}
```

## Pricing

Uses Apify's **Pay-Per-Event** (PPE) model — you are charged per result returned. No charge for queries that return zero results.

| Tier | Price per Result | Apify Plan |
| --- | --- | --- |
| Price for Google Maps Lead Report | $0.01 | Free, Basic, Starter, Professional, Scale |

## Use Cases

- **Influencer Research**: Identify and evaluate potential influencers by engagement metrics and audience quality
- **Competitor Monitoring**: Track competitor presence and activity on Target Platform
- **Lead Generation**: Build targeted lead lists from public profiles and contact information
- **Market Intelligence**: Gather market intelligence and trend data for business decisions
- **Content Aggregation**: Collect content for analysis, archiving, or republication

## FAQ

### Do I need an API key?

Yes, this actor requires an API key. Set it via the secret environment variable in Apify Console.

### How does pricing work?

This actor uses Apify's Pay-Per-Event model. You are charged per successful result returned. No charge for queries that return zero results.

### What are the rate limits?

Rate limits depend on your Apify plan. Higher-tier plans provide more compute units and faster extraction.

### How do I increase success rate?

- Enable **Premium (Residential)** proxy for high-security targets
- Reduce concurrency for rate-limited profiles
- Use debug mode to test before full extraction

### Can I run this on a schedule?

Yes, use Apify Scheduler to run this actor on a cron schedule for continuous monitoring.

### How do I export to CRM?

Set `exportFormat` to `salesforce` or `hubspot` for direct CRM import format.

## Troubleshooting

| Error | Cause | Fix |
| --- | --- | --- |
| NETWORK_ERROR | Network connectivity issue | Check internet connection, retry with proxy |
| VALIDATION_ERROR | Invalid input parameters | Review input schema and retry |

## Known Limitations

- **Private accounts**: Cannot extract data from private accounts without following
- **Rate limiting**: Platform may temporarily block repeated requests from same IP
- **Data freshness**: Extracted data reflects moment of extraction; historical data may be limited
- **Proxy requirements**: High-security targets may require residential proxy for reliable extraction
- **Content limits**: Platform-imposed limits on historical post retrieval

## Legal

**Data Source**: the target platform (the target platform.com)

**Terms of Service**: This actor is provided for legitimate data collection purposes only. Users must comply with the target platform's Terms of Service and applicable laws. Red.cars is not responsible for misuse of this tool.

**Privacy**: All extracted data is processed in accordance with applicable privacy laws. Do not use this tool for unauthorized data collection or privacy-violating activities.

**Attribution**: When using the target platform data, comply with their attribution requirements and data policies.

---

*red.cars Intelligence Fleet • [apify.com/red.cars](https://apify.com/red.cars)*