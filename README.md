# SOC Analyst Bootcamp - Week 1

Hands-on cybersecurity labs focused on TIER 1 SOC Skills: triage, evidence handling, and documentation. Completed April 2026.

## Objective
Build practical, portfolio-ready proof of core SOC abilities using only free tools and Windows built-ins.

## Skills Demonstrated
- **Digital Forensics**: File integrity and system fundamentals
- **Log Analysis**: Windows Event Log filtering and `.evtx` export
- **Network Security**: Firewall/connection analysis and packet capture basics
- **Documentation**: Clear, recruiter-friendly technical writeups
- **Version Control**: Git/GitHub for evidence tracking

## Labs
### Week 1: Fundamentals
Core cybersecurity concepts and system fundamentals.
**Files**: `week1_fundamental.md`

### Week 1: Networking
Network analysis and Windows Firewall/connection review.
**Files**: `week1_networking.md`

### Week 1: Wireshark
Packet capture and traffic analysis basics.
**Files**: `week1_wireshark.md`
### Week 1: Windows Security Log Analysis
Filtered 27,862 Security events → 396 key events using IDs 4624, 4625, 4688. Exported `.evtx`.
**Files**: `week1_logs.md`, `logs/security_sample.evtx`, `screenshots/`
## Tools Used
`PowerShell`, `Windows Event Viewer`, `Windows Defender Firewall`, `Wireshark`, `Git`, `GitHub`

## Next
Week 2: Linux Incident Response
Hands-on Linux SOC labs using Ubuntu WSL2.

### Week 2 Labs 
### Day 6: SSH Brute Force Detection
- Analyzed /var/log/auth.log for failed SSH attempts
- Identified IOC: 192.168.1.100
- Commands: grep, awk, journalctl

### Day 7: Linux Log Analysis
- Filtered syslog noise vs security signal on WSL2
- Learned: 90% of logs are noise, 10% are signal

### Day 8: Log Tampering Detection
- Tested btmp via lastb as backup when auth.log is wiped
- Validated log source reliability on WSL2

### Day 9: Bash History Forensics
- Checked .bash_history for log deletion commands
- Correlated timeline pags in incident response

### Day 10: Incident Tineline Reconstruction
- Built complete case timeline from Days 6-9
- Documented findings like a real SOC report

### Week 2 Skills Demonstrated
- Linux log analysis: auth.log, syslog, btmp, wtmp, bash_history
- Incident documentation & timeline reconstruction
- Log integrity validation and tampering detection
- Evidence management with
