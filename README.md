# Wi-Fi Monitor (Raspberry Pi + Alfa Adapter)

A small project where I used a Raspberry Pi with an Alfa Wi-Fi adapter in **monitor mode** to capture wireless packets (beacon and probe frames). The data was exported and anonymized, and the results are documented here.

---

## Goals
- Learn how Wi-Fi monitoring works.  
- Use `tcpdump` and Wireshark to collect and analyze packets.  
- Document and anonymize findings in an ethical way.  

---

## Setup
- **Hardware:** Raspberry Pi + Alfa AWUS036ACM adapter.  
- **Software:** Raspberry Pi OS, `aircrack-ng`, `tcpdump`, `tshark`, Wireshark.  
- The adapter was set in *monitor mode* (`wlan1mon`) for passive sniffing.

---

## Procedure
1. Set the adapter in monitor mode.  
2. Ran `tcpdump` for 30 seconds to capture packets.  
3. Opened the `.pcap` file in Wireshark to analyze beacon and probe frames.  
4. Anonymized MAC addresses and exported to a TSV file.  

---

## Evidence (screenshots)

**Terminal capture (tcpdump):**  
![Terminal Capture](screenshots/terminal_capture.png)

**Beacon frames in Wireshark:**  
![Wireshark Beacon](screenshots/wireshark_beacon.png)

**Probe requests in Wireshark (Wildcard/Broadcast):**  
![Wireshark Probe](screenshots/wireshark_probe.png)

---

## Ethical considerations
- Tested only on my own network / devices.  
- MAC addresses were anonymized before sharing.  
- Screenshots are either edited or taken on wildcard probes to avoid exposing real SSIDs.  

---

## Future work
- Add a simple Python visualization (number of APs/clients, signal strength).  
- Automate anonymization and export.  

---

## What I learned
- How to set up a Wi-Fi adapter in monitor mode.  
- The difference between beacon frames and probe requests in practice.  
- How to responsibly handle sensitive wireless metadata.
