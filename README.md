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
- The original source is coming from the Kaggle link https://www.kaggle.com/datasets/computingvictor/transactions-fraud-datasets/data
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

####
 | **📊 Key Insights**                                                                                      | **💡 Recommendations**                                                                                |
| -------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------- |
| 🛒 **High Spending Sectors**: Grocery (3.54M), Wholesale Clubs (3.20M), Pharmacies (3.02M).              | 🤝 Build **partnerships & loyalty programs** with grocery, wholesale, and pharmacy chains.            |
| 🍽️ **Lifestyle & Daily Needs**: Service Stations (2.53M), Utilities (2.40M), Restaurants (2.26M).       | 🎯 Run **targeted offers** in dining & bundle deals with fuel/utilities for recurring demand.         |
| 🏬 **Moderate Categories**: Dept. Stores (2.32M), Tolls (2.21M), Auto Shops (2.18M), Telecom (2.14M).    | 📌 Provide **cross-sector promotions** (e.g., retail + telecom bundles, commuting rewards).           |
| 🎲 **Niche but Noticeable**: Betting (0.44M), Drinking (0.55M), Beauty (0.42M), Travel Agencies (0.38M). | 🚀 Expand **engagement campaigns** in lifestyle & travel, target smaller but loyal segments.          |
| 💳 **Digital Payment Gap**: Low card usage in betting, beauty, and local transport.                      | 📲 Promote **digital payment adoption** with rewards & easy-pay features in under-penetrated sectors. |

### 5.3. Spending by Age
<img width="1790" height="590" alt="image" src="https://github.com/user-attachments/assets/39331102-54c9-4548-a67f-61ab86e65583" />

####
| **📊 Key Insights**                                                                    | **💡 Recommendations**                                                                                                          |
| -------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------- |
| 🧑‍💼 **36–50 group** – Highest spenders (187M), but annual spend dropped (19M → 16M). | 🔑 Retention focus: personalized offers, premium upselling, cross-sell groceries/utilities, promote convenience & delivery.     |
| 👨‍🦳 **51–65 group** – Strong spenders (170M) but declining (18M → 15M).              | 💡 Push **health & wellness**, loyalty/cashback, multi-channel (branch + digital), emphasize trust & reliability.               |
| 👵 **65+ group** – Still significant (119M) but shrinking (12M → 10M).                 | 🎯 Senior-focused discounts, assistive tech, financial security tools, community programs, free delivery bundles.               |
| 👩‍💻 **25–35 group** – Small but stable (6–7M yearly, 61M total).                     | 🚀 Growth play: installment financing, digital-first services, career-focused/lifestyle products, travel & experience bundles.  |
| 🎓 **<25 group** – Minimal (2M total, negligible yearly).                              | 🌱 Entry-level engagement: student/youth discounts, trendy affordable products, gamified rewards, heavy social media campaigns. |
| 📉 **Trend** – All groups declined in 2019 (possible economic caution).                | 📌 Prepare **seasonal campaigns** & diversify offers to re-stimulate middle-aged and senior spending.                           |

### 5.4. Spending by Gender
<img width="1355" height="590" alt="image" src="https://github.com/user-attachments/assets/c356c01e-a5d4-47e4-a219-ae0051d61732" />

####
| **📊 Key Insights**                                                                                                                | **💡 Recommendations**                                                                                              |
| ---------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------- |
| 👩 **Female Customers** – Slightly higher spending share (278.87M, 51.6%) vs. men (261.33M, 48.4%). Balanced contribution overall. | 🛍 Target groceries, department stores, personal care. Exclusive loyalty perks, seasonal sales, bundled discounts.  |
| 👨 **Male Customers** – Strong in high-value sectors like automotive, electronics, travel.                                         | 🚗 Focus on cashback for fuel, tech discounts, travel/holiday packages.                                             |
| 📉 **Both Genders** – Spending fell \~17% (2017 → 2019). Decline likely from external market factors.                              | 🔑 “Spend & earn” campaigns, tiered rewards, premium unlocks. Drive urgency with limited-time promotions.           |
| 👫 **Balanced Spending** – Small gap (\$17.5M) means both genders are equally important.                                           | 💡 Joint offers: couple’s dining, family travel, bundled household services.                                        |
| 📊 **Personalization Need** – Parallel decline suggests external, not behavioral cause.                                            | 🎯 Data-driven campaigns: segment by frequency, ticket size, categories. Deliver personalized offers via email/SMS. |
| 🗣 **Feedback Gap** – No direct gender-specific motivator insights available.                                                      | ✅ Run surveys to uncover drivers & barriers. Use insights to refine product mix and partnerships.                   |

