# Curated Capital: Portfolio App
## Product Specification Document

**Version:** 0.1 (Draft)  
**Last Updated:** January 22, 2026  
**Author:** Patrick Sells  
**Status:** Concept Development

---

## 1. Executive Summary

### Vision
Transform how affluent collectors understand and leverage their luxury assets by providing a unified "portfolio view" that treats watches, jewelry, and art as the financial assets they truly are.

### One-Liner
*"The portfolio view for what you actually own."*

### Core Insight
Sophisticated collectors already think of their watches, art, and jewelry as assets—not just possessions. But the financial system doesn't treat them that way. There's no portfolio view, no market price, no liquidity visibility. These assets are invisible capital.

### The Promise
Curated Capital makes your collection legible as what it actually is—a portfolio. See it. Value it. Unlock it.

---

## 2. Target User

### Primary Persona: The Affluent Collector

**Demographics:**
- Net worth: $1M - $10M (mass affluent to lower HNW)
- Age: 35-60
- Location: Major metros (starting with DFW)
- Owns $250K - $500K+ in luxury collectibles across categories

**Psychographics:**
- Views luxury purchases as both enjoyment AND investment
- Lists items on personal financial statements
- Likely has scheduled items on insurance policies
- Frustrated by lack of visibility into asset values
- Values discretion and sophistication over mass-market solutions
- Probably uses a wealth advisor or accountant

**Current Behavior:**
- Tracks collection in spreadsheets (if at all)
- Checks Chrono24 occasionally for watch values
- Gets periodic insurance appraisals (every 2-3 years)
- Has no single source of truth for total collection value
- Doesn't know borrowing capacity against assets

**Pain Points:**
1. "I think my collection is worth $X, but I don't really know"
2. "I can't easily show my advisor what I own and what it's worth"
3. "Getting appraisals is expensive and time-consuming"
4. "I don't know if I should sell something or borrow against it"
5. "My insurance coverage might be outdated"

### Secondary Persona: The Aspiring Collector

- Owns $50K - $250K in collectibles
- Building collection intentionally
- Wants to track performance like investments
- Price-sensitive but willing to pay for value
- May grow into primary persona over time

---

## 3. Product Overview

### What It Is
A subscription-based web/mobile application that allows collectors to:
1. Inventory their luxury assets in one place
2. See real-time (or near-real-time) market valuations
3. Track performance over time (gain/loss vs. purchase price)
4. Understand borrowing capacity against their collection
5. Access liquidity through Curated Capital lending (when ready)

