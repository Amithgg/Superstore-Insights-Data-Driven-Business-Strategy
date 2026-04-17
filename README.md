# Superstore-Insights-Data-Driven-Business-Strategy
📊 End-to-end retail analytics using MySQL &amp; Power BI — uncovering profit leaks, regional performance, and discount traps in the Sample Superstore dataset.


🛒 Superstore Insights: Data-Driven Business Strategy

🖼️ Dashboard Preview

| Total Sales by Region | Total Profit by Region |

| 🟣 West — 725.46K (31.58%) | 🟣 West — 108K |
| 🔵 East — 678.78K (29.55%) | 🔵 East — 92K |
| 🔷 Central — 501.24K (21.82%) | 🟠 South — 47K |
| 🟠 South — 391.72K (17.05%) | 🔷 Central — 40K |

📊 Interactive dashboards built in Power BI — see `/dashboard/` folder for `.pbix` file


📖 About

Superstore Insights is an end-to-end data analytics project built on the classic Sample Superstore retail dataset. It combines MySQL for structured querying and Power BI for interactive visualization to uncover actionable business intelligence from over 9,900 retail transactions across the United States.

This project demonstrates the full analytics pipeline — from raw data ingestion to strategic business recommendations — making it a complete showcase of real-world data analysis skills.


🎯 Purpose

The core objective of this project is to answer a fundamental business question:

Where is the Superstore making money, where is it losing money — and why?

By slicing data across regions, categories, shipping modes, customer segments, and discount structures, this project surfaces the hidden inefficiencies and overlooked opportunities that drive or drain profitability. The goal is not just analysis — it's to equip business decision-makers with the insight to act.


📦 Dataset Overview

| Property | Detail |

| Source | Sample Superstore (Tableau / Kaggle public dataset) |
| Records | ~9,994 rows |
| Time Period | 4 years of US retail transactions |
| Format | CSV → imported into MySQL |
| Key Fields | `Ship_Mode`, `Segment`, `Region`, `Category`, `Sub-Category`, `Sales`, `Quantity`, `Discount`, `Profit` |

Regions Covered: West · East · Central · South

Product Categories: Furniture · Office Supplies · Technology

Customer Segments: Consumer · Corporate · Home Office


🧭 Approach

The project was executed in three phases:

1. 🗄️ Database Setup (MySQL)**
- Created a dedicated `superstore_project` database
- Designed a `sales` table with appropriate data types (`DECIMAL`, `VARCHAR`, `INT`)
- Imported and verified 9,994 rows of clean retail data

2. 🔍 Exploratory & Deep-Dive SQL Analysis**
- Wrote 10+ targeted SQL queries covering revenue, profit, discounts, shipping, and segments
- Used `GROUP BY`, `HAVING`, `ORDER BY`, `NULLIF`, `ROUND`, and aggregate functions
- Identified loss-making sub-categories, high-discount traps, and top-performing geographies

3. 📊 Power BI Visualization**
- Connected Power BI to query outputs
- Built interactive charts: donut chart for regional sales share, bar charts for profit comparison
- Applied consistent color coding by region for clarity


🧩 Questions Solved in the SQL File

The `superstore_analysis.sql` file is structured around 10 analytical blocks:

| # | Query Block | What It Does |

| 1 | Database & Table Setup | Creates schema, defines column types, imports data |
| 2 | Data Verification | `SELECT *` and `COUNT(*)` to confirm successful import |
| 3 | Overall KPIs | Total revenue, total profit, average discount |
| 4 | Category Performance | Revenue and profit breakdown by product category |
| 5 | Loss-Making Sub-Categories | Filters sub-categories where `SUM(profit) < 0` |
| 6 | Top 5 Most Profitable Cities | Best performing cities by total profit |
| 7 | 5 Least Profitable Products | Sub-categories with the lowest profit margins |
| 8 | High Discount Analysis | Avg discount % vs total profit by category |
| 9 | Shipping Mode Performance | Order count, total sales, avg profit per shipping method |
| 10 | Customer Segment Deep Dive | Revenue, profit, and profit margin % by segment |
| 11 | High Sales / High Loss Mystery| Identifies sub-categories that sell well but lose money |
| 12 | Regional Performance Deep Dive | Cities reached, sales, profit, and margin % by region |


