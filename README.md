# Task 1 - Network Port Scanning with Nmap

## Objective
Scan local network to find open ports and understand network exposure.

## Tools Used
- Nmap
- Zenmap (GUI)

## Scan Details
- **Target Range**: 192.168.220.0/24
- **Scan Type**: TCP SYN Scan
- **Hosts Found**: 6 devices up
- **Time Taken**: 50.38 seconds

## Devices & Open Ports Found

| IP Address | Status | Open Ports | Device Type |
|---|---|---|---|
| 192.168.220.1 | Up | 443, 8800 | Router (TP-Link) |
| 192.168.220.36 | Up | 135, 139, 445, 3580 | Laptop (Windows) |
| 192.168.220.37 | Up | All ignored | Unknown Device |
| 192.168.220.38 | Up | Filtered | Intel Device |
| 192.168.220.39 | Up | All ignored | Xiaomi Phone |

## Key Findings
- **Router**: Has HTTPS (443) and admin panel (8800) exposed
- **Laptop**: Windows file sharing ports (135, 139, 445) are open
- **Other devices**: Have firewalls or no services running

## Security Risks Identified
1. Open ports on router could be exploited
2. File sharing ports expose network resources
3. Need firewall rules to restrict access

## Conclusion
Successfully performed TCP SYN scan to identify active hosts and their open ports on the local network.
