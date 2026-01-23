# Data Sources Inventory

## Overview

This document catalogs all data sources evaluated for luxury asset valuation, organized by category. Sources were evaluated during January 2026 research.

---

## Watches

### Chrono24
- **URL**: https://chrono24.com
- **Type**: Marketplace (listings + sold)
- **Access**: Public listings viewable; sold prices may require account
- **Data fields**: Price, condition, year, box/papers, seller location, photos
- **Coverage**: Excellent for Rolex, Patek, AP, Omega
- **API**: Unknown — research needed
- **Notes**: Largest watch marketplace globally. Search by exact reference number (e.g., 116500LN) returns highly relevant results. Listings include condition grades, seller ratings, and transaction protection. Prices found were consistent with other sources. Direct site fetching was blocked during research, but public search results contained sufficient pricing data. **Recommended as primary marketplace source.**

**Evaluation Scores:**
| Criteria | Score | Notes |
|----------|-------|-------|
| Data availability | 5 | Extensive public listings |
| Match accuracy | 5 | Reference numbers enable exact matching |
| Update frequency | 5 | Real-time listings |
| Automation potential | 3 | May have anti-bot protections; investigate API/partnership |
| Coverage depth | 5 | All test items found with multiple listings |
| **Total** | **23/25** | |

---

### WatchCharts
- **URL**: https://watchcharts.com
- **Type**: Aggregator / analytics
- **Access**: Basic data public; detailed analytics may require subscription
- **Data fields**: Market price, price history, volatility, sales velocity, risk scores
- **Coverage**: Strong for popular references
- **API**: Unknown — research needed
- **Notes**: **Best-in-class for watch valuations.** Provides aggregated market prices, historical trends, sales velocity metrics ("sells faster than 97% of market"), and risk scores for depreciation. Already does the aggregation work that Curated Capital would need. Data appears in public search results with specific price points. Investigate API access or data licensing — this could be the core valuation engine for watches.

**Evaluation Scores:**
| Criteria | Score | Notes |
|----------|-------|-------|
| Data availability | 5 | Aggregated pricing publicly visible |
| Match accuracy | 5 | Reference-based matching |
| Update frequency | 5 | Appears near real-time |
| Automation potential | 4 | Likely has data products; research partnership |
| Coverage depth | 5 | All test items found |
| **Total** | **24/25** | |

---

### eBay (Sold Listings)
- **URL**: https://ebay.com
- **Type**: Marketplace (completed sales)
- **Access**: Sold listings viewable with "completed items" filter
- **Data fields**: Sale price, date, condition description, photos
- **Coverage**: Variable — authentication concerns
- **API**: eBay API available but restricted
- **Notes**: Useful as supplemental validation source. Provides actual transaction prices (not just asking prices). Authentication is a concern — listings may include fakes, especially for high-value pieces. Best used to validate ranges found on authenticated platforms rather than as primary source. API access is available but comes with rate limits and restrictions.

**Evaluation Scores:**
| Criteria | Score | Notes |
|----------|-------|-------|
| Data availability | 4 | Sold listings accessible |
| Match accuracy | 3 | Inconsistent listing titles; no standardized refs |
| Update frequency | 5 | Real-time |
| Automation potential | 4 | API exists with restrictions |
| Coverage depth | 4 | Good volume but quality varies |
| **Total** | **20/25** | |

---

### Bob's Watches
- **URL**: https://bobswatches.com
- **Type**: Dealer
- **Access**: Public pricing
- **Data fields**: Price, condition grade, photos
- **Coverage**: Rolex-focused
- **API**: None known
- **Notes**: Established Rolex specialist dealer. Prices tend to be at or above market (retail markup). Useful for Rolex-specific validation but limited to one brand. Blog content includes pricing guides and market commentary that appeared in search results. Not recommended as primary source due to brand limitation.

