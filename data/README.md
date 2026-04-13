# 📂 Data Folder

This folder contains sample log files for testing the notebook.

---

## 📁 Folder Structure

```
data/
└── sample_logs/
    └── sample_auth.log     ← Upload your real log file here
```

---

## 📄 Supported Log Format

The notebook accepts standard **Linux auth.log / syslog** format:

```
Jun 01 03:22:11 server sshd[4821]: Failed password for root from 192.168.1.45 port 22 ssh2
Jun 01 03:22:15 server sshd[4822]: Accepted password for ubuntu from 10.0.0.5 port 22 ssh2
Jun 01 03:22:20 server sshd[4823]: Invalid user admin from 203.45.67.89 port 22 ssh2
Jun 01 03:22:25 server sshd[4824]: Port scan detected from 45.33.32.156 port 80 ssh2
Jun 01 03:22:30 server sshd[4825]: Firewall rule triggered for guest from 198.51.100.1 port 443 ssh2
```

---

## 🔑 Event Keywords (for detection to work)

| Keyword in log line | Alert triggered |
|---|---|
| `Failed password` | Brute-force / Root Login |
| `Invalid user` | Invalid User Login |
| `Port scan detected` | Port Scan |
| `Firewall rule triggered` | Firewall Alert |

---

## ⚠️ Important

- **Never commit real production logs** to GitHub — they may contain sensitive IP addresses and usernames.
- The `.gitignore` is set to exclude `*.log` files (except the sample).
- Use the sample file only for testing purposes.
