# Junior Data Engineer Task: LLM Training Data Pipeline  

**Domain:** Text Data Processing Platform
**Expected Time:** 8–16 Hours

---

## Objective  

Build a **scalable data pipeline** to ingest, clean, and validate unstructured text data for machine learning workflows. Demonstrate proficiency with Python/SQL, Docker, and IaC (Terraform).

---

## Requirements  

### 1. Data Ingestion & Transformation  

- Create a Python script to:
  - Read 1000+ sample text documents (`.txt` files) from a directory.  
    - You may also use text documents from HuggingFace.
  - **Clean data**: Remove special characters, normalize whitespace, filter out short/low-quality text.
  - Split text into chunks (max 512 tokens) using a tokenizer of your choice. (Please explain why you chose this tokenizer in the README.)

### 2. SQL Metadata Management  

- Design a PostgreSQL table to track:  
  - Chunked text content  
  - Source file metadata (file name, chunk ID, quality score)  
  - Processing timestamps  
- Use SQLAlchemy or Django ORM to insert cleaned data into the table.  

### 3. Infrastructure as Code (IaC)  

- Write a Terraform script to provision:  
  - A cloud storage bucket (AWS S3/GCP Cloud Storage) for raw text files.  
  - A managed PostgreSQL instance (e.g., AWS RDS, GCP Cloud SQL).  
- Dockerize the pipeline (create a `Dockerfile` to run your Python script).  

### 4. Data Quality Checks  

- Add validation rules:  
  - Reject chunks with >30% non-alphanumeric characters.  
  - Flag chunks containing PII-like patterns (e.g., mock credit card numbers).  

---

## AI Collaboration Rules  

- **Allowed**:  
  - Use AI for boilerplate code (e.g., Terraform templates, Dockerfile setup).  
- **Required**:  
  - Core data-cleaning logic and SQL schema design **must be your own work**.  
  - Add code comments explaining *why* you chose specific cleaning/validation rules.

---

## Deliverables  

1. GitHub repo containing:  
   - Python data pipeline code  
   - Terraform scripts + Dockerfile  
   - Sample text data (or script to generate mock data)  
2. `README.md` with:  
   - Architecture diagram of your pipeline  
   - Instructions to deploy infrastructure + run the pipeline  
   - **Data quality report** (sample stats: % chunks filtered, avg token count)  

---

## Bonus (Optional)  

1. Add Airflow DAGs to schedule pipeline runs.  
2. Implement data lineage tracking (e.g., log transformations in a metadata table).  
3. Build a simple dashboard (Plotly/Streamlit) showing dataset statistics.  

---

## Evaluation Criteria  

- **Data Quality**: Cleaned chunks meet token/formatting requirements.  
- **SQL Efficiency**: Schema design optimizes for text search/analytics.  
- **IaC Best Practices**: Terraform scripts are modular/reusable.  
- **Pipeline Reproducibility**: Docker setup works out-of-the-box.  
