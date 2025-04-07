# 🛡️ WebInfoGather

## // OFFENSIVE RECONNAISSANCE UTILITY

This Python-based offensive security tool performs comprehensive web enumeration to gather critical intelligence about target domains. Designed for penetration testers, security researchers, and ethical hackers, this utility automates the reconnaissance phase of security assessments by extracting valuable target information.

## ⚠️ LEGAL DISCLAIMER

**FOR AUTHORIZED USE ONLY**. This tool should be used exclusively on systems you own or have explicit permission to test. Unauthorized scanning may violate computer crime laws. The developers assume no liability for misuse.

## 🔍 CAPABILITIES

- **Target Identification**: Resolves domain to IP address for target confirmation
- **HTTP Header Analysis**: Extracts server information and security headers
- **WHOIS Intelligence Gathering**: Retrieves domain registration data and ownership intelligence
- **CMS Fingerprinting**: Identifies underlying Content Management Systems
- **Port Reconnaissance**: Scans for open ports and running services
- **Robots.txt Analysis**: Checks for restricted directories and information disclosure
- **Subdomain Enumeration**: Discovers potential attack surfaces through subdomain mapping
- **XSS Vulnerability Scanning**: Tests for potential Cross-Site Scripting weaknesses

## 🛠️ INSTALLATION

### Prerequisites
- Python 3.x
- Administrative/root privileges (for certain scanning features)

### Deployment
```bash
# Clone the repository
git clone https://github.com/who0xac/WebInfoGather.git

# Navigate to directory
cd WebInfoGather

# Install dependencies
pip install -r requirements.txt
```

## 🚀 EXECUTION

```bash
python3 webinfogather.py --target example.com --aggressive --output report.txt
```

### Command Arguments
```
--target        Target domain to enumerate
--port-range    Range of ports to scan (default: 1-1000)
--timeout       Connection timeout in seconds (default: 5)
--threads       Number of concurrent threads (default: 10)
--aggressive    Enable aggressive scanning mode
--output        Save results to specified file
--no-color      Disable colored output
```

## 🔧 MODULES

| Module | Description | Status |
|--------|-------------|--------|
| IP Resolver | Maps hostname to IP address | Operational |
| Header Scanner | Analyzes HTTP response headers | Operational |
| WHOIS Client | Retrieves domain registration data | Operational |
| CMS Detector | Identifies Content Management Systems | Operational |
| Port Scanner | Detects open ports and services | Operational |
| Robots Analyzer | Examines robots.txt for sensitive paths | Operational |
| Subdomain Brute | Discovers subdomains through wordlist | Operational |
| XSS Tester | Tests for Cross-Site Scripting vulnerabilities | Operational |

## 📋 SAMPLE OUTPUT

```
[+] TARGET: example.com
[+] IP ADDRESS: 93.184.216.34
[+] HTTP HEADERS:
    [*] Server: ECS (dcb/7EC5)
    [*] Content-Type: text/html
    [*] X-Frame-Options: DENY
[+] WHOIS INFO:
    [*] Registrar: IANA
    [*] Creation Date: 1995-08-14T04:00:00Z
[+] CMS DETECTED: None
[+] OPEN PORTS:
    [*] 80/tcp - HTTP
    [*] 443/tcp - HTTPS
[+] ROBOTS.TXT: Present
    [*] Disallowed: /admin/
    [*] Disallowed: /wp-admin/
[+] SUBDOMAINS:
    [*] dev.example.com - 93.184.216.34
    [*] mail.example.com - 93.184.216.34
[+] XSS VULNERABILITY: Not Detected
```

## ⚡ ADVANCED USAGE

### Silent Mode
```bash
python3 webinfogather.py --target example.com --silent --output report.json
```

### Targeted Scans
```bash
python3 webinfogather.py --target example.com --modules ip,headers,ports
```

### Integration with Other Tools
```bash
python3 webinfogather.py --target example.com --output results.xml --format nmap
```

## 🔒 SECURITY CONSIDERATIONS

- Use a VPN or proxy to anonymize your scanning activities
- Implement rate limiting to avoid triggering IDS/IPS systems
- Consider legal implications before scanning any target
- Review and understand all data before including in reports

## 💻 COMPATIBILITY

- Kali Linux (Primary Support)
- Ubuntu/Debian
- Arch Linux
- macOS
- Windows (via WSL)

## 🤝 CONTRIBUTING

Security researchers are encouraged to contribute to this offensive security tool:

1. Fork the repository
2. Create your feature branch (`git checkout -b feature/advanced-scanning`)
3. Commit your changes (`git commit -m 'Add advanced port scanning capability'`)
4. Push to the branch (`git push origin feature/advanced-scanning`)
5. Open a Pull Request

## 📜 LICENSE

[Include your license information here]

## 📞 CONTACT

who0xac - [GitHub Profile](https://github.com/who0xac)

Project Repository: [https://github.com/who0xac/WebInfoGather](https://github.com/who0xac/WebInfoGather)

---

*WebInfoGather - Intelligence gathering for the security professional.*
