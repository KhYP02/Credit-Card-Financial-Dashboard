# Credit Card Financial Dashboard (Power BI)

A 3-page Power BI report on credit card revenue, built from two tables: card transactions and customer profiles. The goal was to answer a simple question a card business cares about: where does revenue actually come from, and who are the customers behind it?

**Data:** 10,108 clients, weekly records from Jan to Dec 2023, joined on `Client_Num` (`credit_card.csv` + `customer.csv`).
**Revenue** here is annual fees + transaction amount + interest earned, as defined in the dataset.

## What's in the report

1. **Overview:** revenue by card category, plus a week-over-week revenue table.
2. **Transaction Report:** revenue, interest, amount and transaction count KPIs, quarterly revenue vs transaction volume, and revenue by expense type, education, job type, usage type and card category.
3. **Customer Report:** weekly revenue trend by gender, plus revenue by age group, state, marital status, income group, dependents and education.

Slicers for quarter, gender, income group, card category and week let you filter every page.

## DAX measures

Week-over-week revenue is built with three measures:

- `Current_Week_Revenue`: revenue for the latest week number in the current filter
- `Previous_Week_Revenue`: revenue for the week before it, ignoring other filters
- `wow_revenue`: `DIVIDE(Current - Previous, Previous)`

Weekly swings in the data range from about -6.7% to +14.5%.

## Key findings

- **Total revenue is about 55M**, with 45M in transaction amount and 8M in interest.
- **Blue cards drive 83% of revenue** (Silver 10%, Gold and Platinum about 7% combined).
- **Swipe is 63% of revenue** (35M), ahead of chip (17M) and online (3M).
- **Revenue dipped about 6.6% from Q3 to Q4** (14.2M to 13.3M), with transaction count also falling (166.6K to 161.6K).
- **Gender and income split:** in the high income group, men generate 22M vs 7M from women. In the low income group it flips: women generate 10M vs 1M from men.
- **Top segments:** Businessman is the top job type (17M) and Bills is the top spend category (14M). TX, NY and CA lead by state.

## Files

| File | What it is |
|---|---|
| `Credit_Card_Report.pbix` | The Power BI file |
| `Credit_Card_Report.pdf` | Overview page export |
| `Credit_Card_Transaction_Report.pdf` | Transaction page export |
| `Credit_Card_Customer_Report.pdf` | Customer page export |
| `credit_card.csv`, `customer.csv` | Source data |

## Tools

Power BI Desktop, DAX, Power Query.

## Author

Kharanshu Papolli, IIT (ISM) Dhanbad
[LinkedIn](https://www.linkedin.com/in/kharanshuyp)
