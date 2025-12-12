# 06. Mitigation Measures 🛡️

This section provides essential strategies to protect systems from  
**EternalBlue (MS17-010)** and similar SMB-based exploits.  
These measures apply not only to Windows 7 but to all systems  
exposing SMB services.

---

## 1. Apply Security Patch (MS17-010) 🔧

The most effective mitigation is installing Microsoft’s official patch.

### Why it matters:
- Fixes the SMBv1 memory corruption bug  
- Prevents remote code execution  
- Blocks EternalBlue exploit completely  

### Action:
✔ Install KB4012212 or KB4012215  
✔ Reboot and verify installation  

---

## 2. Disable SMBv1 Protocol ❌

SMBv1 is outdated and insecure. It should be disabled in all environments.

### Disable via Command Prompt:
dism /online /norestart /disable-feature /featurename:SMB1Protocol

### Why disable SMBv1?
- Vulnerable by design  
- Weak encryption  
- No protection against modern attacks  

---

## 3. Enable Firewall Rules 🔥

Block SMB port access from unauthorized networks.

### Recommended Rule:
Block inbound connections → TCP 445


### Benefits:
- Prevents SMB exploitation  
- Reduces attack surface  
- Stops lateral movement in networks  

---

## 4. Network Segmentation 🧱

Use VLANs or subnet isolation to restrict access to critical systems.

### Segmentation prevents:
- Lateral spread of malware  
- Network-wide ransomware outbreaks  
- Compromise of sensitive machines  

---

## 5. Keep Systems Updated 🔄

Regular updates are essential.

### Update areas include:
- OS patches  
- SMB service updates  
- Security tools  
- Antivirus definitions  

Outdated systems are the primary cause of EternalBlue infections.

---

## 6. Use IDS/IPS Solutions 🛰️

Intrusion Detection/Prevention Systems help identify SMB exploits.

### Tools to use:
- Snort  
- Suricata  
- OSSEC  
- Security Onion  

IDS alerts can detect:
- Unauthorized SMB traffic  
- Exploit attempts  
- Suspicious payload delivery  

---

## 7. Disable Unnecessary Services ⚙️

Turn off unused sharing features to reduce risks.

### Common services to disable:
- File and Printer Sharing  
- Remote Assistance  
- Remote Registry  

Less enabled services = fewer attack vectors.

---

## 8. Strong Password Policies 🔐

Weak passwords make post-exploitation easier.

### Recommendations:
- Minimum 10–12 characters  
- Mix of letters, numbers, symbols  
- Regular password rotation  
- Lockout after failed attempts  

---

## 9. Monitor SMB Traffic 🧪

Use tools like Wireshark or Splunk to monitor traffic patterns.

Look for:
- Repeated SMB negotiation  
- Suspicious SMBv1 packets  
- Unexpected connections on port 445  

Early detection helps prevent full compromise.

---

## 10. Backup and Recovery Practices 💾

Good backups minimize damage from potential attacks.

### Best practices:
- Keep offline backups  
- Test recovery procedures  
- Use versioned backups  
- Protect backup servers  

Backups make ransomware powerless.

---

## 11. Migration to Modern OS 💼

Windows 7 is **End-of-Life** and no longer supported.

### Recommended upgrades:
- Windows 10  
- Windows 11  
- Linux-based systems (for servers)  

Modern OS versions receive:
- Frequent patches  
- SMBv3 support  
- Stronger security controls  

---

## 12. Summary 📝

To secure systems against EternalBlue and similar exploits:

- ✔ Install MS17-010 patch  
- ✔ Disable SMBv1  
- ✔ Restrict port 445  
- ✔ Use IDS/IPS  
- ✔ Segment networks  
- ✔ Keep OS updated  
- ✔ Enforce strong password policies  
- ✔ Monitor SMB traffic  

Together, these measures form a **layered defense strategy**  
that minimizes the risk of exploitation.


