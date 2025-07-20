# 🔐 SSH Hardening on Kali Linux – Secure Like a Pro

This project is part of the **Google Cybersecurity Certificate** and demonstrates how to harden the SSH server on Kali Linux to reduce the attack surface.

---

## 🔍 Overview

SSH (Secure Shell) is a powerful tool — but misconfigured, it becomes a major security risk. In this mini-project, I hardened SSH following security best practices:

- Disabled root login  
- Disabled password-based authentication  
- Restricted login to a specific user  
- Set logging to VERBOSE  
- Verified open SSH port  
- Monitored SSH-related system logs  

---

## 🛠️ System Info

- **OS**: Kali Linux (Rolling)  
- **Kernel**: `uname -r`  
- **User**: `nikunj@kali`  
- **SSH Version**: OpenBSD Secure Shell Server  

---

## ⚙️ Configuration Changes

**File Modified:** `/etc/ssh/sshd_config`

```bash
PermitRootLogin no
PasswordAuthentication no
X11Forwarding no
AllowUsers nikunj
LogLevel VERBOSE
```
