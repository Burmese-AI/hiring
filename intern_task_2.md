# Internship Task: Financial Transaction Tracker

**Domain:** Personal Finance Management  
**Expected Time:** 8–16 Hours (AI collaboration encouraged)  

---  

## Objective  

Build a **Financial Transaction Tracker** using Django to manage income/expenses and demonstrate numerical accuracy.  

- **Backend/System Design**: Must be **80% your own work** (we’ll assess data integrity choices).  
- **Frontend**: AI use allowed for UI, but you **must understand all logic**.  

---  

## Requirements  

### 1. Transaction Model & Data  

- Define a `Transaction` model with:  
  - `amount` (decimal, e.g., `-150.00` for expenses, `+500.00` for income)  
  - `date` (date field)  
  - `category` (e.g., "Food", "Salary")  
  - `transaction_type` (choices: "income" or "expense")  
  - You may add more fields to the model as you see fit.
- Seed 50–200 mock transactions (include both positive/negative amounts).  

### 2. Frontend Interface  

- **Submission Form**: Users can add transactions (amount, category, type, date).  
- **Transaction Table**: Display entries with columns: `Date`, `Description`, `Amount`, `Category`.  
  - Color-code expenses (red) and income (green) in the `Amount` column.  
- **Basic Filter**: Dropdown to show transactions by category (e.g., "Food" only).  

### 3. Financial Reporting  

- Show **Total Income**, **Total Expenses**, and **Net Balance**.  
- Calculate **Average Monthly Expense** (simple total/number of months).  

### 4. Data Validation  

- Ensure users can’t submit $0 or invalid amounts.  
- Prevent future dates in the `date` field.  

---  

## AI Collaboration Rules  

- **Allowed**:  
  - AI for frontend code (HTML tables, CSS styling, form layouts).  
  - Discussing calculations with AI, but **write final logic yourself**.  
- **Minimum**: 80% of backend (models/views/calculations) must be your code.  
- **Required**:  
  - Comment key numerical logic (e.g., "Net balance = total_income - total_expenses").  
  - Explain your decimal field choices during review.  

---  

## Minimum Deliverables  

1. GitHub repo with:  
   - Django project including the `Transaction` model and seed data.  
   - Functional form + table with filtering.  
   - Accurate financial summaries.  
2. `README.md` with:  
   - Setup instructions.  
   - **AI Usage Report** (list frontend components built with AI).  

---  

## Bonus (Optional)  

1. Add a simple chart (e.g., bar graph of expenses by category) using Plotly or Chart.js.  
2. Export transactions to CSV via a button.  
3. Add monthly budget alerts (e.g., "You’ve spent 80% of your Food budget").  

---  

## Evaluation Criteria  

- **Numerical Accuracy**: Correct totals, averages, and decimal handling.  
- **Data Integrity**: Validation prevents invalid amounts/dates.  
- **Code Quality**: Clean Django patterns (e.g., proper `DecimalField` usage).  
- **AI Explanation**: Can you justify AI-generated UI choices?  

---  

**Why This Task?**  
We prioritize candidates who can **learn while doing** and leverage AI responsibly. This task reflects real-world scenarios where you’ll augment your skills with tools while owning critical logic.  
