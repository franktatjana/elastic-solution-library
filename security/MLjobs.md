# ML jobs in Elastic Security
Status 08.03.2022 64 jobs 
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
 
 
