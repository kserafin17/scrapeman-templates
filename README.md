# scrapeman-templates

Community scraping templates for **scrapeman.dev** — the visual web scraper Chrome extension.

## Browse templates

All templates live in [`templates.json`](./templates.json) and are loaded directly in the extension's **Library** tab. No API key or sign-in needed.

## Submit a template

1. Open scrapeman.dev in your browser and configure your scraping setup
2. Go to the **Library** tab → click **+ Share**
3. Fill in description, site and category, then click **Open submission**
4. The JSON is copied to your clipboard — paste it into the GitHub issue and submit

Submissions are reviewed before being merged into the library.

## Template format

```json
{
  "id": "unique-kebab-id",
  "name": "Human-readable name",
  "description": "What does it scrape and from which site?",
  "site": "example.com",
  "category": "ecommerce | jobs | realestate | social | news | travel | other",
  "author": "your-github-username",
  "uses": 0,
  "config": {
    "blockSelector": "CSS selector for the repeating block",
    "fields": [
      {
        "name": "Field name",
        "type": "text | number | link | image | date",
        "required": true,
        "selector": "CSS selector",
        "confidence": 90
      }
    ],
    "maxPages": 5,
    "delayMin": 2,
    "delayMax": 5
  }
}
```

## Categories

| Value | Label |
|---|---|
| `ecommerce` | E-commerce |
| `jobs` | Jobs |
| `realestate` | Real Estate |
| `social` | Social |
| `news` | News |
| `travel` | Travel |
| `other` | Other |
