# Healthcare Analytics Dashboard
![Dashboard Image](https://github.com/HimanshuSharma123-a/Healthcare-Analytics-Dashboard/blob/main/Healthcare%20Dashboard%20.png)

## Dataset

You can find the dataset used for this dashboard [here]().

## Overview

This Healthcare Analytics Dashboard provides a comprehensive overview of various healthcare metrics. It is designed to assist healthcare administrators and professionals in making informed decisions based on the data presented. The dashboard is divided into several sections, each presenting different types of data visualizations and statistics relevant to healthcare management.

## Features

1. **Types of Admission**:
   - A donut chart displays the total number of cases, which is 318,438. The chart is segmented to represent various types of admissions.
   - **Calculation Fields**: 
     - `Admission Count`: COUNT([Admission ID])
     - `Admission Type`: IF [Condition] THEN 'Type 1' ELSE 'Type 2' END

2. **Severity of Illness**:
   - Another donut chart shows the total number of cases (318,438) divided into segments representing different severity levels of illness.
   - **Calculation Fields**: 
     - `Severity Count`: COUNT([Case ID])
     - `Severity Level`: IF [Severity] = 'High' THEN 'High' ELSE 'Low' END

3. **Case by Age**:
   - A bar chart presents the distribution of cases across different age groups. The age groups range from 0-10 to 91-100. The highest number of cases is in the 31-40 and 41-50 age groups, each with around 60K cases.
   - **Calculation Fields**: 
     - `Age Group`: IF [Age] <= 10 THEN '0-10' ELSEIF [Age] <= 20 THEN '11-20' END
     - `Case Count`: COUNT([Case ID])

4. **Case by Length of Stay (LOS)**:
   - An area chart shows the number of cases based on the length of stay in days. The highest number of cases is in the 11-20 days interval, with around 80K cases.
   - **Calculation Fields**: 
     - `LOS Interval`: IF [LOS] <= 10 THEN '0-10' ELSEIF [LOS] <= 20 THEN '11-20' END
     - `Case Count`: COUNT([Case ID])

5. **Department Referral**:
   - This section lists the number of cases referred to different departments:
     - Gynecology: 249,486
     - Anesthesia: 29,649
     - Radiotherapy: 28,516
     - TB & Chest Disease: 9,586
     - Surgery: 1,201
   - **Calculation Fields**:
     - `Referral Count`: COUNT([Case ID])
     - `Department`: [Department]

6. **Average Admission Deposit**:
   - This section shows the average admission deposit, which is $4,881.
   - **Calculation Field**:
     - `Average Deposit`: AVG([Admission Deposit])

7. **Average Available Extra Rooms**:
   - This section indicates the average number of available extra rooms, which is 3,200.
   - **Calculation Field**:
     - `Average Extra Rooms`: AVG([Extra Rooms])

## Insights and Conclusions

This dashboard offers valuable insights into healthcare metrics:
- **Admission Types and Severity**: Identifying the most common types of admissions and severity levels helps in resource allocation and planning.
- **Age Distribution**: Understanding the age groups with the highest number of cases can guide targeted healthcare initiatives.
- **Length of Stay**: Analyzing the length of stay data helps in managing hospital resources effectively.
- **Departmental Referrals**: Knowing the distribution of cases across departments aids in optimizing departmental workloads and improving patient care.
- **Financial Metrics**: The average admission deposit and available extra rooms provide a snapshot of the hospital's financial health and resource availability.