**Evaluation Scores:**
| Criteria | Score | Notes |
|----------|-------|-------|
| Data availability | 4 | Public dealer pricing |
| Match accuracy | 5 | Reference-based |
| Update frequency | 4 | Updated regularly |
| Automation potential | 2 | No API; would require scraping |
| Coverage depth | 2 | Rolex only |
| **Total** | **17/25** | |

---

## Branded Jewelry

### The RealReal
- **URL**: https://therealreal.com
- **Type**: Authenticated consignment
- **Access**: Public listings; some sold prices visible
- **Data fields**: Price, condition grade, photos, authentication status, estimated retail
- **Coverage**: Strong for Cartier, VCA, Tiffany
- **API**: None known
- **Notes**: **Best source for branded jewelry valuations.** All items authenticated by in-house experts. Critically, listings show "estimated retail" alongside asking price, enabling instant value retention calculations. Found multiple listings for all Van Cleef and Cartier test items. Pricing tends toward higher end (consignment commission built in) but consistent and reliable. Search by brand + collection name works well.

**Evaluation Scores:**
| Criteria | Score | Notes |
|----------|-------|-------|
| Data availability | 5 | Authenticated listings with retail comparisons |
| Match accuracy | 4 | Collection-based matching; need brand + model + material |
| Update frequency | 5 | Active marketplace |
| Automation potential | 3 | No API; investigate partnership |
| Coverage depth | 5 | Strong for target brands |
| **Total** | **22/25** | |

---

### 1stDibs
- **URL**: https://1stdibs.com
- **Type**: Curated marketplace
- **Access**: Public listings
- **Data fields**: Price, condition, seller, photos, provenance
- **Coverage**: Good for high-end branded pieces
- **API**: Unknown — research needed
- **Notes**: Large inventory of luxury jewelry including vintage and modern pieces. Found listings for all test items. **Challenge: wide price variance** within same product line due to mix of vintage, modern, plain, and diamond-set versions. Listings ranged from $450 (damaged) to $58,000 (diamond pavé) for "Cartier Love bracelet." Useful for establishing price ranges but requires careful filtering. Better for establishing upper bounds than precise valuations.

**Evaluation Scores:**
| Criteria | Score | Notes |
|----------|-------|-------|
| Data availability | 5 | Large public inventory |
| Match accuracy | 3 | Wide variance; includes vintage/antique |
| Update frequency | 4 | Active marketplace |
| Automation potential | 3 | No known API |
| Coverage depth | 5 | Extensive luxury jewelry |
| **Total** | **20/25** | |

---

### Fashionphile
- **URL**: https://fashionphile.com
- **Type**: Authenticated luxury resale
- **Access**: Public listings
- **Data fields**: Price, condition, photos, authentication
- **Coverage**: Strong for handbags; jewelry selection smaller
- **API**: None known
- **Notes**: Authenticated luxury resale with good reputation. Jewelry inventory smaller than bags but quality is high. Found Cartier Love rings and Van Cleef pieces. Prices competitive with The RealReal. Could serve as secondary validation source for jewelry.

**Evaluation Scores:**
| Criteria | Score | Notes |
|----------|-------|-------|
| Data availability | 4 | Authenticated listings |
| Match accuracy | 4 | Good product categorization |
| Update frequency | 4 | Active marketplace |
| Automation potential | 2 | No API |
| Coverage depth | 3 | Jewelry selection limited vs. bags |
| **Total** | **17/25** | |

---

### Rebag
- **URL**: https://rebag.com
- **Type**: Luxury resale
- **Access**: Public listings
- **Data fields**: Price, condition, photos
- **Coverage**: Bags-focused but carries jewelry
- **API**: None known
- **Notes**: Found useful market analysis content (e.g., Juste un Clou resale guide) that provided value retention data. Actual jewelry inventory limited compared to handbag focus. "The Vault" blog section contains pricing guides with market insights. Better as research/content source than primary pricing source.