### 5.5. Spending by Income
<img width="1389" height="590" alt="image" src="https://github.com/user-attachments/assets/3da25287-b606-4511-9195-b609c44fe818" />

####
| **📊 Key Insights**                                                                                     | **💡 Recommendations**                                                                                                          |
| ------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------- |
| 💵 **30–60K Group** – Core spender with **\$339.46M** (dominant share). Slight decline in recent years. | 🎯 Focus marketing & loyalty here. Value-driven bundles, seasonal discounts, and personalized digital campaigns to retain them. |
| 💳 **60–90K Group** – Second largest at **\$92.09M**, but declining.                                    | ✨ Push “affordable luxury” offers. Tiered memberships (early access, exclusive deals) to boost yearly spend.                    |
| 💲 **<30K Group** – Still contributes **\$65.52M** despite low income.                                  | 📱 Engage with entry-level products, micro-promos, installment plans. Use TikTok/Instagram influencers for reach.               |
| 💎 **High Income (90K–150K & 150K+)** – Very low spending (**\$43.14M combined**) vs. potential.        | 🏆 Create premium lines, VIP events, concierge outreach. Position with luxury branding to unlock untapped demand.               |
| 📉 **Declining Trend (2017–2019)** – All groups show mild but consistent decline.                       | 🔑 Launch revival campaigns (dormant customers). Time-limited promotions to create urgency. Use analytics to monitor shifts.    |

### 5.6. Spending by Credit Score
<img width="1384" height="590" alt="image" src="https://github.com/user-attachments/assets/6cfc3f99-0140-49b3-8aec-29c527f1d802" />

####
| **📊 Key Insights**                                                                                                                                         | **💡 Recommendations**                                                                                                                                                       |
| ----------------------------------------------------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| ⭐ **Good Score (22.85M)** – Largest total spenders. Core driver of activity.                                                                                | 🎯 Priority group: Premium rewards cards, co-branded offers, travel cards. Cross-sell savings, insurance, investments. Keep loyal with perks (lounge, cashback multipliers). |
| 🔹 **Very Good Score (11.55M)** – Solid but lower than “Good”.                                                                                              | ✨ Premium services (wealth mgmt, mortgages, low-interest loans). Personalized perks to shift more spending. Build trust with advisory & transparency.                        |
| 💎 **Excellent Score (3.83M)** – Conservative spenders despite high capacity.                                                                               | 🏆 Elite cards (luxury benefits, concierge). Push long-term financial products (retirement, investments). Encourage card use for recurring payments.                         |
| ⚖ **Fair Score (6.81M)** – Mid-range, credit-building opportunity.                                                                                          | 📈 Offer low-interest installment loans, tiered rewards, and credit score tracking. Incentivize upgrades from Fair → Good segment.                                           |
| 🔴 **Poor Score (1.76M total, but \$49.92 avg/user)** – Small group, highest spend per user, risky.                                                         | 🔐 Engage with **secured cards**, financial literacy, and repayment rewards. Tight risk controls but keep active since they spend heavily.                                   |
| 📉 **Overall Trend** – Good = short-term growth, Fair = medium-term potential, Poor = risk-managed growth, Very Good/Excellent = retention & profitability. | 🔑 Balanced play: (1) Double down on Good, (2) Upgrade Fair, (3) Engage Poor with risk-limits, (4) Retain Very Good/Excellent via status-driven offers.                      |

### 5.7. Spending by Number of Credit Cards
<img width="1389" height="590" alt="image" src="https://github.com/user-attachments/assets/58aad275-8320-4428-afe6-5acdf3ee1444" />

