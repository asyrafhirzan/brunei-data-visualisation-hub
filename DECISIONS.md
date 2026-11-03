# Architecture Decision Record (ADR)

## ADR 1: Front-End Framework Selection
- **Decision:** Use **Evidence.dev** as the static site generator.
- **Alternatives Considered:** Observable Framework (JavaScript/D3), Custom React/Next.js.
- **Reason:** Evidence.dev uses SQL queries embedded in Markdown, matching your strong familiarity with SQL and allowing rapid component generation without writing complex JS.
- **Date:** October 2026

## ADR 2: Intermediate Data Storage Strategy
- **Decision:** Use **local build artifacts** (processed CSVs stored directly in the repository or generated dynamically inside the CI/CD build runner).
- **Alternatives Considered:** External cloud data warehouse (Snowflake, BigQuery, Supabase).
- **Reason:** Keeps infrastructure cost strictly at $0, avoids external database maintenance, and perfectly suits a static site architecture.
- **Date:** October 2026

## ADR 3: Hosting and CI/CD Execution
- **Decision:** **GitHub Pages** powered by **GitHub Actions** for scheduled execution.
- **Alternatives Considered:** Cloudflare Pages, Hugging Face Spaces, Vercel.
- **Date:** October 2026
- **Reason:** GitHub Actions provides native cron scheduling to automatically re-crawl and rebuild the site without server upkeep.