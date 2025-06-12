# PwC-Switzerland-PowerBI-Virtual-Internship-Journey.
"This repository showcases **end-to-end Power BI projects** based on **realistic business simulations in the telecom industry**, focusing on **call center performance**, **customer retention**, and **Diversity & Inclusion**." •
**Skills:** Power BI, DAX, Power Query, Data Modeling, Data Storytelling & Dashboard Design, Business Intelligence.

I completed the **PwC Switzerland Power BI Virtual Case Experience** on **Forage**, a hands-on internship simulation reflecting **real business scenarios**.  

##  Key Highlights  
- **Designed interactive dashboards**  
- **Improved data visualization**  
- **Supported strategic decision-making**  

##  Skills Mastered  
- **Transforming raw data into meaningful insights**  
- **Analyzing performance metrics**  
- **Crafting impactful data stories**  

###  Power BI didn’t just show me the numbers—it gave me the pen to turn **insights into impact**.  

Now, I’m excited to talk you through each task—sharing the **insights, challenges, and learnings** I gained along the way.  

**Let’s dive in!**   

# [ Task 1: Call Centre Trend in PhoneNow Company ] --->

As part of this task, I was assigned to build a **detailed and insightful Power BI dashboard** for **PhoneNow**, a leading telecommunications company.  

##  Goal  
Provide managers with a **clear visual understanding** of key **call centre trends** through **effective and intuitive data visualization**.  

##  Key Focus Areas  
- **Monitoring call volumes**  
- **Evaluating agent efficiency**  
- **Tracking customer satisfaction**  

The dashboard was designed to deliver **meaningful and actionable insights**, with an emphasis on **simplicity, clarity, and supporting fast, data-driven decisions**.  

