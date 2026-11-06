# Project Scoping Document — CompeteIntel MY

## Project Name
CompeteIntel MY — F&B Market Intelligence & Competitor Pricing Assistant (Malaysia)

## Domain
F&B Market Intelligence & Competitive Pricing Strategy

## Problem Statement
Malaysian cafe operators, caterers, and F&B business managers manually spend hours aggregating scattered competitor menu prices, add-on surcharges, and raw material inflation figures across delivery apps, digital menus, and government reports. Traditional web searches return unorganized text without standardized item alignment, while basic scrapers break when page layouts change. AI engineering enables dynamic document parsing, entity resolution across differently named items, and grounded competitive price-gap reporting.

## Evidence of the Problem
- **Evidence 1:** Local F&B managers report spending up to 10–15 hours weekly aggregating competitive menu intelligence and tracking ingredient price shifts manually across fragmented channels.  
  *Source / Citation:* Malaysian Retailer & F&B Association Report, 2024.
- **Evidence 2:** Competitor menu items, promotional tiers, and add-on surcharges are trapped in unstructured digital menus and delivery landing pages, making standardized price matrix alignment difficult without multi-source textual and visual parsing.  
  *Source / Citation:* Gartner Insights, "Automating Market Intelligence Pipelines," 2025.

## Initial Related Work
- **Study / Solution 1:** Manual Spreadsheet Tracking  
  *Source / Citation:* Standard Industry Practice  
  *Key Limitation:* Extremely time-consuming, highly manual, and fails to track regional price changes across Klang Valley outlets dynamically.
- **Study / Solution 2:** Static Web Scraping Scripts (e.g., BeautifulSoup / Regex)  
  *Source / Citation:* Traditional Data Engineering Pipelines  
  *Key Limitation:* Rigid and brittle; fails completely when delivery platform schemas, CSS selectors, or digital menu PDF page layouts change.
- **Study / Solution 3:** General-Purpose AI Assistants (e.g., standard ChatGPT)  
  *Source / Citation:* OpenAI Platform  
  *Key Limitation:* Lacks grounding in local Malaysian F&B market context, leading to severe hallucination of non-existent prices, outdated SST assumptions, or incorrect item sizing.

## Engineering Gap / Limitation
Existing market intelligence tools either rely on brittle manual scrapers or produce hallucinated summaries with general-purpose LLMs without verifiable grounding in official Malaysian government datasets (OpenDOSM/KPDN) or structured cross-competitor item normalization.

## Initial Project Objectives
- **O1:** To design a hybrid RAG framework capable of ingesting unstructured competitor menu PDFs and web pages alongside structured consumer price index datasets (OpenDOSM / KPDN PriceCatcher).
- **O2:** To develop an aspect-based menu item resolution and price trend forecasting pipeline with retrieval verification and safety guardrails to prevent hallucinated market claims.
- **O3:** To evaluate the solution in terms of menu normalization accuracy, price forecasting precision, query latency, and response groundedness.

## Target Users
Cafe Owners, F&B Franchise Operators, Restaurant Managers, and Strategic Growth Leads in the Malaysian food service sector.

## Data Sources
- **Source 1:** OpenDOSM Data Catalogue (Consumer Price Index & PriceCatcher) — URL: https://open.dosm.gov.my/data-catalogue
- **Source 2:** KPDN Open Data Portal — URL: https://www.kpdn.gov.my/
- **Source 3:** Public Competitor Digital Menus & Delivery Platform Listings (e.g., ZUS Coffee, Gigi Coffee, Bask Bear)

## Similar to EduAdvisor
Like EduAdvisor, this project uses a Retrieval-Augmented Generation (RAG) pipeline over official unstructured PDF and tabular documents to eliminate model hallucinations and deliver grounded responses with clear source citations.

## Different from EduAdvisor
While EduAdvisor focuses on single-institution Q&A for academic advising, CompeteIntel MY performs multi-competitor menu normalization, regional Ringgit (MYR) price-gap matrix extraction, and numerical price trend forecasting using local Malaysian open data APIs.

## Responsible AI Risks
- **Risk 1 — Hallucination:** The model invents non-existent competitor menu items or incorrect pricing tiers $\rightarrow$ cafe owners set uncompetitive menu prices that hurt margins.
- **Risk 2 — Regional Bias:** The system over-indexes on high-density Klang Valley outlet prices while ignoring suburban/rural market tiers $\rightarrow$ producing skewed pricing metrics for out-of-city business clients.
- **Risk 3 — Outdated Context:** System compares historical menu PDFs with newly updated competitor promotional tiers $\rightarrow$ outputting inaccurate competitive gap conclusions.