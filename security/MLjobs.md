# ML jobs in Elastic Security
 
 
Status 08.03.2022 64 jobs 
 
## [Anomaly Detection with Machine Learning](https://www.elastic.co/guide/en/security/8.0/machine-learning.html) for job requirements:
1. appropriate license (enteprrise or platinum)
 
2. on-prem deployment elasticsearch node with a ML role
[requirements](https://www.elastic.co/guide/en/machine-learning/8.0/setup.html) **_OR_** cloud deployment with ML nodes activated [by custimization](https://www.elastic.co/guide/en/cloud/current/ec-customize-deployment.html)
 
3. two weeks data "ML jobs look back two weeks of historical data prior to the time they are enabled. After jobs are enabled, they continuously analyze incoming data. When jobs are stopped and restarted within the two-week time frame, previously analyzed data is not processed again."
 
## OOTB ML Jobs
### Linux
**Purpose:** Detect suspicious activity using ECS **Linux** events. [Security: Linux](https://www.elastic.co/guide/en/security/8.0/prebuilt-ml-jobs.html#security-linux-jobs)
 
**General Tags** auditbeat, endpoint, linux, security
 
 
| Goal | So what?   | Job Name | Specific Tags|
| ----------- | ----------- |----------- |----------- |
| unusual destination port activity | command-and-control, </br>persistence mechanism, </br> data exfiltration | v2_linux_anomalous_network_port_activity_ecs| network |
| processes unusual to **all** OR  **particular**  Linux hosts | unauthorized services, </br> malware, </br> persistence mechanisms | v2_linux_anomalous_process_all_hosts_ecs </br>v2_rare_process_by_host_linux_ecs | process |
| anomalous access to metadata | unusual process or users </br> harvesting credentials or user data scripts containing secrets  | v2_linux_rare_metadata_process</br>v2_linux_rare_metadata_user| process|
| rare and unusual users that are not normally active may indicate | unauthorized changes </br> or activity by an unauthorized user </br> credentialed access or lateral movement | v2_linux_anomalous_user_name_ecs | process|
 
 
## Theory and Documentation
 
#### What is Elastic Machine Learning?
The type of analysis that you choose depends on the questions or problems you want to address and the type of data you have available.
 
**Unsupervised machine learning (without any prework) for patterns and relationships**
 
Anomaly detection requires _time series data_. It constructs a model and runs to identify unusual events. The model evolves over time.
 
Outlier detection identifies unusual points in a data set by analyzing how close each data point is to others and the density of points around it. It does not run continuously.
 
**Supervised machine learning (needs training data)**
 
Job creates a copy of data set where each data point is annotated with predictions.
 
Classification learns relationships between your data points in order to predict discrete categorical values, such as whether a DNS request originates from a malicious or benign domain.
 
Regression learns relationships between your data points in order to predict continuous numerical values, such as the response time for a web request.

