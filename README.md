# Internship Learning Journal  
**Name:** Chandrashekhar Umesh Mannur     
**USN:** 2BL22CS051      
**GitHub Username:** Chandrashekhar051   
**Department:** CSE     
**Internship Start Date:** 03-02-2026

---

## 📌 Objective
This repository documents my learning journey during the internship.  
All notes, assignments, and project learnings are organized module-wise and chapter-wise.

---

## 🗂 Course Reference
Course Link: https://tds.s-anand.net/#/

---

## 📚 Modules Covered

| Module | Topics | Status |
|--------|--------|--------|
| Module 01 | Foundations | Completed |
| Module 02 | Tools & Implementation | Completed |
| Module 03 | LLM Concepts, Embeddings, RAG, Multimodal & Deployment | Completed |
| Module 04 | Data Sourcing, API Integration, Web Scraping, Data Preprocessing & Automation | Completed |
| Module 05 | Data Preparation, Cleaning, Shell Processing, DuckDB, dbt, OpenRefine, JSON & Media Data | Completed |
---



## 🚀 Key Learnings So Far

### Module 1

- Set up a complete Linux-based development environment using WSL (Ubuntu 24.04 LTS).
- Understood Linux file system structure and essential terminal commands.
- Learned Git fundamentals and implemented the full version control workflow.
- Configured SSH authentication for secure GitHub collaboration.
- Integrated VS Code with WSL for efficient development.
- Used Homebrew (macOS) for package management.
- Managed Python environments using UV.
- Installed and configured LLM CLI for terminal-based AI interaction.
- Secured API keys using environment variables.
- Leveraged GitHub Copilot to enhance coding productivity.
- Built a fully CLI-driven development workflow across platforms.

### Module 2 

- Learned core containerization concepts using Podman.
- Ran and managed containers with port binding and volume mounting.
- Implemented inter-container communication using custom bridge networks.
- Containerized and executed a local LLM (Ollama + Gemma).
- Built and connected a Flask/FastAPI backend with containerized services.
- Understood API development using FastAPI (GET, POST, validation).
- Practiced secure secret management with environment variables.
- Deployed applications using GitHub Pages, Vercel, and Hugging Face Spaces.
- Explored GitHub Codespaces for cloud-based development.
- Automated workflows using GitHub Actions (CI/CD).
- Completed end-to-end workflow: Develop → Containerize → Deploy → Automate.

### Module 3

- Understood how Large Language Models (LLMs) work using tokens, vectors, and self-attention.
- Learned about context window limits and why chunking is necessary.
- Gained hands-on experience making secure OpenAI API calls using `httpx`.
- Implemented embeddings and cosine similarity for semantic search.
- Built a mini vector database and retrieval pipeline (Generate → Store → Compare → Retrieve).
- Implemented Retrieval Augmented Generation (RAG) to reduce hallucinations.
- Worked with multimodal inputs (text + image using Base64 encoding).
- Used function calling to extract structured JSON outputs.
- Improved prompt engineering using structured and role-based prompts.
- Debugged API errors and resolved deployment issues (FastAPI + Vercel).
- Learned cost optimization techniques for embeddings and API usage.
- Understood the importance of evaluation, testing, and production readiness.

### Module 4 

- Understood different data sourcing strategies for structured, semi-structured, and unstructured data.
- Learned how REST APIs work, including HTTP methods, headers, authentication, and JSON parsing.
- Practiced using CLI tools (curl, wget) for making HTTP requests.
- Performed spreadsheet-based web data extraction using IMPORTHTML and IMPORTXML.
- Scraped static websites using HTML parsing techniques.
- Handled dynamic websites using browser automation tools (Playwright).
- Analyzed DOM structure using Developer Tools, CSS selectors, and XPath.
- Extracted structured data from PDFs and converted documents into Markdown.
- Explored AI-assisted and LLM-based scraping for intelligent data extraction.
- Understood practical challenges like rate limiting, IP blocking, and ethical scraping practices.
- Automated data workflows using GitHub Actions and cron-based scheduling.
- Learned data cleaning, normalization, and preprocessing for analysis-ready datasets.

### Module 5

