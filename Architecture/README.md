# SOC Lab Architecture – Design Phase

## Purpose
This document describes the design and planning phase of a Security Operations Center (SOC) lab.
The objective is to define the architecture, components, and data flow before implementation.

This lab is designed to simulate real-world SOC monitoring, detection, and response workflows.

---

## Lab Components

### SIEM Server
- Platform: Wazuh (with Elastic stack)
- Role: Central log collection, correlation, and alerting

### Endpoint System
- Platform: Windows Systems + Ubuntu
- Role: Primary log source (authentication, system, and security events)

### Attacker System (Planned)
- Platform: Kali Linux
- Role: Generate controlled attack activity during later phases

### Analyst Workstation
- Role: SOC analyst access to dashboards, alerts, and investigations

---

## Network Design
- All systems will operate within an isolated lab network
- The SIEM server will be reachable by monitored endpoints
- External exposure is not required during initial phases

---

## Log Flow
1. Events are generated on the Windows endpoint
2. Logs are forwarded to the Wazuh SIEM
3. The SIEM analyzes events and applies detection logic
4. Alerts are reviewed by the SOC analyst

---

## Design Goals
- Centralized visibility
- Clear separation of roles
- Safe, controlled testing environment
- Expandability for future attack simulations

---

## Phase Scope
This document represents the **design phase only**.
No systems have been installed, configured, or tested at this stage.

Implementation, attacks, detections, and incident response are covered in later phases.