**Evaluation Scores:**
| Criteria | Score | Notes |
|----------|-------|-------|
| Data availability | 3 | Limited jewelry inventory |
| Match accuracy | 3 | Bags-focused categorization |
| Update frequency | 4 | Active |
| Automation potential | 2 | No API |
| Coverage depth | 2 | Jewelry not primary focus |
| **Total** | **14/25** | |

---

### Vestiaire Collective
- **URL**: https://vestiairecollective.com
- **Type**: Peer-to-peer luxury
- **Access**: Public listings
- **Data fields**: Price, condition, seller, photos
- **Coverage**: European-heavy; variable jewelry selection
- **API**: Unknown — research needed
- **Notes**: Not tested in depth during this research phase. European focus may provide different pricing baseline. Consider for international expansion but not critical for MVP.

**Evaluation Scores:**
| Criteria | Score | Notes |
|----------|-------|-------|
| Data availability | 3 | Not fully evaluated |
| Match accuracy | 3 | Not fully evaluated |
| Update frequency | 4 | Active marketplace |
| Automation potential | 2 | Unknown |
| Coverage depth | 3 | European focus |
| **Total** | **15/25** | |

---

## Contemporary Art

*Note: Art category was not fully researched per project scope decision. Initial observations only.*

### Artsy
- **URL**: https://artsy.net
- **Type**: Gallery aggregator + marketplace
- **Access**: Public listings; auction results may require login
- **Data fields**: Price/estimate, medium, dimensions, gallery/seller
- **Coverage**: Good for Mr. Brainwash, KAWS, Murakami
- **API**: Unknown — research needed
- **Notes**: Not evaluated in depth. Would be primary source for art if category proceeds.

### Heritage Auctions
- **URL**: https://ha.com
- **Type**: Auction house
- **Access**: Public results archive
- **Data fields**: Hammer price, date, lot details, provenance
- **Coverage**: Strong for prints and editions
- **API**: Unknown — research needed
- **Notes**: Not evaluated in depth. Historical auction results would be valuable for edition prints.

### Invaluable
- **URL**: https://invaluable.com
- **Type**: Auction aggregator
- **Access**: Public results; some paywalled
- **Data fields**: Price realized, auction house, date
- **Coverage**: Aggregates many regional auctions
- **API**: Unknown — research needed
- **Notes**: Not evaluated.

### Artnet Price Database
- **URL**: https://artnet.com/price-database
- **Type**: Subscription database
- **Access**: Paid subscription required
- **Data fields**: Auction results, price history, analytics
- **Coverage**: Comprehensive but expensive
- **API**: Unknown
- **Notes**: Subscription cost likely prohibitive for consumer product. May not be viable for automated valuations.

---

## Source Evaluation Summary

### Watches — Recommended Stack
| Priority | Source | Use Case |
|----------|--------|----------|
| Primary | WatchCharts | Aggregated market prices, trends, risk scores |
| Secondary | Chrono24 | Individual listing validation, condition-based pricing |
| Tertiary | eBay | Transaction price validation |

### Jewelry — Recommended Stack
| Priority | Source | Use Case |
|----------|--------|----------|
| Primary | The RealReal | Authenticated pricing with retail benchmarks |
| Secondary | 1stDibs | Price range establishment, upper bounds |
| Tertiary | Fashionphile | Secondary validation |

### Art — Not Evaluated
Recommend separate research phase if category is pursued.

---

## Automation Platforms

### Apify
- **URL**: https://apify.com
- **Type**: Scraper marketplace ("Actors")
- **Pricing**: $5 free/month, then $0.25–$0.40 per compute unit
- **Model**: Community-built scrapers; pay per compute usage

