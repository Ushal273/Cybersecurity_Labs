# Week 6 – Splunk Deep Dive

## Objective
Investigate real security incidents using Splunk SIEM and SPL queries.

---

## Labs Completed
- Log Analysis with SIEM (TryHackMe)
- Conti Ransomware Investigation (TryHackMe)

---

## Key SPL Queries Used

### Windows Investigation
- index=task4 ComputerName=WIN-105
- index=task4 ComputerName=WIN-105 EventCode=3 DestinationPort=5678
- index=task4 ComputerName=WIN-105 EventCode=1 Image="C:\\Windows\\Temp\\SharePoInt.exe"
- index=task4 ComputerName=WIN-105 EventCode=1 schtasks

### Linux Investigation
- index=task5 source="auth.log" remote-ssh
- index=task5 source="auth.log" "Accepted password"
- index=task5 source="auth.log" "Failed password" | stats count
- index=task5 sourcetype=syslog ("CRON" OR "cron")

### Web Server Investigation
- index=task6 | stats count by uri_path | sort -count
- index=task6 | stats count by clientip | sort -count
- index=task6 | stats count by useragent | sort -count

### Conti Ransomware Investigation
- index=main EventCode=11 "readme.txt"
- index=main EventCode=8 | table _time, SourceImage, TargetImage
- index=main EventCode=1 Image="c:\\Users\\Administrator\\Documents\\cmd.exe"

---

## Key Windows EventCodes

- EventCode=1 – Process Creation
- EventCode=3 – Network Connection
- EventCode=8 – CreateRemoteThread (Process Injection)
- EventCode=11 – File Created
- EventCode=4624 – Successful Login
- EventCode=4625 – Failed Login

---

## Key Findings from Labs

### Windows Investigation (task4)
- Malicious process: C:\Windows\Temp\SharePoInt.exe
- Connected to IP: 10.10.114.80 on port 5678

### Linux Investigation (task5)
- Brute force SSH attack on ubuntu user
- Python reverse shell persistence via cron on port 7654

### Conti Ransomware Investigation
- Ransomware location: C:\Users\Administrator\Documents\cmd.exe
- Web shell deployed: i3gfPctK1c2x.aspx
- Attacker migrated from powershell.exe to unsecapp.exe
- Credentials dumped via lsass.exe
- CVEs exploited: CVE-2018-13374, CVE-2018-13379, CVE-2020-0796

---

## Key Takeaways
Real SOC investigations require combining multiple SPL queries
across different log sources to build a complete picture of an attack.
Splunk EventCodes and field names are critical for efficient
threat hunting and incident response.
