# SOC Lab Setup

This section documents the design and setup of my Security Operations Center (SOC) lab environment.

## Objectives
- Build a realistic SOC lab environment
- Simulate attacks and collect security logs
- Practice detection, alerting, and incident response workflows

## Lab Components
- Kali Linux (attack simulation)
-Wazuh Manager: Ubuntu Server (version)
	•	Wazuh Dashboard: Windows Server 2025
	•	Endpoints:
	•	Windows 11
	•	Windows 10
	•	Windows Server 2019
	•	Windows Server 2022
	•	Windows Server 2025
	•	Ubuntu (endpoint)
- Wazuh SIEM (log collection, correlation, and alerting)
- Virtualization (VMware / VirtualBox)

## Architecture Overview
The lab is designed to simulate an enterprise environment where endpoint logs are forwarded to a SIEM for monitoring and analysis.

## Skills Demonstrated
- SOC architecture design
- Log collection and analysis
- Security monitoring
- Documentation and reporting

-The virtual machines used in this lab were pre-provisioned as part of an existing home lab. This phase focuses on integrating these systems into the SOC environment via Wazuh agent enrollment and validating log ingestion.
