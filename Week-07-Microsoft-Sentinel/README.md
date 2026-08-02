# Week 7 – Microsoft Sentinel

## Objective
Learn how Microsoft Sentinel works as a cloud-based SIEM tool
and how it collects and stores log data.

---

## What is Microsoft Sentinel?
Microsoft Sentinel is a cloud-native SIEM and SOAR platform
built on Azure. It collects logs from across an organisation
and uses analytics rules to detect threats automatically.

---

## How Sentinel Collects Data

### Data Connectors
- Connect log sources to Sentinel
- Supports Microsoft 365, Azure, Windows, Linux and third party tools
- CEF (Common Event Format) is a standard log format used by many security tools

### Log Analytics Workspace
- Where all logs are stored in Sentinel
- Uses KQL to query and search logs
- Retains logs for investigation and compliance

### CEF Logs
- Common Event Format — industry standard log format
- Used by firewalls, IDS/IPS and security appliances
- Connected to Sentinel via a log forwarder

---

## Sentinel vs Splunk

- Splunk uses SPL — Sentinel uses KQL
- Splunk works on-premise or cloud — Sentinel is cloud only
- Both are widely used in Australian SOC environments
- Sentinel integrates natively with Microsoft 365 and Azure

---

## Key Takeaways
Microsoft Sentinel is one of the most in-demand SIEM tools
in Australian SOC environments. Understanding how it collects
data via connectors and stores logs in a workspace is a core
skill for any SOC analyst working in a Microsoft environment.
