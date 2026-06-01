# Task-1-Waliyullahi-Akorede-Husain
Repository for Task 1

# Decodelabs Internship Diary: Project 1 – Data Cleaning & Profiling

Before we can build stunning, high-impact dashboards, we have to address the overlooked but absolutely critical first step: **Data Cleaning**. 

As part of my Data Analyst internship at Decodelabs, I was tasked with cleaning a sales dataset. This repository documents my data profiling notes and the structural cleaning steps implemented using **Excel** and **Power Query**.

---

## Tech Stack & Tools
* **Excel** (Initial Data Profiling & Quality Checks)
* **Power Query** (ETL: Extraction, Transformation, and Loading)

---

## Dataset Overview & Data Profiling
The dataset captures business transactions running from **January 1, 2023, to June 30, 2025**. 
* **Dimensions:** 14 columns and 1,200 rows.
* **Integrity Checks:** 
  * Confirmed **zero missing values** across core operational columns: `OrderID`, `Date`, `CustomerID`, `Product`, `Quantity`, `UnitPrice`, `Payment Method`, and `OrderStatus`.
  * Verified that `OrderID` and `TrackingNo` contain **zero duplicates**, ensuring every single transaction record is unique.

---

## Key Data Cleaning and profiling Steps

### 1. Date Transformation 

The `Date` column was originally formatted as raw numbers. I converted and standardized this into a clean date format to enable accurate time-series analysis.

### 3. Currency Standardization 

Both `UnitPrice` and `TotalPrice` were stored as basic decimal numbers. These were formatted into standard currency ($) to align with business reporting.

### 4. Data Profiling 

During profiling, I identified recurring `CustomerID` values. In a transactional dataset, this isn't a data entry error, it’s excellent news! It indicates customer retention and repeat purchases, which will be a key metric for future dashboarding.

### 5. Context-Driven Imputation for Missing Data

* Out of 1,200 rows, the `CouponCode` column contained **309 null values**. Instead of dropping these rows and losing ~25% of our operational data, I applied context-driven imputation. A missing coupon code simply means no coupon was applied. I replaced these nulls with the string `"NO COUPON"` to preserve data integrity and make the column ready for categorical analysis.

---


Data cleaning isn't just about fixing errors. It’s about understanding the story behind the rows and columns before you ever write a line of DAX or build a visual.


