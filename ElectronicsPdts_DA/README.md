# Products Dataset
A large-scale e-commerce product catalog containing 10,000+ product records.
---

## 📋 Project Overview
**Products dataset** is a comprehensive synthetic dataset designed for data analysis, e-commerce prototyping, machine learning practice, and dashboard development.

### Key Highlights
- **10,000 rows** × **13 columns**
- No missing values
- Perfect for testing, learning, and portfolio projects
- Mix of numerical, categorical, and text data

---

## 🗂 Dataset Structure
| Column            | Type     | Description                          | Unique Values | Notes |
|-------------------|----------|--------------------------------------|---------------|-------|
| **Index**         | int      | Sequential row ID                    | 10,000        | 1 to 10,000 |
| **Name**          | string   | Product name                         | 7,896         | Many "Smart", "Wireless", "Pro", "Eco" terms |
| **Description**   | string   | Short random product description     | 10,000        | Unique |
| **Brand**         | string   | Brand/Manufacturer                   | 9,241         | Mostly unique |
| **Category**      | string   | Product category                     | 34            | See full list below |
| **Price**         | int      | Price in USD                         | 999           | Range: 1 – 999 |
| **Currency**      | string   | Currency code                        | 1             | Always `USD` |
| **Stock**         | int      | Current inventory quantity           | 999           | Range: 1 – 999 |
| **EAN**           | int      | 13-digit European Article Number     | 10,000        | Unique barcode |
| **Color**         | string   | Product color                        | 140           | Wide variety |
| **Size**          | string   | Size/dimensions                      | 18            | Clothing sizes + measurements |
| **Availability**  | string   | Stock status                         | 6             | Balanced distribution |
| **Internal ID**   | int      | Internal system reference            | 99            | Heavily reused |

---

## 📊 Key Insights & Statistics

### Numerical Columns
- **Price**: Mean ≈ **503 USD**, uniformly distributed (1–999)
- **Stock**: Mean ≈ **499 units**, uniformly distributed (1–999)
- No meaningful correlation between Price and Stock

### Availability Status (Perfectly Balanced)
- `discontinued`: 1,706
- `out_of_stock`: 1,700
- `pre_order`: 1,673
- `limited_stock`: 1,644
- `in_stock`: 1,644
- `backorder`: 1,633

### Top Categories
| Category                  | Count |
|---------------------------|-------|
| Clothing & Apparel        | 320   |
| Kitchen Appliances        | 319   |
| Home & Kitchen            | 316   |
| Team Sports               | 316   |
| Grooming Tools            | 311   |
| Headphones & Earbuds      | 311   |

### Size Formats
Mix of clothing sizes (`S, M, L, XL, XXL, XS`) and dimensions (`5x7 in`, `10x10 cm`, `50x70 cm`, `100x200 mm`, etc.)

---

## ✨ Features
- **Realistic e-commerce fields** (price, stock, availability, EAN, color, size)
- **Diverse categories** beyond just electronics

- Excellent for:
  - Exploratory Data Analysis (EDA)
  - Data visualization dashboards
  - Predictive modeling (stock prediction, price classification, availability forecasting)
  - Database design testing
  - E-commerce app prototyping

---

## 🚀 Getting Started

### Prerequisites
- Python 3.8+
- pandas, numpy, matplotlib/seaborn, plotly (optional)

### Quick Load
```python
import pandas as pd

df = pd.read_csv('Products.csv')
df.head()
