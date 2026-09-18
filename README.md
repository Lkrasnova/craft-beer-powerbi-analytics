# 🍺 Craft & Co. — Brewery Supply Chain & Sales Analytics (Power BI)

## 📌 Project Overview
**Craft & Co.** is an end-to-end Power BI analytics project designed to evaluate sales performance, supply chain efficiency, and quality control across a network of 5 craft breweries and 30 partner venues in Germany.

The primary goal of this business intelligence solution is to monitor cold-chain logistics integrity, quantify financial losses resulting from product spoilage during transport, and track production output across brewing facilities.

---

## 🛠️ Tech Stack & Methodology
* **Data Engineering & Generation:** Python (`pandas`, `numpy`) — developed custom scripts to generate synthetic, relational B2B IoT & sales datasets.
* **Data Modeling:** Power BI Desktop — implemented a clean **Star Schema** with explicit dimensions (`dim_beers`, `dim_bars`, `dim_breweries`, `dim_date`) and fact tables (`fact_sales`, `fact_batches`).
* **ETL & Data Transformation:** Power Query — data type standardization, relationship handling, and parameterization.
* **DAX & Business Logic:** Custom DAX measures leveraging Time Intelligence, aggregation, dynamic loss calculations, and conditional metrics.
* **UI/UX Design:** Multi-page layout, custom color palettes, KPI cards, area trend charts, conditionally formatted matrices, and interactive page navigation.

---

## 📊 Dashboard Architecture

1. **Executive Overview**
   * High-level business performance metrics: Total Revenue, Gross Profit, Profit Margins, and Total Volume Delivered.
   * Revenue trends over time and product portfolio analysis highlighting top-performing beer styles.
   * Geographic revenue breakdown across partner locations and cities.

2. **Cold Chain & Quality Control**
   * Cold-chain integrity monitoring: Tracking transport temperature breaches (>8°C).
   * Spoilage quantification: Identifying volume loss, spoilage rate (%), and direct financial loss (€).
   * Correlation analysis between logistics temperature fluctuations and revenue leakage.
   * Venue-level audit matrix with conditional formatting to pinpoint high-risk delivery locations.

3. **Production & Inventory**
   * Brewery output analysis: Total brewed volume (L), total batch counts, and average batch sizes.
   * Production capacity distribution across brewing facilities.
   * Beer style volume shares and monthly production trends.

---

## 💡 Key Business Insights

* **Logistics & Quality Linkage:** Analysis reveals a direct correlation between transport temperature spikes above 8°C and increased spoilage rates, leading to quantifiable financial loss during delivery.
* **Geographic Spoilage Concentration:** Spoilage and delivery risk are concentrated in specific regional transport corridors, indicating the need for vendor contract reviews or improved cold-chain refrigeration units.
* **Seasonal Demand Shifts:** Production batches peak during summer months, requiring optimized inventory turnover to account for shorter shelf-life styles (e.g., Sour and Wheat beers).

---

## 📁 Repository Structure
```text
├── data/                  # Synthetic CSV datasets
├── screenshots/           # High-resolution dashboard previews
├── generate_data.py       # Python script for dataset generation
├── Craft_Co_Analytics.pbix # Main Power BI report file
└── README.md              # Project documentation
