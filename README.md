# SQL-Snakes-Project-2
# Team Members
1. Quincy Booth @[quincybooth](https://github.com/quincybooth) 
2. Lauren Johnston @[laurenjohnston](https://github.com/laurenjohnston)
3. Jordan Haynes @[jrosehaynes](https://github.com/jrosehaynes)
4. Ella Tedesco @[ellatedesco](https://github.com/ellatedesco)
5. Devin Dickey @[devin-dickey](https://github.com/devin-dickey)
# Problem Description
Our scenario is about creating a database for a healthcare center, like a hospital or clinic, to keep track of everything that goes on with patients, doctors, treatments, bills, and insurance. Think of it as a big system that makes sure all patient info is organized and accessible so that everything runs smoothly without getting lost or messed up. We want to be able to picture any information being inserted into a hospitals database, which includes patient, doctor, and employee information, as well as billing, treatment, and department data. A hospital is one of the busiest places in its community, and with this database, we hope to give more insight and simplify the daily workload.
# Additions to the Data Model 
The main component we added to the data model was the formation of the entity "Appointments". This entity will allow the database to track scheduled interactions between patients and healthcare providers. Because a patient can have many appointments, but an appointment belongs to one patient, we established a one-to-many relationship between the two. The same goes for the HealthCareProvider entity. Lastly, an appointment may consist of many treatments and treatment can occur in many appointments, thus, the two have a many-to-many relationship. 

Additionally, we made some adjustments to the attributes in our pre-existing entities. We added the identifier "startDate" to Patient_Provider and Patient_Insurance due to the fact that a patient may see a provider multiple times, and a patient may decide to leave an insurance plan but can return at a later date. 

Along the same idea, we added the identifier "dateAdministered" to Patient_Treatment because a patient can receive the same treatment on multiple instances, like chemotherapy for example. 

Lastly, we added the following attributes to enhance the accuracy of the data model further

Billing → dueDate
Patients → email, address, allergies
Treatment → type, side effects
Insurance → status 


