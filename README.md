[My Actor](https://apify.com/violet_jewel/my-actor?fpr=data)

## What does Avito Scraped Products Dataset do?

Avito Scraped Products Dataset enables you to extract more data from Avito than the official Avito API.

It can scrape:

- Product title
- Price
- Location
- Posting date
- Category
- Description
- Images
- Seller information (name and verification)

---

## Example input

```
{
  "startUrls": [
    "https://www.avito.ma/fr/maroc/voitures-%C3%A0_vendre"
  ],
  "maxItems": 500
}
```

## Why scrape Avito?

Avito has millions of users and is a valuable data source for:

- Real estate analysis
- E-commerce insights
- Market intelligence

### Use cases

- Market research and trend analysis
- Price monitoring and benchmarking
- Competitor analysis
- Building datasets for machine learning models

---

## How to scrape Avito

It's easy to get started:

1. Click on **Try for free**
2. Enter keywords or paste a category URL
3. Click on **Run**
4. Preview or download results from the **Dataset tab**

---

### Contact

I am mohamed koualil Data enginner,
Email :  [koualilmohammed@gmail.com](mailto:koualilmohammed@gmail.com)

Linkedin : [https://www.linkedin.com/in/mohamed-koualil-162977218/](https://www.linkedin.com/in/mohamed-koualil-162977218/)

### Paid plans

- **Personal plan ($49/month):** higher limits for regular use
- **Team plan ($499/month):** large-scale data extraction

---

## Results

Example JSON output:

```
{
  "title": "Appartement à vendre à Casablanca",
  "price": "850000 MAD",
  "location": "Casablanca",
  "date": "2026-04-20",
  "category": "Immobilier",
  "description": "Appartement bien situé...",
  "image": "https://...",
  "seller": {
    "name": "Ahmed",
    "verified": true
  }
}
```