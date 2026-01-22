# Curated Capital: Asset Valuation Feasibility Report

**Date**: January 22, 2026
**Prepared by**: Claude (Cowork)

---

## Executive Summary

Automated luxury asset valuation is **feasible for Watches and Branded Jewelry**, with sufficient secondary market data to support a consumer portfolio product. Watches show the strongest data availability with standardized reference numbers enabling precise matching. Branded jewelry (Cartier, Van Cleef, Tiffany) is viable with slightly more complexity due to material/size variants. Art was not fully evaluated but would require separate assessment.

### Category Verdicts

| Category | Verdict | Success Rate | Recommendation |
|----------|---------|--------------|----------------|
| Watches | 🟢 Green | 100% (8/8 items) | **Include in MVP** |
| Branded Jewelry | 🟡 Yellow | 100% (8/8 items, 5 high-confidence) | **Include with caveats** |
| Contemporary Art | ⚪ Not Evaluated | — | Separate research needed |

---

## Detailed Findings

### Watches

**Overall assessment**: Excellent data availability. The secondary watch market has mature data infrastructure that Curated Capital can leverage directly.

**Data availability**: Every test item had multiple price points from multiple sources. Prices from different sources converged tightly (typically within 10-15% variance). High-volume models show hundreds of monthly transactions providing robust price signals.

**Best sources identified**:
1. **WatchCharts** — Aggregates market prices, provides trend data, sales velocity, and risk scores. Already does the valuation work; investigate API/partnership.
2. **Chrono24** — Largest marketplace with extensive listings searchable by exact reference number.
3. **eBay (sold listings)** — Transaction validation, though authentication concerns reduce confidence.

**Challenges encountered**:
- Direct site fetching blocked for some domains (workaround: public search results contain data)
- Discontinued models (e.g., Patek 5711) show wider price variance based on year/condition
- Variant pricing exists (bracelet type, dial color) but is manageable

**Sample results**:

| Item | Sources Found | Price Range | Confidence |
|------|---------------|-------------|------------|
| Rolex Daytona 116500LN | 3 | $28K–$40K | High |
| Rolex Submariner 126610LN | 3 | $13K–$16K | High |
| Patek Philippe Nautilus 5711/1A | 3 | $80K–$137K | High |
| Omega Speedmaster 310.30.42.50.01.001 | 3 | $5K–$7K | High |

**Recommendation**: Include watches in MVP. Reference numbers enable exact matching. Prioritize WatchCharts integration for aggregated pricing; supplement with Chrono24 listings.

---

### Branded Jewelry

**Overall assessment**: Viable with conditions. Branded luxury jewelry from Cartier, Van Cleef & Arpels, and Tiffany has sufficient secondary market data, though more input parameters are required than watches.

**Data availability**: All test items found across multiple sources. However, price variance within product lines is higher due to material variants (gold color, stone type, diamond count, size).

**Best sources identified**:
1. **The RealReal** — Best overall. Authenticated consignment with "estimated retail" shown alongside asking price. Enables instant value retention calculations.
2. **1stDibs** — Large inventory but wide price variance; better for establishing ranges than precise values.
3. **Fashionphile** — Good secondary validation source.

**Challenges encountered**:
- Material variants create pricing complexity (same "Love bracelet" ranges $4K–$58K depending on configuration)
- Size significantly affects price and liquidity
- Tiffany pieces had fewer listings and lower confidence than Cartier/Van Cleef
- No WatchCharts equivalent exists for jewelry (no aggregation layer)

**Sample results**:

| Item | Sources Found | Price Range | Confidence |
|------|---------------|-------------|------------|
| Van Cleef Vintage Alhambra pendant (onyx) | 3 | $2,200–$2,895 | High |
| Cartier Love bracelet (yellow gold) | 3 | $5,375–$7,350 | High |
| Cartier Juste un Clou bracelet | 3 | $7,500–$15,000 | High |
| Tiffany HardWear Ball pendant | 3 | $1,000–$4,500 | Low |

**Recommendation**: Include Cartier and Van Cleef in MVP (Tier 1). Include Tiffany with wider valuation ranges (Tier 2). Product must capture Brand + Collection + Metal + Material + Size for accurate matching.

