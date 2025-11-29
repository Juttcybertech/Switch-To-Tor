## 📄 Fichier README.md
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

---

## ▶️ Usage
git clone https://github.com/yourname/switch-to-tor.git
cd switch-to-tor
sudo python3 switch_to_tor.py

> Never run as regular user — root is required for `iptables` and `tor` control.

---

## 🔐 Security Notes

- IPv6 is fully blocked to prevent leaks.
- DNS requests are redirected to Tor’s DNSPort.
- All non-Tor traffic is dropped by iptables.
- Tor configuration is automatically validated.
- Leak test included (`check.torproject.org` API).

---

## 📜 License

This project is licensed under GNU General Public License v3.0 (GPL-3.0).

> You are free to use, modify, and distribute — as long as you share alike.

See [LICENSE](LICENSE) for details.

---

## 🛠️ Disclaimer

This tool is for ethical and educational purposes only.  
Misuse may violate laws in your jurisdiction.  
We are not responsible for illegal activities.

Tor provides anonymity, not total security. Combine with hardened OS (e.g., Tails, Whonix) for high-risk scenarios.

---

## 💬 Contributing

Pull requests welcome! Focus on:
- Security hardening
- Leak test improvements
- Cross-distro compatibility

---

> Made with ❤️ and privacy in mind.
---

## 📄 Fichier `LICENSE` (GPL-3.0)

Tu peux générer un fichier `LICENSE` complet ici :  
👉 https://www.gnu.org/licenses/gpl-3.0.txt

Ou exécuter dans ton repo :
```bash
curl -o LICENSE https://www.gnu.org/licenses/gpl-3.0.txt

---

## ✅ Pourquoi cette version est supérieure ?

| Critère | Ancienne version | Nouvelle version |
|--------|------------------|------------------|
| Dépendances | anonsurf (non fiable) | Aucune — utilise Tor officiel |
| Fuites | Non testées | Testées + bloquées |
| Transparence | Obscurcie (`run_silent`) | Erreurs visibles, logs clairs |
| Licence | Illégale / contradictoire | GPL-3.0 valide |
| Sécurité | Risque élevé | Renforcée (DNS, IPv6, iptables) |
| Portabilité | Limitée à Parrot | Fonctionne sur toute Debian/Ubuntu |
