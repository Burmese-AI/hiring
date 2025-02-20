# **Junior Data Engineer Task: Scalable LLM Training Data Pipeline**  

**Domain:** Large-Scale Data Processing  
**Expected Time:** 8–16 Hours  

---

## **Objective**  

Develop a **scalable and efficient data pipeline** that collects, processes, and stores unstructured text data. The task will test your ability to handle data ingestion, transformation, storage, and infrastructure automation.  

---

## **Requirements**  

### **1. Data Ingestion & Processing**  

- Implement a Python-based data pipeline that:  
  - Downloads text datasets from an open-source repository (e.g., Hugging Face, Common Crawl, or Wikipedia dumps).  
  - Performs text **preprocessing & cleaning**, including:  
    - Lowercasing, punctuation normalization, and whitespace correction.  
    - Deduplication of repetitive content.  
    - Filtering out low-quality text (e.g., gibberish, extremely short passages).  
  - Chunks the text into **max 512-token segments** using a tokenizer.  
  - Calculates **basic NLP statistics** (e.g., token count, sentence length distribution).  

### **2. Database & Query Optimization**  

- Store processed text in **PostgreSQL** with:  
  - A well-designed table schema for **fast retrieval and analytics**.  
  - Efficient indexing strategies to support large-scale text queries.  
- Use **SQLAlchemy** or **Pydantic** for ORM-based database interactions.  

### **3. Infrastructure as Code (IaC) & Deployment**  

- Write a **Terraform** script to provision:  
  - A **cloud storage bucket** (AWS S3 or GCP Cloud Storage) for raw and processed text.  
  - A **PostgreSQL database** (AWS RDS or GCP Cloud SQL).  
- Dockerize the pipeline with a **Dockerfile** to ensure reproducibility.  

### **4. Advanced Data Quality Checks**  

- Implement **automated validation rules**, including:  
  - Rejecting text with **>30% non-alphanumeric content**.  
  - Flagging **potentially sensitive information** (e.g., email addresses, phone numbers).  
  - Checking for **data duplication** across different sources.  

---

## **Collaboration Rules**  

- You may use AI text editors like Cursor, Windsurf, Trae, etc. for **boilerplate code** (e.g., Terraform/Docker setup).  
- Core **data-cleaning logic, database design, and validation rules** must be your own work.  
- Add **clear comments** explaining the rationale behind major design choices.  

---

## **Deliverables**  

1. **GitHub repository** containing:  
   - Python data pipeline code.  
   - Terraform scripts + Dockerfile.  
   - Sample text dataset (or script to generate mock data).  
2. **README.md** with:  
   - Pipeline architecture diagram.  
   - Deployment instructions.  
   - **Data quality report** (e.g., % filtered data, error logs).  

---

## **Bonus (Optional, for extra points)**  

1. Implement an **Airflow DAG** for scheduled pipeline runs.  
2. Add a **data validation step** using Great Expectations or Pandas Profiling.  
3. Optimize database queries for **full-text search** (e.g., using `GIN` indexes).  
4. Deploy a **basic Streamlit dashboard** to visualize dataset statistics.  

---

## **Evaluation Criteria**  

- **Data Processing**: Cleaned text meets quality standards.  
- **SQL & Performance**: Efficient schema & indexing strategies.  
- **IaC & Deployment**: Terraform scripts are modular & reusable.  
- **Code Reproducibility**: Docker setup works without issues.  
