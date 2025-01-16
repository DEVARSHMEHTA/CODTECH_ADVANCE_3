# CODTECH_ADVANCE_3
# Pentest Toolkit
## Details
- Name    : Devarsh Mehta
- Company : CODTECH IT SOLUTIONS PVT.LTD
- ID      : CT08DAL
- Domain  : Cyber Security & Ethical Hacking
- Duration: 20th Dec 2024 To 20th Jan 2025
- Mentor  : Neela Santhosh Kumar

# Overview
Pentest Toolkit is a Python-based penetration testing script that includes multiple modules for conducting security assessments. This toolkit currently supports:

1. **Port Scanning**
2. **SSH Brute-Force Attacks**

## Features

- **Port Scanner:** Scans a range of ports on a target and displays open ports along with banners (if available).
- **SSH Brute-Force Attack:** Attempts to brute-force SSH credentials using a provided username and password list.

## Prerequisites

Ensure you have Python installed on your system. You can download it from [python.org](https://www.python.org/).

### Required Python Libraries

Install the following libraries before running the script:

```bash
pip install pyfiglet paramiko colorama
```

## Installation

```sh
git clone https://github.com/DEVARSHMEHTA/CODTECH_ADVANCE_3.git
```

```sh
cd CODTECH_ADVANCE_3
```

```sh
pip install -r requirements.txt
```

```sh
chmod +x Pentest-toolkit.py
```

```sh
python3 Pentest-toolkit.py
```

## Usage

### Running the Toolkit

To start the toolkit, run the following command:

```bash
python pentest_toolkit.py
```

You will be prompted to select a module:

1. **Port Scanner**
2. **Brute Forcer**

### Port Scanner

The port scanner allows you to scan a range of ports on a target.

#### Steps:

1. Select **1** for Port Scanner.
2. Enter the target's IP address or domain name.
3. Specify the start and end ports for the scan.

#### Example Output:

![image](https://github.com/user-attachments/assets/cc0da957-c007-441d-a4e2-835a1c9b2220)


### SSH Brute-Force Attack

The brute-force module attempts to log in to an SSH server using a username and a list of passwords.

#### Steps:

1. Select **2** for Brute Forcer.
2. Enter the target's IP address or domain name.
3. Provide the username to brute-force.
4. Enter the path to the password list file.

#### Example Output:

![image](https://github.com/user-attachments/assets/47a274e1-9600-46fa-a0f0-07479c694bb5)


## Script Structure

### Common Ports

The script includes a dictionary of common port numbers and their corresponding protocols. You can expand this dictionary as needed:

```python
common_ports = {
    21: "FTP",
    22: "SSH",
    23: "Telnet",
    25: "SMTP",
    53: "DNS",
    80: "HTTP",
    110: "POP3",
    143: "IMAP",
    443: "HTTPS",
    3306: "MySQL",
    3389: "RDP",
    8080: "HTTP Proxy"
}
```

### Functions

- **`resolve_host(target)`**: Resolves a domain name to an IP address.
- **`banner_grabbing(ip, port)`**: Attempts to grab the service banner from an open port.
- **`scan_port(ip, port)`**: Checks if a specific port is open.
- **`port_scan(target, start_port, end_port)`**: Scans a range of ports.
- **`brute_force_attack(target, username, password_list)`**: Performs brute-force attacks on an SSH server.

### Error Handling

The script handles common errors such as:
- Invalid host resolution
- Connection timeouts
- File read errors for the password list

## Disclaimer

This toolkit is for educational purposes only. Unauthorized use of this script against systems you do not own or have explicit permission to test is illegal and unethical. The creators are not responsible for any misuse of this tool.


## Author
- Devarsh Mehta