**Available Scrapers:**
| Marketplace | Scraper Status | Notes |
|-------------|----------------|-------|
| Chrono24 | ✅ Multiple available | [Chrono24 Watch Price Scraper](https://apify.com/misterkhan/chrono24-search-scraper) recommended; some older ones deprecated |
| Vestiaire Collective | ✅ Available | [Vestiaire Scraper](https://apify.com/parseforge/vestiairecollective-scraper) — free tier limited to 100 items/run |
| eBay | ✅ Multiple available | Robust options for sold listings |
| StockX/GOAT | ✅ Available | Useful if sneakers added later |
| TheRealReal | ❌ Not found | Would need custom build |
| 1stDibs | ❌ Not found | Would need custom build |
| WatchCharts | ❌ Not found | Would need custom build |

**Pros:**
- Large ecosystem (14,000+ scrapers)
- Transparent pricing
- Can build custom scrapers or hire developers
- Free tier sufficient for testing

**Cons:**
- Deprecation risk (saw 3 deprecated Chrono24 scrapers)
- No ready-made scrapers for key jewelry sources
- More complex than simple API calls
- Proxy costs can add up for heavy usage

**Evaluation Scores:**
| Criteria | Score | Notes |
|----------|-------|-------|
| Watch coverage | 4 | Chrono24 good; no WatchCharts |
| Jewelry coverage | 2 | Only Vestiaire; missing TheRealReal, 1stDibs |
| Pricing clarity | 5 | Transparent compute unit model |
| Ease of use | 3 | Learning curve for Actors/CUs |
| Reliability | 3 | Community-maintained; deprecation risk |
| **Total** | **17/25** | |

---

### Retailed.io
- **URL**: https://retailed.io
- **Type**: Curated API wrappers
- **Pricing**: 50 free requests, then contact sales
- **Model**: Pre-built REST APIs for specific marketplaces

**Available APIs:**
| Marketplace | API Status | Notes |
|-------------|------------|-------|
| Chrono24 | ✅ Available | Product and Search endpoints |
| eBay | ✅ Available | Integrated |
| StockX | ✅ Available | Strong coverage |
| GOAT | ✅ Available | Sneaker focus |
| TheRealReal | ❓ Unknown | Not confirmed in research |
| 1stDibs | ❓ Unknown | Not confirmed in research |
| Vestiaire | ❓ Unknown | Not confirmed in research |

**Pros:**
- Simple REST API interface
- They handle maintenance/updates
- Free trial to test
- Good for watches and sneakers

**Cons:**
- Pricing opaque beyond free tier
- Appears narrower than Apify (watches/sneakers focus)
- Jewelry sources unconfirmed
- Potential ToS concerns (scraping Chrono24)

**Evaluation Scores:**
| Criteria | Score | Notes |
|----------|-------|-------|
| Watch coverage | 4 | Chrono24 good; no WatchCharts |
| Jewelry coverage | 2 | Unconfirmed for key sources |
| Pricing clarity | 2 | Must contact sales for paid tiers |
| Ease of use | 5 | Simple REST API |
| Reliability | 4 | Maintained by company |
| **Total** | **17/25** | |

---

## Automation Considerations

**Barriers Identified:**
- Direct site fetching blocked for some domains (Chrono24, WatchCharts)
- No public APIs identified for jewelry sources
- Anti-bot protections likely on high-traffic marketplaces
- Neither automation platform has TheRealReal or 1stDibs scrapers

**Recommended Approach:**

**For Watches:**
1. Test Apify's Chrono24 scraper (free tier)
2. If successful, use for listing-level data
3. Still pursue WatchCharts partnership for aggregated pricing

**For Jewelry:**
1. Test Apify's Vestiaire Collective scraper
2. For TheRealReal/1stDibs, options are:
   - Build custom Apify Actor
   - Pursue direct data partnership
   - Manual research for MVP, automate later

**Platform Recommendation:**
Start with **Apify** — more transparent pricing, larger ecosystem, and ability to build custom scrapers if needed. Retailed.io is simpler but narrower.

---

*Last updated: January 2026*
