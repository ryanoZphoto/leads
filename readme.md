# Non-Medical Home Care Company Automation Program  
*A budget-friendly system to automate company research, categorization, and contact discovery for Arizona-based senior care providers.*  

---

## **Project Overview**  
**Goal**: Automatically identify, categorize, and extract executive contacts for Arizona non-medical home care companies offering private pay/duty services.  

**Key Features**:  
- Web scraping for company discovery.  
- AI/Keyword-based service categorization.  
- Automated email/LinkedIn contact extraction.  
- Collaboration-friendly workflows.  

**Budget**: $0–$100/month (scalable).  

---

## **Phases & Tools**  

### **Phase 1: Data Collection & Expansion**  
**Objective**: Collect Arizona-based companies from Google Maps, directories, and state databases.  

#### **Tools**  
- **Octoparse** (Free Plan): Scrape Google Maps/Yelp for company data.  
- **Google Sheets** (Free): Store initial data.  
- **Arizona DHS Database** (Free): Cross-reference licensed providers.  

#### **Setup**  
1. Use Octoparse’s [Google Maps Template](https://www.octoparse.com/use-case/how-to-scrape-google-maps) to scrape:  
   - Company Name  
   - Address  
   - Website  
   - Phone  
2. Export results to Google Sheets.  
3. Download [AZDHS Licensed Providers](https://azdhs.gov/licensing/index.php) and merge with your list.  

---

### **Phase 2: Service Categorization**  
**Objective**: Flag companies as **private pay** or **private duty**.  

#### **Tools**  
- **Screaming Frog SEO Spider** (Free Tier): Crawl websites for keywords.  
- **Zapier** (Free Plan): Send templated emails for verification.  

#### **Setup**  
1. Use Screaming Frog to scan company websites for:  
   - “Private pay” → Tag column `Private Pay`.  
   - “Private duty” → Tag column `Private Duty`.  
2. Use Zapier to automate emails:  
   - **Trigger**: New row in Google Sheets.  
   - **Action**: Send email via Gmail/Outlook asking, “Do you offer private pay or private duty services?”  
   - **Reply Handling**: Auto-update Google Sheets with responses.  

---

### **Phase 3: Collaboration & Selection**  
**Objective**: Let rep review and select target companies.  

#### **Tools**  
- **Airtable** (Free Plan): Shared database for team collaboration.  
- **Slack** (Free Plan): Notifications.  

#### **Setup**  
1. Import Google Sheets data into Airtable.  
2. Add columns:  
   - ✅ `Selected` (Checkbox for rep picks).  
   - 📝 `Notes` (Comments from rep).  
3. Use Zapier to send Slack alerts when rep selects companies.  

---

### **Phase 4: Contact Discovery**  
**Objective**: Extract executive emails/phones for selected companies.  

#### **Tools**  
- **Hunter.io** (Free: 25 searches/month): Bulk email lookup.  
- **Phantombuster** ($30/month): LinkedIn scraping for titles (CEO, Owner).  
- **Clay.com** (Free Trial): AI-powered contact enrichment.  

#### **Setup**  
1. **Hunter.io**:  
   - Upload selected company URLs → Export CEO/Founder emails.  
2. **Phantombuster**:  
   - Use [LinkedIn Company Scraper](https://phantombuster.com/linkedin-automations) to extract profiles with titles like “COO” or “CFO.”  
3. **Clay.com**:  
   - Input company domains → Auto-detect leadership contacts.  

---

## **Cost Breakdown**  
| Tool               | Cost (Monthly)   | Use Case                     |  
|--------------------|------------------|------------------------------|  
| Octoparse          | $0 (Free Plan)   | Web scraping                 |  
| Google Sheets      | $0               | Database                     |  
| Zapier             | $0 (100 tasks)   | Automation                   |  
| Hunter.io          | $0 (25 searches) | Email discovery              |  
| Phantombuster      | $30              | LinkedIn scraping            |  
| **Total**          | **$30–$100**     | Scalable with paid upgrades  |  

---

## **Step-by-Step Setup**  
1. **Phase 1**:  
   - Scrape Google Maps with Octoparse → Export to Google Sheets.  
   - Merge with AZDHS data.  
2. **Phase 2**:  
   - Run Screaming Frog on websites → Tag services.  
   - Set up Zapier email automation.  
3. **Phase 3**:  
   - Share Airtable link with rep.  
   - Configure Slack alerts.  
4. **Phase 4**:  
   - Run Hunter.io/Phantombuster on rep’s selections.  

---

## **Example Output**  
**Airtable View**:  
| Company Name       | Service Type  | CEO Email          | Selected |  
|--------------------|---------------|--------------------|----------|  
| Abrio Home Care    | Private Pay   | john@abriocare.com | ✅       |  
| Cypress HomeCare   | Private Duty  | sarah@cypress.com  | ✅       |  

---

## **Troubleshooting**  
- **Duplicates**: Use Airtable’s “Merge Records” tool.  
- **Invalid Emails**: Verify with [EmailChecky](https://emailchecky.com).  
- **Scraping Blocks**: Use Octoparse’s proxy rotation (paid).  

---

## **Legal & Compliance**  
- Respect website `robots.txt` rules.  
- Avoid aggressive scraping (stay under 100 requests/hour).  
- Comply with LinkedIn’s terms when using Phantombuster.  

🚀 **Let’s automate!**  