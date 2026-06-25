## Day 7: Syslog Analysis - Noise vs Signal Filtering

**Date**: 2026-05-05
**OS**: Ubuntu 22.04 WSL2
**Log**: /var/log/syslog

**Key Findings**
1. **System Errors**: Found ACPI and WSL Kernel errors at 2026-05-01T13:24:49
2. **Service Errors**: `snapd` system key comparison error
3. **Network**: WSL getaddrinfo() DNS resolution failed

   **SOC Analysis**
   - No evidence of SSH service crashes or cron persistence in current logs
   - All errors are WSL system-level, not security-related
   - Demonstrates log noise filtering - critical SOC skill

   **Detection Command**
   `grep -i "error\|fail\|crash\|segfault" /var/log/syslog | tail -10

   **Screenshot**: [day7_syslog_noise_evidence.png](screenshots/day7_syslog_noise_evidence.png)