####
| **📊 Key Insights**                                                                                            | **💡 Recommendations**                                                                                                           |
| -------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------------------------- |
| ⭐ **3–4 Cards Segment (Sweet Spot)** – Peak spending (≈137M for 4 cards, 122M for 3). Core revenue driver.     | 🎯 Loyalty tiers (Platinum for 3+ cards), exclusive partnerships (airlines, retail, digital), spend dashboards to track rewards. |
| 🔹 **1–2 Cards Segment (Entry-Level)** – Strong per-user spend (\~\$49), good growth potential.                | 📈 Push 2nd card adoption via cross-sell & bundles. Student/young professional education on card benefits.                       |
| ⚠ **5–7 Cards Segment (Declining Value)** – Total & per-user spend drops (as low as \$39). Risk of inactivity. | 🔄 Reactivation promos (“use it or lose it”), consolidate into premium cards, send usage alerts and reward reminders.            |
| 💎 **8–9 Cards Segment (Niche Premium)** – Few users, but highest per-user spend (\~\$56). Likely affluent.    | 🏆 VIP clubs with concierge, luxury brand tie-ins, expanded credit lines, investment-linked benefits.                            |
| 📉 **Trend** – Spending increases with card count up to 4, then drops sharply until rebounding at 8–9.         | 🔑 Balanced play: (1) Push 1–2 → 3–4 growth, (2) Retain & upsell 3–4, (3) Revive 5–7, (4) Pamper 8–9 with VIP offers.            |

### 5.8. Spending by Credit Limit
<img width="1389" height="590" alt="image" src="https://github.com/user-attachments/assets/86c0dcd7-2b2c-46b9-98b1-012c7456917b" />

####
| **🔍 Key Insights**                                                                              | **💡 Recommendations**                                                                                                             |
| ------------------------------------------------------------------------------------------------ | ---------------------------------------------------------------------------------------------------------------------------------- |
| 💳 **High limit group** spends the most (\$156.75M) but doesn’t fully utilize credit.            | 👑 Deepen engagement with **premium perks, black cards, concierge services, wealth tie-ins, and luxury partnerships**.             |
| ⚖️ **Medium group** (\$138.6M spend, 10.9K avg. limit) is balanced and strong.                   | 🎯 Drive incremental growth with **tiered rewards (groceries/dining), cross-sell (loans/insurance), and lifestyle/travel offers**. |
| ⚠️ **Upper-Medium group** (16.9K avg. limit) spends almost same as Medium → under-utilization.   | ✈️ Re-engage with **exclusive experiences (travel, dining, lifestyle)** and **reward accelerators** (“spend more, earn more”).     |
| 🏦 **Low limit group** (3.3K avg. limit, \$107.7M spend) is highly engaged despite small limits. | 📈 Offer **controlled credit line increases**, **basic cashback**, and **credit-building education tools**.                        |
| 📉 Spending does not scale linearly with credit limits → some groups underperform.               | 🔍 Use **data-driven personalization** to tailor credit, rewards, and product offers to usage patterns.                            |
| 🚀 Significant **untapped headroom** in High & Upper-Medium groups.                              | 🎟️ Launch **VIP-only programs, investment cross-sell, and exclusive events** to unlock spending potential.                        |

### 5.9. Main Variables Correlations
<img width="625" height="528" alt="image" src="https://github.com/user-attachments/assets/3462eed4-016b-438c-a2cf-8bcc494cf53a" />

#### 🔍 Key Insides
| Variables in Pair               | Correlation | Strength   | Quick Takeaway                                  |
| ------------------------------- | ----------- | ---------- | ----------------------------------------------- |
| credit\_score vs yearly\_income | -0.03       | Negligible | Credit score is not related to yearly income    |
| credit\_score vs total\_debt    | -0.11       | Weak       | More debt slightly lowers credit score          |
| credit\_score vs amount         | -0.02       | Negligible | Spending not linked to credit score             |
| yearly\_income vs total\_debt   | 0.49        | Moderate   | Higher income is moderately linked to more debt |
| yearly\_income vs amount        | 0.14        | Weak       | Higher income → slightly more spending          |
| total\_debt vs amount           | 0.06        | Negligible | Debt level has almost no link to spending       |

