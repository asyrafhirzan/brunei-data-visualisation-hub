# Brunei Open Data Hub

> An automated, open-source data hub and visual analytics platform for Brunei Darussalam public data, inspired by the UK Office for National Statistics (ONS).



---

## About This Project
Government open portals provide raw spreadsheets, but rarely clear insights. This project bridges the gap by building an automated pipeline that ingests raw government data, standardizes it into tidy tables, and publishes an interactive, SQL-driven analytics hub at **zero hosting cost**.

### Key Features
- **Automated Pipeline:** Scheduled GitHub Actions workflow handles data ingestion and site rebuilding.
- **Tidy Data Engineering:** Custom Python parsers clean messy government spreadsheets into validated tabular formats.
- **SQL-Driven Analytics:** Built with Evidence.dev, combining markdown commentary with dynamic SQL queries.
- **Flagship Cost of Living Analysis:** Deep dive into Consumer Price Index (CPI) and retail price trends.

---

## Architecture & Tech Stack
- **Ingestion & Processing:** Python, Pandas
- **Front-End & Visualization:** Evidence.dev, SQL, Tailwind CSS
- **Automation & Hosting:** GitHub Actions, GitHub Pages ($0 stack)

---

## Disclaimer
*This is an independent, unofficial presentation of public data sourced from data.gov.bn. It is not affiliated with, endorsed by, or officially connected to the Government of Brunei.*