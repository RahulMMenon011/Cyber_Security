### 1. What is splunk ? 
Splunk's software can be used to examine, monitor, and search for machinegenerated
big data through a browser-like interface.

![image](https://github.com/RahulMMenon011/Cyber_Security/assets/140642506/c3482aec-5b64-45e8-873f-a08e65c18917)

### 2. Using splunk web
Splunk web is pre configured environment, there are three pre defined roles in splunk enterprise
a. Admin - Full access b. Power - It will perform real time searches. c. User - user can access own
knowleadge object.

![image](https://github.com/RahulMMenon011/Cyber_Security/assets/140642506/93cb0883-968f-49fa-ba2e-1b06d1565254)

Splunk default lauch environment

![image](https://github.com/RahulMMenon011/Cyber_Security/assets/140642506/7d09e49c-12c6-4652-91c5-d2b199760fd3)

### 3. Using search
Search option is used to search the incident log with time span.
Limiting a search by time is a key to faster result and is a best pratice. Eg. Installing cmatrix inremote VM (Kali) and we can see the installation logs in splunk enterprises.

![image](https://github.com/RahulMMenon011/Cyber_Security/assets/140642506/fd715d87-9adc-469a-a225-226a80eb657c)

Commands that create statics and visualisation are called transforming commands. We can share theshare job log with other user it will remian active for 7 days, and every 10 min we need to refresh thelog search. We can dowload the report in csv,xml,json.

### 4. Exploring Events
If we search the objects in filters by default the event will turn the list, filtered keyword would behighlighted and we can examine the logs with timespan

![image](https://github.com/RahulMMenon011/Cyber_Security/assets/140642506/5afa86a0-2eb9-403a-93fd-28d51b4d72dd)

### 5. Using search term In filters we can use terms of keywords. Eg. fail*, failed, FAILURE

![image](https://github.com/RahulMMenon011/Cyber_Security/assets/140642506/89258c40-c67c-4219-b83b-d54ba9a4e114)

search terms are not case senstive and booleans also we can use Boolean operations have anorder of evaluation a. NOT b. OR c. AND Note: parenthesis () should be used

![image](https://github.com/RahulMMenon011/Cyber_Security/assets/140642506/2fb053b9-31db-4824-8254-96ebcaaf355d)

![image](https://github.com/RahulMMenon011/Cyber_Security/assets/140642506/9a297246-17de-4f11-a1ee-dc547351af9b)

### 6. What are commands ? 
Search splunk language contain 5 component’s a. search term - Foundation of search query. b. commands - Commands is used to customize the log as per the need likecharts, statistics and formatting. c. functions - How we need to display the charts and evaluate theresults. d. arguments - It is the variables which we want to apply in the functions. e. clauses - It willgroup the result as per the requirement.

![image](https://github.com/RahulMMenon011/Cyber_Security/assets/140642506/7b8c25f1-b3e6-4e35-8fbb-6737ccae41a2)

### 7. What are knowledge objects? 
It is tools that help you discover and analyse the data, will begrouped in 5 categories . a.Data Interpretation b.Data classifications c.Data Enrichment d.DataNormalisation e.Data Model Knowleage object is use full for several reasons it can be create byone user and share with other user with permission granted. It is powerful tool for yourdeployment Data Interpretation - Fields

![image](https://github.com/RahulMMenon011/Cyber_Security/assets/140642506/f71c3be8-b7f2-48cb-88dc-4a5b4226c895)

![image](https://github.com/RahulMMenon011/Cyber_Security/assets/140642506/90423da5-217e-4058-9fe2-24d566eb9b77)

### 8. Creating Reports Customize the report using visualization trick and statistics charts

![image](https://github.com/RahulMMenon011/Cyber_Security/assets/140642506/c04de4ca-3e80-46e2-a4f6-1267e4357a21)

### 9. Creating Dashboards Creating new dashboard for User

![image](https://github.com/RahulMMenon011/Cyber_Security/assets/140642506/f29178bf-3cdd-46eb-87ac-73f0e8a0fb03)

### 10. Dashboard Studio Classic Dashboard

![image](https://github.com/RahulMMenon011/Cyber_Security/assets/140642506/c0281d51-6591-4640-a466-586b666e38c4)

