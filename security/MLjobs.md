# ML jobs in Elastic Security
Status 08.03.2022 64 jobs 
## Linux
**Purpose:** Detect suspicious activity using ECS **Linux** events. 
**General Tags** auditbeat, endpoint, linux, security</br>
[Security: Linux](https://www.elastic.co/guide/en/security/8.0/prebuilt-ml-jobs.html#security-linux-jobs)</br>
[Security: Auditbeat authentication](https://www.elastic.co/guide/en/security/8.0/prebuilt-ml-jobs.html#security-auditbeat-authentication-jobs)

 
 
| Goal                  | So what?              | Job Name      | Specific Tags, Comments   |
| -----------           | -----------           |-----------    |-----------                |
| An unusual destination port activity | command-and-control </br>persistence mechanism </br> data exfiltration | v2_linux_anomalous_network_port_activity_ecs| network |
| Processes unusual to **all** OR  **particular**  Linux hosts | unauthorized services </br> malware </br> persistence mechanisms | v2_linux_anomalous_process_all_hosts_ecs </br>v2_rare_process_by_host_linux_ecs | process |
| Anomalous access to metadata | unusual process or users </br> harvesting credentials or</br> user data scripts containing secrets  | v2_linux_rare_metadata_process</br>v2_linux_rare_metadata_user| process|
| Rare and unusual users that are not normally active | unauthorized changes </br> or activity by an unauthorized user </br> credentialed access or lateral movement| v2_linux_anomalous_user_name_ecs | process| 
 |  An unusually high number of authentication attempts | -- | suspicious_login_activity_ecs| authentication |
 
</br>

## Security:  authentication
**Purpose:** Detect anomalous activity in your ECS-compatible authentication logs.</br>
**General Tags** authentication, security</br>
[Security: Authentication](https://www.elastic.co/guide/en/security/8.0/prebuilt-ml-jobs.html#security-authentication)</br> 

| Goal                  | So what?              | Job Name      | Specific Tags, Comments   |
| -----------           | -----------           |-----------    |-----------                |
| An unusually large spike in **successful** authentications </br>  (also from a particular source IP address)  | password spraying</br> user enumeration</br> brute force activity| auth_high_count_logon_events</br> auth_high_count_logon_events_for_a_source_ip | -- |
| An unusually large spike in **failed** authentications  | password spraying</br> user enumeration</br> brute force activity</br> account takeover </br> credentialed access |auth_high_count_logon_fails|-- |
| A user logging in at a time of day or source IP address </br> that is unusual for the user| redentialed access via a compromised account </br> when the user and the threat actor are </br> in different time zones or locations| auth_rare_hour_for_a_user</br> auth_rare_source_ip_for_a_user| _An unauthorized user activity often takes place </br> during non-business hours. </br></br>An unusual source IP for a username could be lateral movement </br>  when a compromised account is used to pivot between hosts._| 
| An unusual user name in the authentication logs | credentialed access by means </br>of a new or dormant user account  |auth_rare_user|_An inactive user account becomes active due to</br> credentialed access via a compromised account password.</br></br> Threat actors can create new users as a means of persisting </br> in a compromised web application._ |


