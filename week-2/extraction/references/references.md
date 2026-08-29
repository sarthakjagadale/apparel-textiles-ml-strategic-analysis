# Week 2 References

This file contains the public sources used for the Yuva Intern Week 2
task: Data Collection Strategy & Data Quality Assessment.

The sources were selected based on relevance to the Apparel & Textiles
industry, Machine Learning applications, data availability and
reliability.

---

## 1. Open Government Data Platform India

### Source

Government of India – Open Government Data Platform

### Website

https://www.data.gov.in/

### Used For

- Textile export data
- Apparel export data
- Country-wise export analysis
- State/UT-wise export analysis
- Category-wise export analysis

### Relevance

The platform provides official Indian government datasets that can be
used for market analysis, trade analysis and future forecasting.

---

## 2. India OGD – Country-wise Textile & Apparel Exports

### Dataset

Country-wise Export of India of Textiles and Apparel Including
Handicrafts, 2019–20 to 2023–24

### Source

https://www.data.gov.in/resource/country-wise-export-india-textiles-and-apparel-including-handicrafts-2019-20-2023-24

### Potential Applications

- Export analysis
- Market analysis
- Time-series forecasting
- Country comparison

---

## 3. India OGD – State/UT-wise Textile & Apparel Exports

### Dataset

State/UT-wise Details of Export of Textile and Apparel Including
Handicrafts

### Source

https://www.data.gov.in/resource/stateut-wise-details-export-textile-and-apparel-including-handicrafts-2022-23-2023-24

### Potential Applications

- Regional analysis
- State-level market analysis
- Export forecasting

---

## 4. India OGD – Textile Product Exports

### Dataset

Exports of Textile Products

### Source

https://www.data.gov.in/catalog/exports-textile-products

### Potential Applications

- Product-category analysis
- Export analysis
- Textile market research

---

## 5. Ministry of Textiles – Government of India

### Organization

Ministry of Textiles, Government of India

### Website

https://texmin.nic.in/

### Used For

- Industry statistics
- Textile sector information
- Apparel industry information
- Export information
- Government policies
- Annual reports

### Potential Applications

- Market analysis
- Industry research
- Forecasting features
- Validation of secondary research

---

## 6. Ministry of Textiles – Annual Report 2024–25

### Source

https://texmin.nic.in/sites/default/files/MOT%202024-25%20English%20Report%2012.03.2025.pdf

### Used For

- Textile industry context
- Export information
- Industry statistics
- Sector-level analysis

### Data Extraction Method

PDF/table extraction can be used, followed by manual validation against
the original report.

---

## 7. MoSPI / eSankhyiki

### Organization

Ministry of Statistics and Programme Implementation

### Source

https://esankhyiki.mospi.gov.in/

### Used For

- Manufacturing statistics
- Industrial indicators
- Economic statistics
- Sector-level information

### Potential Applications

- Demand forecasting
- Manufacturing analysis
- Economic forecasting

---

## 8. MoSPI Data Access Information

### Source

https://www.mospi.gov.in/faq

### Used For

Understanding data access categories and limitations.

### Importance

Before using a dataset, its access conditions should be checked to
determine whether it is openly available, requires registration or has
other restrictions.

---

## 9. U.S. Census International Trade

### Organization

U.S. Census Bureau

### Source

https://usatrade.census.gov/

### Used For

- Import data
- Export data
- International trade
- Product categories
- Country comparisons

### Potential Applications

- International market analysis
- Trade forecasting
- Country comparison

---

## 10. Google Trends

### Source

https://trends.google.com/

### Used For

- Fashion search interest
- Consumer interest
- Product trends
- Regional search interest
- Seasonal trend analysis

### Potential Applications

- Trend forecasting
- Demand prediction
- Consumer behavior analysis

### Important Limitation

Google Trends represents search interest and should not be interpreted
as direct sales or revenue data.

---

## 11. Google Trends Dataset Documentation

### Source

https://support.google.com/trends/answer/12764470

### Used For

Understanding the availability and characteristics of public Google
Trends datasets.

---

## 12. Google Trends Data FAQ

### Source

https://support.google.com/trends/answer/4365533

### Used For

Understanding:

- Sampling
- Aggregation
- Normalization
- Search-interest interpretation

---

## 13. Fashion-MNIST

### Organization

Zalando Research

### Source

https://www.kaggle.com/zalando-research/fashionmnist

### Dataset

Fashion-MNIST

### Characteristics

- 70,000 images
- 28 × 28 pixel images
- 10 fashion categories

### Potential Applications

- Computer Vision
- Image classification
- Apparel classification
- Deep Learning experiments

### Limitation

Fashion-MNIST is primarily a benchmark dataset and should not be
considered a representative dataset of the current fashion retail
market.

---

## 14. Hugging Face Fashion Dataset

### Source

https://huggingface.co/datasets/nreimers/fashion-dataset

### Potential Data

- Gender
- Product category
- Subcategory
- Article type
- Color
- Season
- Year
- Usage
- Product name

### Potential Applications

- Product classification
- Product analytics
- Recommendation research
- Feature engineering

### Limitation

The dataset should be evaluated for provenance, licensing, coverage and
representativeness before being used in a production system.

---

# Source Classification

| Source | Type | Main Purpose |
|---|---|---|
| India OGD | Government | Trade and market data |
| Ministry of Textiles | Government | Industry information |
| MoSPI | Government | Manufacturing/economic data |
| U.S. Census | Government | International trade |
| Google Trends | Search data | Consumer interest/trends |
| Fashion-MNIST | ML dataset | Computer Vision |
| Hugging Face Fashion Dataset | ML dataset | Product analytics |

---

# Preferred Source Hierarchy

The preferred order for data collection is:

```text
Official Government API
        ↓
Official CSV / JSON
        ↓
Official Structured Dataset
        ↓
Official PDF Report
        ↓
Permitted Web Extraction
        ↓
Survey Data
