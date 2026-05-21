# Week 4 Day 1-2: HTTP Traffic Analysis with WireShark

**Objective**
Analyze `http.cap` from Wireshark Sample Captures to identify the HTTP GET requests, domain, IP address, and file requested by the client.

**Findings**
- HTTP GET request for `/download.html` sent to `www.ethereal.com`
- Server IP resolved to `216.239.59.99` via DNS
- Server response: `HTTP/1.1 200 OK`, `Content-Type: text/html`, `Content-Length:1870`
- Traffic filtered using `ip.addr == 216.239.59.99`

![HTTP Filter Evidence](./screenshots/wireshark/http_filter.png)

**Analysis**
The client performed a DNS lookup for `www.ethereal.com`, received IP `216.239.59.99`, then sent an HTTP GET request for `/download.html`. The server responded with status 200 OK, indicating the file was successfully retrieved. No errors or suspicious activity observed in this flow.

**IOCs**
- Domain: `www.ethereal.com`
- IP Address: `216.239.59.99`
- Requested Filed: `/download.html`
- Protocol: HTTP/1.1

**Conclusion / Next Steps**
Confirmed normal HTTP traffic to a known domain. Next step is to analyze a malicious PCAP from CyberDefenders to identify suspicious connections and external IPs using filters like `tcp.port == 443 or tcp.port == 4444`.