### What It Is NOT
- A marketplace (we don't facilitate buying/selling between users)
- An appraisal service (valuations are indicative, not certified)
- A replacement for insurance (but complements it)
- A social network for collectors

### Core Value Propositions

| For User | Benefit |
|----------|---------|
| Clarity | Know what your collection is actually worth today |
| Convenience | One dashboard instead of spreadsheets + multiple sites |
| Confidence | Data-backed valuations from real market sources |
| Liquidity | See and access borrowing capacity instantly |
| Legacy | Documented collection for estate planning/insurance |

---

## 4. Feature Set

### 4.1 MVP Features (Phase 1)

#### Asset Inventory Management
- Add assets manually with structured fields
- Upload photos (up to 6 per asset)
- Attach documents (COAs, receipts, appraisals, insurance docs)
- Categorize by type (Watch, Jewelry, Art)
- Record purchase details (date, price, seller, condition)
- Track location (home, safe deposit, on loan, etc.)

#### Automated Valuations
- Match assets to market data sources
- Display current estimated market value
- Show value range (low/mid/high) where data supports
- Display data sources used for valuation
- Update valuations on regular cadence (daily for watches, weekly for others?)
- Flag when valuation confidence is low

#### Portfolio Dashboard
- Total portfolio value (aggregate)
- Value by category (watches, jewelry, art)
- Performance metrics (total gain/loss, % change)
- Individual asset cards with key metrics
- Filter/sort capabilities

#### Borrowing Capacity Display
- Show LTV ratio available (e.g., 50%)
- Calculate borrowing capacity per asset
- Show total portfolio borrowing capacity
- CTA to initiate loan inquiry

### 4.2 Phase 2 Features

#### Enhanced Valuations
- Price history charts per asset
- Market trend indicators (rising/falling/stable)
- Comparable sales display
- Integration with auction results

#### Alerts & Notifications
- Value change alerts (asset up/down X%)
- Insurance coverage gap warnings
- Market opportunity alerts ("Your Daytona is at 52-week high")

#### Reporting
- Portfolio summary report (PDF export)
- Insurance documentation report
- Tax basis report
- Performance report by time period

#### User Account Features
- Profile management
- Notification preferences
- Data export
- Account security (2FA)

### 4.3 Phase 3 Features (Future)

#### Loan Integration
- Apply for loan directly in app
- Upload required documents
- Track loan status
- Manage active loans
- Payment history

#### Advanced Analytics
- Portfolio diversification analysis
- Risk assessment
- Optimization suggestions
- Market insights/research

#### Concierge Services
- Request professional appraisal
- Insurance review scheduling
- White-glove asset pickup for loans

#### Multi-User / Advisor Access
- Share portfolio with wealth advisor (read-only)
- Family office multi-account management
- Beneficiary access controls

---

## 5. User Stories

### Inventory Management

```
As a collector,
I want to add a new watch to my portfolio
So that I can track its value alongside my other assets

Acceptance Criteria:
- Can select "Watch" as asset category
- Required fields: Brand, Model, Reference Number
- Optional fields: Serial number, purchase date, purchase price, 
  condition, box/papers, seller, notes
- Can upload up to 6 photos
- Can attach documents (PDF, images)
- System attempts to match to known reference for valuation
- Asset appears in portfolio immediately after save
```

```
As a collector,
I want to upload my insurance schedule
So that the app can pre-populate my inventory

Acceptance Criteria:
- Accept PDF or image upload
- Parse scheduled items (may require manual review)
- Create draft asset entries for review
- User confirms/edits before adding to portfolio
```

```
As a collector,
I want to record where each asset is physically located
So that I can track items across multiple locations

Acceptance Criteria:
- Location field with presets (Home, Safe Deposit, Vault, On Loan, Other)
- Custom location option
- Location history tracking
- Filter portfolio by location
```

### Valuations

```
As a collector,
I want to see the current market value of my Rolex Daytona
So that I know what it's worth today

Acceptance Criteria:
- Display estimated market value prominently
- Show value range if available (low/mid/high)
- List data sources used (e.g., "Based on Chrono24, WatchCharts")
- Show last updated timestamp
- Indicate confidence level (high/medium/low)
```

```
As a collector,
I want to understand why an asset's valuation changed
So that I can make informed decisions

Acceptance Criteria:
- Show previous value and new value
- Display % change
- Link to comparable listings/sales if available
- Provide market context where possible
```

```
As a collector,
I want to manually override a valuation
So that I can use my own appraisal or knowledge

Acceptance Criteria:
- "Set custom value" option per asset
- Can enter custom value with optional note/source
- Custom value clearly marked in UI
- Can revert to automated valuation anytime
- Custom values excluded from automated updates
```

### Portfolio View

```
As a collector,
I want to see my total portfolio value at a glance
So that I understand my overall position

Acceptance Criteria:
- Total value displayed prominently on dashboard
- Breakdown by category visible
- Total gain/loss shown ($ and %)
- Comparison to cost basis
```

```
As a collector,
I want to filter my portfolio by category
So that I can focus on specific asset types

Acceptance Criteria:
- Filter buttons for All, Watches, Jewelry, Art
- Counts and subtotals update with filter
- Filter state persists during session
- URL updates for shareability/bookmarking
```

### Borrowing

```
As a collector,
I want to see how much I could borrow against my collection
So that I understand my liquidity options

Acceptance Criteria:
- Display total borrowing capacity (portfolio level)
- Show capacity per asset
- Explain LTV ratio used
- CTA to learn more / start application
```

```
As a collector,
I want to request a loan against a specific asset
So that I can access liquidity without selling

Acceptance Criteria:
- "Borrow against this asset" button on asset detail
- Shows estimated loan amount
- Captures contact info if not logged in
- Routes to loan application flow
- Loan inquiry tracked in system
```

### Account & Settings

```
As a collector,
I want to export my portfolio data
So that I can use it for insurance, taxes, or estate planning

Acceptance Criteria:
- Export to CSV option
- Export to PDF report option
- Include all asset details and current valuations
- Include photos in PDF export
- Timestamp on export
```

```
As a collector,
I want to set up alerts for value changes
So that I stay informed without checking constantly

Acceptance Criteria:
- Configure alert threshold (e.g., notify if value changes >5%)
- Choose notification method (email, push, SMS)
- Per-asset or portfolio-level alerts
- Ability to mute/snooze alerts
```

---

## 6. Data Model

### Core Entities

#### User
```
User {
  id: UUID
  email: String (unique)
  password_hash: String
  first_name: String
  last_name: String
  phone: String (optional)
  created_at: Timestamp
  updated_at: Timestamp
  subscription_tier: Enum (free, premium)
  subscription_status: Enum (active, canceled, past_due)
  settings: JSON
}
```

#### Asset
```
Asset {
  id: UUID
  user_id: UUID (FK -> User)
  category: Enum (watch, jewelry, art)
  status: Enum (active, sold, lost, archived)
  
  // Identity
  name: String (display name)
  brand: String
  model: String (optional)
  reference_number: String (optional)
  serial_number: String (optional, encrypted)
  
  // Acquisition
  purchase_date: Date (optional)
  purchase_price: Decimal (optional)
  purchase_currency: String (default: USD)
  seller: String (optional)
  acquisition_method: Enum (purchase, gift, inheritance, other)
  
  // Condition & Details
  condition: Enum (mint, excellent, very_good, good, fair)
  condition_notes: Text (optional)
  
  // Location
  location: String
  location_details: String (optional)
  
  // Valuation
  current_value: Decimal
  current_value_low: Decimal (optional)
  current_value_high: Decimal (optional)
  valuation_confidence: Enum (high, medium, low)
  valuation_sources: JSON Array
  valuation_updated_at: Timestamp
  custom_value: Decimal (optional, user override)
  custom_value_note: String (optional)
  
  // Lending
  ltv_ratio: Decimal (default: 0.50)
  loan_capacity: Decimal (computed)
  
  // Metadata
  notes: Text (optional)
  created_at: Timestamp
  updated_at: Timestamp
}
```

#### Asset_Photo
```
Asset_Photo {
  id: UUID
  asset_id: UUID (FK -> Asset)
  storage_url: String
  thumbnail_url: String
  display_order: Integer
  caption: String (optional)
  created_at: Timestamp
}
```

#### Asset_Document
```
Asset_Document {
  id: UUID
  asset_id: UUID (FK -> Asset)
  document_type: Enum (coa, receipt, appraisal, insurance, warranty, other)
  file_name: String
  storage_url: String
  uploaded_at: Timestamp
}
```

#### Valuation_History
```
Valuation_History {
  id: UUID
  asset_id: UUID (FK -> Asset)
  value: Decimal
  value_low: Decimal (optional)
  value_high: Decimal (optional)
  sources: JSON Array
  recorded_at: Timestamp
}
```

#### Loan_Inquiry
```
Loan_Inquiry {
  id: UUID
  user_id: UUID (FK -> User)
  asset_id: UUID (FK -> Asset, optional if portfolio-level)
  requested_amount: Decimal (optional)
  status: Enum (submitted, contacted, converted, declined, expired)
  notes: Text
  created_at: Timestamp
  updated_at: Timestamp
}
```

### Category-Specific Extensions

#### Watch_Details
```
Watch_Details {
  asset_id: UUID (FK -> Asset)
  
  movement: String (optional)
  case_material: String (optional)
  case_size: String (optional)
  dial_color: String (optional)
  bracelet_type: String (optional)
  year_of_production: Integer (optional)
  
  box_included: Boolean
  papers_included: Boolean
  service_history: Text (optional)
  last_service_date: Date (optional)
}
```

#### Jewelry_Details
```
Jewelry_Details {
  asset_id: UUID (FK -> Asset)
  
  jewelry_type: Enum (ring, bracelet, necklace, earrings, brooch, other)
  metal_type: String (optional)
  metal_purity: String (optional)
  gemstones: JSON Array (optional)
  total_carat_weight: Decimal (optional)
  size: String (optional)
  collection_name: String (optional)
  
  certification: String (optional, e.g., GIA number)
  box_included: Boolean
  papers_included: Boolean
}
```

#### Art_Details
```
Art_Details {
  asset_id: UUID (FK -> Asset)
  
  artist: String
  title: String
  year_created: Integer (optional)
  medium: String (optional)
  dimensions: String (optional)
  edition_info: String (optional, e.g., "45/100")
  signed: Boolean
  
  provenance: Text (optional)
  exhibition_history: Text (optional)
  literature: Text (optional)
  
  framed: Boolean
  coa_included: Boolean
}
```

---

## 7. Valuation Engine

### Overview
The valuation engine is the core differentiator. It aggregates pricing data from multiple sources to provide automated market valuations.

### Data Sources by Category

#### Watches
| Source | Data Type | Access Method | Confidence |
|--------|-----------|---------------|------------|
| Chrono24 | Listings, sold | Scraping/API | High |
| WatchCharts | Aggregated prices | API (paid?) | High |
| eBay Sold | Completed sales | API | Medium |
| Bob's Watches | Dealer prices | Scraping | Medium |

#### Jewelry
| Source | Data Type | Access Method | Confidence |
|--------|-----------|---------------|------------|
| The RealReal | Listings, sold | Scraping | Medium |
| 1stDibs | Listings | Scraping | Medium |
| Rebag | Listings | Scraping | Medium |
| Vestiaire Collective | Listings | Scraping | Low-Medium |

#### Art
| Source | Data Type | Access Method | Confidence |
|--------|-----------|---------------|------------|
| Artsy | Listings, auction | API? | Medium |
| MyArtBroker | Valuations (prints) | Partnership? | High |
| Heritage Auctions | Auction results | Scraping | High |
| Artnet | Auction database | Subscription | High |

### Matching Algorithm

1. **Exact Match**: Reference number / SKU matches known item
   - Confidence: High
   - Use: Average of recent listings/sales

2. **Fuzzy Match**: Brand + Model + Key attributes match
   - Confidence: Medium
   - Use: Range based on similar items

3. **Category Match**: Only category and brand match
   - Confidence: Low
   - Use: Prompt user for more details or manual valuation

### Update Cadence

| Category | Update Frequency | Rationale |
|----------|------------------|-----------|
| Watches | Daily | Active market, good data density |
| Jewelry | Weekly | Less liquid, fewer comps |
| Art | Weekly | Auction-driven, episodic data |

### Confidence Scoring

```
High Confidence:
- 3+ sources with data
- Exact reference match
- Recent data (<30 days)
- Tight price range (<20% spread)

Medium Confidence:
- 2 sources with data
- Fuzzy match on key attributes
- Moderate price range (20-40% spread)

Low Confidence:
- 1 source or no matches
- Wide price range (>40% spread)
- Stale data (>90 days)
- User should consider professional appraisal
```

---

## 8. Business Model

### Pricing Tiers

#### Free Tier
- Inventory management (unlimited assets)
- Manual valuations only (user enters values)
- Basic portfolio view
- No automated valuations
- No borrowing capacity display

**Purpose:** Drive adoption, build habit, capture data

#### Premium Tier ($19.99/month or $199/year)
- Everything in Free
- Automated market valuations
- Valuation history & charts
- Borrowing capacity display
- Value alerts
- PDF reports
- Priority support

**Purpose:** Core revenue, value delivery

#### Future: Concierge Tier ($99/month?)
- Everything in Premium
- Professional appraisal credits
- Dedicated account manager
- Advisor sharing
- API access

### Revenue Streams

1. **Subscriptions** (primary)
   - Target: 1,000 premium subscribers = $240K ARR

2. **Lending Revenue** (strategic)
   - Loans originated through app
   - Lower CAC than cold acquisition
   - Pre-qualified, pre-appraised collateral

3. **Future Potential**
   - Appraisal referral fees
   - Insurance referral fees
   - Data licensing (anonymized market insights)

---

## 9. Technical Architecture (High-Level)

### Frontend
- **Web App:** React / Next.js
- **Mobile:** React Native (Phase 2) or PWA
- **Hosting:** Vercel or similar

### Backend
- **API:** Node.js / Express or Python / FastAPI
- **Database:** PostgreSQL
- **Auth:** Auth0 or Supabase Auth
- **File Storage:** AWS S3 or Cloudflare R2
- **Hosting:** AWS / Railway / Render

### Valuation Engine
- **Scheduler:** Cron jobs for periodic updates
- **Scrapers:** Python scripts (respect ToS, rate limits)
- **Data Pipeline:** Queue-based processing
- **Caching:** Redis for frequently accessed valuations

### Third-Party Services
- **Payments:** Stripe
- **Email:** SendGrid / Postmark
- **Analytics:** Mixpanel / PostHog
- **Error Tracking:** Sentry

---

## 10. Success Metrics

### North Star Metric
**Total Portfolio Value Tracked** — Represents user trust and engagement

### Primary Metrics

| Metric | Definition | Target (Year 1) |
|--------|------------|-----------------|
| Registered Users | Total accounts | 5,000 |
| Premium Subscribers | Paying users | 500 |
| Monthly Active Users | Logged in past 30 days | 2,000 |
| Assets Tracked | Total assets in system | 15,000 |
| Portfolio Value Tracked | Sum of all valuations | $50M |

### Secondary Metrics

| Metric | Definition | Target |
|--------|------------|--------|
| Free → Premium Conversion | % of free users who upgrade | 10% |
| Churn Rate | Monthly premium cancellations | <5% |
| Loan Inquiries | Users requesting loans | 50/month |
| NPS | Net Promoter Score | >50 |
| Valuation Accuracy | User-reported accuracy | >85% satisfied |

---

## 11. Risks & Mitigations

| Risk | Impact | Likelihood | Mitigation |
|------|--------|------------|------------|
| Valuation data unavailable | Core feature broken | Medium | Multiple sources, manual fallback, partnerships |
| Scraping blocked by sources | Loss of data | Medium | Respect ToS, diversify sources, pursue APIs |
| Low conversion to premium | Revenue shortfall | Medium | Strong free tier hook, clear premium value |
| Privacy/security breach | Reputation, legal | Low | Encryption, SOC2, minimal PII storage |
| Competitor launches similar | Market share loss | Medium | Speed to market, lending integration moat |
| Users don't trust valuations | Low engagement | Medium | Transparency on sources, conservative estimates |

---

## 12. Open Questions

1. **Freemium balance:** Is inventory-only compelling enough for free tier, or do we need some valuation preview?

2. **Mobile priority:** Start web-only and add mobile later, or go mobile-first?

3. **Brand architecture:** Same "Curated Capital" brand for app and lending, or separate?

4. **B2B opportunity:** Offer white-label or API to wealth advisors, family offices, insurance companies?

5. **Geographic scope:** DFW-only initially (matches lending footprint) or national from day one?

6. **Data partnerships:** Pursue formal partnerships with Chrono24, WatchCharts, Artsy vs. scraping?

7. **Appraisal integration:** Partner with appraisers for "upgrade to certified" flow?

---

## 13. Roadmap (Tentative)

### Q1 2026: Validation
- [x] Concept development
- [x] Competitive analysis
- [ ] Data source feasibility study (Cowork)
- [ ] User interviews (5-10 target persona)
- [ ] Finalize MVP feature set

### Q2 2026: MVP Build
- [ ] Design system & UI components
- [ ] Core inventory functionality
- [ ] Watch valuation integration
- [ ] Basic dashboard
- [ ] User auth & accounts

### Q3 2026: Beta Launch
- [ ] Invite-only beta (50-100 users)
- [ ] Jewelry & art valuations
- [ ] Borrowing capacity display
- [ ] Iterate based on feedback
- [ ] Payment integration

### Q4 2026: Public Launch
- [ ] Open registration
- [ ] Marketing push (DFW focus)
- [ ] Loan integration
- [ ] Mobile app development begins

---

## Appendix A: Competitive Landscape

| Product | Strengths | Weaknesses | Our Differentiation |
|---------|-----------|------------|---------------------|
| Chrono24 Watch Collection | Great watch data, free | Watches only, no lending | Multi-category, lending |
| WatchCharts | Excellent analytics | Watches only, paid | Multi-category, inventory |
| MyArtBroker MyPortfolio | Good for prints | Art only, narrow focus | Multi-category, lending |
| Artwork Archive | Strong inventory | No auto-valuations | Auto-valuations |
| Collectibles.com | Broad categories | New, unproven | Luxury focus, lending |

---

## Appendix B: Sample Screens

See: `client-portal.html` for interactive prototype

---

*Document Status: Living document. Update as decisions are made.*
