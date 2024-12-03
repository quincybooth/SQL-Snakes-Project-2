# SQL-Snakes-Project-2
# Team Members
1. Quincy Booth @[quincybooth](https://github.com/quincybooth) 
2. Lauren Johnston @[laurenjohnston](https://github.com/laurenjohnston)
3. Jordan Haynes @[jrosehaynes](https://github.com/jrosehaynes)
4. Ella Tedesco @[ellatedesco](https://github.com/ellatedesco)
5. Devin Dickey @[devin-dickey](https://github.com/devin-dickey)
# Problem Description
Our project focuses on designing a database for a healthcare center, like a hospital or clinic, to manage the large amount of information needed to keep everything running smoothly. This database is intended to organize and track patient, doctor, and employee information alongside billing, insurance, appointments, treatments, and departmental data. By streamlining these processes, the database will ensure that critical information is accessible and secure, reducing errors and improving efficiency.

We want this system to store data and help better run hospitals on a daily basis. For example, it should help the hospital monitor patient insurance coverage, analyze provider performance, and create clear summaries of patient billing. Our goal is to simplify the daily workload in a hospital, improve decision-making, and ultimately create a system that benefits both healthcare providers and their patients. By integrating all these elements, we aim to develop a database that supports the fast-paced environment of a hospital while ensuring high-quality care and resource management.

# Additions to the Data Model 
The main component we added to the data model was the formation of the entity "Appointments". This entity will allow the database to track scheduled interactions between patients and healthcare providers. Because a patient can have many appointments, but an appointment belongs to one patient, we established a one-to-many relationship between the two. The same goes for the HealthCareProvider entity. Lastly, an appointment may consist of many treatments and treatment can occur in many appointments, thus, the two have a many-to-many relationship. 

Additionally, we made some adjustments to the attributes in our pre-existing entities. We added the identifier "startDate" to Patient_Provider and Patient_Insurance due to the fact that a patient may see a provider multiple times, and a patient may decide to leave an insurance plan but can return at a later date. 

Along the same idea, we added the identifier "dateAdministered" to Patient_Treatment because a patient can receive the same treatment on multiple instances, like chemotherapy for example. 

Lastly, we added the following attributes to enhance the accuracy of the data model further

Billing: Due Date


Patients: email, address, allergies

Treatment: type, side effects

Insurance: status 

<img width="679" alt="Screenshot 2024-12-02 at 4 51 53 PM" src="https://github.com/user-attachments/assets/b3dc9e09-5d77-42a1-ace7-7e1c9089a666">

# Queries

1. Query 1: This query retrieves detailed information about patients and their associated insurance coverage, including the coverage period, by joining the Patient, Patient_Insurance, and Insurance tables.

![image](https://github.com/user-attachments/assets/281d94bd-7450-4ff4-9411-49739283a5e1)

Managerial Relevance: The query enables hospital managers to monitor patient insurance coverage status effectively, ensuring compliance with billing and eligibility requirements for medical services. This query is important for tracking patient insurance details by linking patients to their insurance plans and coverage periods. By using inner joins, we ensure that only records with matching patient and insurance information are included, which helps maintain accurate and relevant data. This improves efficiency, reduces billing errors, and supports a better experience for both patients and staff.

2. Query 2: The query creates a unified view of appointments, patients, and healthcare providers to simplify access to frequently needed data.

![image](https://github.com/user-attachments/assets/197919fa-2f97-413d-897c-31548216657c)

Managerial Relevance: This query creates a unified view of appointments by joining patient, appointment, and healthcare provider information. By using a view, we can simplify access to key details like appointment status, patient contact info, and provider roles while limiting direct access to sensitive underlying data. When creating this query, we wanted to use a view to ensure that we followed HIPPA guidelines and only allowed people with certain authority to access this data. This approach enhances hospital management by streamlining scheduling and coordination while maintaining great data security.


3. Query 3: This query helps find which doctors perform the most treatments over a certain period of time. We use a stored procedure in order to control data exposure, keeping our data secure.

![image](https://github.com/user-attachments/assets/15c2d604-7aae-42e0-b73e-42f156317e84)

Managerial Relevance: This query provides relevance by distinguishing the healthcare providers who have the highest number of treatments completed. We think that the higher amount of treatments one has provider, the more experienced they are, and therefore they are better at administration. Using a stored procedure helps control data exposure, ensuring sensitive information remains secure while allowing specific analysis. This has managerial relevance because it supports better allocation of the healthcare providers by highlighting experienced providers. 


4. Query 4: This query creates a GetTotalTreatmentCost function which calculates the total cost of all treatments administered to a specific patient, using their patient ID as input.

<img width="503" alt="Screenshot 2024-12-03 at 3 11 11 PM" src="https://github.com/user-attachments/assets/3ced1416-5c1b-49cb-86f4-f789eac40cf7">

Managerial Relevance: This query makes it easy to calculate a patient’s total treatment costs, helping ensure billing is clear and accurate. It’s a simple way for administrators to track expenses and make better financial decisions. By using joins, it connects relevant treatment data while maintaining data integrity, making it a valuable tool for financial management in healthcare.

5. Query 5: This query creates a view, PatientBillingSummary, that provides a comprehensive summary of each patient's billing details, including their name, email, last appointment date, treatments received, total billing amount, and assigned provider, and then retrieves records where the total billing amount exceeds $500.

<img width="883" alt="Screenshot 2024-12-03 at 3 14 47 PM" src="https://github.com/user-attachments/assets/e812802e-1d2a-42cb-b351-bd8f163254bb">
<img width="1047" alt="Screenshot 2024-12-03 at 3 15 13 PM" src="https://github.com/user-attachments/assets/423b52bb-d71b-4538-9128-c73b13c3ecb1">

Managerial Relevance: This query creates a detailed view of each patient’s billing information, including their name, email, last appointment date, treatments received, total billing amount, and assigned provider. By combining data from multiple tables with joins, it consolidates relevant details into one place, making it easier to identify accounts with high billing amounts. This view improves financial oversight, supports better patient communication, and simplifies billing processes by focusing on actionable insights.


# Data Dictionary 
<img width="721" alt="Screenshot 2024-12-02 at 4 57 57 PM" src="https://github.com/user-attachments/assets/68868091-0547-474d-b3a1-fdbac2a23e48">
<img width="720" alt="Screenshot 2024-12-02 at 4 59 02 PM" src="https://github.com/user-attachments/assets/ad9f13d4-20d0-45e5-84c6-f1dcfd15f686">
<img width="718" alt="Screenshot 2024-12-02 at 5 01 35 PM" src="https://github.com/user-attachments/assets/38b95ebb-c4cd-486e-b90f-815aa96a6f56">
<img width="722" alt="Screenshot 2024-12-02 at 11 32 23 PM" src="https://github.com/user-attachments/assets/f8229f93-1677-4707-bbca-c64e8e86ff07">
<img width="721" alt="Screenshot 2024-12-02 at 11 33 18 PM" src="https://github.com/user-attachments/assets/f65951a0-3be9-4f88-8350-9f2553eb6ce2">
<img width="721" alt="Screenshot 2024-12-02 at 11 34 12 PM" src="https://github.com/user-attachments/assets/d9be64df-4634-4346-9d93-714412a14245">
<img width="713" alt="Screenshot 2024-12-02 at 11 36 52 PM" src="https://github.com/user-attachments/assets/b094ba98-b698-4848-bf9d-2f1bf20b0b13">
<img width="717" alt="Screenshot 2024-12-02 at 11 37 22 PM" src="https://github.com/user-attachments/assets/32c73c42-1368-4b9a-b646-6ea3517cf18b">
<img width="716" alt="Screenshot 2024-12-02 at 11 42 49 PM" src="https://github.com/user-attachments/assets/df7cc355-ede7-4a69-9674-4d45fe4b3882">
<img width="715" alt="Screenshot 2024-12-02 at 11 43 38 PM" src="https://github.com/user-attachments/assets/7a897b44-0da7-4a3e-b04f-8cf59796e509">
<img width="715" alt="Screenshot 2024-12-02 at 11 44 12 PM" src="https://github.com/user-attachments/assets/39be5437-0326-409e-abcb-852de480a824">
<img width="714" alt="Screenshot 2024-12-02 at 11 52 40 PM" src="https://github.com/user-attachments/assets/db0d0263-55bb-43df-bf15-8c4234039fab">
<img width="740" alt="Screenshot 2024-12-02 at 11 55 41 PM" src="https://github.com/user-attachments/assets/f3d3068d-9c8c-4b0b-b247-ecd26cdf3ad6">



# Visualizations
                                              Visualization 1
<img width="1058" alt="Screenshot 2024-12-02 at 6 26 47 PM" src="https://github.com/user-attachments/assets/b355a62f-560f-4500-8f5b-bb0b01266579">
Our first visualization aims to attack the question of which treatments carry the most financial burden. Visualizing treatment costs can help track where healthcare expenditures are going, allowing organizations to manage their budgets better and optimize spending. In addition, by visualizing the distribution of treatment costs, patterns can emerge, such as higher-than-expected costs in certain areas, which could signal inefficiencies, overuse of services, or potential fraud.

                                             Visualization 2
<img width="1066" alt="Screenshot 2024-12-02 at 6 27 03 PM" src="https://github.com/user-attachments/assets/2da2e7ec-26fe-4a31-b76e-0aad499289da">
Our second visualization helps in understanding how different age groups and genders are distributed within a patient population. This is critical for health planning, as different age groups and genders often have different healthcare needs. Understanding the age-gender distribution allows healthcare providers to tailor services and resources, ensuring they meet the needs of various patient segments (e.g., pediatric care, women's health, geriatric care). It could reveal health trends or disparities in treatment needs between genders or age groups, which could help in identifying areas for intervention or health awareness campaigns.

                                             Visualization 3

<img width="637" alt="Screenshot 2024-12-02 at 6 26 54 PM" src="https://github.com/user-attachments/assets/6d1ee86b-f78f-4d0f-a7be-745679422293">

Our third visualization aids in visualizing the number of patients per insurance provider. This could prove to be helpful as it allows for easy identification of which providers are most commonly used by patients. This can be valuable for understanding market share, assessing the strength of partnerships, and allocating resources more effectively. Health organizations can identify if certain insurance providers have a larger patient base, which might require more attention, specialized services, or dedicated teams.

                                              Dashboard 
<img width="1005" alt="Screenshot 2024-12-02 at 6 27 53 PM" src="https://github.com/user-attachments/assets/0d09f236-ef26-48db-8e22-746c220b0b97">

# Database Information

