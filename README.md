# SOC KQL Query Mastery and Data Exploration Lab
<p align="center">

  ![Screenshot 2024-10-09 193938](https://github.com/user-attachments/assets/95bbce84-d8bc-49fd-b45f-039db02caca1)

</p>

In this lab, I took a deep dive into Kusto Query Language (KQL), focusing on writing efficient queries to explore and analyze data within a SOC environment. I practiced using the most common KQL operators to query data from Azure Sentinel and Log Analytics, enhancing my ability to quickly extract actionable insights from large datasets. This hands-on project showcases my growing expertise in KQL for data exploration and security monitoring.




<h2>Environments and Technologies Used</h2>

- Microsoft Log Analytics Workspace
- KQL (Kusto Query Language)

<h2>Operating Systems Used </h2>

- Windows Server 2022
- Windows 10 (21H2)


<h2>KQL Query Examples for Security Log Analysis</h2>
In this section, I used Kusto Query Language (KQL) to analyze security events within my Log Analytics Workspace. I executed queries that filtered security events by EventID 4625 (failed login attempts) and narrowed down the results by targeting specific accounts such as "ADMINISTRATOR." The queries also filtered the data based on recent time frames (e.g., within the last 10 minutes), providing real-time insights into failed login attempts and potential security risks. These examples highlight my ability to write efficient KQL queries to extract actionable security data for monitoring and threat detection.

![Screenshot 2024-10-09 191317](https://github.com/user-attachments/assets/1a7b2442-640f-497e-8e59-4feea0b47d3d)

<h2>KQL Query for Failed Logon Attempts by IP Address</h2>

![Screenshot 2024-10-09 192232](https://github.com/user-attachments/assets/605dd5f7-fdd3-4245-b25f-ba7ec7259285)
This query identifies repeated failed logon attempts on a system, filtering by EventID 4625 (failed login). It specifically tracks failed logins over the past 60 minutes and counts the number of failed attempts by IP address. The query summarizes the data, grouping by Source IP, EventID, and Activity, and flags IPs with 10 or more failed logins. This query is useful for identifying potential brute force attacks or unauthorized access attempts, showcasing my ability to leverage KQL for security monitoring and threat detection in real-time.

<h2>KQL Query for Failed Logins and Attack Analysis</h2>

In this query, I tracked failed logon attempts using EventID 4625, summarizing failures over the past 60 minutes. The query groups the data by Source IP, EventID, and Activity, specifically highlighting IPs with 10 or more failed login attempts. Additionally, the data is projected to identify attacker patterns, such as Source IP and number of failed logins (FailureCount). The second part of the query lists detailed information about each failed logon attempt, including the account name, computer, and event source. This query aids in identifying potential brute force attacks and provides actionable insights for further security investigation.

![Screenshot 2024-10-09 193214](https://github.com/user-attachments/assets/fee61d65-d7f5-4896-9666-f89d7d8e19a7)