###  Task Brief  
Here’s the **task brief** I received via email:
![Pwc Task 1  mails 1 image](https://github.com/user-attachments/assets/8149436e-6a53-4f82-a2bc-b86d54528ffb)


##  KPI Analysis for Task 1  

As highlighted in the **task email**, I was required to reflect **all key performance indicators (KPIs)** from the dataset. After **analyzing the data**, I identified the **most relevant KPIs** for this dashboard, including:  

###  Key Performance Indicators (KPIs)  
- **Total number of calls**  
- **Answered Calls and Abandoned Calls**  
- **Resolved Calls**  
- **Average speed of answer**  
- **Length of calls (duration)**  
- **Overall customer satisfaction rating**  

###  My Extra Work  
- **Agent Statistics quadrant**  
- **Agents’ call handling efficiency**  
- **Every agent's performance, visualized by charts**  

###  Final Dashboard Preview  
And here’s a **quick view of my final dashboard for Task 1**:
![pwc task 1 Call Centre Dashboard image](https://github.com/user-attachments/assets/ca6916d0-65c0-474f-a18e-e8ed85e99c2b)

##  Dashboard Overview  

I completed all the required tasks and ensured the dashboard remained **simple and user-friendly**, especially for managers.  

###  Key Features  
- **Filters on the left** for easy data exploration and quick decision-making.  
- Enables **agents to track their own performance** efficiently.  

##  Insights from the Dashboard  
- **Total Calls Handled:** 5,000  
- **Abandonment Rate:** 18.92% _(needs urgent attention)_  
- **Average Customer Satisfaction Score:** 3.40 _(reflects mixed feedback)_  
- **Issues Resolved:** 73% _(indicating a need for faster call handling)_  

---

##  Step 1: Import and Transform Data  

Before loading data into **Power BI**, I used **Power Query** for **data cleaning and preparation**, ensuring:  
- Removal of unnecessary columns and rows.  
- Verification of data types.  
- Readiness of all fields for analysis.  

This step was **crucial for reliable and accurate insights**. 

##  Step 2: Enhance Columns with DAX  

Many columns contained **binary or unclear values**, making interpretation difficult. To resolve this, I created **calculated columns using DAX** to replace them with **descriptive labels**, making the data more accessible for **managers and analysts**.  

###  Example DAX Transformations  
```DAX
Total Calls = COUNT(Sheet1[Call Id])  
Answered = CALCULATE(COUNT(Sheet1[Call Id]), FILTER(Sheet1, Sheet1[Answered (Y/N)]="Y"))  
Resolved (Y) = CALCULATE(COUNT(Sheet1[Call Id]), FILTER(Sheet1, Sheet1[Resolved]="Y"))  
Avg. Calls Resolved = Sheet1[Resolved (Y)] / Sheet1[Total Calls] * 100  
Abandoned (Not answered) = CALCULATE(Sheet1[Total Calls] - Sheet1[Answered])  
Call Length 📞 = AVERAGE(Sheet1[AvgTalkDuration]) * 24 * 60  

// OR  
Avg. Length of call 📞 (M) = MINUTE(Sheet1[AvgTalkDuration]) + SECOND(Sheet1[AvgTalkDuration]) / 60 
```

##  Step 3: Data Visualization  

Using **Microsoft Power BI Desktop**, I designed a **dashboard** focused on key **KPIs**, ensuring clarity and actionable insights.  

###  Key Metrics Displayed  
- **Total calls**, **answered calls**, **resolved calls**, and **abandoned calls**  
- **Average calls resolved**  
- **Average speed of answer (seconds)**  
- **Call length (minutes)**  
- **Overall customer satisfaction**  
- **Agents' call handling efficiency**  
- **Agent Statistics quadrant**  
- **Every agent's performance visualized by charts**  

---

##  Step 4: Data Analysis with Measures  

I developed **DAX measures** to calculate **critical metrics**, enabling clear **visual insights** on the dashboard.  

###  Key DAX Measures  
- **Percentage of calls answered**  
- **Total calls answered vs. missed (Abandoned)**  
- **Issues resolved**  
- **Length of calls**  

These measures helped structure the data for **actionable insights** and **efficient decision-making**.  

##  Key Insights from Dashboard  

- **Average Satisfaction Rating:** 3.40  
- **Total Calls:** 5,000  
- **Total Calls Answered:** 4,054  
- **Issues Resolved:** 3,646  
- **Abandoned Calls:** 946  
- **Average Call Duration:** 3.75 minutes  
- **Fastest Average Speed of Answer:** 67.52 seconds  

###  Agent Performance  
- **Top Performer:** Jim, with **536 calls answered**  
- **Lowest Calls Answered:** Stewart, with **477 calls**  
- **Most Rated Agent:** Martha, **3.47 rating**  


##  Dashboard Design  

I designed the dashboard with a **clean color palette** from **COLORS website** and applied **creative visualization** to ensure clarity and ease of interpretation.  
This dashboard doesn’t just **display data**—it **tells the story** of call center performance in a clear and meaningful way.

I hope this gives you a **clear idea of my process and results**. Now, **let’s move on to the second task!** 

---
---



# [ Task 2: Customer Retention Dashboard (Step-by-Step Explanation) ] --->

##  Problem Statement  

A few weeks after presenting the **previous dashboard**, I was contacted directly by the **Retention Manager** of the telecom company.  

They appreciated my **previous report** and said:
![Pwc Task 2 mail 2](https://github.com/user-attachments/assets/4b2665b5-b577-4bc7-8acc-03c5beaa5c3f)

			
				
##  Problem Statement  

> “It’s difficult to acquire customers—we don’t want to lose them.”  

> “Currently, we reach out to customers only after they terminate their contracts — which is a reactionary approach.”  

> “We want to identify at-risk customers in advance, so we can proactively engage them.”  

> “Our Excel-based analysis hasn’t yielded meaningful insights.”  

> “We need a dashboard that is clear, visual, and management-friendly.”  

---

##  Objectives  

The **PwC Engagement Partner** outlined three **key responsibilities** for me:  

1. **Define the most important KPIs** related to customer retention.  
2. **Build an interactive, insight-driven dashboard** using **Power BI**.  
3. **Write a short email/report** summarizing **key insights and actionable recommendations**.  

##  Step-by-Step Work I Performed   

###  Step 1: Uploading the Dataset  
The dataset was provided by the **PwC Switzerland Virtual Internship**.  

 **Dataset Overview:**  
- **Total Rows:** 7,043  
- **Total Columns:** 23  
- Included **customer demographics, account info, services, and churn status**.  

---

###  Step 2: Data Cleaning (In Power Query)  
The dataset was loaded into **Power BI Desktop** and refined through **Power Query**.  

 **Fixed incorrect data types** _(e.g., text instead of number)_  
 **Removed null values and redundant rows**  
 **Cleaned and structured the dataset for analysis**  

---

###  Step 3: Data Transformation & Modelling  
 **Organized Data Structure:**  
- **Primary table:** ‘01 Churn-Dataset’ _(cleaned and prepared data)_  
- **Separate table:** ‘All Measures’ _(managed all KPIs and DAX measures)_  

---

##  Step 4: DAX Measures (KPIs & Feature-Level Analysis)  
To make the dashboard **smart and dynamic**, I created the following **important DAX Measures**: 
![Pwc Task 2 measure image](https://github.com/user-attachments/assets/7827b831-477b-4846-a68a-3742f6a12bc1)



##  General KPIs  

```DAX
Average MonthlyCharges = AVERAGE('01 Churn-Dataset'[MonthlyCharges])  
Average TotalCharges = AVERAGE('01 Churn-Dataset'[TotalCharges])  
Churn Count = CALCULATE(COUNT('01 Churn-Dataset'[Churn]), '01 Churn-Dataset'[Churn]="Yes")  
Churn Rate % = DIVIDE(CALCULATE(COUNT('01 Churn-Dataset'[Churn]), '01 Churn-Dataset'[Churn]="Yes"), COUNTROWS('01 Churn-Dataset'))
```
##  Feature-wise Churn Breakdown

```DAX
% Senior Citizen = DIVIDE(CALCULATE(COUNT('01 Churn-Dataset'[SeniorCitizen]),  
'01 Churn-Dataset'[SeniorCitizen]=1, '01 Churn-Dataset'[Churn]="Yes"),  
CALCULATE(COUNT('01 Churn-Dataset'[SeniorCitizen]), '01 Churn-Dataset'[Churn]="Yes"))  

% Partner = DIVIDE(CALCULATE(COUNT('01 Churn-Dataset'[Partner]),  
'01 Churn-Dataset'[Partner]="Yes", '01 Churn-Dataset'[Churn]="Yes"),  
CALCULATE(COUNT('01 Churn-Dataset'[Partner]), '01 Churn-Dataset'[Churn]="Yes"))  

% Dependents = DIVIDE(CALCULATE(COUNT('01 Churn-Dataset'[Dependents]),  
'01 Churn-Dataset'[Dependents]="Yes", '01 Churn-Dataset'[Churn]="Yes"),  
CALCULATE(COUNT('01 Churn-Dataset'[Dependents]), '01 Churn-Dataset'[Churn]="Yes"))  

% Tech Support = DIVIDE(CALCULATE(COUNT('01 Churn-Dataset'[TechSupport]),  
'01 Churn-Dataset'[TechSupport]="Yes", '01 Churn-Dataset'[Churn]="Yes"),  
CALCULATE(COUNT('01 Churn-Dataset'[TechSupport]), '01 Churn-Dataset'[Churn]="Yes"))  

% Device Protection = DIVIDE(CALCULATE(COUNT('01 Churn-Dataset'[DeviceProtection]),  
'01 Churn-Dataset'[DeviceProtection]="Yes", '01 Churn-Dataset'[Churn]="Yes"),  
CALCULATE(COUNT('01 Churn-Dataset'[DeviceProtection]), '01 Churn-Dataset'[Churn]="Yes"))  

% Online Security = DIVIDE(CALCULATE(COUNT('01 Churn-Dataset'[OnlineSecurity]),  
'01 Churn-Dataset'[OnlineSecurity]="Yes", '01 Churn-Dataset'[Churn]="Yes"),  
CALCULATE(COUNT('01 Churn-Dataset'[OnlineSecurity]), '01 Churn-Dataset'[Churn]="Yes"))  

% Phone Services = DIVIDE(CALCULATE(COUNT('01 Churn-Dataset'[PhoneService]),  
'01 Churn-Dataset'[PhoneService]="Yes", '01 Churn-Dataset'[Churn]="Yes"),  
CALCULATE(COUNT('01 Churn-Dataset'[PhoneService]), '01 Churn-Dataset'[Churn]="Yes"))  

% Streaming TV = DIVIDE(CALCULATE(COUNT('01 Churn-Dataset'[StreamingTV]),  
'01 Churn-Dataset'[StreamingTV]="Yes", '01 Churn-Dataset'[Churn]="Yes"),  
CALCULATE(COUNT('01 Churn-Dataset'[StreamingTV]), '01 Churn-Dataset'[Churn]="Yes"))  

% Streaming Movies = DIVIDE(CALCULATE(COUNT('01 Churn-Dataset'[StreamingMovies]),  
'01 Churn-Dataset'[StreamingMovies]="Yes", '01 Churn-Dataset'[Churn]="Yes"),  
CALCULATE(COUNT('01 Churn-Dataset'[StreamingMovies]), '01 Churn-Dataset'[Churn]="Yes"))
```

##  Step 5: Dashboard Visualization (Power BI) 
![Pwc Task 2  Dashboard 1 image (Welcome To PhoneNow)](https://github.com/user-attachments/assets/b04a62a7-7973-4011-95a3-96bd2e2486a9)



The dashboard was divided into three main sections:

![Pwc Task 2  Dashboard 2 image (Churn Dashboard)](https://github.com/user-attachments/assets/b929d1f9-cea0-4cfc-9d1d-3031564f7219)


##  Key Insights from Customer Retention Analysis  


### 1. Demographic Analysis  
- **Gender Distribution:** Male (50.24%), Female (49.76%)  
- **Effect on Churn:**  
  - Higher churn observed in **young, single customers with no dependents**  
  - Lower churn among customers with **dependents or partners**  
  - **Senior citizens** show **lower churn rates** compared to younger groups  

---

### 2. Account & Contract Analysis  
- **Contract Type:** Month-to-month contracts had the **highest churn** _(42%)_  
- **Payment Method:** Highest churn among customers using **Electronic Check** _(57.30%)_  
- **Billing Pattern:** Paperless billing users showed **higher churn rates**  
- **Tenure Effect:** Customers with **tenure <1 year** had a **churn rate of 47.44%**

---

### 3. Services-Based Analysis  
- Customers who did **not opt for Tech Support, Online Security, or Device Protection** showed **higher churn potential**  
- **Highest churn rate among Fiber Optic users** _(69.4%)_  
- **Impact of Services on Churn:**  
   - Streaming TV & Movies  
   - Multiple Lines  
   - Phone Services

     
![Pwc Task 2  Dashboard 3 image (Customer Risk Analysis)](https://github.com/user-attachments/assets/c574d1f1-e2b2-49f7-a7da-e68c9a036788)
     

##  Key Findings (Insights)  

###  High Churn Risk Customers  
- **Customers on month-to-month contracts**  
- **Customers paying via electronic check**  
- **Paperless Billing users**  
- **Those without Tech Support / Security / Device Protection**  
- **Fiber Optic Internet users**  
- **Young, single customers with no dependents**  

###  Low Churn Risk Customers  
- **Customers on 1–2 year contracts**  
- **Senior citizens**  
- **Married / Dependent-having customers**  
- **Auto-payment users (Bank Transfer / Credit Card)**

 
![Pwc Task 2  Dashboard 4 image (Churn Analysis)](https://github.com/user-attachments/assets/6ee8be40-16b1-4769-b475-72be588b1b0b)



##  Actionable Suggestions (Retention Strategy)  

| **Action Item**          | **Recommendation**  
|--------------------------|--------------------------------------------|  
| - **Longer Contracts**   | Month-to-month से **3 या 6 months** पर switch कराना |  
| - **Bundled Services**   | **Tech Support + Protection + Security** combo |  
| - **Targeted Discounts** | Younger / Single users के लिए **loyalty offers** |  
| - **Senior Citizen Benefits** | **Long-term exclusive plans & rewards** |  
| - **Promote Auto-Payments** | **Credit card / Bank transfer** incentives | 



##  Email/Report  
---

**Subject:** Customer Retention Dashboard – Findings & Strategic Suggestions  
-

**Dear [Engagement Partner],**  

As per the assignment, I’ve completed the **customer churn analysis** using **Power BI**.  

###  Key Findings:  
- High churn risk among **monthly contract** and **paperless billing customers**  
- Customers without **Tech Support, Security, or Device Protection** are more likely to leave  
- **Fiber Optic users** show **significantly higher churn rate**  
- **Electronic check payment method** is linked to the **highest churn-related loss**  

###  Suggestions:  
- **Promote longer contracts** (3–6 months)  
- **Bundle Security + Tech Support**  
- **Target single & young segments** with loyalty plans  
- **Reward senior citizens** with exclusive benefits  
- **Push auto-payments** _(reduce manual check churn)_  

The **dashboard is fully interactive and ready for demonstration**.  
I’d be happy to walk you through it.  

Best Regards,  
**NAEEM KHAN**  
(Data Analyst- Virtual Intern, PwC Switzerland)  

##  Conclusion  

In this task, I designed a **data-driven dashboard** tailored to the needs of the **Retention Manager**, focusing not just on **understanding churn** — but also **predicting it**.  
With **Power BI**, the visualization is **clear and insightful**, allowing any **stakeholder** to take **immediate action** just by viewing it.  

**Now, let’s move on to the third task!**   

---
---




#  [ Task 3: Diversity & Inclusion – Completed Step-by-Step ] 

##  Problem Statement  
The goal of this task was to **analyze diversity and inclusion metrics** within the organization, focusing on **key performance indicators (KPIs)** related to:  
- **Hiring**  
- **Promotion**  
- **Performance**  
- **Turnover**  

We aimed to **visualize these KPIs**, **identify root causes** behind slow progress, and **suggest proactive solutions** to **manage retention risks—especially before contract terminations**.  

---

##  Step 1: Data Upload  
- **Dataset Source:** PwC Switzerland  
- **Total Observations:** 500  
- **Total Columns:** 32  
- **Data Coverage:** Gender, region, age, performance, job changes  

---

##  Step 2: Data Cleaning  

Data cleaning was done using **Power Query in Power BI Desktop**, ensuring:  
- Corrected **data types** for each column  
- Removed **irrelevant rows**  
- Filtered out **unnecessary or null entries**  
- **Core table used:** Diversity and Inclusion  

---

##  Step 3: Data Transformation & Modeling  

###  Data Transformation  
- **Unnecessary columns removed** in Power Query  
- **Validated column data types** for accuracy  
- **Eliminated irrelevant rows**  
- **Applied filters** to retain only relevant records  

###  Data Modeling  
- Created a separate table: **Basic Measures** to store all **key DAX measures** used in the report  

---

##  Gender Distribution – Key DAX Measures  

```DAX
% Female = DIVIDE([# Female], COUNT('Pharma Group AG'[Employee ID]), "NA")  
% Male = DIVIDE([# Male], COUNT('Pharma Group AG'[Employee ID]), "NA")  
```
##  Step 4: Data Visualization – Summary with Key Insights  

Interactive **Power BI dashboards** provided a **comprehensive view** of the company’s **Diversity & Inclusion landscape**.  
> The data was visualized across multiple dimensions:  
- **Department**  
- **Age**  
- **Region**  
- **Gender**  

This approach enabled **clear, data-driven, and inclusive decision-making.** 
![Pwc Task 3 and Dashboard image 1](https://github.com/user-attachments/assets/bca526f1-023f-41aa-9ecc-d3baaf359517)
![Pwc Task 3 and Dashboard image 2](https://github.com/user-attachments/assets/899eecef-811b-4a8b-bb3e-cbea6cdc1a02)
![Pwc Task 3 and Dashboard image 3](https://github.com/user-attachments/assets/47aa8cce-725c-4bfe-b530-10f21e3cfdee)

##  Key Highlights (Human-Centric & Insightful)  

###  Workforce Snapshot  
- **Total Employees:** 500 _(Male: 295, Female: 205)_  
- **FY20 Promotions:** 87  
- **Turnover Rate:** 9.40%  

###  Promotion Trends  
- **Promotion Rate** increased from **7.2% in FY20** to **10.2% in FY21**  
- **Gender-wise promotions:** _Male – 61, Female – 26_  
- **Junior Officer roles** had the **highest promotion rate**, with **approximately 50% female share**  
- **Promotion rates grew across all levels for both genders**    


##  Hiring Insights  

###  Overall Hiring  
- **Male:** 59%  
- **Female:** 41%  

- **Executive hires** were **heavily male-dominated** _(Male: 88%, Female: 13%)_  
- **Junior Officer hiring** favored **females** _(Female: 53%)_  

---

##  Job Role Gender Gap  
- **Female representation decreases** with **seniority**  
- At the **Executive level**, females make up only **15.79%**  

---

##  Performance Ratings  
> **FY20 Average Rating:**  
- **Male:** 2.41  
- **Female:** 2.42  

- Ratings were **fairly balanced** across genders  

---

##  Age Diversity  
- **Most employees** are aged **20–29** _(215 employees)_  
- **Junior Officer roles** are **dominated by younger employees** _(94.67%)_  

---

##  Regional & National Diversity  
- **Top Nationalities:**  
- **Switzerland:** 264  
- **France:** 95  
- **Germany:** 65  

- **Strong European representation** _(Female – 120, Male – 169)_  

---

##  Turnover by Level  
- **Highest Turnover:**  
- **Senior Officer:** 3.67%  
- **Junior Officer:** 3.25%  

- **Executive level had the lowest turnover**  

##  Data Analysis – Measures Used in Visualization 
![Pwc Task 3 measure image](https://github.com/user-attachments/assets/6a1aef47-07f8-46f6-a31e-d99d432a169e)

###  Key DAX Measures  

####  Average Performance Ratings  
```DAX
Average Female Rating = CALCULATE(AVERAGE('Pharma Group AG'[FY20 Performance Rating]),  
FILTER('Pharma Group AG', 'Pharma Group AG'[Gender] = "Female"))
→ Average FY20 rating for female employees


Average Male Rating = CALCULATE(AVERAGE('Pharma Group AG'[FY20 Performance Rating]),  
FILTER('Pharma Group AG', 'Pharma Group AG'[Gender] = "Male")) 
→ Average FY20 rating for male employees


Employee Distribution
# Female = CALCULATE(DISTINCTCOUNT('Pharma Group AG'[Employee ID]),  
FILTER('Pharma Group AG', 'Pharma Group AG'[Gender] = "Female"))  
→ Total unique female employees

# Male = CALCULATE(DISTINCTCOUNT('Pharma Group AG'[Employee ID]),  
FILTER('Pharma Group AG', 'Pharma Group AG'[Gender] = "Male"))  
→ Total male employees

Turnover & Promotions
Turnover Rate = DIVIDE(CALCULATE(COUNT('Pharma Group AG'[FY20 leaver?]),  
FILTER('Pharma Group AG', 'Pharma Group AG'[FY20 leaver?] = "Yes")),  
COUNT('Pharma Group AG'[Employee ID]), "NA")  
→ Percentage of employees who left in FY20

Total Number Promotion = CALCULATE(COUNT('Pharma Group AG'[Promotion in FY20?]),  
FILTER('Pharma Group AG', 'Pharma Group AG'[Promotion in FY20?] = "Y")) +  
CALCULATE(COUNT('Pharma Group AG'[Promotion in FY21?]),  
FILTER('Pharma Group AG', 'Pharma Group AG'[Promotion in FY21?] = "Yes"))  
→ Total promotions in FY20 and FY21

Gender Representation
% Female = DIVIDE([# Female], COUNT('Pharma Group AG'[Employee ID]), "NA")  
→ Percentage of female employees

% Male = DIVIDE([# Male], COUNT('Pharma Group AG'[Employee ID]), "NA")  
→ Percentage of male employees
```

#  Insights & Suggestions – Diversity & Inclusion Summary  

##  1. Gender Balance – Hiring is Good, but Leadership Gap Persists  
- **Overall hiring is balanced** _(Female – 41%, Male – 59%)_  
- **Executive-level female representation** is only **15.79%**  
- **In FY21, no female executive hires**—an urgent focus area  

---

##  2. Promotions Show Growth, but Gender Gap Remains  
- **Promotion rate increased** from **7.2% (FY20) to 10.2% (FY21)**  
- **Only 26 women promoted vs. 61 men**  
- **Most promotions** occurred at **Junior Officer level**, with **~50% female representation**  

---

##  3. Female Representation Drops with Seniority  
- **Junior Officer:** **53.85% Female**  
- **Director Level:** **12.12% Female**  
- **Executive Level:** **15.79% Female**  

---

##  4. Age Diversity is Limited  
- **43% of employees are aged 20–29**  
- **Very few employees aged 40+ in senior roles**  
- **94% of Junior Officer roles** held by **young professionals**  

---

##  5. Regional Diversity Mostly European  
- **Top nationalities:** _Switzerland, France, Germany_  
- **Minimal presence** from **Asia, Africa, and other regions**  

---

##  6. Turnover High at Mid-Levels  
- **Senior Officer turnover highest** at **3.67%**  
- **Junior Officer turnover:** **3.25%**  
- **Executives show strong retention**  

---

##  7. Performance Ratings Fair & Balanced  
- **Male average rating:** 2.41  
- **Female average rating:** 2.42  
- **Most employees scored 2 or 3**  


##  Strategic Suggestions for Growth  

###  Grow Female Leadership  
- Launch **targeted hiring & mentorship** for senior roles  
- Set **KPIs for female leadership representation**  

###  Control Mid-Level Turnover  
- Develop **clear career paths & internal promotion policies**  
- Strengthen **employee feedback mechanisms**  

###  Increase Age Inclusivity  
- Offer **flexible roles** for employees aged **40+**  
- Implement **reverse mentoring & second-career programs**  

###  Expand Global Talent Pool  
- Extend hiring to **Asia, Africa, LATAM**  
- Foster **diverse cultural backgrounds** in the workplace  

###  Transparent Promotion Process  
- Ensure **merit-based, bias-free promotions**  
- Monitor **gender-wise promotion data quarterly**  

###  Proactive Attrition Tracking  
- Build **live Power BI dashboard** to predict turnover risks  
- Launch **early support programs** for low-engagement employees  

---

##  Conclusion  

The company is **progressing well in diversity**, but **meaningful impact** requires **focused efforts** in:  
- **Leadership Diversity**  
- **Equitable Promotions**  
- **Broader Global Outreach**  

This **data-driven approach** forms a **strong foundation** for an **inclusive, future-ready culture**. 



