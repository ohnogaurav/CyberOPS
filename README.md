# CYBEROPS — Real Cyber Investigation System

## BEFORE YOU RUN

### Step 1 — Install Npcap (for packet capture)
Download: https://npcap.com/#download
Install with "WinPcap API-compatible mode" checked.

### Step 2 — Install Python packages (as Administrator)
```
pip install flask scapy pywin32
```

### Step 3 — (Optional) Get free AbuseIPDB API key
Register: https://www.abuseipdb.com/register
Free tier = 1000 checks/day.
Set key:
```
set ABUSEIPDB_KEY=your_key_here
```

### Step 4 — Run as Administrator (REQUIRED)
Right-click Command Prompt → "Run as administrator"
```
cd cybercrime_real
python app.py
```

Open browser: http://127.0.0.1:5000

---

## FEATURES (ALL REAL)

| Feature | Data Source |
|---|---|
| Auth Log | Windows Security Event Log (Event IDs 4624/4625) |
| Port Scanner | Real socket connections to any host |
| Packet Capture | Scapy live capture via Npcap |
| Threat Intel | AbuseIPDB API + local blacklist |

## FILES
```
cybercrime_real/
├── app.py            — Flask web app
├── analyzer.py       — (not used, replaced by below)
├── log_scanner.py    — Windows Event Log + port scanner
├── packet_capture.py — Scapy live capture
├── threat_intel.py   — AbuseIPDB + blacklist
└── requirements.txt
```
