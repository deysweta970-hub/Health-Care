# Health-Care Dashboard

# We Care – Hospital Analytics Dashboard
A comprehensive Power BI healthcare analytics dashboard designed to help hospitals monitor patient flow, demographics, and key performance indicators (KPIs).
# 
<a href="https://github.com/deysweta970-hub/Health-Care/commit/c7056891a184618dbeb9d36c6b91573275593715">We Care</a>

# Project Overview

The We Care Healthcare Dashboard provides a comprehensive analysis of patient flow, wait times, demographics, and service efficiency.
This dashboard helps hospital management monitor patient admissions, operational performance, and patient satisfaction to improve healthcare delivery.

# Business Objective

• The objective of this project is to:

• Track patient admissions and visit volume

• Monitor average wait time and service efficiency

• Analyze patient demographics (age, gender, blood group)

• Measure patient satisfaction

• Evaluate whether patients are seen within target wait time

# Dataset Information

• Domain: Healthcare Analytics

• Records: ~5,000 patients

• Time Period: Monthly patient visits

• Key Fields:

• Patient ID

• Admission Status

• Age Group

• Gender

• Blood Group

• Doctor

• Department

• Waiting Time

• Satisfaction Score

• Visit Month

# Tools & Technologies Used

• Excel – Data cleaning and formatting

• Power BI – Data modeling, DAX measures, and dashboard creation
# Dax Formula
• Total Patients = COUNT(Patients[Patient_ID])

• Average Age = AVERAGE(Patients[Age])

• Average Waiting Time =AVERAGE(Patients[Waiting_Time])

• Satisfaction Score = AVERAGE(Patients[Satisfaction_Score])

• Admitted Patients =CALCULATE(
    COUNT(Patients[Patient_ID]),
    Patients[Admission_Status] = "Admitted"
)

• Not Admitted Patients = CALCULATE(
    COUNT(Patients[Patient_ID]),
    Patients[Admission_Status] = "Not Admitted" )

• Age Group = SWITCH(
    TRUE(),
    Patients[Age] <= 9, "0-9",
    Patients[Age] <= 19, "10-19",
    Patients[Age] <= 29, "20-29",
    Patients[Age] <= 39, "30-39",
    Patients[Age] <= 49, "40-49",
    Patients[Age] <= 59, "50-59",
    Patients[Age] <= 69, "60-69",
    "70+" )

   
•  Patients Seen Within 30 Min = CALCULATE(  COUNT(Patients[Patient_ID]),
    Patients[Waiting_Time] <= 30 )
•    Patients by Blood Group = COUNT(Patients[Patient_ID])

# Key KPIs

• Total Patients: 4,999

• Average Age: 39.92 years

• Average Waiting Time: 35.64 minutes

• Patient Satisfaction Score: 4.90 / 5

• These KPIs provide a quick snapshot of overall hospital performance.

#  Dashboard Insights
1 Patient Admission Status

• 90% patients were admitted, indicating high inpatient demand

• A smaller portion of visits were non-admissions, useful for OPD analysis

# Helps management plan bed capacity and resources.

2 Patients by Age Group

• Highest patient volume is observed in adult and senior age groups

• Balanced distribution across age ranges shows diverse healthcare demand

# Supports age-specific treatment and staffing planning.

3 Patients by Blood Group

• Blood groups O+ and A+ have the highest patient count

• Rare blood groups have significantly lower representation

# Useful for blood bank inventory and emergency preparedness.

4 Monthly Patient Trend

• Patient visits increased steadily from January to May

• Slight drop in June, indicating possible seasonal variation

# Helps forecast future patient inflow and staffing needs.

5 Gender Distribution

• Patient visits are almost equally split between male and female

• Indicates balanced access to healthcare services

# Supports gender-inclusive healthcare planning.

6 Patients Seen Within 30 Minutes

• 60% of patients met the target wait time

• 40% exceeded the target, highlighting process improvement areas

•  Helps improve service quality and reduce waiting time.

# Key Business Takeaways

• High patient volume requires efficient operational planning

• Average waiting time can be reduced to improve satisfaction

• Demographic insights help personalize healthcare services

• Performance tracking enables better hospital decision-making
# Dashboard
<img width="773" height="441" alt="We Care" src="https://github.com/user-attachments/assets/ba508372-a91b-4353-b9aa-70914977463c" />
