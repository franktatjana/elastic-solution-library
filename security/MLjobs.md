

# ML jobs in Elastic Security
 
 
Status 08.03.2022 64 jobs 
</br>[Anomaly Detection with Machine Learning](https://www.elastic.co/guide/en/security/8.0/machine-learning.html) 
## Why Machine Learning in Elastic Security? 
- 
## How to start with Anomaly Detection with Machine Learning

1. Deploy elasticsearch cluster [on-prem](https://www.elastic.co/guide/en/machine-learning/8.0/setup.html) or [in cloud](https://www.elastic.co/guide/en/cloud/current/ec-customize-deployment.html).

2. Activate an appropriate license [enteprrise or platinum](https://www.elastic.co/subscriptions). 
 
3. Ingest data with [Agents or Beats](https://www.elastic.co/guide/en/fleet/current/beats-agent-comparison.html).

4. Tune [security priviledges](https://www.elastic.co/guide/en/machine-learning/8.1/setup.html#setup-privileges).  

5. Enable MLs in SIEM top right corner "ML job settings", find ML processes and activate it with one click.

 
## How much data ML needs? 
- You can apply ML from day one, jobs will notify you if there is no enough data.  
- Machine learning jobs look back and analyze two weeks of historical data prior to the time they are enabled. After jobs are enabled, they continuously analyze incoming data. 
- When jobs are stopped and restarted within the two-week time frame, previously analyzed data is not processed again.
## How to choose ML job?
- **available-data approach**: if you ship with auditbeat, packetbeat or winlogbeat check [Prebuilt job reference](https://www.elastic.co/guide/en/security/8.0/prebuilt-ml-jobs.html) 
- **scenario-driven approach**: check tables below with "goal" and "so what" columns and for ECS-compatible logs [Prebuilt job reference](https://www.elastic.co/guide/en/security/8.0/prebuilt-ml-jobs.html) 
- **MITRE-driven approach**: find the tactic, hover over [MITRE Att&ck coverage matrix](https://ela.st/tj-mitre-an) green fields, prefix [ML] points to ML-based detection 

## So what?
1. Check results: 
    - in Host Details and check "Max anomaly score by job" scoring 
    - in Host Data Tables "Anomalies" discovered by machine learning jobs

2. Enable notifications about the anomalies [Generating alerts for anomaly detection jobs](https://www.elastic.co/guide/en/machine-learning/8.1/ml-configuring-alerts.html) 
</br>

# What ready ML jobs are available?
## Linux
**Purpose:** Detect suspicious activity using ECS **Linux** events. 
[Security: Linux](https://www.elastic.co/guide/en/security/8.0/prebuilt-ml-jobs.html#security-linux-jobs)

**General Tags** auditbeat, endpoint, linux, security
 
 
| Goal | So what?   | Job Name | Specific Tags|
| ----------- | ----------- |----------- |----------- |
| unusual destination port activity | command-and-control, </br>persistence mechanism, </br> data exfiltration | v2_linux_anomalous_network_port_activity_ecs| network |
| processes unusual to **all** OR  **particular**  Linux hosts | unauthorized services, </br> malware, </br> persistence mechanisms | v2_linux_anomalous_process_all_hosts_ecs </br>v2_rare_process_by_host_linux_ecs | process |
| anomalous access to metadata | unusual process or users </br> harvesting credentials or user data scripts containing secrets  | v2_linux_rare_metadata_process</br>v2_linux_rare_metadata_user| process|
| rare and unusual users that are not normally active may indicate | unauthorized changes </br> or activity by an unauthorized user </br> credentialed access or lateral movement | v2_linux_anomalous_user_name_ecs | process|
 
 
 
## What is Elastic Machine Learning?

Unsupervised machine learning (without any prework) for patterns and relationships
 
- Anomaly detection requires _time series data_. It constructs a model and runs to identify unusual events. The model evolves over time.
 
- Outlier detection identifies unusual points in a data set by analyzing how close each data point is to others and the density of points around it. It does not run continuously.
 
**Supervised machine learning (needs training data)**
- Classification learns relationships between your data points in order to predict discrete categorical values, such as whether a DNS request originates from a malicious or benign domain.
 
- Regression learns relationships between your data points in order to predict continuous numerical values, such as the response time for a web request.


## Advanced analytics with ML in security and logs
If your data is in Elasticsearch, it's ready for machine learning. The Elastic Stack processes data upon ingestion, ensuring that you have the metadata you need to identify root causes or add context to any event.

Info https://www.elastic.co/what-is/elasticsearch-machine-learning </br>
Docs https://www.elastic.co/guide/en/security/current/machine-learning.html</br>
Free Book (incl Screenshots) https://events.elastic.co/machinelearningwithelastic </br>
Log Catgeories https://www.elastic.co/guide/en/observability/current/categorize-logs.html </br>
Log Anomalies https://www.elastic.co/guide/en/observability/current/inspect-log-anomalies.html </br>
Free training https://www.elastic.co/training/elastic-security-fundamentals-siem </br>
Webinar https://www.elastic.co/videos/training-how-to-series-security </br>
Free Workshops https://events.elastic.co/emea-workshops-hub-page </br>
Blogs https://www.elastic.co/blog/author/elastic-security-intelligence-&-analytics-team </br>