# Week 1: Networking Basics

## OSI Model
7. Application - User apps like chrome, Outlook
6. Presentation - Encryption, JPEG, ASCII
5. Session - Start/stop connections
4. Transport - TCP vs UDP, Port numbers
3. Network - IP addresses, routers
2. Data Link - MAC addresses, switches
1. Physical - Cables, WiFi signals

## Common Ports
| Port | Protocol | Use | Why SOC Cares |
| --- | --- | --- | --- |
| 22 | SSH | Secure remote login | Brute Force T1110 targets this |
| 53 | DNS | Domain name lookup | DNS tunneling for C2 |
| 80 | HTTP | Unencypted web | Malware callback |
| 443 | HTTPS | Encrypted web | Encrypted C2 hides here |
| 445 | SMB | Windows file sharing | Ransomware spreads via this |
| 3389 | RDP | Windows remote desktop | RDP brute force common |
| 25 | SMTP | Send email | Phishing originates here |
| 110 | POP3 | Receive email | Cred harvest from mail |

## TCP 3-Way Handshake
1. Client → SYN → Server: " Can we talk?"
2. Server → SYN/ACK → Client: "Yes, can you hear me?"
3. Client → ACK → Server: "Yes, let's talk"
Connection established. Needed before any data moves.

## TryHackMe
Completed: Pre Security > Network Fundamentals
Key takeaway: Ports tell you what service an attacker is targeting.
