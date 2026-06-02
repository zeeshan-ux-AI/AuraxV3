<div align="center">
  
# 💀 AURAX NUCLEAR v3.0 - AI-Powered Pentesting Framework

[![Version](https://img.shields.io/badge/version-3.0-red.svg)](https://github.com/zeeshan-ux-AI/AuraxV3)
[![Python](https://img.shields.io/badge/python-3.8+-blue.svg)](https://www.python.org/)
[![License](https://img.shields.io/badge/license-MIT-green.svg)](LICENSE)
[![Status](https://img.shields.io/badge/status-active-brightgreen.svg)]()

<p align="center">
  <img src="https://readme-typing-svg.demolab.com?font=Fira+Code&weight=600&size=24&duration=3000&pause=500&color=FF0000&center=true&vCenter=true&width=600&lines=💀+NUCLEAR+POWER+UNLEASHED+💀;⚡+AI+DRIVEN+PENTESTING+⚡;🔥+FULL+API+INTEGRATION+🔥" alt="Typing SVG" />
</p>

> **⚠️ DISCLAIMER:** This tool is for educational purposes and authorized testing only. Use only on systems you own or have written permission to test. Unauthorized access is illegal.

</div>

---

## 📋 Table of Contents

- [Features](#-features)
- [Installation](#-installation)
- [Quick Start](#-quick-start)
- [Usage Guide](#-usage-guide)
- [Attack Vectors](#-attack-vectors)
- [API Integration](#-api-integration)
- [Configuration](#-configuration)
- [Reporting](#-reporting)
- [Contributing](#-contributing)
- [License](#-license)
- [Support](#-support)

---

## 🌟 FEATURES

| Category | Features |
|----------|----------|
| **💀 Attack Vectors** | SQL Injection, XSS, LFI/RFI, SSRF, XXE, NoSQLi, Command Injection |
| **🕵️ Intelligence** | Shodan, Censys, ZoomEye, VirusTotal, AlienVault OTX, SecurityTrails |
| **🔓 Exploitation** | Reverse Shell Generator, Payload Customization, MSFVenom Integration |
| **📊 Reporting** | Professional HTML Reports, JSON Export, Vulnerability Scoring |
| **🥷 Stealth** | Random Delays, Header Randomization, Request Obfuscation |
| **🤖 AI Integration** | Machine Learning-based vulnerability detection and pattern recognition |
| **⚙️ Automation** | Automated scanning, exploitation, and reporting workflows |
| **🔐 Advanced Options** | Proxy support, Custom headers, Cookie management, SSL bypass |

---

## 🚀 INSTALLATION

### 📋 Prerequisites

```bash
# Python 3.8+ required
python3 --version

# Ensure pip is up to date
pip3 install --upgrade pip
```

### 📦 Install from Repository

```bash
# Clone the repository
git clone https://github.com/zeeshan-ux-AI/AuraxV3.git
cd AuraxV3

# Install required dependencies
pip3 install -r requirements.txt

# Make main script executable (Linux/Mac)
chmod +x aurax.py
```

### 📚 Dependencies

- **requests** - HTTP requests library
- **beautifulsoup4** - HTML/XML parsing
- **urllib3** - Advanced URL handling
- **colorama** - Terminal colors
- **pydantic** - Data validation
- **lxml** - XML processing
- **selenium** - Browser automation
- **cryptography** - Encryption support

---

## ⚡ QUICK START

### Basic Usage

```bash
# Run interactive menu
python3 aurax.py

# Scan a target URL
python3 aurax.py --target https://example.com --scan

# Full exploitation workflow
python3 aurax.py --target https://example.com --full-scan --report

# Generate reverse shell
python3 aurax.py --generate-shell --type bash --lhost 192.168.1.100 --lport 4444
```

### Command Line Arguments

```bash
python3 aurax.py -h              # Show help menu
python3 aurax.py --version        # Show version
python3 aurax.py --target <URL>   # Specify target
python3 aurax.py --scan           # Run scanning mode
python3 aurax.py --full-scan      # Complete vulnerability assessment
python3 aurax.py --report         # Generate report
python3 aurax.py --quiet          # Suppress output
python3 aurax.py --debug          # Enable debug mode
```

---

## 📖 USAGE GUIDE

### 1. Target Scanning

```bash
# Basic scan
python3 aurax.py --target https://target.com --scan

# Advanced scan with custom parameters
python3 aurax.py --target https://target.com --scan --timeout 30 --threads 10

# Scan specific port
python3 aurax.py --target https://target.com --port 8080 --scan
```

### 2. Vulnerability Testing

```bash
# Test SQL Injection
python3 aurax.py --target https://target.com --test sqli

# Test XSS vulnerabilities
python3 aurax.py --target https://target.com --test xss

# Test all vulnerabilities
python3 aurax.py --target https://target.com --test all
```

### 3. API Intelligence

```bash
# Search using Shodan API
python3 aurax.py --api shodan --query "Apache 2.4"

# Get data from Censys
python3 aurax.py --api censys --target 1.1.1.1

# VirusTotal lookup
python3 aurax.py --api virustotal --hash abc123...
```

### 4. Exploitation

```bash
# Generate custom payloads
python3 aurax.py --generate-payload --type sqli --param "id"

# Create reverse shell
python3 aurax.py --generate-shell --type bash --lhost <IP> --lport <PORT>

# MSFVenom integration
python3 aurax.py --msfvenom --payload windows/meterpreter/reverse_tcp
```

---

## 🎯 ATTACK VECTORS

### SQL Injection (SQLi)
```bash
python3 aurax.py --target https://target.com --test sqli --param username
# Tests for: UNION-based, Blind, Time-based, Stacked queries
```

### Cross-Site Scripting (XSS)
```bash
python3 aurax.py --target https://target.com --test xss --param search
# Tests for: Reflected, Stored, DOM-based XSS
```

### Local File Inclusion (LFI)
```bash
python3 aurax.py --target https://target.com --test lfi --param file
# Tests for: /etc/passwd, /etc/shadow, Log files
```

### Remote File Inclusion (RFI)
```bash
python3 aurax.py --target https://target.com --test rfi --param url
# Tests for: Remote PHP injection, Shell upload
```

### Server-Side Request Forgery (SSRF)
```bash
python3 aurax.py --target https://target.com --test ssrf --param url
# Tests for: Internal services, Metadata endpoints
```

### XML External Entity (XXE)
```bash
python3 aurax.py --target https://target.com --test xxe --content-type xml
# Tests for: Entity expansion, External entity inclusion
```

### NoSQL Injection (NoSQLi)
```bash
python3 aurax.py --target https://target.com --test nosqli --param query
# Tests for: MongoDB, CouchDB, Firebase payloads
```

### Command Injection
```bash
python3 aurax.py --target https://target.com --test cmd-inject --param command
# Tests for: ; | & backtick execution
```

---

## 🔗 API INTEGRATION

### Configure API Keys

Edit `config/api_keys.json`:

```json
{
  "shodan": "your_shodan_api_key",
  "censys": {
    "api_id": "your_censys_id",
    "api_secret": "your_censys_secret"
  },
  "virustotal": "your_virustotal_api_key",
  "alienvault": "your_otx_api_key",
  "securitytrails": "your_securitytrails_api_key",
  "zoomeyse": "your_zoomeyse_api_key"
}
```

### Using Intelligence APIs

```bash
# Shodan reconnaissance
python3 aurax.py --api shodan --query "nginx"

# Censys IP lookup
python3 aurax.py --api censys --ip 8.8.8.8

# VirusTotal domain check
python3 aurax.py --api virustotal --domain example.com

# AlienVault OTX threat intelligence
python3 aurax.py --api alienvault --hash <file_hash>

# SecurityTrails domain investigation
python3 aurax.py --api securitytrails --domain target.com

# ZoomEye scan
python3 aurax.py --api zoomeyse --query "webcam"
```

---

## ⚙️ CONFIGURATION

### Main Configuration File

Create/Edit `config/settings.json`:

```json
{
  "target": {
    "timeout": 30,
    "retries": 3,
    "threads": 5
  },
  "scanning": {
    "aggressive": false,
    "stealth_mode": true,
    "random_delay": [1, 5],
    "randomize_headers": true
  },
  "proxy": {
    "enabled": false,
    "type": "http",
    "address": "proxy.example.com:8080"
  },
  "output": {
    "format": "html",
    "generate_json": true,
    "include_screenshots": false
  },
  "logging": {
    "level": "INFO",
    "save_logs": true
  }
}
```

### Stealth Configuration

```bash
# Enable stealth mode
python3 aurax.py --stealth --target https://target.com

# Use proxy
python3 aurax.py --proxy "http://proxy.com:8080" --target https://target.com

# Custom headers
python3 aurax.py --headers "User-Agent: Mozilla/5.0" --target https://target.com
```

---

## 📊 REPORTING

### Generate Reports

```bash
# HTML report
python3 aurax.py --target https://target.com --full-scan --report --format html

# JSON export
python3 aurax.py --target https://target.com --full-scan --report --format json

# PDF report (requires wkhtmltopdf)
python3 aurax.py --target https://target.com --full-scan --report --format pdf
```

### Report Contents

- Executive Summary
- Vulnerability Severity Score
- Detailed Findings
- Proof of Concept
- Remediation Recommendations
- Technical Details
- Timeline

### Sample Report Output

```bash
python3 aurax.py --target https://example.com --full-scan --report
# Output: reports/example.com_2026-06-02_143022.html
```

---

## 🔧 ADVANCED FEATURES

### Custom Payloads

```bash
# Create custom SQL injection payload
python3 aurax.py --custom-payload --type sqli --payload "' OR '1'='1"

# Custom XSS payload
python3 aurax.py --custom-payload --type xss --payload "<img src=x onerror=alert('XSS')>"
```

### Automation Workflows

```bash
# Automated daily scanning
python3 aurax.py --schedule daily --target https://target.com --full-scan --report

# Batch scanning
python3 aurax.py --batch targets.txt --full-scan --report
```

### AI-Powered Detection

```bash
# Enable AI pattern recognition
python3 aurax.py --ai-detection --target https://target.com --scan
```

---

## 📝 EXAMPLES

### Scenario 1: Quick Website Audit

```bash
python3 aurax.py --target https://mywebsite.com --full-scan --report --format html
```

### Scenario 2: API Security Testing

```bash
python3 aurax.py --target https://api.example.com --test all --headers "Authorization: Bearer TOKEN"
```

### Scenario 3: Reconnaissance with Intelligence

```bash
python3 aurax.py --api shodan --query "site:example.com"
python3 aurax.py --api censys --target example.com
python3 aurax.py --target https://example.com --full-scan --report
```

### Scenario 4: Payload Generation

```bash
python3 aurax.py --generate-shell --type php --lhost 192.168.1.100 --lport 4444
python3 aurax.py --generate-payload --type sqli --database mysql
```

---

## 🤝 CONTRIBUTING

### Development Setup

```bash
# Clone repository
git clone https://github.com/zeeshan-ux-AI/AuraxV3.git
cd AuraxV3

# Create virtual environment
python3 -m venv venv
source venv/bin/activate  # Linux/Mac
# or
venv\Scripts\activate  # Windows

# Install dev dependencies
pip3 install -r requirements-dev.txt

# Run tests
pytest tests/
```

### Contribution Guidelines

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit changes (`git commit -m 'Add AmazingFeature'`)
4. Push to branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

### Code Standards

- Follow PEP 8 style guide
- Add docstrings to functions
- Include unit tests
- Update documentation

---

## 🐛 TROUBLESHOOTING

### Common Issues

**Q: "ModuleNotFoundError: No module named 'requests'"**
```bash
# Solution: Install missing dependencies
pip3 install -r requirements.txt
```

**Q: "SSL: CERTIFICATE_VERIFY_FAILED"**
```bash
# Solution: Disable SSL verification (use with caution)
python3 aurax.py --target https://target.com --no-ssl-verify
```

**Q: "Connection timeout"**
```bash
# Solution: Increase timeout value
python3 aurax.py --target https://target.com --timeout 60
```

**Q: "API key not working"**
```bash
# Solution: Verify API key configuration
python3 aurax.py --verify-api-keys
```

---

## 📞 SUPPORT

### Getting Help

- **Documentation**: [Wiki](https://github.com/zeeshan-ux-AI/AuraxV3/wiki)
- **Issues**: [GitHub Issues](https://github.com/zeeshan-ux-AI/AuraxV3/issues)
- **Discussions**: [GitHub Discussions](https://github.com/zeeshan-ux-AI/AuraxV3/discussions)

### Reporting Bugs

Please include:
1. Python version (`python3 --version`)
2. OS information
3. Exact command that failed
4. Error message and traceback
5. Steps to reproduce

---

## 📄 LICENSE

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

---

## ⚖️ LEGAL NOTICE

**IMPORTANT:** This tool should only be used for:
- ✅ Educational purposes
- ✅ Authorized penetration testing
- ✅ Testing on your own systems
- ✅ Systems with written permission

**Prohibited use:**
- ❌ Unauthorized access to systems
- ❌ Illegal hacking activities
- ❌ Testing without explicit written permission
- ❌ Any malicious purposes

Users are solely responsible for their actions. The author assumes no liability for misuse.

---

## 🙏 ACKNOWLEDGMENTS

Special thanks to:
- Security research community
- Open source contributors
- Bug reporters and testers

---

## 📊 Repository Stats

![GitHub stars](https://img.shields.io/github/stars/zeeshan-ux-AI/AuraxV3?style=social)
![GitHub forks](https://img.shields.io/github/forks/zeeshan-ux-AI/AuraxV3?style=social)
![GitHub watchers](https://img.shields.io/github/watchers/zeeshan-ux-AI/AuraxV3?style=social)

---

<div align="center">

**Made with ❤️ by Zeeshan**

⭐ If you found this helpful, please consider giving it a star!

[⬆ Back to Top](#-aurax-nuclear-v30---ai-powered-pentesting-framework)

</div>
