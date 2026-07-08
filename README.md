# Sentinel KQL Detection Library

A collection of KQL (Kusto Query Language) detection and hunting queries for Microsoft Sentinel, organized by data source.

## Detections

| Data Source | Description |
|---|---|
| [Entra ID](detections/entra-id/README.md) | Authentication monitoring, suspicious activities, privileged access, account management, conditional access, risky sign-ins, and application/service principal activity. Each query maps to MITRE ATT&CK techniques with severity and false-positive guidance. |
| [Top 20 — Microsoft Ecosystem](detections/top-20-microsoft-ecosystem/README.md) | A curated cross-product set spanning Azure infrastructure, network telemetry, Windows endpoints, Microsoft Defender for Endpoint, Microsoft 365, Defender for Cloud Apps, and Defender for Identity. Includes sample output mockups for each query. |

## Sample Output

Illustrative mockups of query output for all 20 queries in the [Top 20 — Microsoft Ecosystem](detections/top-20-microsoft-ecosystem/README.md) set (fictitious `contoso.com` sample data — not real captures):

#### 01. [Spike in Azure Resource/Role Deletions](detections/top-20-microsoft-ecosystem/kql-queries/01-azure-resource-deletion-spike.kql)
![Spike in Azure Resource/Role Deletions](detections/top-20-microsoft-ecosystem/screenshots/01-azure-resource-deletion-spike.png)

#### 02. [Privileged Role Assignment Outside Business Hours](detections/top-20-microsoft-ecosystem/kql-queries/02-privileged-role-assignment-after-hours.kql)
![Privileged Role Assignment Outside Business Hours](detections/top-20-microsoft-ecosystem/screenshots/02-privileged-role-assignment-after-hours.png)

#### 03. [Anomalous Secret/Key Access Volume](detections/top-20-microsoft-ecosystem/kql-queries/03-keyvault-secret-access-spike.kql)
![Anomalous Secret/Key Access Volume](detections/top-20-microsoft-ecosystem/screenshots/03-keyvault-secret-access-spike.png)

#### 04. [Anonymous/Public Access to Storage Container](detections/top-20-microsoft-ecosystem/kql-queries/04-storage-public-access-exposure.kql)
![Anonymous/Public Access to Storage Container](detections/top-20-microsoft-ecosystem/screenshots/04-storage-public-access-exposure.png)

#### 05. [Brute Force Against Azure SQL Server](detections/top-20-microsoft-ecosystem/kql-queries/05-sql-bruteforce-login.kql)
![Brute Force Against Azure SQL Server](detections/top-20-microsoft-ecosystem/screenshots/05-sql-bruteforce-login.png)

#### 06. [Internal Port Scanning via NSG Flow Logs](detections/top-20-microsoft-ecosystem/kql-queries/06-nsg-internal-port-scan.kql)
![Internal Port Scanning via NSG Flow Logs](detections/top-20-microsoft-ecosystem/screenshots/06-nsg-internal-port-scan.png)

#### 07. [Spike in Denied Outbound Connections](detections/top-20-microsoft-ecosystem/kql-queries/07-firewall-denied-traffic-spike.kql)
![Spike in Denied Outbound Connections](detections/top-20-microsoft-ecosystem/screenshots/07-firewall-denied-traffic-spike.png)

#### 08. [Query to Newly Observed / Malicious Domain](detections/top-20-microsoft-ecosystem/kql-queries/08-dns-malicious-domain-query.kql)
![Query to Newly Observed / Malicious Domain](detections/top-20-microsoft-ecosystem/screenshots/08-dns-malicious-domain-query.png)

#### 09. [Successful Windows Logon After Repeated Failures](detections/top-20-microsoft-ecosystem/kql-queries/09-windows-failed-logon-then-success.kql)
![Successful Windows Logon After Repeated Failures](detections/top-20-microsoft-ecosystem/screenshots/09-windows-failed-logon-then-success.png)