- Understood the importance of data preparation before performing analysis or building machine learning models.
- Learned how to inspect datasets to understand structure, size, and potential data quality issues.
- Practiced identifying and removing duplicate records to maintain dataset accuracy.
- Learned techniques to detect and handle missing or incomplete data values.
- Used shell utilities such as `grep`, `cut`, `sort`, `uniq`, `sed`, and `awk` for efficient data processing.
- Understood how command-line tools help process large CSV or text datasets quickly.
- Learned how to standardize and clean text data to maintain consistency in datasets.
- Explored using text editors and regular expressions for bulk data corrections.
- Learned how DuckDB can be used to query and transform datasets using SQL.
- Understood how dbt helps organize and manage data transformation workflows.
- Explored OpenRefine for identifying inconsistencies and cleaning messy datasets.
- Learned basic preparation techniques for working with JSON, image, and audio data.

### Module 6

- Performed exploratory data analysis (EDA) to understand dataset structure, distributions, and data quality issues.
- Applied statistical techniques such as correlation and regression to identify relationships between variables.
- Implemented forecasting methods using historical data to estimate future trends.
- Detected and analyzed outliers to improve data reliability and accuracy of analysis.
- Used Excel for quick analysis including pivot tables, correlation, regression, and visualization.
- Analyzed datasets programmatically using Python libraries like pandas and numpy.
- Executed SQL queries for filtering, grouping, and aggregating large datasets efficiently.
- Performed database-level analysis to handle large-scale data without loading into memory.
- Explored datasets interactively using Datasette for quick inspection and sharing.
- Utilized DuckDB for high-performance analytical queries directly on CSV/Parquet files.
- Leveraged AI tools to generate insights, assist analysis, and improve exploratory workflows.
- Conducted geospatial analysis to understand location-based patterns and spatial relationships.
- Used QGIS and Python tools for advanced geographic data visualization and analysis.
- Applied network analysis techniques in Python to study relationships between entities using graph structures.
- Integrated multiple tools and techniques to extract meaningful insights from structured and semi-structured data.
  
---

## ❓ Doubts / Topics to Revisit
- Topic 1  
- Topic 2  

---

## 🔄 Weekly Update Log
| Week | What I Learned |
|------|----------------|
| Week 1 | Set up Linux-based development using WSL/macOS, mastered Git & SSH workflow, configured CLI tools (UV, LLM), and integrated AI tools into terminal workflow. |
| Week 2 | Implemented containerization using Podman, built FastAPI applications, enabled inter-container networking, deployed apps (GitHub Pages, Vercel, Hugging Face), and automated workflows with GitHub Actions. |
| Week 3 | Understood LLM fundamentals (tokens, self-attention, context limits), implemented embeddings and cosine similarity, built a complete RAG pipeline with vector search, worked with multimodal inputs (text + image via Base64), applied structured prompt engineering and function calling, optimized API usage, and resolved deployment/debugging issues for production-ready AI systems. |
| Week 4 | Learned data sourcing techniques including API data retrieval with Python, spreadsheet scraping, CLI crawling (curl/wget), web scraping of static and dynamic sites using HTML parsing and Playwright, PDF data extraction with Tabula, and automation of scraping workflows using GitHub Actions. |
| Week 5 | Learned comprehensive data preparation workflows including dataset inspection, duplicate removal, handling missing values, text standardization, and column extraction using shell utilities (`grep`, `sed`, `awk`, `cut`, `sort`, `uniq`). Practiced restructuring and aggregating datasets, preparing structured data using SQL queries in DuckDB, and organizing transformation pipelines using dbt. Explored cleaning messy datasets with OpenRefine, parsing semi-structured JSON data, and preparing multimedia datasets such as images and audio for downstream data analysis and machine learning workflows. |
| Week 6 | Performed EDA and statistical analysis (correlation, regression, forecasting, outlier detection) using Excel and Python. Executed SQL-based analysis and utilized DuckDB and Datasette for efficient data querying. Applied geospatial and network analysis techniques, and leveraged AI tools to enhance insight generation and analysis workflows. || Week 7 | Created data visualizations using tools such as Excel, Seaborn, and RAWGraphs, including charts for trends, distributions, and correlations. Built animated and network visualizations using Flourish and Kumu, and developed interactive notebooks with Marimo. Applied data storytelling techniques and leveraged AI tools to generate and communicate insights effectively. |

---


