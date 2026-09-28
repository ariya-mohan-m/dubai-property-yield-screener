# Dubai Property Yield Screener

> **Status:** In progress

**Business question:** An investor has AED 1.5M. Which Dubai area and unit type gives the best rental yield, with enough market liquidity to sell later?

**What this project delivers:** A Power BI screener built on official Dubai Land Department data. Enter a budget and get a ranked shortlist of areas by gross rental yield, price momentum and liquidity, with a warning where prices are rising faster than rents.

## Key findings
_To be added once the analysis is complete._

## Approach
1. **Data:** DLD sales transactions (36 months) and Ejari rent contracts (24 months)
2. **Cleaning (Python):** ready residential sales only, new rent contracts only, area-name matching between datasets, outliers removed within each segment
3. **Modelling (SQL Server):** star schema, median-based yield by area × type × bedrooms, minimum sample thresholds
4. **Screener (Power BI):** budget what-if, yield ranking, price-vs-rent momentum, liquidity score

## Repository structure
| Folder | Contents |
|---|---|
| `data/sample` | 1,000-row samples of the source data (full files not committed) |
| `sql` | Table definitions and analysis views |
| `python` | Cleaning and matching notebooks |
| `powerbi` | The .pbix report |
| `images` | Dashboard screenshots |
| `docs` | Business brief and insight memo |

## Data source
[Dubai Land Department – Open Data](https://dubailand.gov.ae/en/open-data/real-estate-data/)

## Tools
SQL Server · Python (pandas, rapidfuzz) · Power BI

---
**Author:** Ariya Mohan M · [LinkedIn](https://www.linkedin.com/in/ariya-mohan-m/)
