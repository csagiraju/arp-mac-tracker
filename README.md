# ARP-MAC Tracker with OUI Vendor Mapping

This tool automates the collection of ARP tables and MAC address tables from network devices, stitches IP to MAC addresses, identifies vendor details via OUI lookup, and compares pre/post snapshots to detect added or missing devices.

## 📦 Features
- Collects ARP table and MAC table using SSH
- Matches IP to MAC addresses
- Performs OUI lookup for vendor identification
- Tracks changes (missing/added devices) between snapshots
- Supports Pre/Post data collection and comparison

## 📂 Folder Structure
```
arp_mac_tracker/
├── inventory/
│   └── inventory.csv
├── scripts/
│   ├── collect.py
│   └── compare.py
├── data/
│   ├── pre_snapshot.json
│   └── post_snapshot.json
├── logs/
├── reports/
└── README.md
```

## 🧪 Dependencies
```bash
pip install netmiko requests
```

## ▶️ Usage
1. Run `collect.py` before and after to collect snapshots:
```bash
python scripts/collect.py pre
python scripts/collect.py post
```

2. Run `compare.py` to identify changes:
```bash
python scripts/compare.py
```

