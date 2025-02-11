# Security Monitoring and Threat Detection Using Splunk

## Overview: 
This project aimed to create a robust security monitoring environment for a fictional organization using Splunk. The system was tested against simulated attacks, with a focus on analyzing Windows Server and Apache Web Server logs to identify, assess, and respond to potential security threats based on suspicious patterns detected in the log data.

## Tools & Technologies:

  -  **Splunk**: The primary platform used for log ingestion, monitoring, and analysis.
  -  **Windows Server Logs**: Analyzed to detect suspicious changes in severity, failed login attempts, successful logins, and account deletions.
  -  **Apache Web Server Logs**: Monitored for anomalies in HTTP methods, response codes, and international traffic patterns."

## Key Findings:

### Windows Logs Suspicious Activity:
  -  **Severity Escalation**: A significant increase in incident severity, with events rising from 329 to 1111.
  -  **Failed Logins**: A spike in failed login attempts on 3/25/2020 promped to an adjustment of alert thresholds.
  -  **Unusual Successful Logins**: Notably abnormal login activity from 'User_j,' who logged in 194 times within an hour, raising red flags.

### Web Server Log Analysis:
  -  **HTTP POST Surges**: A dramatic increase in POST requests, from 106 to 1324, suggesting potential data exfiltration or exploit attempts.
  -  **International Traffic**: An unusually high volume of traffic from Ukraine, accounting for 877 counts, with Kyiv (440 counts) and Kharkiv (432 counts) showing significant activity.
  -  **Suspicious URIs**: Repeated access to 'VSI_Account_Logon.php' hinted at credential harvesting or brute-force attacks.

### Alert & Dashboard Configurations:
  -  Custom thresholds were adjusted to balance sensitivity while minimizing false positives.
  -  Dashboards with time charts, cluster maps, and statistical graphs helped visualize suspicious patterns in user behavior and HTTP method usage.

### Analytical Insights:
  -  **User Behavior Analysis**: Anomalies were detected in user activities, particularly with "User_a" and "User_k," correlating with login attempts and account lockouts.
  -  **Signature Analysis**: Frequent events like "Account locked out" and "Password reset attempts" were observed during critical periods.
  -  **Dynamic Reporting**: Highlighted the strengths and trade-offs of using bar graphs, pie charts, and statistical reports for visualizing data.

### Challenges & Adjustments:
  -  Fine-tuning alert thresholds was essential due to the significant spikes during the simulated attacks.
  -  The project emphasized the importance of cross-referencing different log sources and employing varied visualization techniques for a more comprehensive understanding of suspicious activities.

## Project Presentation

You can view the full project presentation on Google Drive here:

[View Presentation](https://docs.google.com/presentation/d/1-7Z_2JT2iIwdQAW4ESyzvhLEmIEFKNPDv64Ei3Km8fk/edit?usp=sharing)

## Log Analysis 

For a in-depth analysis of system activity and security events, including suspicious behavior and potential vulnerabilities, please review the detailed findings in the document available on Google Drive:

[View Log Analysis](https://docs.google.com/document/d/1oIVVlALTcOxZIryWWDuWNsU8Bh-SsbwqBXC_nJ3QSjY/edit?tab=t.0)
