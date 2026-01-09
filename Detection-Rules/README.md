### Detection Rules

This phase demonstrates the implementation of security detections within the SOC lab using Wazuh.  
The goal is to identify malicious or suspicious activity across Windows and Linux endpoints.

---

## 1. File Integrity Monitoring (FIM)

### Objective
Detect unauthorized changes to critical system files.

### Configuration
- Linux monitored paths:
  - /etc/passwd
  - /etc/shadow
- Windows monitored path:
  - C:\Windows\System32\drivers\etc\hosts

### Detection Outcome
- File modifications triggered Wazuh alerts
- Alerts were visible on the Wazuh dashboard

### Evidence
*(Screenshot references will be added here)*

---

## 2. Malware / Suspicious File Detection

### Objective
Detect potentially malicious files using hash-based or reputation-based detection.

### Method
- Suspicious file introduced on endpoint
- Wazuh generated alert upon detection

### Detection Outcome
- Alert severity reflected potential malware activity

---

## 3. Windows Security Event Detection

### Objective
Detect suspicious authentication or privilege-related activity on Windows systems.

### Events Monitored
- Failed login attempts
- User account-related events

### Detection Outcome
- Security events successfully ingested and correlated

---

## Summary
This phase validates the SOC lab’s ability to detect file tampering, suspicious binaries, and security-relevant Windows events using Wazuh.
