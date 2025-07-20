
# 🔐 SSH Hardening on Kali Linux – Secure Like a Pro

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

---

## 🧪 Verification Commands

```bash
sudo systemctl status ssh
sudo netstat -tuln | grep :22
```

---

## ✅ Validation Checklist

- ✅ SSH service is **running**  
- ✅ Port **22** is **open and listening**  
- ✅ Only user **nikunj** allowed to log in  
- ✅ **Root login** and **password authentication** are disabled  

---

## 🖼️ Screenshots

| Task                        | Screenshot                              |
|----------------------------|-----------------------------------------|
| SSH Service Status         | ![](screenshots/01-ssh-status.png)      |
| SSH Config (`sshd_config`) | ![](screenshots/02-sshd-config.png)     |
| SSH Port via Netstat       | ![](screenshots/03-netstat-port.png)    |
| Logwatch Output            | ![](screenshots/04-logwatch-output.png) |

---

## 🧪 Tools Used

- `nano`  
- `systemctl`  
- `netstat`  
- `logwatch`  
- `ssh`  

---

## 🧠 Lessons Learned

- Why disabling root login improves SSH security  
- How to enforce key-based authentication only  
- How to use system logs for intrusion detection  
- Importance of service-level hardening on Linux systems  

---

## 🚀 Future Enhancements

- Implement key-based login  
- Integrate `fail2ban` for brute-force protection  
- Create a script for automatic SSH hardening  

---

## 👤 Author

**Nikunj Adatiya**  
- GitHub: [@nik-cybersec](https://github.com/nik-cybersec)  
- LinkedIn: [Nikunj Adatiya](https://www.linkedin.com/in/nikunj-adatiya-3a5bb72ab)

---

> 🛡️ *Real security begins with awareness and hands-on practice.*
