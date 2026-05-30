Wi-Fi Auditor (doss.py)
A Python script that automates the Aircrack-ng suite on Linux to demonstrate network discovery and wireless deauthentication testing.
⚠️ Disclaimer
EDUCATIONAL PURPOSE ONLY: Running this script against networks you do not own or have explicit written permission to test is illegal Use this strictly in your own lab environment. The developer assumes no liability for misuse.
🛠️ Linux Requirements
OS: Kali Linux or any distribution with the Aircrack-ng suite installed.
Hardware: A Wi-Fi adapter that supports Monitor Mode and Packet Injection.
Install dependencies:
Bash
sudo apt update && sudo apt install aircrack-ng wireless-tools -y
🚀 Setup & Usage
1. Configure the Interface Index
The script detects wireless cards automatically using iwconfig. By default, it selects the first interface index (0). If you have multiple cards and need to switch, update the variable at the top of doss.py:
Python
wlan = 0  # Change 0 to your preferred interface index number
2. Run the Script
Wireless automation requires root privileges. Execute with sudo:
Bash
sudo python3 doss.py
3. How to Use
The script will start scanning for nearby access points.
Press Ctrl + C to stop the live scan.
Type the No (index number) of your target network and press Enter.
To stop the test, restore your network card, and restart system networking, press Ctrl + C again.
