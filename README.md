# SQL-Snakes-Project-2
# Team Members
1. Quincy Booth @[quincybooth](https://github.com/quincybooth) 
2. Lauren Johnston @[laurenjohnston](https://github.com/laurenjohnston)
3. Jordan Haynes @[jrosehaynes](https://github.com/jrosehaynes)
4. Ella Tedesco @[ellatedesco](https://github.com/ellatedesco)
5. Devin Dickey @[devin-dickey](https://github.com/devin-dickey)
# Problem Description
Our scenario is about creating a database for a healthcare center, like a hospital or clinic, to keep track of everything that goes on with patients, doctors, treatments, bills, and insurance. Think of it as a big system that makes sure all patient info is organized and accessible so that everything runs smoothly without getting lost or messed up. We want to be able to picture any information being inserted into a hospitals database, which includes patient, doctor, and employee information, as well as billing, appointment, treatment, and department data. A hospital is one of the busiest places in its community, and with this database, we hope to give more insight and simplify the daily workload.
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

Query 1: This query retrieves detailed information about patients and their associated insurance coverage, including the coverage period, by joining the Patient, Patient_Insurance, and Insurance tables.

Relevance: The query enables hospital managers to monitor patient insurance coverage status effectively, ensuring compliance with billing and eligibility requirements for medical services.


Query 2: The query creates a unified view of appointments, patients, and healthcare providers to simplify access to frequently needed data.

Relevance: The query enhances hospital management by providing a streamlined, comprehensive view of appointments, enabling efficient scheduling, coordination, and decision-making.

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


