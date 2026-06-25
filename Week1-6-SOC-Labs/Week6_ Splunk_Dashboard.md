# Week 6: Splunk SOC Dashboard - Web Attack Detection

**Date:** 2026-06-02  
**Tool:** Splunk Enterprise  
**Dataset:** apache_access_upload logs

### Threats Detected
1. **DoS / Backend Overload**: 264 HTTP 503 errors
2. **Brute Force / Auth Attacks**: 56 HTTP 401 errors  
3. **Peak Time**: 12:20 PM - 80+ errors/minute

### SPL Queries
```spl
// Panel A: Failed requests by status
index=main sourcetype="apache_access_upload"
| rex "\"\s(?<status>\d{3})\s\d+"
| stats count by status
| where status=503 OR status=401

// Panel B: Attack timeline
index=main sourcetype="apache_access_upload" status=503
| timechart span=1m count

![Dashbaord](screenshots/Week6_SOC_Dashbaord.png)
