# PwC-Switzerland-PowerBI-Virtual-Internship-Journey.
"This repository presents end-to-end data analytics projects that address real business challenges in Telecom and HR using Power BI." 
Dashboards include: 📞 Call Center KPIs • 🔁 Customer Churn Prediction • 🌍 Diversity &amp; Inclusion Insights. 
Skills: Power BI, DAX, Power Query, Data Modeling, Data Storytelling, Business Intelligence.

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

#  First Task: Call Centre Trend in PhoneNow Company  

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

