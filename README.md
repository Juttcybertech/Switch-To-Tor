# 🔒 Switch To Tor

> **Secure, transparent Tor proxy with kill switch, leak protection & real-time monitoring — no third-party dependencies.**

![Switch To Tor](https://via.placeholder.com/800x400?text=Switch+To+Tor+Dashboard)  
*A modern, terminal-based Tor anonymization tool for Linux.*

---

## ✨ Features

- **Full system Tor routing** via transparent proxy (no browser config needed)
- **Kill switch**: blocks all non-Tor traffic
- **IPv4/IPv6 leak prevention**
- **DNS leak protection**
- **Real-time IP rotation dashboard**
- **Leak detection & validation**
- **No dependency on `anonsurf` or other third-party tools**
- Beautiful TUI with [Rich](https://github.com/Textualize/rich)

---

## ⚠️ Requirements

- Linux (Debian/Ubuntu/Kali/Parrot recommended)
- Python 3.8+
- Root access (`sudo`)
- Packages: `tor`, `iptables`, `iproute2`

Install dependencies:
```bash
sudo apt update && sudo apt install -y tor iptables python3 python3-pip
pip3 install requests stem rich

git clone https://github.com/yourname/switch-to-tor.git
cd switch-to-tor
sudo python3 switch_to_tor.py




---

## 📄 Fichier `LICENSE` (GPL-3.0)

Tu peux générer un fichier `LICENSE` complet ici :  
👉 https://www.gnu.org/licenses/gpl-3.0.txt

Ou exécuter dans ton repo :
```bash
curl -o LICENSE https://www.gnu.org/licenses/gpl-3.0.txt
