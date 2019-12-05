# CIS
Draft changes from v.1.1.0 to v1.2.0

|  Status |Control #   | Level  |  Scored |  Description | Reasoning |
|---|---|---|---|---|---|
| Added  | 2.2   |  2 | Not Scored  | Ensure that standard pricing tier enabled for PaaS SQL servers  | Same reasoning as 2.1
| Added  |  2.3 | 2  | Not Scored  |  Ensure that standard pricing tier enabled for App Service | Same reasoning as 2.1
| Added  |  2.4 |  2 | Not Scored  | Ensure that standard pricing tier enabled for Storage Accounts  | Same reasoning as 2.1
| Added  |  2.5 | 2  | Not Scored  |  Ensure that Windows Defender ATP (WDATP) integration with Security Center is selected  | WDATP integration brings comprehensive Endpoint Detection and Response (EDR) capabilities within security center. This integration helps to spot abnormalities, detect and respond to advanced attacks on Windows server endpoints monitored by Azure Security Center. Windows Defender ATP in Security Center supports detection on Windows Server 2016, 2012 R2, and 2008 R2 SP1 operating systems in a Standard service subscription.  WDATP works only with Standard Tier subscriptions.
| Added  | 2.6  | 2  | Not Scored   |  Ensure that Microsoft Cloud App Security (MCAS) integration with Security Center is selected |Security Center offers an additional layer of protection by using Azure Resource Manager events, which is considered to be the control plane for Azure. By analyzing the Azure Resource Manager records, Security Center detects unusual or potentially harmful operations in the Azure subscription environment. Several of the preceding analytics are powered by Microsoft Cloud App Security. To benefit from these analytics, subscription must have a Cloud App Security license. MCAS works only with Standard Tier subscriptions.
| Added  | 2.8  | 1  |  Not Scored |  Ensure any of the ASC Default policy setting is not set to "Disabled"  | A security policy defines the desired configuration of your workloads and helps ensure compliance with company or regulatory security requirements. ASC Default policy is associated with every subscription by default. ASC default policy assignment is set of security recommendations based on best practices. Enabling recommendations in ASC default policy ensures that Azure security center provides ability to monitor all of the supported recommendations and allow automated action optionally for few of the supported recommendations
| Added  | 4.2.5  | 2  |  Scored | Ensure that ADS - Vulnerability Assessment (VA) is enabled on a SQL server by setting a Storage Account  | Enabling Advanced Data Security on a SQL server does not enables Vulnerability Assessment capability for individual SQL databases unless storage account is set to store the scanning data and reports.  The Advanced Data Security - Vulnerability Assessment service scans databases for known security vulnerabilities and highlight deviations from best practices, such as misconfigurations, excessive permissions, and unprotected sensitive data. Results of the scan include actionable steps to resolve each issue and provide customized remediation scripts where applicable. Additionally an assessment report can be customized by setting an acceptable baseline for permission configurations, feature configurations, and database settings.
| Added  | 4.2.6  | 2  |  Scored |  Enable ADS - VA Periodic recurring scans for critical SQL servers and corresponding SQL databases. |  VA setting 'Periodic recurring scans' schedules periodic (weekly) vulnerability scanning for the SQL server and corresponding Databases. Periodic and regular vulnerability scanning provides risk visibility based on updated known vulnerability signatures and best practices.
|  Added | 4.2.7  | 2  |  Scored |  Ensure that ADS - VA setting Send scan reports to is configured for a SQL server | ADS - VA scan reports and alerts will be sent to email ids configured at 'Send scan reports to'. This may help in reducing time required for identifying risks and taking corrective measures.
| Added  | 4.2.8  | 2  |  Scored |  Enable ADS - VA setting 'Also send email notifications to admins and subscription owners'. |ADS - VA scan reports and alerts will be sent to admins and subscription owners by enabling setting 'Also send email notifications to admins and subscription owners'. This may help in reducing time required for identifying risks and taking corrective measures.
|  Removed | 2.3  | 1  |Scored  |  Ensure ASC Default policy setting "Monitor System Updates" is not "Disabled" |
|  Removed | 2.4  | 1  |Scored   |  Ensure ASC Default policy setting "Monitor OS Vulnerabilities" is not "Disabled" |
| Removed  | 2.5  | 1  | Scored  |  Ensure ASC Default policy setting "Monitor Endpoint Protection" is not "Disabled"  |
|Removed   | 2.6  | 1  | Scored  |   Ensure ASC Default policy setting "Monitor Disk Encryption" is not "Disabled"|
|  Removed |  2.7 | 1  | Scored  | Ensure ASC Default policy setting "Monitor Network Security Groups" is not "Disabled  |
| Removed  |  2.8 | 1  |  Scored | Ensure ASC Default policy setting "Monitor Web Application Firewall" is not "Disabled  |
| Removed  | 2.9  |1   | Scored  |  Ensure ASC Default policy setting "Enable Next Generation Firewall(NGFW) Monitoring" is not "Disabled" |
|Removed   | 2.10  |  1 | Scored |Ensure ASC Default policy setting "Monitor Vulnerability Assessment" is not "Disabled   | 
|  Removed |2.11   |  1 | Scored  | Ensure ASC Default policy setting "Monitor Storage Blob Encryption" is not "Disabled"  |
|  Removed | 2.12  | 2  |  Scored |Ensure ASC Default policy setting "Monitor JIT Network Access" is not "Disabled"   |
| Removed  | 2.13  | 1  |  Scored |  Ensure ASC Default policy setting "Monitor Adaptive Application Whitelisting" is not "Disabled"  |
| Removed  | 2.14  | 1  | Scored  | Ensure ASC Default policy setting "Monitor SQL Auditing" is not "Disabled"  |
|  Removed | 2.15  |  1 |  Scored | Ensure ASC Default policy setting "Monitor SQL Encryption" is not "Disabled"  |
| Changed  | 2.1  | 2  | Not Scored  |  Ensure that standard pricing tier enabled for Virtual Machines | Language changed to specify VMs and not general services
| Changed  | 2.2  |  1 |  Scored | Ensure that 'Automatic provisioning of monitoring agent' is set to 'On'  | Now benchmark 2.7
|  Changed | 2.16  |  1 |  Scored | Ensure that 'Security contact emails' is set  | Now benchmark 2.9
| Changed  |  2.17 | 1  |  Scored |  Ensure that security contact 'Phone number' is set |Now benchmark 10
| Changed  |  2.18 | 1  | Scored  |  Ensure that 'Send email notification for high severity alerts' is set to 'On | Now benchmark 2.11
| Changed  |  2.19 | 1  |  Scored |  Ensure that 'Send email also to subscription owners' is set to 'On' | Now benchmark 2.12
|  Changed | 4.1  |  1 |  Scored |  Ensure that 'Auditing' is set to 'On'  | Now benchmark 4.1.1 under subcategory "SQL Server Auditing"
|  Changed  | 4.2  | 1  | Scored  |  Ensure that 'AuditActionGroups' in 'auditing' policy for a SQL server is set properly | Now benchmark 4.1.3 under subcategory "SQL Server Auditing"
|Changed   |   4.3|  1 | Scored  | Ensure that 'Auditing' Retention is 'greater than 90 days'  | Now benchmark 4.1.4 under subcategory "SQL Server Auditing"
|  Changed | 4.4  |  2 | Scored  | Ensure that Advanced Data Security (ADS) and Advanced Threat Protection (ATP) on a SQL server is set to 'On'   | Now benchmark 4.2.1 under subcategory "SQL Server ADS".  Recommendation was also renamed to reflect that ATP is now part of ADS
|Changed   |  4.5 |  2 |  Scored | Ensure that ADS - 'Advanced Threat Protection types' (ATP) is set to 'All' | Now benchmark 4.2.2 under subcategory "SQL Server - ADS".  Recommendation was also renamed to incorporate ATP
| Changed  | 4.6  |  2 |  Scored | Ensure that ADS - ATP 'Send alerts to' is set  |Now benchmark 4.2.3 under subcategory "SQL Server - ADS".  Recommendation was also renamed to incorporate ATP.
| Changed  |  4.7 |  2 | Scored  |  Ensure that ADS - ATP 'Email service and co-administrators' is 'Enabled' | Now benchmark 4.2.4 under subcategory "SQL Server - ADS".  Recommendation also renamed to incorporate ATP.
| Changed  | 4.8  | 1  |Scored   | Ensure that Azure Active Directory Admin is configured  | Now benchmark 4.4
|  Changed | 4.9  | 1  | Scored |  Ensure that 'Data encryption' is set to 'On' on a SQL Database' | Now benchmark 4.1.2 under subcategory "SQL Server Auditing"
|  Changed |  4.10 | 2  |  Scored |  Ensure SQL server's TDE protector is encrypted with BYOK (Use your own key) | Now benchmark 4.5
|  Changed | 4.11  |  1 | Scored  |  Ensure 'Enforce SSL connection' is set to 'ENABLED' for MySQL Database Server | Now benchmark 4.3.2 under subcategory "Postgres SQL Database Server"
|   Changed| 4.12  | 1  |  Scored |  Ensure server parameter 'log_checkpoints' is set to 'ON' for PostgreSQL Database Server  | Now benchmark 4.3.4 under subcategory "Postgres SQL Database Server"
| Changed  |  4.13 | 1  | Scored  |  Ensure 'Enforce SSL connection' is set to 'ENABLED' for PostgreSQL Database Server | Now benchmark 4.3.1 under subcategory "Postgres SQL Database Server"
|   Changed|  4.14 |  1 |  Scored |  Ensure server parameter 'log_connections' is set to 'ON' for PostgreSQL Database Server | Now benchmark 4.3.4 under subcategory "Postgres SQL Database Server"
| Changed  |  4.15 |  1 |  Scored | Ensure server parameter 'log_disconnections' is set to 'ON' for PostgreSQL Database Server  | Now benchmark 4.3.5 under subcategory "Postgres SQL Database Server"
| Changed  | 4.16  |  1 | Scored  |  Ensure server parameter 'log_duration' is set to 'ON' for PostgreSQL Database Server |
| Changed  |  4.17 | 1  |  Scored |  Ensure server parameter 'connection_throttling' is set to 'ON' for PostgreSQL Database Server |
| Changed  | 4.18  |  1 |Scored   | Ensure server parameter 'log_retention_days' is greater than 3 days for PostgreSQL Database Server  |
| Changed  | 4.19  |1  |Scored   |  Ensure that Azure Active Directory Admin is configured  |This was mistakenly a duplicate of recommendation 4.8 in v1.1.0 and has been merged into 4.4




