# Switch to Tor: Advanced Tor Management Tool

A Python-based command-line tool for managing your Tor connection on Kali Linux and Parrot OS. It provides a feature-rich dashboard for IP rotation, a robust `iptables` kill switch, and other security utilities to enhance your anonymity.

Developed by **justt cyber tech**.

!Screenshot 
*(Note: You can replace the above URL with a real screenshot of the tool in action.)*

---

## Features

*   **Live IP Rotation Dashboard:** Continuously requests new Tor exit nodes at a user-defined interval and displays your changing public IP address and geo-location data in real-time.
*   **Customizable Rotation Speed:** Choose from pre-defined quality levels (Poor, Good, Perfect) or set a custom rotation interval in seconds.
*   **Robust Kill Switch:** Implements `iptables` rules to block all non-Tor traffic, preventing IP leaks if the connection fails. It automatically detects the correct Tor user ID (`debian-tor`) on the system.
*   **Persistent IPv6 Control:** Easily enable or disable IPv6 across system reboots to prevent potential leaks.
*   **System Status Overview:** The main menu displays the live status of your IPv6 configuration and the active traffic policy (kill switch).
*   **Redundant IP Geolocation:** Uses multiple public APIs to fetch IP address details, ensuring reliability.
*   **Rich Terminal UI:** A modern and easy-to-read interface built with the Python `rich` library.

---

## Requirements

This tool is designed for **Kali Linux** and **Parrot OS**.

1.  **Python 3:** Should be pre-installed on both systems.
2.  **Required Python Libraries:** `requests`, `rich`, `stem`.
3.  **Tor Service:** The `tor` daemon must be installed and running.
4.  **Anonsurf:** This tool is used to route traffic through Tor. It's pre-installed on Parrot OS.
5.  **Root Privileges:** The script must be run as root to manage network services and `iptables` rules.

---

## Installation

1.  **Clone the repository:**
    ```bash
    git clone https://github.com/juttcybertech/Switch-To-Tor.git
    cd Switch-To-Tor
    ```

2.  **Install Python libraries:**
    ```bash
    sudo pip3 install -r requirements.txt
    ```

3.  **Install Tor:**
    If not already installed, open a terminal and run:
    ```bash
    sudo apt update && sudo apt install tor -y
    ```

4.  **Install Anonsurf (for Kali Linux users):**
    Parrot OS users can skip this step.
    ```bash
    git clone https://github.com/ParrotSec/anonsurf
    cd anonsurf
    sudo ./installer.sh
    ```

---

## Usage

Run the script with `sudo` privileges:

```bash
sudo python3 1.py
```

### Main Menu Options

*   **1. Kill Switch (Tor-only internet):** Activates `iptables` rules to block all traffic except for traffic initiated by the Tor service. This is the safest mode.
*   **2. Normal Internet (all traffic allowed):** Flushes all `iptables` rules, restoring normal internet connectivity.
*   **3. Rotation Timing Dashboard:** Starts the main IP rotation feature. You will be prompted to select a rotation interval, after which the dashboard will launch, start `anonsurf`, and begin cycling your Tor IP address. Press `Ctrl+C` to exit the dashboard safely.
*   **4. IPv6 Settings (Sub-menu):** Allows you to permanently enable or disable IPv6 system-wide.
*   **5. Exit:** Quits the program.

---

## ⚠️ Disclaimer

This tool modifies critical network settings and firewall rules (`iptables`). It requires root access to function. While it is designed to enhance anonymity, improper use or bugs could potentially lead to network issues or IP leaks. Use this tool responsibly and at your own risk. Always verify your connection status using independent tools.
