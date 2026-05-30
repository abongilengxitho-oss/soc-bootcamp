# Day 6: Splunk Detection Alert - DanaBot C2 Beaconing

**Date:** 2026-04-30  
**Analyst:** Cynthia Ngxitho
**Scenario:** After Day 5 PCAP analysis identified DanaBot C2, create a detection alert in Splunk

### 1. Objective
Build a Splunk SPL query to detect DanaBot command-and-control traffic using IOCs extracted on Day 5:
- C2 Domain: `portfolio.serveirc.com`, `update.serveirc.com`
- C2 IP: `62.173.142.148`
- Endpoint: `/login.php`
- User-Agent: `DanaBot/3.2`

### 2. Evidence Ingested
**File:** `evidence/fake_dns.log`  
**sourcetype:** `danabot_dns`  
**host:** `Mandilakhe_N`  
**source:** `fake_dns.logs`

3 simulated log entries created to mimic DanaBot beaconing:

![Evidence](Day6_DanaBot_DataInput_Splunk.png)
