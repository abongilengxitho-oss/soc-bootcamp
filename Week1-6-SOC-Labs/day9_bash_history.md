## Day 9: Bash History Forensics

**Date**: 2026-05-06
**OS**: Ubuntu 22.04 WSL2

**Detection Command**:
`sudo cat /root/.bash_history | grep -E"> /var/log|history -c|rm

**Findings**:
- No log detection or history clearing commands found in root bash history
- Bash history is clean - no evidence of cover up activity

**SOC Lesson**:
A clean bash history with no `history -c` or `rm /var/log/*` command suggests no attempt to hide activity via bash.

**Screenshot**: [day9_bash_history.png](screeenshots/day9_bash_history.png)
