# SQL-Snakes-Project-2
# Team Members
1. Quincy Booth @[quincybooth](https://github.com/quincybooth) 
2. Lauren Johnston @[laurenjohnston](https://github.com/laurenjohnston)
3. Jordan Haynes @[jrosehaynes](https://github.com/jrosehaynes)
4. Ella Tedesco @[ellatedesco](https://github.com/ellatedesco)
5. Devin Dickey @[devin-dickey](https://github.com/devin-dickey)
# Problem Description
Our scenario is about creating a database for a healthcare center, like a hospital or clinic, to keep track of everything that goes on with patients, doctors, treatments, bills, and insurance. Think of it as a big system that makes sure all patient info is organized and accessible so that everything runs smoothly without getting lost or messed up. We want to be able to picture any information being inserted into a hospitals database, which includes patient, doctor, and employee information, as well as billing, treatment, and department data. A hospital is one of the busiest places in its community, and with this database, we hope to give more insight and simplify the daily workload.
# Data Model 
Our hospital management data model is designed to illustrate the core operations of a hospital, including patient care, billing, insurance, and healthcare providers. Each entity models an important aspect of hospital operations, and the relationships between these entities help to organize the flow of work throughout the hospital system.
The Department entity represents different areas of the hospital, such as Surgery, Cardiology, or Administration. Each single department has many healthcare providers working within it, so we established a one-to-many relationship between the Department and healthcareprovider entities. The Department table holds attributes like the department ID, name, and location, which are important for identifying where providers work.
