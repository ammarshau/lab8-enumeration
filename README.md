# Lab Week 8 - Enumeration

## Student Information

| Name | ID |
|------|------|
| Ammar Shauqi bin Nor Amran | 52215125018 |

---

# Challenge 2: Fast Nmap Scan

### Description
This fast scan allows an attacker to quickly identify active services running on the victim machine before conducting deeper enumeration or exploitation.

### Security Impact
- Helps attackers map exposed services rapidly
- Provides an overview of the target system
- Reduces time needed for reconnaissance

---

# Challenge 5: TTL OS Fingerprinting

### Findings
The returned packets showed a **TTL value of 64**, indicating that the target operating system is likely **Linux**.

### Explanation
TTL (Time To Live) values can help identify the operating system of a target host because different OS types use different default TTL values.

| TTL Value | Possible OS |
|---|---|
| 64 | Linux/Unix |
| 128 | Windows |
| 255 | Cisco/Network Devices |

---

# Challenge 7: SMTP VRFY/EXPN

### Description
SMTP enumeration techniques such as `VRFY` and `EXPN` can be used to verify valid usernames on the target mail server.

### Security Impact
- Usernames can be discovered remotely
- Helps attackers perform brute-force attacks
- Assists phishing and credential attacks

---

# Challenge 9: FTP Banner Grabbing

### Findings
- **vsFTPd 2.3.4** was identified on the target system.

### Security Impact
This version is widely known for containing a famous backdoor vulnerability.

### Possible Risks
- Remote unauthorized access
- Exploitation through public exploit frameworks
- Full system compromise

---

# Challenge 10: Anonymous FTP Login

### Findings
The target system allows **Anonymous FTP Logins**.

### Security Impact
This is considered a severe security risk because unauthenticated users may:
- List files
- Download sensitive data
- Potentially upload malicious files

### Risks
- Data leakage
- Malware uploads
- Unauthorized access to internal files

---

# Challenge 12: Enum4linux

### Findings

#### User Enumeration
Successfully retrieved a full list of local system users along with their RIDs.

#### Share Enumeration
Successfully identified exposed Samba shares on the target system.

### Security Impact
- Exposed usernames assist password attacks
- Samba shares may contain sensitive information
- Misconfigured shares can lead to unauthorized access

---

# Challenge 13: NFS Exports

### Findings
The target system exports its root directory (`/`) to all network hosts (`*`).

### Security Impact
This is a critical security vulnerability because attackers can:
- Mount the entire filesystem remotely
- Read sensitive files
- Modify system data
- Gain full system compromise

### Risks
- Unauthorized remote access
- Complete data exposure
- Privilege escalation

---

# Challenge 16: Version Detection

### Findings

| Port | Service |
|---|---|
| 21/tcp | FTP |
| 80/tcp | HTTP |

### Purpose
Version detection helps identify:
- Running services
- Service versions
- Potential vulnerabilities

---

# Challenge 17: OS Detection

### Findings
- **OS Details:** Linux kernel versions `2.6.9 - 2.6.33`

### Security Impact
Older Linux kernel versions may contain known vulnerabilities that attackers can exploit.

---

# Challenge 19: RPC Info

### Findings
Active file-sharing daemons such as:
- `nfs`
- `mountd`

were identified on the target system.

### Security Impact
Attackers can use this information to:
- Discover exposed RPC services
- Perform vulnerability scanning
- Attempt remote exploitation

---

# Conclusion

This lab demonstrated multiple enumeration techniques used during the reconnaissance phase of penetration testing. The identified vulnerabilities, including anonymous FTP access, exposed NFS exports, and outdated services, highlight the importance of proper system hardening and secure service configuration.

---

# Tools Used

- Nmap
- Enum4linux
- FTP
- RPCInfo
- SMTP Enumeration Tools

---

# Thank You

Thank you for reviewing this enumeration lab report.
