# 2. Requirement and Analysis

## 2.1 Problem Definition

Modern cybersecurity threats continue to evolve, and outdated systems such as **Windows 7**
remain highly vulnerable. The **EternalBlue exploit** targets a flaw in the **SMBv1 protocol**
allowing attackers to execute remote code and take full control of systems.

The problem addressed in this project includes:

### 1. Vulnerability of Outdated Systems  
Many organizations still use unsupported or outdated operating systems. These systems often:
- Lack security patches  
- Use old, insecure protocols  
- Are easy targets for cybercriminals  

### 2. SMBv1 Protocol Weakness  
EternalBlue exploits a critical flaw in the SMBv1 file-sharing protocol, enabling:
- Remote code execution  
- Unauthorized access  
- Complete system takeover  

### 3. Real-World Impact  
Attacks like **WannaCry (2017)** exploited this vulnerability, causing:
- Data breaches  
- Ransomware infections  
- Financial losses  
- Global disruptions  

### 4. Lack of Awareness  
Users and organizations often fail to:
- Apply security updates  
- Disable outdated protocols  
- Understand cybersecurity risks  

### 5. Need for Practical Security Solutions  
There is a strong need for:
- Demonstrations of how vulnerabilities are exploited  
- Preventive security measures  
- Awareness about system updates and patches  

---

## 2.2 Requirement Specification

### **1. Tools Required**

#### **Kali Linux**
- For penetration testing  
- Tools used: Metasploit, Nmap, Wireshark  

#### **Windows 7 (Unpatched)**
- Target system for the EternalBlue exploit  
- SMBv1 enabled  

#### **Metasploit Framework**
- Used to launch the MS17-010 EternalBlue exploit  

#### **Firewall / Antivirus**
- To test detection and prevention capabilities  

#### **Virtualization Software**
- VMware or VirtualBox  
- Required for creating isolated test environments  

#### **Debugging / Development Tools**
- VS Code or similar editor  
- For observation, scripting, and documentation  

---

## 2.3 Hardware & Software Requirements

### **Hardware Requirements**

| Component | Minimum Requirement |
|----------|---------------------|
| RAM | 8 GB (Recommended 12+ GB for multiple VMs) |
| Processor | Intel i5 equivalent or higher |
| Storage | 40+ GB free disk space |
| Virtualization Support | BIOS-enabled VT-x / AMD-V |

---

### **Software Requirements**

| Sr. No. | Software Component | Specification Details |
|--------|--------------------|------------------------|
| 1 | Operating System | Windows 7 VM, Kali Linux |
| 2 | Exploitation Framework | Metasploit Framework |
| 3 | Network Analysis Tool | Wireshark |
| 4 | Port Scanner | Nmap |
| 5 | Virtualization | VirtualBox / VMware |
| 6 | Security Patches | Microsoft Patch MS17-010 |

---

## 2.4 Planning and Scheduling

### **Project Planning**

| Activity | Time Duration |
|----------|--------------|
| Requirement Gathering | 2 Weeks |
| System Design | 2 Weeks |
| Development & Coding | 3 Weeks |
| Quality Assurance | 1 Week |
| Testing & Implementation