❓ Key Questions Answered
💰 Which region generates the most revenue and profit?
West leads in both sales ($725K) and profit ($108K), followed by East ($678K sales, $92K profit). The Central region trails significantly in profit despite decent sales volume — signalling an efficiency gap.

📉 Which sub-categories are losing money?
Tables and Bookcases are the primary loss-makers in the Furniture category. These items are frequently sold at steep discounts, completely eroding their margins.

🏙️ Which cities are most profitable?
The top 5 most profitable cities are concentrated in the West and East regions, confirming their dominance as growth markets.

🚚 Which shipping mode performs best?
Same Day shipping delivers the highest average profit per order, while Standard Class handles the most volume but at lower per-order profitability.

🎯 Which customer segment is most efficient?
The Home Office segment achieves the highest profit margin percentage, making it the most efficient segment despite not being the largest by revenue.

🔥 Why do high-sales products sometimes lose money?
The discount analysis reveals that products like Tables have average discounts exceeding 30%, which turns high-sales volume into net losses — the classic "sell more, lose more" trap.

Repository Structure

superstore-insights/
│
├── 📁 data/
│   └── SampleSuperstore.csv          # Raw dataset
│
├── 📁 sql/
│   └── superstore_analysis.sql       # All 12 SQL query blocks
│
├── 📁 dashboard/
│   └── Superstore_Dashboard.pbix     # Power BI dashboard file
│
├── 📁 screenshots/
│   └── dashboard_preview.png         # Chart previews
│

🔚 Conclusion

This project confirms that revenue and profitability do not always move together. The Superstore's biggest challenge isn't sales volume — it's margin erosion through excessive discounting, particularly in the Furniture category. Meanwhile, regions like the West consistently outperform not just in sales, but in operational efficiency.

The combination of SQL for precision querying and Power BI for visual storytelling proved highly effective in transforming raw transaction data into a clear, decision-ready business narrative.

💡 Recommendations

Based on the analysis, here are the top strategic recommendations:

| Priority | Recommendation | Impact |

| 🔴 High | Cap discounts on Tables and Bookcases at 10% — current discounts exceed 30% and cause direct losses | Immediate profit recovery |
| 🔴 High | Audit the Central region — high sales, low profit margin signals operational inefficiency or pricing issues | Margin improvement |
| 🟡 Medium | Double down on the West region — highest sales AND profit margin; ideal for expansion investment | Revenue growth |
| 🟡 Medium | Prioritize Home Office segment marketing — highest profit margin %; underserved relative to its efficiency | Scalable growth |
| 🟢 Low | Evaluate Same Day shipping pricing — high avg profit per order; consider upselling it more actively | Incremental gains |
| 🟢 Low | Investigate Technology sub-category opportunities — strong margins; potential for bundling with loss-making Furniture items | Portfolio optimization |

💬 Feedback and Suggestions

Have ideas to improve this analysis? Found an interesting pattern in the data I missed?
🤝 Want to contribute Fork the repo, make your changes, and submit a Pull Request
📧 Direct feedback Reach me at [amithgowda210@gmail.com]

All feedback is genuinely welcome — this project is a learning journey and every perspective helps

⭐ Support This Project

If this project helped you learn something new, inspired your own analysis, or saved you time — consider showing your support:

⭐ Star the repository — it helps others discover this project
🍴 Fork and build on it— extend the analysis with your own queries
📢 Share it — tag me on LinkedIn if you use this as inspiration for your own project

Data is the new oil — but only if you know how to refine it.

Made with 🟣 SQL + 📊 Power BI | © 2026
