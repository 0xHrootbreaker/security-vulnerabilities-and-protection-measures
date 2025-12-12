# 02. Environment Setup

A controlled, isolated virtual lab environment was created to safely test and analyze the  
EternalBlue vulnerability without risking any real systems or networks.

This section details all components, configurations, and network settings used in the assessment.

---

## 1. Lab Overview

The vulnerability assessment was performed using two virtual machines:

| Role | Operating System | Purpose |
|------|------------------|---------|
| **Attacker Machine** | Kali Linux | Scanning, exploitation, network sniffing |
| **Victim Machine** | Windows 7 (Unpatched) | Target vulnerable to EternalBlue |

To ensure safety, the entire setup was kept **offline** and **sandboxed**.

---

## 2. System Requirements

### 2.1 Hardware Requirements (Host PC)

| Component | Minimum | Recommended |
|----------|----------|-------------|
| RAM | 8 GB | 12–16 GB |
| CPU | Intel i5 / Ryzen 5 | i7 / Ryzen 7 |
| Storage | 40 GB free | 80+ GB free |
| Virtualization | VT-x/AMD-V enabled | Required |

---

## 3. Virtual Machines Setup

### 3.1 Windows 7 VM (Victim)

- Windows 7 SP1 (32-bit or 64-bit)
- No security updates installed  
- SMBv1 enabled by default  
- No antivirus  
- Firewall temporarily disabled (for controlled testing)  
- Static IP assigned

#### Windows 7 Recommended Settings
RAM: 2 GB+
CPU: 2 cores
Network Adapter: Host-Only Adapter


---

### 3.2 Kali Linux VM (Attacker)

- Latest Kali Linux ISO
- Metasploit installed (default in Kali)
- Nmap installed
- Wireshark installed

#### Kali Recommended Settings
RAM: 2–4 GB
CPU: 2 cores
Network Adapter: Host-Only Adapter


---

## 4. Network Configuration

To keep the test safe, a **Host-Only Network** was used. This isolates both VMs from the internet 
and the host network.

### 4.1 Network Details

| Setting | Value |
|---------|--------|
| Network Type | Host-Only |
| Subnet | 192.168.56.0/24 |
| Windows 7 IP | 192.168.56.10 |
| Kali Linux IP | 192.168.56.20 |
| Internet Access | Disabled |
| DHCP | Optional |

---

## 5. Tools Installed in Kali Linux

### 5.1 Metasploit Framework
Used for launching the EternalBlue exploit:
msfconsole

### 5.2 Nmap
Used for vulnerability scanning:
nmap --script smb-vuln-ms17-010 -p445 <target-ip>


### 5.3 Wireshark
Used for packet inspection:
wireshark

---

## 6. Tools Installed in Windows 7

- SMBv1 enabled by default (vulnerable)
- No patches applied
- System deliberately left unprotected for testing (safe environment)

---

## 7. Environment Validation

Before starting the assessment, the following checks were completed:

✔ Both VMs can ping each other  
✔ Port 445 (SMB) is open on Windows 7  
✔ Metasploit modules load correctly  
✔ Windows 7 shows no MS17-010 patch installed  
✔ Wireshark captures SMB traffic  

---

## 8. Summary

This controlled environment ensures that:

- Testing is safe  
- Results are accurate  
- No external networks are affected  
- EternalBlue behavior is fully observable  

The next step is performing a vulnerability scan on the Windows 7 system.

