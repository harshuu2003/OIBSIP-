# Task 1: Basic Network Scanning with Nmap

**Internship:** Oasis Infobyte  
**Track:** Cyber Security – Security Analyst  
**Task:** Basic Network Scanning with Nmap  
**Tool:** Nmap 7.993  
**Platform:** Windows

## Objective
To perform network scanning on a local machine using Nmap, identify open ports and services, and understand their potential security risks.

## What is Nmap?
Nmap (Network Mapper) is an open-source network discovery and security auditing tool. It helps identify active hosts, open ports, running services, and possible operating system information.

## Why is Network Scanning Important?
- Identifies open ports and running services.
- Helps administrators understand network exposure.
- Supports security auditing and asset discovery.
- Helps identify services that may need restriction or updates.

## Installation
1. Download Nmap from https://nmap.org/download.html.
2. Run the Windows installer.
3. Follow the installation wizard.
4. Keep the Npcap installation option enabled if prompted.
5. Open Command Prompt and verify installation using `nmap --version`.

## Scan Commands Used

**Basic scan**
```cmd
nmap 192.168.31.213
```

**Service version detection**
```cmd
nmap -sV 192.168.31.213
```

**Operating system detection**
```cmd
nmap -O 192.168.31.213
```

**Port verification**
```cmd
nmap -sV -p 6646,7070 192.168.31.213
```

## Results
The initial basic scan identified six open TCP ports: 135, 139, 445, 3306, 6646, and 7070.

The service scan identified Windows RPC, NetBIOS, MySQL, and probable RealServer service labels. Port 6646 was closed during the later verification scan.

The OS detection scan suggested Microsoft Windows 11, but did not provide an exact confirmed match.

See `nmap_scan_results.txt` for detailed findings.

## Potential Security Risks
- RPC and NetBIOS services should be restricted to trusted networks.
- SMB should be updated and securely configured.
- MySQL should not be accessible to untrusted networks.
- The application using port 7070 should be identified and reviewed.

## Ethical Guidelines
- Scan only systems you own or have explicit permission to test.
- Do not scan external or production systems without authorization.
- Perform security testing responsibly.
- Do not attempt unauthorized access to discovered services.

## Project Files
- `basic_scan.txt` – Basic Nmap scan output.
- `service_scan.txt` – Service detection output.
- `os_detection.txt` – OS detection output.
- `nmap_scan_results.txt` – Detailed findings and security analysis.
- `Screenshots` – Terminal screenshots of the scans.

## Conclusion
This task provided practical experience with Nmap and helped identify network services running on a local Windows machine. It also demonstrated why open ports should be reviewed and secured.
