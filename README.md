# 🛡️ Real-Time Cybersecurity Log Monitoring & Alerting Dashboard

![Python](https://img.shields.io/badge/Python-3.10+-blue?logo=python)
![Colab](https://img.shields.io/badge/Google%20Colab-Ready-orange?logo=googlecolab)
![License](https://img.shields.io/badge/License-MIT-green)
![Domain](https://img.shields.io/badge/Domain-Cybersecurity-red)

> A lightweight, real-time log monitoring and alerting system that detects cybersecurity threats from system logs using rule-based detection and visualizes them in an interactive dashboard.

---

## 📌 Project Overview

| Field | Details |
|---|---|
| **Domain** | Cybersecurity, Data Analytics |
| **Type** | Industry-Oriented Project |
| **Platform** | Google Colab |
| **Database** | SQLite |
| **Visualization** | Plotly, Seaborn, Matplotlib |

---

## 🎯 Objective

Modern systems generate a large volume of security logs. Manual monitoring is inefficient and error-prone. This project proposes a **real-time log monitoring system** that:

- Detects suspicious activities like **brute-force attacks**, **port scans**, and **root login attempts**
- Classifies threats by **severity** (Low / Medium / High)
- Stores logs and alerts in a **local SQLite database**
- Displays everything in an **interactive dashboard**

---

## 🚀 Features

- ✅ Synthetic log generation (no real server needed)
- ✅ Support for real log file upload (`/var/log/auth.log`)
- ✅ 5 rule-based threat detection rules
- ✅ Severity classification (Low / Medium / High)
- ✅ SQLite database storage
- ✅ 6 interactive Plotly + Seaborn charts
- ✅ Color-coded alert report table
- ✅ CSV + DB export

---

## 🔍 Threat Detection Rules

| Rule | Trigger | Severity |
|---|---|---|
| Brute-Force Attack | ≥5 failed logins from same IP in 10 min | 🔴 High |
| Port Scan | `Port scan detected` event | 🔴 High |
| Root Login Attempt | Failed login for `root` user | 🔴 High |
| Firewall Rule Triggered | `Firewall rule triggered` event | 🟠 Medium |
| Invalid User Login | `Invalid user` event | 🟠 Medium |

---

## 📁 Project Structure

```
real-time-log-monitoring/
│
├── notebooks/
│   └── RealTime_Log_Monitoring.ipynb   # Main Colab notebook
│
├── data/
│   ├── sample_logs/
│   │   └── sample_auth.log             # Sample log file for testing
│   └── README.md                       # Data format description
│
├── requirements.txt                    # Python dependencies
├── .gitignore                          # Files to exclude from Git
├── LICENSE                             # MIT License
└── README.md                           # This file
```

---

## ⚙️ Setup & Usage

### Option 1 — Google Colab (Recommended)

1. Click the badge below or open the notebook manually:

   [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/)

2. Upload `notebooks/RealTime_Log_Monitoring.ipynb`
3. Run all cells: **Runtime → Run All**
4. Done! The dashboard renders automatically.

### Option 2 — Run Locally

```bash
# 1. Clone the repo
git clone https://github.com/ROODARGDARA/real-time-log-monitoring.git
cd real-time-log-monitoring

# 2. Install dependencies
pip install -r requirements.txt

# 3. Launch Jupyter
jupyter notebook notebooks/RealTime_Log_Monitoring.ipynb
```

---

## 📊 Dashboard Preview

The notebook generates 6 visualizations:

| Chart | Description |
|---|---|
| 🔴 Severity Pie Chart | Distribution of High / Medium / Low alerts |
| ⚠️ Threat Type Bar Chart | Count of each detected threat type |
| 📈 Events Over Time | Hourly timeline of security events |
| 🌐 Top Attacker IPs | Most active malicious IP addresses |
| 🔥 Heatmap | Failed logins by hour of day × day of week |
| 📂 Category Breakdown | Logs grouped by category (auth, network, system) |

---

## 📂 Using Your Own Log Data

### Upload a Real Log File
Set `USE_UPLOADED_FILE = True` in Section 4 of the notebook, then upload any `.log` or `.txt` file.

Supported format (standard Linux auth.log):
```
Jun 01 03:22:11 server sshd[4821]: Failed password for root from 192.168.1.45 port 22 ssh2
```

Real log locations on Linux:
- `/var/log/auth.log` — Ubuntu/Debian
- `/var/log/secure` — CentOS/RHEL

---

## 🔭 Future Scope

- [ ] Machine Learning based anomaly detection (Isolation Forest)
- [ ] Support for Windows Event Logs, Apache, Nginx formats
- [ ] Cloud deployment using Docker
- [ ] Advanced alert correlation and reporting
- [ ] Email / SMS alerting integration

---

## 🛠️ Tech Stack

| Tool | Purpose |
|---|---|
| Python 3.10+ | Core language |
| Pandas | Data processing |
| Plotly | Interactive charts |
| Seaborn / Matplotlib | Heatmap & static charts |
| SQLite3 | Local database |
| Faker | Synthetic data generation |
| Google Colab | Cloud notebook environment |

---

## 📄 License

This project is licensed under the **MIT License** — see the [LICENSE](LICENSE) file for details.

---

## 👤 Author

**Your Name**
- GitHub: [@ROODARGODARA](https://github.com/YOUR_USERNAME)

---

> ⭐ If you found this project helpful, please give it a star!
