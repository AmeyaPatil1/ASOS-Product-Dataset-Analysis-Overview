ASOS Product Dataset Analysis
Overview

This project explores product-level data from ASOS to uncover brand performance, pricing patterns, stock availability issues, and potential lost revenue due to stockouts.

The analysis focuses on cleaning raw product data, extracting brand information from text descriptions, and generating strategic insights at the brand level.

Dataset

The dataset (products_asos.csv) contains product-level information, including:

Product name

Description

Price

Size availability

Stock status

The data required preprocessing to standardize pricing, extract brands, and quantify stock availability issues.

Objectives

The key goals of this analysis were:

Clean and prepare the dataset for analysis

Extract brand names from unstructured product descriptions

Identify and quantify stockout patterns

Estimate potential lost revenue due to unavailable sizes

Generate brand-level strategic insights

Methodology
1. Data Cleaning

Converted price column to numeric format

Removed rows with invalid or missing prices

Standardized the description column for text processing

2. Brand Extraction

Parsed product descriptions to extract brand names (using text patterns such as "by BrandName")

Applied a mapping dictionary to correct inconsistent brand labels

Filtered out brands with very low product counts to focus on meaningful analysis

3. Stockout & Lost Revenue Analysis

A custom function was built to:

Parse size availability strings

Count total available sizes

Identify out-of-stock sizes

Calculate:

stockout_count

stockout_rate

lost_revenue (estimated phantom revenue due to unavailable sizes)

4. Brand-Level Aggregation

Grouped cleaned data by brand and calculated:

Average price

Total stockout count

Average stockout rate

Total estimated lost revenue

Product count

This provides a structured view of performance and operational gaps by brand.

Key Metrics

Stockout Count – Total number of unavailable size instances

Stockout Rate – Proportion of sizes unavailable per product

Lost Revenue – Estimated revenue impact due to out-of-stock sizes

Average Price – Mean price per brand

Product Volume – Number of products per brand

Strategic Insight Focus

The final output aggregates brand-level metrics to support:

Inventory optimization decisions

Revenue recovery opportunities

Pricing comparisons across brands

Identification of high-risk stockout brands

Tech Stack

Python

Pandas

NumPy

Seaborn

Matplotlib

How to Run

Clone the repository

Place products_asos.csv in the project directory

Open ASOS_Dataset_Analysis.ipynb

Run all cells in sequence
