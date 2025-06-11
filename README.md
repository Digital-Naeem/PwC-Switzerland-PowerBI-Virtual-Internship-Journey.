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

# [ Task 1: Call Centre Trend in PhoneNow Company ] 

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

---

##  Dashboard Design  

I designed the dashboard with a **clean color palette** from **COLORS website** and applied **creative visualization** to ensure clarity and ease of interpretation.  

This dashboard doesn’t just **display data**—it **tells the story** of call center performance in a clear and meaningful way.  

---

I hope this gives you a **clear idea of my process and results**. Now, **let’s move on to the second task!**   



# [ Task 2: Customer Retention Dashboard (Step-by-Step Explanation) ] 

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

**Subject:** Customer Retention Dashboard – Findings & Strategic Suggestions  

---

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


