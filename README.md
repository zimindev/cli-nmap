
# 🔍 `nmap` — Network Mapper

`nmap` (Network Mapper) is a powerful open-source tool for network discovery and security auditing. It's widely used by system administrators and security professionals to scan networks, detect open ports, services, and vulnerabilities.

---

## ✅ Features

- Host discovery
- Port scanning (TCP/UDP)
- Version detection of services
- OS detection
- Scriptable interaction using NSE (Nmap Scripting Engine)
- Output in multiple formats (normal, XML, grepable)

---

## 🔧 Installation

### On Debian/Ubuntu:
```bash
sudo apt update && sudo apt install nmap
```

### On Red Hat/CentOS/Fedora:
```bash
sudo dnf install nmap
```

### On Arch Linux:
```bash
sudo pacman -S nmap
```

---

## 🚀 Basic Usage

### Scan a single IP:
```bash
nmap 192.168.1.1
```

### Scan a range of IPs:
```bash
nmap 192.168.1.1-100
```

### Scan a subnet:
```bash
nmap 192.168.1.0/24
```

### Detect service versions:
```bash
nmap -sV 192.168.1.1
```

### Detect operating system:
```bash
sudo nmap -O 192.168.1.1
```

### Scan specific ports:
```bash
nmap -p 22,80,443 192.168.1.1
```

### Run default scripts:
```bash
nmap -sC 192.168.1.1
```

### Save output to files:
```bash
nmap -oN output.txt 192.168.1.1
```

---

## ⚙️ Advanced Usage

### Aggressive scan (includes OS, version, script, and traceroute):
```bash
sudo nmap -A 192.168.1.1
```

### Stealth SYN scan:
```bash
sudo nmap -sS 192.168.1.1
```

### UDP scan:
```bash
sudo nmap -sU 192.168.1.1
```

### Full TCP connect scan:
```bash
nmap -sT 192.168.1.1
```

### Scan multiple targets:
```bash
nmap 192.168.1.1 192.168.1.2 192.168.1.3
```

---

## 🧠 Useful Tips

- Always run `nmap` with `sudo` for more accurate results (especially OS detection and ping sweeps).
- Use `-T4` for faster scans (good balance of speed and stealth).
- Combine with `grep` or save results for automation.

---

## 📁 Output Formats

- `-oN` — Normal text file
- `-oX` — XML
- `-oG` — Grepable format
- `-oA` — Output in all three formats

Example:
```bash
nmap -oA scan_result 192.168.1.1
```

---

## 📚 More Info

- Website: [https://nmap.org](https://nmap.org)  
- NSE Scripts: [https://nmap.org/nsedoc/](https://nmap.org/nsedoc/)
- GitHub: [https://github.com/nmap/nmap](https://github.com/nmap/nmap)

