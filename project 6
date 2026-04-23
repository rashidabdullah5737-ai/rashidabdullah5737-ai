# 🛡️ MacPF-SOC-Setup 🔒

```
 ███╗   ███╗ █████╗  ██████╗███████╗██████╗ 
 ████╗ ████║██╔══██╗██╔════╝██╔════╝██╔══██╗
 ██╔████╔██║███████║██║     █████╗  ██████╔╝
 ██║╚██╔╝██║██╔══██║██║     ██╔══╝  ██╔══██╗
 ██║ ╚═╝ ██║██║  ██║╚██████╗███████╗██║  ██║
 ╚═╝     ╚═╝╚═╝  ╚═╝ ╚═════╝╚══════╝╚═╝  ╚═╝
SOC-style PF Firewall for macOS Security
```

![macOS](https://img.shields.io/badge/OS-macOS-blue?style=for-the-badge&logo=apple) ![Status](https://img.shields.io/badge/Status-Active-success?style=for-the-badge) ![Author](https://img.shields.io/badge/Author-Abdullah_Rashid-black?style=for-the-badge)

---

## 🚀 Features

* 🌐 **Threat Intelligence Blocklists** – Blocks 50k+ known malicious IPs automatically.  
* 🔐 **SSH Protection** – Defends against brute-force attacks with SSHGuard.  
* 🌍 **Optional GeoIP Filtering** – Restrict traffic by country or region.  
* 📜 **Logging & Auditing** – Keep detailed logs of blocked connections.  
* 🔎 **Real-Time Monitoring** – Inspect attacks live via the `pflog0` interface.  

---

## 🛠 Prerequisites

* macOS 11+ (Monterey or later recommended)  
* PF firewall enabled (`sudo pfctl -e`)  
* SSHGuard installed  
* Optional: GeoIP database for country-based filtering  

---

## ⚡ Installation

```bash
# Backup existing PF config
sudo cp /etc/pf.conf /etc/pf.conf.backup

# Copy new PF configuration
sudo cp pf.conf /etc/pf.conf

# Enable PF and load config
sudo pfctl -f /etc/pf.conf
sudo pfctl -e

# Verify PF status
sudo pfctl -s all
```

---

## 📊 Usage & Monitoring

* **View blocked connections in real-time**  
```bash
sudo tcpdump -ni pflog0
```

* **Check PF rules & status**  
```bash
sudo pfctl -sr   # Show rules
sudo pfctl -si   # Show PF info
```

* **Start SSHGuard**  
```bash
brew services start sshguard
```

---

## 🌐 Optional: GeoIP Filtering

```bash
brew install geoip
```
* Configure PF rules to block/allow traffic by country.  

---

## 📝 Logging & Auditing

* PF logs stored in `/var/log/pflog`  
* Analyze with `pflogd` or `tcpdump`  
* Rotate logs periodically  

---

## ⚠️ Security Notes

* Always **backup `/etc/pf.conf`** before changes  
* Keep blocklists updated  
* Update SSHGuard & GeoIP databases regularly  

---

## 🤝 Contributing

PRs welcome for:  

* Updated threat blocklists  
* Optimized PF rules  
* Monitoring scripts or dashboards  

---

## 📬 Author & Contact

**Abdullah Rashid**  
🐧 Cybersecurity Enthusiast | SOC & Linux Security  

🌐 Portfolio: [Portfoliorashidabdullah5737-ai.github.io](https://Portfoliorashidabdullah5737-ai.github.io)  
💼 LinkedIn: [linkedin.com/in/abdullah-rashid-a1554b388](https://www.linkedin.com/in/abdullah-rashid-a1554b388)  
✉️ Email: rashidabdullah5737@gmail.com  
🐺 Club: Cyber Wolf Club — Member
