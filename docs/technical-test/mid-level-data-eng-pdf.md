# Data Engineer — Take-Home Technical Test (≈4h)

Background Context

Your task is to design and implement a small ETL pipeline that extracts structured information from unstructured PDF files. These PDFs simulate real-world scenarios where data can be text-based, table-based, or scanned images.

The goal is to:
1. Extract relevant fields
2. Transform and clean the data
3. Load it into a relational database or spreadsheet
4. Analyze the resulting dataset
5. Automatically generate a structured report

## Test Overview

Estimated execution time: ~4 hours

Deliverables:
- Source code (GitHub repo or zip archive)
- Example structured outputs (CSV/Excel or PostgreSQL dump)
- Example generated report (Markdown, PDF, or HTML)
- Documentation (README.md)

## Input Data — Sample PDFs

Choose at least two PDFs from the following public sources and save them into a local data/input/ folder:
1. Text-heavy contract specification
Jordan 2019 Standard Specifications for Construction (PDF)
2. Invoice with tabular data
Sample Invoice (PDF)
3. Scanned receipts (image-based, OCR required)
Receipts Dataset on Kaggle

## Your Task

1. Extract
- Parse your chosen PDFs and extract:
- Document ID (e.g., project ID, invoice number, receipt number)
- Contractor/client/supplier name
- Description
- Line items (item, quantity, unit price, total)

2. Transform
- Normalize and clean the data (consistent naming, enforce numeric types)
- Ensure high accuracy, quality, and reliability (e.g., handle missing/invalid fields gracefully)
- If semantics differ across documents, map them to a consistent schema and note your decisions in the docs

3. Load
- Save the structured data into:
- A PostgreSQL database (preferred) or
- A CSV/Excel file
- Propose a simple schema (e.g., documents, contractors, line_items) and justify your design in the README

4. Analyze
- Perform a basic analysis of the dataset, such as:
- Number of documents processed
- Total contract/invoice/receipt value
- Top 5 contractors/suppliers by value
- Most common line items


## Requirements
- Use Python (preferred) or another language you’re comfortable with
- Recommend and implement libraries/tools/services you find most suitable
- Code should be modular, reusable, and documented
- Provide clear documentation for internal use and possible handoff, including:
- Setup and execution steps
- Tool/service choices and reasoning
- Assumptions and semantic adjustments

## Evaluation Criteria

We’ll assess your submission on:
- Correctness – Did you extract, transform, load, analyze, and report successfully?
- Code quality – Clean, modular, well-structured, readable
- Accuracy & reliability – Is the data consistent, clean, and validated?
- Tooling & design – Did you choose appropriate tools and explain why?
- Documentation – Clear instructions and reasoning for future handoff
- Automation – End-to-end pipeline execution

## Bonus Deliverables (Optional, if time allows)

(Not required — scope these only if you have time beyond the core 4 hours)
1. Cloud integration: Fetch PDFs from AWS S3 or similar itead of local folder
2. CLI or API interface: Trigger the pipeline with pameters (e.g., FastAPI endpoint, CLI command)
3. AI-assisted parsing: Use AWS Textract, Azure Form Rognizer, or LLM-based parsing for scanned PDFs
4. Containerization/CI: Add a Dockerfile or GitHub Actions workflow for easy deployment

## Submission

Submit as a GitHub/GitLab repo or zipped folder containing:
- src/ → source code
- data/ → chosen sample PDFs + outputs
- reports/ → generated analysis reports
- README.md → documentation