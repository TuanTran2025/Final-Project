# 💳 Customers’ behavior on credit cards

<img width="2240" height="1260" alt="image" src="https://github.com/user-attachments/assets/965c5dab-9bc6-42a3-918e-5c9a33b1209b" />

## 1. Introduction

The credit card industry plays a crucial role in shaping consumer financial behavior, offering convenience, access to credit, and a wide range of spending opportunities. However, understanding **how different customer groups use credit cards** is essential for financial institutions aiming to maximize profitability while minimizing risk.

This project, **“Customers’ Behavior on Credit Cards,”** focuses on analyzing customer spending patterns, demographic influences, and credit card usage characteristics. By examining purchase behaviors, value accumulation, and group-level contributions, the study seeks to uncover which customer segments provide the **highest long-term value (LTV)** and how these insights can inform **retention strategies, targeted marketing campaigns, and product optimization**.

Through this analysis, we aim to:

* Identify high-value customer segments that significantly impact profitability.
* Explore common behavioral and demographic patterns that drive card usage.
* Provide actionable recommendations to prioritize customer groups for marketing and retention.

Ultimately, this project bridges the gap between raw transaction data and strategic decision-making, helping financial institutions create **data-driven, customer-centric strategies** for growth and sustainability.

## 2. Dataset Description

This comprehensive dataset combines transaction records, customer information, and card data from a banking institution, spanning across the 2010s decade.

### 2.1. Data Source
- The original source is coming from Kaggle (the link https://www.kaggle.com/datasets/computingvictor/transactions-fraud-datasets/data)
- Alternative link can be retrieved from https://drive.google.com/drive/folders/1eglwYm7bw-4Ebh73shGaIJssfGxqkxlq?usp=sharing

### 2.2. Data Structure
#### 2.2.1. Transaction Data
- transactions_data.csv includes 12 columns and 1,048,575 rows 
- Detailed transaction records including amounts, timestamps, and merchant details
- Covers transactions throughout the 2010s
- Features transaction types, amounts, and merchant information
<img width="534" height="201" alt="image" src="https://github.com/user-attachments/assets/c519b021-c8fe-41bb-ad05-52b86f33fcb8" />

#### 2.2.2. User Data 
- users_data includes 13 columns and 6,146 rows
- Demographic information about customers
- Account-related details
<img width="532" height="137" alt="image" src="https://github.com/user-attachments/assets/1a0cf208-5c89-4396-a7cf-2ef83677a656" />

#### 2.2.3. Card Information
- cards_data.csv includes 14 columns and 2,000 rows
- Credit and debit card details
- Includes card limits, types, and activation dates
- Links to customer accounts via card_id
<img width="533" height="127" alt="image" src="https://github.com/user-attachments/assets/d45ef661-9077-43a6-8a93-1d425bbee601" />

#### 2.2.4. Merchant Category Codes 
- mcc_codes.json includes 2 columns and 109 rows 
- Standard classification codes for business types
<img width="491" height="303" alt="image" src="https://github.com/user-attachments/assets/84ee9114-b93a-474a-8406-086c96404309" />

### 2.3. Data Model
The data model consists of:
- 4 tables which contains the card information and related transactions
- 1 calendar table
- 1 table of Gross Margin (which is based on a reseach online from the link: https://pages.stern.nyu.edu/~adamodar/New_Home_Page/datafile/margin.html)
<img width="958" height="727" alt="image" src="https://github.com/user-attachments/assets/17f4cfdc-9980-430f-9deb-092c001b788d" />

## 3. Main Goals
### 3.1. Purpose:
- Identify customer groups that bring the highest value from credit card usage in order to persude the retention strategies and optimizing profits.

### 3.2. Key Analytical Questions:
-	What do the customer purchase behavior/value accumulation patterns have in common?
-	Which customer groups should be prioritized for marketing and retention?
-	Is there a relationship between demographic characteristics and spending behavior?

## 4. Methodology
### 4.1. Data Cleaning
-	Process the amount columns containing $ characters, negative data → convert and filter.
-	Check and normalize data types (int, datetime, str, etc.)
-	Remove records missing important information (if neccessary such as NaN, duplicate, refund transactions, etc.)

### 4.2. Exploratory Data Analysis (EDA):
-	Analyze spending distribution by age group, gender, income.
-	Analyze behavior by mcc (industry), card_type, credit_limit.
-	Statistics on transaction frequency, sales by week/month/year.

### 4.3. Analysis & Modeling 
-	Cluster customers by K-Means Clustering.
-	Analyze correlation between credit_score, income, debt, spending.

### 4.4. Visualization & Storytelling 
-	Interactive Dashboard using Power BI
    * Customer distribution map by region.
    * Bar chart analyzing behavior by MCC.
    * Timeline of spending by segment.

## 5. Results
### 5.1. Spending by Cards
#### 📊 Transactions Frequency
<img width="1031" height="451" alt="image" src="https://github.com/user-attachments/assets/18d6e44a-3b49-4952-a6d2-629507237a87" />

#### 💳 Spending by Brand & Type
<img width="1532" height="948" alt="image" src="https://github.com/user-attachments/assets/800e81ef-3162-420b-98d6-13ad735ad342" />

####
| **📊 Key Insights**                                                                                                            | **💡 Recommendations**                                                                                                             |
| ------------------------------------------------------------------------------------------------------------------------------ | ---------------------------------------------------------------------------------------------------------------------------------- |
| 📈 **Transactions Growth**: Steady increase from \~82K/month (2010) → \~103–105K/month (2019), with predictable seasonal dips. | 🎯 Use seasonal slowdowns for targeted promotions & smarter budget planning.                                                       |
| 💳 **Brand Spending**: Mastercard dominates (Debit \$1.6M–1.8M, Credit \$500K–600K). Visa follows. Amex & Discover = niche.    | ✅ Mastercard & Visa: maintain dominance, cross-sell services. ⚡ Amex & Discover: strengthen positioning with rewards & incentives. |
| 🔄 **Card Type Trends**: Debit dominates Mastercard & Visa; Credit dominates Amex & Discover; Prepaid minimal.                 | 📌 Upsell debit users into credit (Mastercard/Visa). 🚀 Grow prepaid adoption for unbanked/young customers.                        |
| 🔔 **Stability & Seasonality**: Mastercard & Visa stable; Amex & Discover volatile with sharp spikes/drops.                    | ⚠️ Amex & Discover: run incentive campaigns in low months to reduce volatility.                                                    |
| 🌍 **Market Positioning**: Mastercard & Visa = broad dominance; Amex & Discover = premium/niche.                               | 🏆 Tailor campaigns: broad market upsell for Mastercard/Visa, premium-targeted rewards for Amex/Discover.                          |

### 5.2. Spending by MCC

<img width="996" height="590" alt="image" src="https://github.com/user-attachments/assets/4b3be0ee-f675-48b6-aa64-64cd99d3ff68" />

 