#### 💡 Recommendations
- Credit score is not related to income or spending → Don’t rely on income or spending level to predict credit score. Instead, focus on repayment history and on-time payments when building credit scoring models.
- Higher debt slightly lowers credit score → Encourage customers to manage debt responsibly. Consider introducing debt restructuring products (e.g., consolidation loans) or offering incentives for on-time repayment to improve credit scores.
- Higher income is moderately linked to higher debt (0.49 correlation) → High-income customers tend to borrow more. This segment is attractive for premium credit products (e.g., Platinum cards, low-interest loan packages). However, risk management is essential as debt levels also rise.
- Higher income → slightly higher spending (weak correlation 0.14) → High-income customers may spend more, but not significantly. Focus on personalized offers and luxury services instead of assuming all high-income customers are heavy spenders.
- Debt level has almost no link to spending → Spending behavior is mostly independent of debt. Promotional programs such as cashback, loyalty points, and vouchers can be applied broadly across customer segments.

#### 👉 In summary:
- Manage risk and help debt-heavy customers improve their credit score.
- Target high-income customers with premium financial products.
- Keep running broad spending incentive programs since spending is not strongly tied to debt.

### 5.10. Customers Cluster Analysis
#### 📈 Clusters by Ebowl Method
<img width="567" height="455" alt="image" src="https://github.com/user-attachments/assets/398c08b4-13f2-4c2f-ab18-6eb5962b0c68" />

#### 📊 K-mean Segmentations (n_clusters = 3)
<img width="989" height="690" alt="image" src="https://github.com/user-attachments/assets/d6018306-f23e-493a-b086-626ffc0e63a8" />

#### 🎯 Cluster results
|       Cluster | Avg Credit Score | Avg Yearly Income | Description                        |
| ------------: | ---------------: | ----------------: | ---------------------------------- |
| **Cluster 0** |              746 |          \$38,883 | 🟣 **Creditworthy but Low Income** |
| **Cluster 1** |              724 |          \$80,894 | 🟢 **High-Income, Good Credit**    |
| **Cluster 2** |              641 |          \$42,993 | 🟡 **Low Credit, Moderate Income** |

#### 💡 Recommendations
| **Cluster**                              | **Profile**                              | **Key Characteristics**                                                                                                                                         | **Recommendations**                                                                                                                                                                                                                                   |
| ---------------------------------------- | ---------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| 🟣 **Cluster 0 — "Stable Low-Income"**   | Low-income but disciplined credit users  | 🔹 High average credit score (746)<br>🔹 Conservative spenders, long-term customers<br>🔹 Likely prefer low-limit cards or installment payments                 | ✅ Offer small credit limit increases to encourage loyalty<br>✅ Provide installment-based products and essential rewards (groceries, utilities)<br>✅ Launch “financial stability” perks (e.g., fee waivers, cashback on essentials)                    |
| 🟢 **Cluster 1 — "Prime Customers"**     | High-income, strong credit history       | 🔹 Avg. income \~\$81K<br>🔹 Professionals/high-earners using premium cards<br>🔹 Likely frequent travelers or business users<br>🔹 High-value purchases common | ✅ Strengthen premium card offers (travel rewards, concierge services)<br>✅ Build partnerships with airlines, hotels, and luxury brands<br>✅ Cross-sell wealth products (loans, investments, insurance)<br>✅ Target retention with elite loyalty tiers |
| 🟡 **Cluster 2 — "At-Risk or Emerging"** | Moderate income, weaker credit stability | 🔹 Lowest avg. credit score (641)<br>🔹 Avg. income \~\$43K<br>🔹 Possibly younger, financially unstable<br>🔹 Higher risk of outstanding debts/missed payments | ✅ Provide secured credit or starter cards with limited lines<br>✅ Offer financial education and credit-building tools<br>✅ Incentivize on-time repayment with small rewards<br>✅ Closely monitor for default risk but keep engaged                    |

### 5.11. Dashboard Screenshots
<img width="1755" height="891" alt="image" src="https://github.com/user-attachments/assets/0e9eee88-be6c-4b2d-abd6-36a2499b7c08" />

### a. Average Revenue Per User
#### Monthly ARPU
Average Revenue Per User (ARPU) = Total Revenue / Number of Users
(where Total Revenue = Total Amount of Transactions)

<img width="895" height="797" alt="image" src="https://github.com/user-attachments/assets/58f9c36e-72d2-4cc3-8a52-dc21997e8a8a" />

#### ARPU 2018 vs 2019
- avg_arpu_2019 =  3881.80
- avg_arpu_2018 =  3899.40

