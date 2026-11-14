# MarketLens MY
> An AI market research assistant that helps Malaysian F&B entrepreneurs and SME owners compare published market indicators and prepare briefs with charts and source citations.

## Problem Statement
Malaysian F&B entrepreneurs need information about consumer spending, the business landscape and price changes when researching a market. This information is spread across reports with different definitions and reference periods, making comparisons difficult. MarketLens MY will use AI to retrieve and synthesise relevant evidence, supported by checked calculations, to produce clear market briefs initially focused on Johor and Selangor.

## Evidence of the Problem
- DOSM publishes consumer expenditure and F&B business statistics in separate reports with different reference periods: the Household Expenditure Survey covers 2024, while the Economic Census 2023 F&B release reports on 2022. This shows the need to combine sources carefully when preparing market assessments. Sources: DOSM Household Expenditure Survey Report 2024 and DOSM Economic Census 2023 F&B release.
- Chen et al. (2021) found that the models evaluated in FinQA struggled with complex numerical reasoning over financial documents. Although the dataset differs from Malaysian market reports, it supports explicitly checking calculations in an AI analysis system. Source: FinQA: A Dataset of Numerical Reasoning over Financial Data.

## Initial Related Work / Existing Approaches
- **Retrieval-Augmented Generation** — Lewis et al. (2020): Combines retrieved evidence with language generation. Its reported tasks do not establish accurate Malaysian market comparisons or calculations. Source: Retrieval-Augmented Generation for Knowledge-Intensive NLP Tasks.
- **FinQA** — Chen et al. (2021): Provides a dataset for evaluating numerical reasoning over financial reports. Its financial-report questions do not directly evaluate Malaysian F&B indicators or market briefs. Source: FinQA: A Dataset of Numerical Reasoning over Financial Data.
- **TableRAG** — Yu, Jian and Chen (2025): Supports reasoning across documents containing text and tables. Its general benchmarks do not establish correct interpretation of this project's indicator definitions, periods and geographic coverage. Source: TableRAG: A Retrieval Augmented Generation Framework for Heterogeneous Document Reasoning.

## Engineering Gap / Limitation
Current market intelligence tools lack a hybrid pipeline capable of combining unstructured multi-competitor menu parsing with structured local time-series data (OpenDOSM) into verified, citation-backed feature and pricing matrices.

## Project Objectives
- **O1**: To design a document-grounded market research assistant that preserves indicator definitions, units, reference periods, geography and sources.
- **O2**: To develop evidence retrieval, supported indicator comparisons, checked calculations, charts and cited market briefs for the selected Malaysian F&B reports.
- **O3**: To evaluate factual and numerical accuracy, citation support, handling of insufficient evidence, response time and the usefulness of generated briefs.

## Target Users
Malaysian F&B SME owners, prospective entrepreneurs and junior business analysts conducting initial market research, particularly comparisons between Johor and Selangor.

## Data Sources
- **Source 1**: DOSM Household Expenditure Survey Report 2024 — PDF.
- **Source 2**: DOSM Economic Census 2023: Food and Beverage Services Sector, official release (reference year 2022) — PDF.
- **Source 3**: DOSM Analysis of Annual Consumer Price Index Malaysia 2024 — PDF.

## Weekly Progress
| Week | Focus | Deliverable | Status |
|------|-------|-------------|--------|
| W1 | System map + project scope | README + docs | ✅ |