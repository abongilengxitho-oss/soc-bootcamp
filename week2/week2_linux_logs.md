# Week 2 Day 1: Linux Auth Log Analysis

## Objective
Learn to parse `/var/log/auth.log` to detect SSH brute force attack using native Linux commands.

## Lab Setup
- **OS**: Ubuntu 22.04 LTS via WSL2 on Windows 11
- **User**: root@MandilakheN
- **Date**: 2026-05-01

 ## Commands Used
1. **Verify log location**
 ```bash
   ls /var/log
2. **Generate test data**
  logger -p auth.info "Failed password for root from 192.168.1.100 port 22 ssh2"
  logger -p auth.info "Failed password for root from 192.168.1.100 port 22 ssh2"
  logger -p auth.info "Failed password for admin from 192.168.1.105 port 22 ssh2"
3. **Hunt failed logins
 cat /var/log/auth.log | grep "Failed" | tail -5
4. **Count attacks per source IP**
  cat /var/log/auth.log | grep "Failed" | awk '{print $9}' | sort | uniq -c | sort -nr | head -5
 ## Results
  2 192.168.1.100
  1 192.168.1.105
   ![Evidence](screenshots/week2_day1_auth_log_evidence.png)
