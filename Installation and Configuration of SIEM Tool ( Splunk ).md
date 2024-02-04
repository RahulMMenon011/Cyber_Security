## Usage of SIEM Tool

* Log Analysis
* Security Investigation
* Log Monitoring and perform Incident Response
* Customized Dashboards can be created to analysis and investigate Logs
* Analyze data through patterns in a Analytical Manner

## Splunk Architecture Components
* Data Collection:

Splunk efficiently gathers data from diverse sources such as servers, network devices, applications, and sensors. This is achieved through the utilization of agents and connectors.

* Data Indexing:

Collected data undergoes indexing and is stored in Splunk's proprietary format. The indexing process involves breaking down data into events, extracting 
fields, and creating an index for each field.

* Search and Analysis:

Splunk boasts a robust search and analysis engine, enabling users to query indexed data using SPL (Splunk Processing Language). Users can perform ad-hoc searches or save them as dashboards and alerts for future reference.

* Visualization:

Splunk provides diverse visualization options, including charts, graphs, and tables. Users can effectively comprehend and analyze their data, with customization options available for tailoring visualizations to specific requirements.

* Deployment Options:

Splunk offers versatile deployment options, supporting on-premises, cloud-based, or hybrid setups. Splunk Enterprise can be deployed as a single instance or as part of a distributed environment with multiple indexers, search heads, and forwarders.

## Advantages:

* Real-time Monitoring: Enables real-time monitoring and analysis of machine-generated data.
* Scalability: Distributed architecture allows horizontal scaling to handle increasing data volumes.
* Can add multiple Plug-ins so we can create our own customized dashboards
* Search Capabilities - Powerful search language (SPL) for complex queries and analytics.
* Large community support and numerous pre-built apps and integrations.

## Disadvantages:

* Licensing costs can be significant for large-scale deployments.
* Setting up and maintaining Splunk in a distributed environment can be complex.
* Requires significant hardware resources, especially for large deployments.
* There should be enough knowledge to work with search queries and other apps so effectively one can resolve the security breaches

## Features:

* Search Processing Language (SPL): Allows complex querying and analysis.
* Customized Dashboards: Enables creation of customizable visualizations and dashboards.
* Machine Learning Toolkit: Allows predictive analytics and anomaly detection.
* Data Ingestion: Supports various data sources and formats (logs, metrics, etc.).
* Security and Compliance: Provides features for securing data and meeting compliance requirements.

## Steps to Install and Configure Splunk

1. First of all install Splunk Enterprise on your host OS can be windows, kali Linux , Mac

![WhatsApp Image 2024-01-07 at 14 26 32_77676aee](https://github.com/RahulMMenon011/Cyber_Security/assets/140642506/64e97afe-9530-4a32-bb7c-5d9043f9fba8)

2. After Installing setup with Username and Password in Splunk Enterprise

![image](https://github.com/RahulMMenon011/Cyber_Security/assets/140642506/7a6c0b07-547e-4934-b376-11d5126f78ba)

3. Go into Settings and Configure the universal forwarder to send data to the Splunk Enterprise indexer by adding a new recieving port as 9997

![image](https://github.com/RahulMMenon011/Cyber_Security/assets/140642506/f19a605e-4954-42c9-867f-4f3fb79cc73a)

4.Now Start Installing Universal Forwarder in the system where you usually attack in my case i have done in kali linux

![WhatsApp Image 2024-01-07 at 13 53 14_603ab970](https://github.com/RahulMMenon011/Cyber_Security/assets/140642506/fcb2d77a-807e-46b7-b0d3-e9c8fc095902)

5. Now start with accepting license and set up username and Password

![image](https://github.com/RahulMMenon011/Cyber_Security/assets/140642506/1640539b-7dd2-4334-bfa3-e28e51cfb309)

6. Now Configure with 2 parameters

* ./splunk add forward-server :9997

* ./splunk set deploy-poll : (This you have to enable on Universal Forwarder where host ipaddress will be of the system on which universal forwarder is downloaded and management port no. you have to specify)

![294746870-5011a370-474d-4ef5-952b-d2f885afa64d](https://github.com/RahulMMenon011/Cyber_Security/assets/140642506/a60797cf-fa15-4429-91aa-29ab814a374f)

7.We have to write a command what to monitor

![image](https://github.com/RahulMMenon011/Cyber_Security/assets/140642506/89d47b89-2644-41ec-8dbc-410eed6bc471)

8.Now restart splunk

![image](https://github.com/RahulMMenon011/Cyber_Security/assets/140642506/85694fea-d670-4edb-a5ef-f26bf2f693e4)

9.Realtime Logs on SIEM Tool:

![image](https://github.com/RahulMMenon011/Cyber_Security/assets/140642506/5b019d49-7949-4fa0-90e2-0121c7235da3)







