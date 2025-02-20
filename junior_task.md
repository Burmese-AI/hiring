# **Task: Build a Transaction Audit Dashboard**  

**Domain:** Financial Transaction Auditing  
**Expected Time:** 8–16 Hours (AI collaboration encouraged)  

---

## **Objective**  

Develop a **Transaction Audit Dashboard** using Django and HTMX to display, filter, and approve financial transactions. The focus is on backend logic, data handling, and transactional integrity.  

- **Backend/System Design**: **80% must be your own work** (we’ll assess your decisions).  
- **Frontend**: AI assistance is allowed but you must be able to **explain all AI-generated code** in detail.  

---

## **Requirements**  

### **1. Transaction Model & Data**  

- Define a `Transaction` model with fields:  
  - `amount` (Decimal)  
  - `status` (`pending`, `completed`, `failed`)  
  - `timestamp` (auto-generated)  
  - `merchant` (CharField)  
  - `is_flagged` (Boolean, for compliance review)  
  - `approved_by` (Nullable ForeignKey to `User`, set when approved)  
  - **Bonus**: Track historical changes (e.g., using Django Signals or a history tracking library).  
- Seed **10,000+ transactions** using Django fixtures or a script.  

### **2. Dashboard & Filtering (HTMX encouraged)**  

- Display transactions in a **paginated table** with:  
  - `Merchant`, `Amount`, `Status`, `Flagged`, `Approved By`.  
- Add an **HTMX-powered filter dropdown** for `status`.  
- Implement **search functionality** for filtering transactions by `merchant`.  

### **3. Auditing Actions (HTMX-powered, no page reloads)**  

- **Approve Transactions**:  
  - Add an “Approve” button to set `status="completed"` and assign `approved_by=current_user`.  
- **Flag Transactions**:  
  - Add a “Flag” button to toggle `is_flagged=True`.  

### **4. Reporting & Insights**  

- **Summary Statistics**: Display:  
  - Total transaction amounts per status (`completed`, `pending`, `failed`).  
  - Total transaction amounts per merchant.  
- **Bonus**: Implement **charts** using Plotly or Chart.js for visual insights.  

---

## **AI Collaboration Rules**  

✅ **Allowed**:  

- Full AI assistance for frontend (HTML/CSS/JS/HTMX).  
- AI-generated boilerplate for Django settings, forms, or serializers.  
- Discussing code logic with AI (but you must **write the final implementation**).  

❌ **Not Allowed**:  

- AI writing your transaction model, approval logic, or database queries.  
- Using AI-generated comments without **understanding and explaining them**.  

🔍 **Review Requirement**: You must be prepared to **verbally explain** your backend decisions.  

---

## **Minimum Expected Deliverables**  

1. **GitHub Repository** with:  
   - Django project, seeded transaction data.  
   - HTMX-integrated dashboard.  
   - Basic transaction reporting.  
2. **README.md** with:  
   - Setup instructions.  
   - Explanation of key decisions (e.g., database indexing, approval logic).  

---

## **Bonus (Optional)**  

1. **API Integration**: Expose transaction data via a REST API (Django REST Framework).  
2. **Dockerization**: Add a `Dockerfile` + `docker-compose.yml` for easy deployment.  
3. **Role-Based Access Control (RBAC)**: Restrict approvals to admin users.  
4. **Historical Change Tracking**: Store transaction modifications (e.g., Django Simple History).  
5. **Full-Text Search**: Use PostgreSQL's `GIN` indexes for efficient transaction search.  

---

## **Evaluation Criteria**  

- **Data Handling**: Proper model design, indexing, and efficient queries.  
- **Code Quality**: Clean, modular, and follows Django best practices.  
- **Asynchronous Interactions**: Smooth approval & filtering with HTMX (if used).  
- **System Understanding**: Clear explanations of **backend decisions**.  
- **AI Collaboration**: AI is used **strategically**, not as a crutch.  

---

We value engineers who can **augment their skills with AI** while maintaining deep ownership of architecture and system design. This task reflects our real-world workflows where AI accelerates development but doesn’t replace critical thinking.
