# Architecture & Pipeline Workflow

## Conceptual Overview (How the Pipeline Works)
If you are new to automated data pipelines, think of this as an assembly line in a factory:
1. **Source:** Raw spreadsheets sit on a government web page.
2. **Ingest (Crawler):** A Python script visits the page, detects download links, downloads raw files (`.xlsx`, `.csv`), and saves them with a manifest record.
3. **Standardize (Parsers):** Specialized Python scripts clean up the messy spreadsheets (dropping bad rows, fixing column names) and output clean "tidy" tables.
4. **Describe (Config):** YAML configuration files tell the front-end how to display each dataset (titles, axis labels, chart types).
5. **Build & Publish (Static Site Generator):** Evidence.dev takes the tidy data and YAML configs, compiles them into HTML/CSS/JS, and GitHub Pages publishes them to the world for free.

## Data Flow Diagram

```mermaid
graph TD
    A[data.gov.bn Portal] -->|GitHub Actions Cron| B[1. Ingest: Crawler & Manifest]
    B -->|Raw Files / XLSX / CSV| C[2. Standardize: Tier 1 & 2 Parsers]
    C -->|Tidy Data / Parquet / CSV| D[3. Describe: YAML Configs]
    D -->|SQL Queries & Markdown| E[4. Build: Evidence.dev Static Site]
    E -->|HTML / CSS / JS Output| F[5. Publish: GitHub Pages ($0 Hosting)]