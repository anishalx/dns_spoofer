# SpoofShifter

**SpoofShifter** is a lightweight and powerful DNS spoofing tool designed for ethical hackers and penetration testers. Written in Python, it leverages the `Scapy` library to manipulate DNS responses, allowing attackers to redirect DNS queries to a specified IP. When used in combination with ARP spoofing, SpoofShifter can perform effective Man-in-the-Middle (MitM) attacks, redirecting traffic seamlessly.

## Features
- Real-time DNS spoofing for specified domains.
- Efficient packet manipulation with `Scapy`.
- Ability to target specific DNS queries (e.g., redirect `www.google.com`).
- Easy integration with ARP spoofing for comprehensive network attacks.
- Lightweight and simple command-line interface.

## Requirements
Before running SpoofShifter, ensure that the following dependencies are installed:

### System Dependencies:
```bash
sudo apt-get update
sudo apt-get install libnetfilter-queue-dev
```

### Pyhton Libraries:
```bash
pip install netfilterqueue scapy
```

## Setup and Usage

1. Run iptables Rule: Redirect the network traffic to the NFQUEUE by running the following command:

```bash
sudo iptables -I FORWARD -j NFQUEUE --queue-num 0
```
2. Set Up ARP Spoofing: Run an ARP spoofing tool to intercept and manipulate traffic between the target and the router.

3. Execute SpoofShifter: Run the Python script to start DNS spoofing:
