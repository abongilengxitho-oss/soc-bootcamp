## Day 10: Incident Timeline Reconstruction

**Case**: Suspected SSH Brute Force + Log Tampering
**Environment**: Ubuntu 22.04 WSL2
**Analyst**: SOC Bootcamp Day 10

### Timeline of Events
| Time | Event | Evidence | Source |
| --- | --- | --- | --- |
| 2026-05-01 12:14 | Failed SSH login attempt | 192.168.1.100 in auth.log | Day 6 |
| 2026-05-01 13:24 | Sytem kernel errors | ACPI, snapd, WSL DNS errors | Day 7 |
| 2026-05-05 | Log tampering test | auth.log manually wiped | Day8 |
| 2026-05-06 | History check | No deletion commands in bash_history | Day 9 |

### Key Findings
1. **Initial Access Attempt**: Brute force from 192.168.1.100 detected in Day 6
2. **Log Intergrity**: auth.log wipe simulated in Day 8, btmp empty on WSL2
3. **No Cover-up Detected**: Bash histroy clean in Day 9

### SOC Conclusion
No active compromise confirmed. WSL2 does not fully simulate Linux logging for btmp.
In production Linux, correlate auth.log + bash_history for full timeline.
