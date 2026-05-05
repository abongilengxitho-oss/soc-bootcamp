## Day 8: Log Tampering Detection

**Date**: 2026-05-05
**OS**: Ubuntu 22.04 WSL2

**Scenario**: Testing log tempering detection usimg btmp backup logs

**Detection Results**:
 - `sudo lastb | head -5  > `btmp begins Fri May 1 12:14:05 2026` (no entries)
 - **Findings**: No failed login records in btmp WSL2

**SOC Lesson**
WSL2 does not populate btmp by defualt. In a real Linux server, btmp would contain failed logon attempts even if auth.log was wiped. This shows the importance of validating log sources in your environment before relying on them.

**Screenshot**: [day8_lastb_evidence.png](screenshots/day8_lastb_evidence.png)
 
