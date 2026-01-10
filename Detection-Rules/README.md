# Detection Phase

This phase of the project focuses on **detection**, where security-relevant activity is identified and surfaced by the SIEM.

The goal of this phase is to demonstrate how Wazuh detects suspicious or malicious behavior on endpoints using different detection techniques. Rather than relying on a single signal, multiple detection methods are used to provide better visibility into what is happening on the system.

In this project, detection is demonstrated using:

- **File Integrity Monitoring (FIM)** to detect unauthorized changes to sensitive files
- **Malware detection techniques** to identify potentially malicious files or activity

For File Integrity Monitoring, a sensitive directory on a Windows endpoint was monitored. Files such as `password.txt` and `sensitive files.txt` were created, modified, and deleted to simulate realistic scenarios involving sensitive data. Wazuh successfully detected these actions and generated alerts, showing how integrity violations can be identified in a SOC environment.

This phase establishes the foundation for the next steps of the project. Once detection is confirmed and validated, the detected activity is treated as a security incident in the **Incident Response** phase, followed by deeper analysis during **Threat Hunting**.

The sections below provide detailed breakdowns of each detection technique used in this phase.
