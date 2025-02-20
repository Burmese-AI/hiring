# Internship Task: Build a Data Submission Portal

**Domain:** Training Data Management
**Expected Time:** 8–16 Hours (AI collaboration encouraged)  

---

## Objective

Build a **Data Submission Portal** using Django to collect and manage training data entries.  

- **Backend/System Design**: Must be **80% your own work**.  
- **Frontend**: You may **fully delegate to AI Agents** (e.g., Cursor, Windsurf, Trae, etc.), but you must **understand and able to explain** all generated code.  

---

## Requirements  

1. **Data Model & Mock Data**  
   - Define a `DataEntry` model with fields: `content` (text), `category` (e.g., "text", "image_url"), `is_reviewed` (boolean), and `timestamp`.  
   - You may add more fields to the model as you see fit.
   - Seed 50–100 mock entries via Django admin or a script.  

2. **Frontend Interface**  
   - A form to submit new `DataEntry` instances (plain text or URLs).  
   - Display entries in a table with columns: `Content`, `Category`, `Reviewed?`, `Actions`.  
   - Add a filter to show entries by `category` (e.g., "text" only).  

3. **Basic Review Workflow**  
   - Add a "Mark as Reviewed" button to toggle `is_reviewed` for each entry (HTMX is highly encouraged but optional).  

4. **Simple Reporting**  
   - Show total entries per category (e.g., "Text: 30 entries, Image: 20 entries").  

---

## AI Collaboration Rules  

- **Allowed**:  
  - Full use of AI for frontend code (HTML/CSS/JavaScript).  
  - Discussing logic with AI, but **final code must be reviewed and understood by you**.  
- **Minimum**: 80% of backend/Django logic must be written by you.  
- **Required**:  
  - Add **code comments** (written by you!) explaining AI-generated sections.  
  - Be ready to explain your design choices during review.  

---

## Minimum Expected Deliverables  

1. A GitHub repository containing:  
   - Django project with the `DataEntry` model and seed data.  
   - Functional submission form and data table.  
2. A `README.md` with:  
   - Setup instructions.  
   - A brief **AI Usage Report** (list which parts used AI).  

---

## Bonus (Optional)  

1. Add a search bar to filter entries by keywords in `content`.  
2. Implement basic pagination for the data table.  
3. Use HTMX for everything related to the frontend.

---

## Evaluation Criteria  

- **Functionality**: Form submission, filtering, and review workflow work as described.  
- **Code Quality**: Readable code with Django best practices (e.g., proper models, views).  
- **Learning Agility**: Ability to explain AI-generated code and system design choices.  
- **Documentation**: Clear setup steps and AI usage transparency.  

---

**Why This Task?**  
We prioritize candidates who can **learn while doing** and leverage AI responsibly. This task reflects real-world scenarios where you’ll augment your skills with tools while owning critical logic.  