#### 10. [New Member Added to Privileged Group](detections/top-20-microsoft-ecosystem/kql-queries/10-windows-privileged-group-membership-change.kql)
![New Member Added to Privileged Group](detections/top-20-microsoft-ecosystem/screenshots/10-windows-privileged-group-membership-change.png)

#### 11. [Suspicious Encoded PowerShell Command Line](detections/top-20-microsoft-ecosystem/kql-queries/11-windows-encoded-powershell-process.kql)
![Suspicious Encoded PowerShell Command Line](detections/top-20-microsoft-ecosystem/screenshots/11-windows-encoded-powershell-process.png)

#### 12. [Encoded/Obfuscated PowerShell Execution (MDE)](detections/top-20-microsoft-ecosystem/kql-queries/12-mde-encoded-powershell-execution.kql)
![Encoded/Obfuscated PowerShell Execution (MDE)](detections/top-20-microsoft-ecosystem/screenshots/12-mde-encoded-powershell-execution.png)

#### 13. [Rare Outbound Connection to Uncommon Port/IP](detections/top-20-microsoft-ecosystem/kql-queries/13-mde-rare-outbound-connection.kql)
![Rare Outbound Connection to Uncommon Port/IP](detections/top-20-microsoft-ecosystem/screenshots/13-mde-rare-outbound-connection.png)

#### 14. [Mass File Modification Consistent with Ransomware](detections/top-20-microsoft-ecosystem/kql-queries/14-mde-mass-file-modification-ransomware.kql)
![Mass File Modification Consistent with Ransomware](detections/top-20-microsoft-ecosystem/screenshots/14-mde-mass-file-modification-ransomware.png)

#### 15. [Lateral Movement via Multiple Host Logons](detections/top-20-microsoft-ecosystem/kql-queries/15-mde-lateral-movement-multiple-logons.kql)
![Lateral Movement via Multiple Host Logons](detections/top-20-microsoft-ecosystem/screenshots/15-mde-lateral-movement-multiple-logons.png)

#### 16. [Suspicious Inbox Forwarding Rule Creation](detections/top-20-microsoft-ecosystem/kql-queries/16-o365-inbox-forwarding-rule.kql)
![Suspicious Inbox Forwarding Rule Creation](detections/top-20-microsoft-ecosystem/screenshots/16-o365-inbox-forwarding-rule.png)

#### 17. [Mass File Download Consistent with Exfiltration](detections/top-20-microsoft-ecosystem/kql-queries/17-o365-mass-file-download-exfiltration.kql)
![Mass File Download Consistent with Exfiltration](detections/top-20-microsoft-ecosystem/screenshots/17-o365-mass-file-download-exfiltration.png)

#### 18. [External Domain File Sharing Spike (Teams)](detections/top-20-microsoft-ecosystem/kql-queries/18-teams-external-file-sharing-spike.kql)
![External Domain File Sharing Spike (Teams)](detections/top-20-microsoft-ecosystem/screenshots/18-teams-external-file-sharing-spike.png)

#### 19. [Impossible Travel with Mass Download from Cloud App](detections/top-20-microsoft-ecosystem/kql-queries/19-mcas-impossible-travel-mass-download.kql)
![Impossible Travel with Mass Download from Cloud App](detections/top-20-microsoft-ecosystem/screenshots/19-mcas-impossible-travel-mass-download.png)

#### 20. [Suspicious Directory Replication (DCSync) Activity](detections/top-20-microsoft-ecosystem/kql-queries/20-mdi-suspicious-dcsync-activity.kql)
![Suspicious Directory Replication (DCSync) Activity](detections/top-20-microsoft-ecosystem/screenshots/20-mdi-suspicious-dcsync-activity.png)

## Usage

Each data source folder contains:
- A `README.md` describing the queries, their MITRE ATT&CK mappings, and usage guidance.
- A `kql-queries/` folder with the individual `.kql` files, ready to paste into Microsoft Sentinel Logs or use as the basis for scheduled analytics rules.

## License

MIT — see [LICENSE](LICENSE).
