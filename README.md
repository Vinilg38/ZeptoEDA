# Zepto Product Pricing and Inventory Analysis

This repository contains SQL scripts for exploratory data analysis (EDA) of Zepto product pricing and inventory data. The analysis aims to uncover insights related to product categories, discounts, stock levels, and revenue.

## Table of Contents

- [Project Overview](#project-overview)
- [Data Source](#data-source)
- [Database Schema (DDL)](#database-schema-ddl)

## Project Overview

This project focuses on analyzing Zepto's product data to gain insights into various aspects of their operations. The SQL scripts perform data cleaning, transformations, and run analytical queries to answer questions such as:
- Top discounted products.
- High-value out-of-stock items.
- Revenue breakdown by category.
- Average discount rates per category.
- Product weight categorization.
- Inventory weight by category.

## Data Source

The dataset used for this analysis is sourced from Kaggle:

**Zepto Product Pricing Insights**
- **Link:** [https://www.kaggle.com/code/palvinder2006/zepto-product-pricing-insights](https://www.kaggle.com/code/palvinder2006/zepto-product-pricing-insights)
- This dataset contains information on various products, including their names, pricing, discounts, stock availability, and weight.

## Database Schema (DDL)

The data is loaded into a PostgreSQL database. Below is the Data Definition Language (DDL) for the `zepto` table:

```sql
CREATE TABLE zepto (
  sku_id SERIAL PRIMARY KEY,
  category VARCHAR(120),
  name VARCHAR(150) NOT NULL,
  mrp NUMERIC(8,2),
  discountPercent NUMERIC(5,2),
  availableQuantity INTEGER,
  discountedSellingPrice NUMERIC(8,2),
  weightInGms INTEGER,
  outOfStock BOOLEAN,
  quantity INTEGER
);
