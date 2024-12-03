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




