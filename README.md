# Honeypy 🐝

Honeypy is a simple honeypot written in Python, designed to capture and log suspicious attacker activity.  
The project is intended for educational and research purposes to analyze unauthorized access attempts.

---

## 📌 Features

- SSH honeypot
- HTTP (web) honeypot
- Logging of:
  - IP addresses
  - usernames and passwords
  - HTTP requests
  - commands (SSH)
- Simple architecture
- Easy to extend

---

## 📁 Project Structure

```

Honeypy/
├── templates/              # HTML templates for web honeypot
├── honeypy.py              # Main launcher file
├── ssh_honeypot.py         # SSH honeypot
├── web_honeypot.py         # HTTP honeypot
├── reqs.txt                # Python dependencies
├── audits.log              # General logs
├── cmd_audits.log          # SSH command logs
├── http_audits.log         # HTTP request logs
├── .gitignore
└── README.md

````

---

## 🧠 Requirements

- Python 3.x
- pip

---

## 📦 Installation

```bash
git clone https://github.com/AtakOskonbaev/Honeypy.git
cd Honeypy
````

```bash
pip install -r reqs.txt
```

---

## ▶️ Usage

### Run SSH honeypot

```bash
python3 honeypy.py -a 127.0.0.1 -p 2223 -u username --password password --ssh
```

### Run Web honeypot

```bash
python3 honeypy.py -a 127.0.0.1 -p 2223 -u username --password password --http
```

---

## 📊 Logs

Honeypy stores all attacker activity in log files:

| File            | Description                      |
| --------------- | -------------------------------- |
| audits.log      | General events                   |
| cmd_audits.log  | Commands entered via SSH         |
| http_audits.log | HTTP requests and login attempts |

Example log entry:

```
2025-12-19 14:22:10 | 192.168.1.15 | admin:admin | SSH login attempt
```

---

## ⚙️ Configuration

You can modify:

* service ports
* banners
* allowed usernames
* log format

All configuration options are located directly in the source files of the modules.

---

## ⚠️ IMPORTANT

This honeypot is **not intended for use on production servers** without proper isolation.
Use it only:

* in lab environments
* on virtual machines
* for educational purposes
* for attack analysis and research
