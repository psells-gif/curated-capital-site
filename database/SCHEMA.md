# Curated Capital Database Schema

## Overview

This database structure is designed to support the Curated Capital web/mobile application for luxury asset valuation. It separates **retail reference data** from **secondary market listings** while enabling value retention calculations.

## Architecture

```
┌─────────────────────────────────────────────────────────────┐
│                     CURATED CAPITAL DB                       │
├─────────────────────────────────────────────────────────────┤
│  brands.csv           - Brand master data                    │
│  products.csv         - Master product catalog (retail)      │
│  secondary_listings.csv - Secondary market price data        │
│  value_metrics.csv    - Calculated value retention stats     │
└─────────────────────────────────────────────────────────────┘
```

## Table Definitions

### 1. brands.csv
Brand reference data with tier classifications.

| Column | Type | Description |
|--------|------|-------------|
| brand_id | string | Unique identifier (e.g., "cartier", "van-cleef") |
| brand_name | string | Display name |
| brand_type | enum | "jewelry" or "watches" |
| tier | int | 1=Premium, 2=Standard (affects confidence levels) |
| headquarters | string | Country |
| founded | int | Year founded |
| parent_company | string | Parent company if applicable |

### 2. products.csv
Master product catalog from retail sources (brand websites).

| Column | Type | Description |
|--------|------|-------------|
| product_id | string | Unique identifier (brand-collection-sku) |
| brand_id | string | FK to brands |
| collection | string | Product line (Love, Alhambra, etc.) |
| product_name | string | Full product name |
| category | enum | bracelets, rings, necklaces, earrings, watches |
| material_primary | string | Main metal (yellow gold, white gold, platinum) |
| material_secondary | string | Additional materials (diamonds, gemstones) |
| retail_price_usd | decimal | Current retail price |
| size_options | string | Available sizes if applicable |
| reference_number | string | SKU/reference if available |
| source_url | string | Retail source URL |
| date_captured | date | When price was captured |
| date_updated | date | Last update date |
| is_active | boolean | Currently available at retail |
| notes | string | Additional details |

### 3. secondary_listings.csv
Secondary market listings from resale platforms.

| Column | Type | Description |
|--------|------|-------------|
| listing_id | string | Unique identifier |
| brand_id | string | FK to brands |
| product_id | string | FK to products (if matched) |
| product_name | string | Listing title |
| category | enum | Same as products |
| material | string | Material description |
| asking_price_usd | decimal | Listed price |
| original_price_usd | decimal | Original retail if shown |
| discount_pct | decimal | Discount from original/list |
| condition | string | Condition description |
| demand_score | int | 0-10 based on cart indicators |
| source_platform | string | 1stDibs, TheRealReal, Chrono24, etc. |
| listing_url | string | Direct link |
| seller_type | enum | dealer, consignment, private |
| has_certification | boolean | GIA, SSEF, etc. |
| has_box_papers | boolean | Original packaging |
| is_vintage | boolean | Pre-owned vintage item |
| date_captured | date | When captured |
| date_listed | date | When item was listed (if available) |
| notes | string | Additional details |

### 4. value_metrics.csv
Pre-calculated value retention metrics for quick lookups.

| Column | Type | Description |
|--------|------|-------------|
| metric_id | string | Unique identifier |
| brand_id | string | FK to brands |
| collection | string | Product collection |
| category | string | Product category |
| avg_retail_price | decimal | Average retail price |
| avg_secondary_price | decimal | Average secondary market price |
| value_retention_pct | decimal | (secondary/retail) * 100 |
| price_range_low | decimal | Low end of secondary range |
| price_range_high | decimal | High end of secondary range |
| sample_size | int | Number of listings analyzed |
| confidence_level | enum | high, medium, low |
| demand_index | decimal | Average demand score |
| last_calculated | date | When metrics were computed |

## Relationships

```
brands (1) ──────────< (many) products
brands (1) ──────────< (many) secondary_listings
products (1) ────────< (many) secondary_listings (optional match)
brands (1) ──────────< (many) value_metrics
```

## Indexing Strategy

For web/mobile performance:
- Primary: brand_id + category + collection
- Secondary: material_primary, price ranges
- Full-text: product_name (for search)

## API Use Cases

1. **Portfolio Valuation**: Query products by brand/collection → get value_metrics
2. **Item Lookup**: Search secondary_listings by product match
3. **Market Trends**: Aggregate value_metrics over time
4. **Price Alerts**: Monitor secondary_listings for price changes

## Data Freshness

| Table | Update Frequency | Source |
|-------|------------------|--------|
| brands | Quarterly | Manual |
| products | Monthly | Brand website scrapes |
| secondary_listings | Weekly | 1stDibs, TheRealReal APIs |
| value_metrics | Weekly | Calculated from listings |

---

*Schema version 1.0 - January 2026*
