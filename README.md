[My Actor](https://apify.com/sanztheo/my-actor?fpr=data)

# AliExpress Product Scraper API - Supplier Score & Profit Calculator

Extract AliExpress products with **supplier reliability scores (0-100)** and **automated profit analysis** for Amazon, eBay, Shopify dropshipping. The only scraper with ISM-based supplier quality ratings and ROI calculations.

## What Data Can You Extract from AliExpress?

| Data Field | Description | Example |
| --- | --- | --- |
| **Product Info** | Title, ID, URL, images | "Wireless Bluetooth Earbuds TWS" |
| **Pricing** | Current price, original, discount % | $12.99 (was $25.98, -50%) |
| **Ratings** | Score, review count | 4.7/5 (3,245 reviews) |
| **Sales** | Units sold | 15,420 sold |
| **Shipping** | Free shipping, delivery time | Free, 15-25 days |
| **Supplier Score** | 0-100 reliability rating | 92/100 "Good" |
| **Supplier Details** | Name, years active, followers | "Official Store", 5 years, 125K |
| **Profit Analysis** | ROI, margin, platform fees | 36.6% margin, $9.15 profit |
| **Tariffs** | Import duties by country | US, UK, EU, CA, AU rates |

---

## AliExpress Scraper Unique Features

### Supplier Reliability Scoring (Industry-First)

Automatically evaluates supplier quality using **ISM supply chain standards**:

- **0-100 reliability score** based on 5 weighted factors
- **Trust levels**: Excellent (95+), Good (85+), Acceptable (75+), Fair (65+), Poor (<65)
- **Score components**: Quality (35%), Delivery (30%), Communication (15%), Maturity (12%), Certifications (8%)
- Filter out risky suppliers before placing orders

### Automated Dropshipping Profit Calculator

Get instant ROI analysis for every product:

- **Platform fees**: Amazon FBA (15%), eBay (13.25%), Shopify (2.9% + $0.30), Etsy (6.5%), Walmart (15%)
- **Import tariffs 2025**: Automatic duty calculation (US, UK, EU, CA, AU)
- **Profit margin & breakeven** calculations
- **Recommendation**: Excellent (30%+), Good (20%+), Acceptable (15%+), Low (<15%)

### Multi-Region AliExpress Support

Scrape from 5 regional domains:

| Region | Domain | Currency |
| --- | --- | --- |
| French | fr.aliexpress.com | EUR |
| English | [www.aliexpress.com](http://www.aliexpress.com) | USD |
| Spanish | es.aliexpress.com | EUR |
| German | de.aliexpress.com | EUR |
| Italian | it.aliexpress.com | EUR |

### Enterprise Anti-Detection System

- **Playwright cookie harvester** with stealth plugin
- **Dynamic fingerprint rotation** (user-agent, headers, screen resolution)
- **Session management** (10-min expiry, 50 requests/session)
- **Human-like delays** with Gaussian distribution
- **95%+ success rate** with residential proxies

---

## How Much Does AliExpress Scraper Cost?

**$0.0025 per product** ($2.50 per 1,000 products)

| Products | Cost | Use Case |
| --- | --- | --- |
| 100 | $0.25 | Quick product research |
| 1,000 | $2.50 | Category analysis |
| 10,000 | $25.00 | Full market research |
| 50,000 | $125.00 | Enterprise sourcing |

**No monthly fees. No minimum. Pay only for results.**

---

## How to Use AliExpress Scraper

### Required Input

- **keywords** (array) - 1-10 search terms

### Optional Settings

| Parameter | Default | Description |
| --- | --- | --- |
| maxPages | 2 | Pages per keyword (~20 products/page) |
| maxConcurrency | 2 | Parallel requests (1-5) |
| language | fr | Regional domain (fr/en/es/de/it) |
| useProxy | true | Use Apify residential proxies |
| proxyCountryCode | FR | Proxy location (FR/US/GB/DE/ES/IT) |
| minDelay | 2000 | Minimum delay between requests (ms) |
| maxDelay | 6000 | Maximum delay between requests (ms) |

### Example Input

```
{
  "keywords": ["wireless earbuds", "phone holder", "usb cable"],
  "maxPages": 3,
  "language": "en",
  "maxConcurrency": 2,
  "useProxy": true,
  "proxyCountryCode": "US"
}
```

---

## AliExpress Product Data Output

Each product includes complete data with supplier scoring and profit analysis:

```
{
  "id": "1005007890123456",
  "title": "Original Wireless Bluetooth Earphones TWS Earbuds",
  "url": "https://www.aliexpress.com/item/1005007890123456.html",
  "imageUrl": "https://ae01.alicdn.com/kf/S12345678.jpg",

  "price": {
    "current": 12.99,
    "original": 25.98,
    "currency": "USD",
    "discount": 50
  },

  "rating": {
    "score": 4.7,
    "count": 3245
  },

  "sales": {
    "count": 15420,
    "display": "15K+ sold"
  },

  "shipping": {
    "isFreeShipping": true,
    "price": 0,
    "estimatedDays": "15-25 days"
  },

  "supplier": {
    "id": "1234567",
    "name": "Official Store",
    "reliabilityScore": 92,
    "trustLevel": "Good",
    "feedbackScore": 4.8,
    "positiveRate": 98.5,
    "followerCount": 125000,
    "yearsActive": 5,
    "certifications": ["Top Brand", "Official Store"]
  },

  "profitAnalysis": {
    "costs": {
      "productCost": 12.99,
      "platformFees": 2.85,
      "tariff": 0,
      "totalCost": 15.84
    },
    "profit": {
      "grossProfit": 9.15,
      "profitMargin": 36.6,
      "roi": 57.8
    },
    "recommendation": "excellent"
  },

  "keyword": "wireless earbuds",
  "scrapedAt": "2026-01-22T10:30:00Z"
}
```

---

## AliExpress Scraper Use Cases

### Dropshipping Product Research

- Find winning products with high sales and good ratings
- **Filter suppliers by reliability score** (avoid <75)
- Calculate profit margins before adding to store

### Amazon FBA / eBay Arbitrage

- **Automated profit analysis** for your target platform
- Identify products with 30%+ profit margins
- Factor in import duties and VAT automatically

### Market Research & Competitor Analysis

- Track pricing trends across categories
- Analyze top sellers and their suppliers
- Compare prices across 5 regional domains

### Wholesale Supplier Verification

- **Verify supplier quality** with 0-100 reliability scores
- Check delivery performance and on-time rates
- Validate certifications (Top Brand, Official Store)

---

## How AliExpress Scraper Works

1. **Input keywords** - Provide 1-10 search terms
2. **Cookie harvesting** - Playwright auto-harvests session cookies with stealth
3. **Dual-mode scraping**:

- **API mode** (with cookie) - Uses AliExpress internal API for accuracy
- **HTML mode** (fallback) - Direct HTML parsing if API unavailable
4. **Anti-detection** - Rotates fingerprints, sessions, and proxies
5. **Supplier scoring** - Calculates 0-100 ISM-based reliability score
6. **Profit calculation** - Analyzes ROI with platform fees and tariffs
7. **Dataset export** - Download results as JSON, CSV, or Excel

### Performance

| Metric | Value |
| --- | --- |
| Products per page | ~20 (AliExpress standard) |
| Recommended concurrency | 2-3 requests |
| Typical speed | 500-1,000 products/hour |
| Success rate | 95%+ with proxies |

---

## AliExpress Scraper vs Competitors

| Feature | This Scraper | Other Scrapers |
| --- | --- | --- |
| Supplier reliability score | **0-100 ISM-based** | Basic info only |
| Profit calculator | **7 platforms + 2025 tariffs** | Not included |
| Anti-detection | **Playwright + stealth + fingerprints** | Basic headers |
| Multi-region support | **5 domains** (FR, EN, ES, DE, IT) | 1-2 domains |
| Cookie harvesting | **Automatic Playwright** | Manual setup |
| Session rotation | **Auto (10min/50 requests)** | None |

---

## Frequently Asked Questions

### Do I need an AliExpress account to scrape?

No. The scraper works without authentication. Cookies are harvested automatically.

### How accurate is the supplier reliability score?

- **Search results only**: Estimated score with ~70% confidence
- **With store data**: Accurate score with ~95% confidence

### Can I calculate profit for custom platforms?

Yes! Use `platform: "custom"` and provide your `customPlatformFee` percentage.

### How do I avoid getting blocked by AliExpress?

- Enable **residential proxies** (`useProxy: true`)
- Lower **maxConcurrency** to 1-2
- Increase delays (`minDelay: 5000`, `maxDelay: 10000`)

### What export formats are available?

JSON, CSV, Excel, and direct API access via Apify datasets.

### Is this scraper compliant with AliExpress terms?

This tool is for research purposes. Users are responsible for compliance with AliExpress ToS.

---

## Support & Custom Development

- **Issues?** Open a ticket in the Issues tab
- **Custom features?** Contact for enterprise solutions
- **Updates**: Actor is actively maintained with regular updates

---

**Keywords**: aliexpress scraper, aliexpress api, aliexpress product data, dropshipping scraper, supplier quality score, profit calculator, amazon fba arbitrage, ebay dropshipping, shopify product research, aliexpress bulk extractor, supplier verification, import duty calculator, roi analysis tool, aliexpress crawler, product research api