# CompeteIntel MY — F&B Market Intelligence & Pricing Assistant
> A document-grounded and time-series AI assistant that analyzes Malaysian F&B competitor menus, delivery platform pricing, and OpenDOSM consumer price indices to generate audit-ready competitive positioning matrices and price forecasts for local business clients.

## Problem Statement
Malaysian cafe operators and F&B business owners spend significant manual effort tracking rapidly changing competitor menu prices and raw ingredient cost spikes. Traditional manual spreadsheet tracking fails to scale across regional markets, while static web scrapers break under layout updates. CompeteIntel MY leverages Retrieval-Augmented Generation (RAG) paired with numerical forecasting over government datasets (OpenDOSM, KPDN PriceCatcher) to deliver citation-backed competitive pricing insights and inflation-adjusted menu recommendations.

## Evidence of the Problem
- Local F&B managers report spending 10–15 hours weekly manually monitoring competitor delivery platform tiers and ingredient cost changes across fragmented channels (Source: Malaysian Retailer & F&B Association Report, 2024).
- Competitor menu items, promotional tiers, and add-on surcharges are published in unstructured digital menus and delivery web pages, making standardized price normalization difficult without automated textual parsing (Source: Gartner Insights, "Automating Market Intelligence Pipelines," 2025).

## Initial Related Work / Existing Approaches
- **Manual Spreadsheet Tracking:** High domain accuracy but extremely time-consuming, highly manual, and fails to track regional price updates dynamically.
- **Static Web Scraping Scripts:** Fast for standard HTML tables but brittle; fails when delivery platform page structures or PDF menu layouts change.
- **General-Purpose AI Assistants:** Flexible conversational text generation but prone to severe hallucination regarding local Malaysian Ringgit (MYR) pricing, regional store tiers, and SST tax impacts.

## Engineering Gap / Limitation
Current market intelligence tools lack a hybrid pipeline capable of combining unstructured multi-competitor menu parsing with structured local time-series data (OpenDOSM) into verified, citation-backed feature and pricing matrices.

## Project Objectives
- **O1:** To design a hybrid RAG framework capable of parsing unstructured local F&B competitor menus (PDFs/web pages) alongside structured government price indices (OpenDOSM/KPDN PriceCatcher).
- **O2:** To develop an aspect-based menu item resolution and price trend forecasting pipeline with citation verification guardrails.
- **O3:** To evaluate the system on menu item normalization accuracy, price forecasting precision, query latency, and response groundedness.

## Target Users
Cafe Owners, F&B Franchise Operators, Restaurant Managers, and Enterprise Caterers in Malaysia.

## Data Sources
- **Source 1:** OpenDOSM Open Data & PriceCatcher Datasets — URL: https://open.dosm.gov.my/data-catalogue
- **Source 2:** KPDN Open Data & Consumer Price Datasets — URL: https://www.kpdn.gov.my/
- **Source 3:** Public Competitor Digital Menus & Price Guides (e.g., ZUS Coffee, Gigi Coffee, Bask Bear)

## Weekly Progress
| Week | Focus | Deliverable | Status |
|------|-------|-------------|--------|
| W1 | System map + project scope | README + docs | ✅ |