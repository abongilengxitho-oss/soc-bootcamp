## Week 1: SOC Fundamentals
## SOC Definition:
A Security Operations Centre monitors, detects, investigates and responds to cyber threats 24/7. Tier 1 analysts triage alerts to find real incidents by correlating logs, entwork traffic, and threat intel.
## CIA Triad Examples:
- Confidentiality: Password leak from breach exposes user data
- Integrity: Attacker edits audit logs to hide tracks
- Availibility: Ransomware encrypts file server, stopping business
  ## APT TTP TABLE
  | APT  | ID | TECHNIQUE | LOG SOURCE/ WHY SOC CARES |
  | ---  | ---| ----      | ----|
  |APT 28| T1134| Access Token Manipulation| Windows Event ID 4672: Special privileges assigned to new logon|
  |APT28| T1119 | Automated Collection | Sysmon Event ID 11: File created in temp directories |
  | APT28 | T1547.001| Boot or Logon Autostart:Registry from Run Keys| Windows Event ID 4657: Registry value modified|
  |APT 29 | T1548.002 | Abuse Elevation Control Mechanism: Bypass UAC | Windows Event 4624: Powershell script block logging |
  | APT 29| T1595.002| Active Scanning: Vulnerability Scanning | Zeek conn.log: High rate of outbound SYN to many IPs/ports |
  | APT 29 | T1651| Cloud Admininstration Command | Azure Activity Logs: Invoke-AzVMRunCommand by new user |
  |LAZARUS GROUP| T1098 | Account Manipulation | Windows Event ID 4720 or 4722: Account created/enabled |
  | LAZARUS GROUP |T1622| Debugger Evasion | EDR alerts: IsDebuggerPresent API calls before payload |
  | LAZARUS GROUP | T1140 |Deobfuscate/Decode Files or Information | Sysmon Event ID 7: Image load of powershell.exe with -enc flag|
  ## KILL CHAIN VS ATT&CK
  Kill chain = 7 linear stages of an attack from recon to actions. Att&ck = 200+ specific techniques mapped to real behaviours thats SOCs detect in logd. Kill Chain tells the story. Att&ck gives you the search queries.
