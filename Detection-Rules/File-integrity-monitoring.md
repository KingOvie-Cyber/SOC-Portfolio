## Detection – File Integrity Monitoring (FIM)

## What is this phase is about ?

This phase focuses on **detection**, using **File Integrity Monitoring (FIM)** in **Wazuh** to identify unauthorized or suspicious changes to sensitive files on a Windows endpoint.

The objective was to confirm that once detection is enabled, **Wazuh** can reliably detect and alert on file creation, modification, and deletion events within a sensitive directory. This represents a common SOC detection use case involving credential files or sensitive user data.

---

## Lab context

- **SIEM:** Wazuh  
- **Wazuh Manager:** Ubuntu Server  
- **Endpoint:** Windows system with Wazuh agent installed  
- **Detection technique:** File Integrity Monitoring (Syscheck)  
- **Configuration approach:** Manual agent-side configuration  

This phase builds on the previous lab setup and agent enrollment phase.

---

## Monitored directory and files

File Integrity Monitoring was configured to monitor the following directory on the Windows endpoint: C:\Users\Windows 10\Sensitive Data

This directory was selected to simulate a realistic location where sensitive user or application data might be stored.

The following files were created and monitored inside this directory:

- `password.txt`
- `sensitive files.txt`

These files were intentionally named to represent sensitive or high-value data.

---

## Detection activity performed

After enabling File Integrity Monitoring and restarting the Wazuh agent, the following actions were carried out inside the monitored directory:

- Creation of new files  
- Addition of content to the files  
- Modification of file contents  
- Deletion of files  

These actions simulate common security scenarios such as insider threats, unauthorized access, or malware tampering with sensitive data.

---

## Detection results

Wazuh successfully detected all file-related activities performed during the test.

The Wazuh dashboard displayed alerts for:

- File added to the system  
- Integrity check triggered due to file modification  
- File deleted from the system  

Each detection event included details such as the affected file path, the type of change, the endpoint involved, and the timestamp of the activity.

---

## Inventory behavior and observations

After the initial baseline scan completed, the monitored files appeared in the **File Integrity Monitoring inventory**. This confirmed that the files were successfully indexed and placed under active monitoring.

An important observation during this phase is that **directories themselves do not appear in the inventory**. Only files that have been scanned and baselined are displayed. Inventory entries are created after files are indexed, not simply when a directory is added to the configuration.

---

## Why this detection matters in a SOC

File Integrity Monitoring is a critical detection capability in a SOC environment. It helps identify:

- Unauthorized changes to sensitive files  
- Possible persistence or tampering attempts  
- Insider threat activity  
- Malware modifying or deleting important data  

This phase demonstrates practical detection skills, including validating alerts, understanding baseline behavior, and correlating endpoint activity with SIEM events.

---

## Key takeaways

- File Integrity Monitoring operates as a detection mechanism within the SOC  
- An initial baseline scan is required before detection events are generated  
- Inventory displays monitored files, not directories  
- File creation, modification, and deletion are all reliably detected once monitoring is active  

---

## Next phase

The next phase of this project will focus on **Incident Response**, where the detected file integrity events will be analyzed, documented, and handled as a simulated security incident.
