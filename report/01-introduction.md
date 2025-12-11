# 1. Introduction

## 1.1 Background

In today’s digital era, cybersecurity has become one of the most essential areas of focus.  
With the increasing dependence on computers, networks, and the internet, the risks of  
cyberattacks have grown significantly. As a BCA student with a keen interest in how systems  
function and how they can be protected, this project focuses on one of the most well-known  
cybersecurity vulnerabilities in recent history — the **EternalBlue exploit** and its impact on  
older systems, particularly **Windows 7**.

### Why This Topic?

The EternalBlue exploit gained global attention after being used in the **WannaCry  
ransomware attack of 2017**, which infected over 200,000 computers in more than 150  
countries. This incident highlighted how a single unpatched vulnerability can cause  
huge financial losses and disrupt critical operations worldwide.

Studying this topic helps in understanding:

- How attackers exploit vulnerabilities  
- How outdated systems increase risk  
- What security practices prevent such attacks  
- Why organizations should maintain regular updates and patches  

### What is EternalBlue?

EternalBlue is a powerful cyberattack tool that exploits a vulnerability in the  
**SMBv1 (Server Message Block version 1)** protocol used for file sharing in  
Windows systems.  
The vulnerability allows attackers to:

- Execute remote code  
- Install malware  
- Steal sensitive data  
- Gain complete system control  

The exploit was originally developed by the **NSA (National Security Agency)**  
and later leaked by the hacker group **Shadow Brokers**.

### Why Windows 7?

Windows 7 was one of the most affected operating systems because:

- Many users did not install the security patch  
- SMBv1 was enabled by default  
- The OS reached end-of-life, making systems more vulnerable  
- Organizations continued to use it for compatibility reasons  

This makes Windows 7 a perfect case study for understanding real-world  
cybersecurity risks.

### Importance of Security Patches

One of the biggest lessons from EternalBlue is the importance of applying  
security patches on time. Microsoft released the **MS17-010 patch** before  
WannaCry happened, but millions of systems remained unpatched, allowing the  
attack to spread rapidly.

This project emphasizes:

- Applying security updates  
- Disabling outdated protocols like SMBv1  
- Using firewalls and IDS tools  
- Practicing good cybersecurity hygiene  

---

## 1.2 Objectives

1. Understand how the EternalBlue exploit works  
2. Study the SMBv1 protocol vulnerability  
3. Analyze how Windows 7 is affected  
4. Demonstrate exploitation in a controlled lab environment  
5. Explore security measures like patches, firewalls, and IDS  
6. Raise awareness about updating systems regularly  

---

## 1.3 Purpose

The purpose of this project is to:

- Educate users about the dangers of outdated systems  
- Show how cybercriminals exploit vulnerabilities  
- Demonstrate the importance of applying updates and patches  
- Provide practical solutions to secure operating systems  
- Promote better cybersecurity habits  

---

## 1.4 Scope

The scope of this project includes:

- Detailed study of the EternalBlue exploit  
- Understanding the SMBv1 protocol and its weaknesses  
- Demonstrating the exploitation process using Metasploit  
- Studying the impact on outdated systems like Windows 7  
- Testing preventive measures such as disabling SMBv1  
- Using tools like Nmap and Wireshark for vulnerability analysis  
- Raising awareness about real-world cyber threats  

This project does **not** involve attacking real systems; all tests were performed  
in a controlled virtual environment.

---

## 1.5 Applicability

The concepts learned in this project are applicable in:

- Network security  
- Penetration testing  
- Incident response  
- Vulnerability assessment  
- Cybersecurity awareness training  

Organizations, students, and security enthusiasts can use this research to  
understand how vulnerabilities like EternalBlue work and how to prevent such  
attacks.

---
