# 📄 01-overview.md
## 1. Introduction

EternalBlue (MS17-010) is one of the most dangerous vulnerabilities ever discovered in Windows systems.  
It targets a flaw in the **SMBv1 (Server Message Block)** protocol, enabling **remote code execution (RCE)**  
without authentication.

The exploit became widely known after it was used in the **WannaCry ransomware attack (2017)**, which  
affected over 200,000 computers worldwide.

This document provides a **complete vulnerability assessment** of EternalBlue on **Windows 7**, performed  
in a safe and isolated virtual environment.

---

## 2. What is EternalBlue?

EternalBlue is an advanced exploit originally developed by the **NSA** and leaked by the hacker group  
**Shadow Brokers**. It abuses a memory corruption bug in SMBv1 that allows attackers to:

- Execute malicious code remotely  
- Install malware/backdoors  
- Steal or encrypt data  
- Take full system control  

The vulnerability is officially referenced as:CVE-2017-0144
Microsoft Security Bulletin: MS17-010


---

## 3. Why Windows 7 is Vulnerable

Windows 7 is ideal for studying EternalBlue because:

- SMBv1 is enabled by default  
- Many users never applied the MS17-010 patch  
- The OS reached End-of-Life, increasing risk  
- It’s still used in older environments and legacy systems  

---

## 4. Assessment Scope

This assessment includes:

- Detecting MS17-010 using Nmap  
- Capturing SMB traffic using Wireshark  
- Exploiting Windows 7 with Metasploit  
- Validating whether the Microsoft patch fixes the vulnerability  
- Documenting how to mitigate and prevent EternalBlue attacks  

---

## 5. Ethical & Legal Considerations

⚠ **All tests were performed in an offline, isolated virtual environment.**  
⚠ **No real systems were harmed.**  
⚠ **This repository is for educational & research purposes only.**

Unauthorized exploitation of systems is illegal.

---

## 6. Summary

EternalBlue demonstrates how catastrophic unpatched vulnerabilities can be.  
This assessment provides a hands-on, safe demonstration of how the exploit works and how to secure  
systems effectively.


