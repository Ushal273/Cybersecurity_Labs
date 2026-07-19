# Week 5 – Splunk Basics

## Objective
Learn how to use Splunk as a SIEM tool and write basic SPL queries.

---

## What is a SIEM?
A Security Information and Event Management (SIEM) tool collects
logs from all systems across an organisation in one central place.
SOC analysts use it to search, detect and investigate threats.

---

## What is Splunk?
Splunk is one of the most widely used SIEM tools in Australian SOCs.
It ingests log data from multiple sources, indexes it, and allows
analysts to search through it using SPL (Search Processing Language).

---

## Key Splunk Concepts

- Index – Where Splunk stores log data
- Source – Where the log came from
- Sourcetype – The format of the log data
- SPL – Search Processing Language used to query data
- Event – A single log entry in Splunk

---

## Basic SPL Queries Practised

- index=main
- index=main source="WinEventLog"
- stats count by user
- sort -count
- table user, count

---

## Key Takeaways
Splunk is a powerful SIEM tool used by SOC analysts to investigate
security incidents. Writing SPL queries is a core skill for any
blue team analyst role in Australia.
