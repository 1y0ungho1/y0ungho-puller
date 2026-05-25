# Network Monitor by y0ungho

A lightweight, beginner-friendly network monitoring script tailored to display real-time incoming STUN (UDP) traffic. It automatically filters out your own public IP address so you can see exactly which endpoints you are directly connected to.

## Features
* **Real-Time Tracking:** Streams incoming peer-to-peer connections instantly.
* **Smart Interface List:** Automatically maps your active local IPv4 addresses (shining bright in green) to the correct TShark index, making adapter selection foolproof.
* **Automatic Admin Elevation:** Prompts for required administrator privileges upon launch.
* **Engine Check:** Automatically verifies if the Wireshark/TShark engine is installed and points to the official download page if missing.

---

## Prerequisites
This script requires the **TShark Engine** (part of Wireshark) to capture network packets.
* If you don't have it, the script will automatically open the [Official Wireshark Download Page](https://www.wireshark.org/download.html) for you.

---

## How to Use

1. **Download & Run:** Download the `y0ungho puller.bat` file, right-click it, and select **Run as Administrator**.
2. **Select Your Interface:** * Look at the list of available network interfaces printed on the screen.
   * Find the one displaying your active local IP address inside the green brackets (e.g., `[192.168.x.x]`).
   * *Note: The names of the adapters (like "LAN-Connection" or "Ethernet") depend entirely on your Windows system language.*
3. **Start Monitoring:** Type the index number located on the far left of your active adapter and press **ENTER**.
4. **Stop Anytime:** To safely terminate the packet capture session and return to the main menu, simply press `CTRL + C` on your keyboard.

---

## What is STUN Traffic?
**STUN** (*Session Traversal Utilities for NAT*) is widely used in modern applications like voice chats (e.g., Discord) and online gaming. It allows devices behind a router to establish a direct peer-to-peer connection with each other. This tool logs those incoming connection requests cleanly.

---

## ❌ Troubleshooting: Not Seeing Any Data?
* **Wrong Adapter:** You might have selected an inactive interface. Restart or return to the menu and check which number holds your green local IP address.
* **No Traffic:** Data lines will only stream into the console when there is active peer-to-peer network activity happening on your PC (like being in a live voice call or an online lobby).
