# Security-Monitoring-and-Threat-Detection-Using-Splunk

## Overview: 
This project aimed to create a robust security monitoring environment for a fictional organization using Splunk. The system was tested against simulated attacks, with a focus on analyzing Windows Server and Apache Web Server logs to identify, assess, and respond to potential security threats based on suspicious patterns detected in the log data.

## Tools & Technologies:

  -  **Splunk**: Used as the primary platform for log ingestion, monitoring, and analysis.
  -  **Windows Server Logs**: Analyzed for suspicious changes in severity, failed attempts, successful logins, and account deletions.
  -  **Apache Web Server Logs**: Monitored for HTTP method anomalies, response codes, and international traffic patterns.

## Key Findings:

### Windows Logs Suspicious Activity:
  -  Severity Escalation: Incident severity increased from 329 to 1111 events.
  -  Failed Logins: A spike in failed login attempts on 3/25/2020 led to an adjustment of alert thresholds.
  -  Unusual Successful Logins: Abnormal login activity, especially from "User_j," who logged in 194 times within one hour.

### Web Server Log Analysis:
  -  HTTP POST Surges: POST requests increased from 106 to 1324, suggesting possible data exfiltration or exploitation attempts.
  -  International Traffic: A significantly high volume of traffic from Ukraine (877 counts), divided mostly by two of the largest cities:  Kyiv (440) & Kharkiv (432).
  -  Suspicious URIs: Repeated access to 'VSI_Account_Logon.php' hinted at credential harvesting or brute-force attacks.

### Alert & Dashboard Configurations:
  -  Custom thresholds were tuned to balance sensitivity while minimizing false positives.
  -  Dashboards included time charts, cluster maps, and statistical graphs to visualize suspicious patterns in user behavior and HTTP method usage.

### Analytical Insights:
  -  User Behavior Analysis: Anomalies were detected in user activities, particularly with "User_a" and "User_k," correlating with login attempts and account lockouts.
  -  Signature Analysis: Frequent events like "Account locked out" and "Password reset attempts" were observed during critical periods.
  -  Dynamic Reporting: Highlighted the strengths and trade-offs of using bar graphs, pie charts, and statistical reports for visualizing data.

### Challenges & Adjustments:
  -  Fine-tuning alert thresholds was essential due to the significant spikes during the simulated attacks.
  -  The project emphasized the importance of cross-referencing different log sources and employing varied visualization techniques for a more comprehensive understanding of suspicious activities.

## Project Presentation

You can view the full project presentation on Google Drive:

[View Presentation] (https://docs.google.com/presentation/d/1-7Z_2JT2iIwdQAW4ESyzvhLEmIEFKNPDv64Ei3Km8fk/edit?usp=sharing)
