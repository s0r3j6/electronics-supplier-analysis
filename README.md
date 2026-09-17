# Electronics Supplier Analysis

## Project Overview

This project analyzes electronics import transactions to identify active suppliers, understand sourcing patterns and support supplier-shortlisting decisions.

The original dataset contained **770,137 import records**. Python and Power Query were used to clean, classify and prepare the data before developing an interactive four-page Power BI dashboard.

> The original business dataset is not included because it contains commercially sensitive supplier, importer and pricing information.

## Business Objectives

- Identify active electronics-component suppliers
- Compare suppliers by transaction activity and importer reach
- Understand sourcing countries and product coverage
- Search for exact products and manufacturer part numbers
- Create a data-driven shortlist of potential suppliers
- Monitor electronics import trends

## Data Preparation

The following data-cleaning activities were performed:

- Removed records with missing supplier names
- Classified products into five component categories
- Excluded overlapping product classifications
- Removed **12,833 duplicate records**
- Standardized supplier and product text
- Prepared date and numerical fields for analysis
- Produced **183,137 analysis-ready transactions**

### Product Categories

| Category | Transactions |
|---|---:|
| Resistor | 59,166 |
| Capacitor | 48,905 |
| Integrated Circuit (IC) | 39,056 |
| Diode | 19,368 |
| Inductor | 16,642 |
| **Total** | **183,137** |

## Dashboard Pages

### 1. Supplier Analysis

Provides an overview of supplier activity and electronics-import patterns.

Key features:

- Supplier, country and product-category slicers
- KPI cards for suppliers, importers, countries and transactions
- Top-supplier comparison
- Origin-country analysis
- Import trend analysis
- Interactive filtering across visuals

### 2. Product Search

Allows users to locate specific electronic components using product descriptions or manufacturer part numbers (MPNs).

Key features:

- Exact product and MPN search
- Keyword-based product filtering
- Supplier identification for the selected product
- Country and category filters
- Quick comparison of available sourcing options

### 3. Supplier Evaluation

Evaluates and ranks suppliers using transaction activity, importer reach and product coverage.

Only suppliers with at least **10 transactions** were considered eligible. From **3,097 suppliers**, **1,036 suppliers** met this threshold.

The supplier score uses the following weighted criteria:

| Criterion | Weight |
|---|---:|
| Unique importer reach | 35% |
| Transaction activity | 30% |
| Product coverage | 25% |
| Category coverage | 10% |

The ranking represents a **data-driven candidate shortlist** based on the available transaction activity. It should not be interpreted as proof of supplier trustworthiness or product quality.

### 4. Product Details

Provides transaction-level details for products selected through the dashboard filters.

Key features:

- Complete product descriptions
- Supplier and importer information
- Origin country
- Product category and HS code
- Import date
- Unit value and invoice currency
- Detailed transaction-level comparison

## Key Results

- Processed **770,137** original import records
- Created **183,137** analysis-ready transactions
- Removed **12,833** duplicate records
- Analyzed five electronics-component categories
- Evaluated **3,097** suppliers
- Ranked **1,036** eligible supplier candidates
- Developed an interactive three-page Power BI dashboard
- Implemented exact product and MPN search functionality

## Tools and Technologies

- Python
- Pandas
- NumPy
- Power Query
- Power BI
- DAX
- Excel
- GitHub

## Repository Structure

```text
electronics-supplier-analysis/
├── README.md
├── data/
├── python/
├── dax/
├── dashboard/
└── images/
