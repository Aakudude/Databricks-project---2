# Databricks-project---2
Resume–JD matching pipeline using Databricks, PySpark, and Medallion Architecture
# Resume–JD Matching Pipeline (Databricks)

## Overview
This project implements an end-to-end Resume–Job Description matching pipeline using Databricks and PySpark. The pipeline follows Medallion Architecture (Bronze, Silver, Gold) to extract skills from PDF resumes, match them against a job description, and rank candidates based on relevance.

 Tech Stack
- Databricks
- PySpark
- Python
- Delta Lake
- PyMuPDF

## Architecture
- Bronze: PDF ingestion and text extraction
- Silver: Skill extraction and normalization
- Gold: JD matching, scoring, and candidate ranking

## How to Run
1. Upload resumes and JD to Databricks Volume
2. Run notebooks in order:
   - 01_bronze_pdf_extraction
   - 02_silver_skill_extraction
   - 03_gold_jd_matching_scoring
3. Final ranking is exported as CSV

## Output
- Ranked list of candidates with matching and missing skills

## Notes
Rule-based skill extraction is used for explainability. The pipeline is designed to be extensible with NLP models such as spaCy.