|index|year\_month|total\_revenue|active\_users|arpu|
|---|---|---|---|---|
|96|2018-01-01 00:00:00|4780716\.87|1206|3964\.1101741293533|
|97|2018-02-01 00:00:00|4344874\.41|1206|3602\.7150995024876|
|98|2018-03-01 00:00:00|4795983\.31|1204|3983\.3748421926907|
|99|2018-04-01 00:00:00|4631021\.03|1204|3846\.362981727575|
|100|2018-05-01 00:00:00|4759965\.88|1205|3950\.179153526971|
|101|2018-06-01 00:00:00|4651327\.62|1204|3863\.2289202657807|
|102|2018-07-01 00:00:00|4827954\.29|1204|4009\.928812292359|
|103|2018-08-01 00:00:00|4818141\.35|1204|4001\.7785299003317|
|104|2018-09-01 00:00:00|4609024\.18|1204|3828\.093172757475|
|105|2018-10-01 00:00:00|4767724\.3|1204|3959\.903903654485|
|106|2018-11-01 00:00:00|4647905\.46|1204|3860\.3865946843853|
|107|2018-12-01 00:00:00|4726861\.05|1205|3922\.706265560166|
|108|2019-01-01 00:00:00|4761237\.98|1205|3951\.234838174274|
|109|2019-02-01 00:00:00|4280985\.01|1205|3552\.6846556016594|
|110|2019-03-01 00:00:00|4811501\.44|1206|3989\.6363515754565|
|111|2019-04-01 00:00:00|4630872\.03|1206|3839\.860721393035|
|112|2019-05-01 00:00:00|4785771\.43|1206|3968\.301351575456|
|113|2019-06-01 00:00:00|4664187\.55|1206|3867\.4855306799336|
|114|2019-07-01 00:00:00|4772649\.67|1206|3957\.420953565506|
|115|2019-08-01 00:00:00|4748442\.2|1206|3937\.348424543947|
|116|2019-09-01 00:00:00|4586445\.68|1206|3803\.022951907131|
|117|2019-10-01 00:00:00|4753052\.64|1203|3950\.9997007481293|

<img width="989" height="590" alt="image" src="https://github.com/user-attachments/assets/c4ff6952-b61f-473b-b22b-6df89b257af4" />

####
| 🔍 **Key Insights**                                                                     | 💡 **Recommendations**                                                                         |
| --------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------- |
| 📉 **Flat ARPU** – 2019 avg ($3,882) slightly below 2018 avg ($3,899), showing stagnation.  | 🚀 **Boost ARPU** by introducing new bundles, upselling, or premium features.                  |
| 📊 **Volatility in 2019** – Sharper dips (e.g., Feb 2019 \~$3,550) compared to 2018.      | ⚡ **Stabilize performance** – investigate churn, seasonality, or external economic factors.    |
| 🔄 **Recurring seasonal dips** – Both years show early-year drops followed by rebounds. | 📆 **Seasonal campaigns** – run promotions in low months (e.g., Q1) to smooth dips.            |
| 🔐 **No growth momentum** – Most months hover around \~$3,900, no upward trend.           | 🎯 **Retention & loyalty** – focus on keeping high-value users and reward consistent spenders. |

### b. New Customers

=> The transaction data absolutely does not have enough information on new customers for each year

|index|year|new\_clients|
|---|---|---|
|0|2010|1137|
|1|2011|30|
|2|2012|15|
|3|2013|12|
|4|2014|8|
|5|2015|9|
|6|2016|6|
|7|2017|2|

### c. Gross Margin
- The Gross Margin information is based on a research online from the link: https://pages.stern.nyu.edu/~adamodar/New_Home_Page/datafile/margin.html
<img width="796" height="649" alt="image" src="https://github.com/user-attachments/assets/7d9db532-004c-4239-be2f-2fc2ea5b99b9" />

- 'Gross Margin' value for other MCC will be calculated by 25% of Average Gross Margin from the research table above.
- We will have the final Average Gross Margin (%): 22.20

### d. Lifetime Value (LTV)
<img width="344" height="507" alt="image" src="https://github.com/user-attachments/assets/7889dbcf-f6a1-4265-b099-7dd8146a10e4" />

- We will have the Lifetime Value) = 3,867 (USD)