---

### Contemporary Art

**Overall assessment**: Not evaluated per project scope decision.

**Data availability**: Unknown. Initial observations suggest art valuation is more complex due to edition sizes, provenance requirements, condition sensitivity, and authenticity verification.

**Best sources identified**: Not evaluated. Likely candidates include Artsy, Heritage Auctions, and Artnet (subscription).

**Challenges encountered**: N/A

**Sample results**: N/A

**Recommendation**: Conduct separate research phase if art category is desired. Expect higher complexity and lower confidence than watches/jewelry.

---

## Key Insights

### What Works
- **Reference numbers are powerful**: Watch valuations work because 116500LN means exactly one product globally
- **Branded jewelry has standardized product lines**: "Cartier Love bracelet yellow gold" is a known, comparable product
- **Multiple sources converge**: When 3 sources show similar prices, confidence is high
- **Authenticated platforms add value**: The RealReal's authentication + retail benchmark is uniquely useful
- **Value retention data exists**: Cartier reports 79% retail retention, 95% for Juste un Clou — this is marketable

### What Doesn't Work
- **Unbranded/custom jewelry**: Without standardized products, matching is impossible
- **Unauthenticated marketplaces**: FB Marketplace, Craigslist add noise without signal
- **Art (likely)**: Edition complexity, provenance, and authenticity create valuation challenges
- **Direct scraping**: Sites block automated access; partnerships/APIs needed for production

### Automation Potential

| Source | Automation Path | Effort |
|--------|-----------------|--------|
| WatchCharts | API/data licensing partnership | Medium — they may have existing products |
| Chrono24 | Unknown — investigate API | Medium-High |
| The RealReal | Partnership needed | High — no public API |
| eBay | API exists (restricted) | Medium — rate limits apply |

**Recommended approach**: Build relationships with 2-3 key data providers rather than attempting to scrape many sources. WatchCharts for watches, The RealReal for jewelry would cover 80% of use cases.

---

## Product Implications

### MVP Scope Recommendation

**Include at launch:**
- ✅ Watches: Rolex, Patek Philippe, Audemars Piguet, Omega
- ✅ Jewelry Tier 1: Cartier (Love, Juste un Clou, Panthère), Van Cleef & Arpels (Alhambra, Perlée)
- ⚠️ Jewelry Tier 2: Tiffany (T Collection, HardWear) — with wider ranges and lower confidence display

**Exclude from launch:**
- ❌ Contemporary Art — requires separate validation
- ❌ Non-branded jewelry
- ❌ Vintage/antique pieces (too variable)

### Valuation Methodology

**Recommended approach: Ranges with confidence indicators**

Rather than showing single values, display:
- **Estimated range**: $14,000 – $17,000
- **Confidence level**: High / Medium / Low
- **Based on**: X listings from Y sources
- **Value retention**: "This piece typically retains 95% of retail value"

This approach:
- Sets appropriate user expectations
- Accounts for condition variance
- Provides defensible valuations
- Adds educational value (retention %)

### User Experience Considerations

**Required user inputs:**
- Watches: Brand, Model, Reference Number, Condition, Box/Papers
- Jewelry: Brand, Collection, Metal Color, Material (stone type), Size

**Display elements:**
- Current estimated value (range)
- Retail price benchmark
- Value retention percentage
- Historical trend (if available from WatchCharts)
- Confidence indicator

**Transparency features:**
- "How we calculate this" explainer
- Links to source listings
- Last updated timestamp

### Future Expansion

**Phase 2 candidates:**
- Additional watch brands (Tudor, IWC, Vacheron Constantin)
- Additional jewelry brands (Bvlgari, Harry Winston)
- Handbags (Hermès, Chanel — strong secondary market data exists)

**Phase 3 candidates (require separate research):**
- Contemporary art (prints and editions only)
- Wine and spirits
- Collectible sneakers

---

## Appendix

### A. Complete Valuation Results
See: `valuation-results.csv`

### B. Data Source Evaluations
See: `data-sources.md`

### C. Test Items Used
See original: `references/test-items.md`

---

*Report completed January 22, 2026*
