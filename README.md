Data Cleaning and Transformation Project: E-Commerce Sales Dataset

Project Overview

This project focuses on the essential data preparation phase of the analytics lifecycle. The goal was to take a raw, uncleaned e-commerce dataset and perform a comprehensive data transformation to produce a structured, high-quality dataset ready for analysis and reporting.

The primary objective was to correct structural errors, standardize formats, and create calculated metrics to enhance the dataset's usability and analytical value. This process simulates a real-world scenario where raw business data is seldom ready for immediate analysis.

Dataset Details

· Source: Raw data appeared as a single, unstructured table with formatting issues and unclear column headers.
· Target: A clean, normalized dataset split into two logical tables for better organization.
· Key Entities: Orders, Customers, Products.
· Scope: This project involves a sample of 12 transaction records.

Data Transformation Methodology

The project followed a systematic data cleaning and transformation process:

1. Structural & Formatting Corrections

· Column Headers: Renamed and clarified ambiguous column headers.
  · ShippingAddress → Shipping Address
  · PaymentMethod → Payment Method
  · TrackingNum → Tracking Number
  · ItemsInCar → Items In Cart
  · CouponCode → Coupon Code
  · Referrals → Referral Source
· Case Standardization: Standardized text in columns like Shipping Address, Product, and Payment Method (e.g., correcting "Main" to "Main St").
· Data Type Alignment: Ensured columns contained appropriate data types (e.g., numeric values for Unit Price and Quantity).

2. Data Splitting and Normalization

The original single table was separated into two logical tables for better data management and analysis:

· Table 1 (Core Order Info):
  · Order ID (Extracted from the original combined OrderID)
  · Date (Extracted from the original combined OrderID)
  · Customer ID
  · Product
  · Quantity
  · Unit Price
  · Shipping Address
  · Payment Method
  · Order Status
  · Tracking Number
· Table 2 (Order Details & Marketing):
  · Unit Price (Key to join with Table 1)
  · Shipping Address
  · Payment Method
  · Order Status
  · Tracking Number
  · Items In Cart
  · Coupon Code
  · Referral Source
  · Total Price

3. Feature Engineering

· Total Price Calculation: The Total Price column was calculated by multiplying Quantity and Unit Price (TotalPrice = Quantity * UnitPrice), providing a key metric for analysis.
· Handling Missing/Null Values: The raw data had missing values for Coupon Code, which were logically replaced with "N/A" in the cleaned dataset to avoid null-value errors.

Key Results

· Clean Dataset: Transformed a messy, unstructured table into a well-organized, analysis-ready dataset.
· Data Integrity: Ensured consistency in formatting, data types, and text entries.
· Enhanced Usability: Created a dataset suitable for immediate use in Business Intelligence tools (like Power BI, Tableau) or statistical analysis, allowing for insights into:
  · Order Status: Distribution (e.g., Shipped, Returned, Cancelled).
  · Revenue: Total and average Total Price per order.
  · Customer Trends: Prevalent payment methods (Credit Card, Online).
  · Product Performance: Total Quantity sold per product.
  · Marketing Channel Effectiveness: Influence of Referral Source on orders.

Tools Used

· Excel / Google Sheets: Used for all data cleaning, transformation, and calculation steps.

How to Use

1. Clone this repository.
2. Open the Dataset_Original.csv to view the raw, messy data.
3. Open Dataset_Cleaned.csv to review the final, transformed dataset.
4. Review the provided documentation to understand the transformation logic.

Future Steps

· Data Enrichment: Merge with external datasets (e.g., product categories, shipping costs) for more comprehensive analysis.
· Dashboard Creation: Build an interactive dashboard in Power BI or Tableau to visualize the key performance indicators (KPIs) derived from this data.
· Data Validation: Implement more robust validation rules to automatically detect anomalies during data ingestion.

Contributor: Tosin Sileola Akin-Oyewole 

📱 Built on Mobile

This entire project was completed using only my smartphone! 🎯

· Tools: Google Sheets / Excel Mobile
· Challenges: Small screen navigation, precise cell selection, formula input
· Takeaway: Data analytics doesn't require expensive hardware—just determination, patience, and a willingness to learn.
