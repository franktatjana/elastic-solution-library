


 # Machine Learning in Elastic Security
 
</br>[Anomaly Detection with Machine Learning](https://www.elastic.co/guide/en/security/8.0/machine-learning.html) 
## Why Machine Learning in Elastic Security? 
-

## Can you give an example?
- Event rates per device (low and high): This was for operational knowledge of how devices are working. The existing logic was only looking for zero events from a device. ML determined that the way users interacted with  systems was significantly different than normal.

- Login volume over VPN: The team had no insight into how the VPN was being used and wanted to see this for licensing, capacity planning. --> results?

- Volume of traffic over VPN -- They wanted to know there were anomalies in the amount of data used over VPN. --> results?
- System and network discovery may be among the initial activities a threat actor engages in. Normal use of these commands is also often too voluminous for conventional search based alerting or data sifting.
These packages look for unusual discovery activity. This approach is much for feasible and scalable then manual hunting by means of searching and sifting vast numbers of events related to discovery commands. 

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


## Advanced analytics with ML in security and logs
If your data is in Elasticsearch, it's ready for machine learning. The Elastic Stack processes data upon ingestion, ensuring that you have the metadata you need to identify root causes or add context to any event.

- Info https://www.elastic.co/what-is/elasticsearch-machine-learning </br>
- Docs https://www.elastic.co/guide/en/security/current/machine-learning.html</br>

- Free Book (incl Screenshots) https://events.elastic.co/machinelearningwithelastic </br>
- Log Catgeories https://www.elastic.co/guide/en/observability/current/categorize-logs.html </br>
- Log Anomalies https://www.elastic.co/guide/en/observability/current/inspect-log-anomalies.html </br>
- Free training https://www.elastic.co/training/elastic-security-fundamentals-siem </br>
- Webinar https://www.elastic.co/videos/training-how-to-series-security </br>
- Free Workshops https://events.elastic.co/emea-workshops-hub-page </br>
- Blogs https://www.elastic.co/blog/author/elastic-security-intelligence-&-analytics-team </br>