# Nmap Network Scanning Report

## Objective
To identify active hosts, open ports, services and operating system information.

## Target Details

- Target IP: 192.168.56.101
- Operating System: Metasploitable2
- Scanner: Kali Linux
- Tool: Nmap

## Commands Performed

### 1. Host Discovery
nmap -sn 192.168.56.0/24

### 2. TCP SYN Scan
sudo nmap -sS 192.168.56.101

### 3. UDP Scan
sudo nmap -sU 192.168.56.101

### 4. Service Version Detection
nmap -sV 192.168.56.101

### 5. OS Detection
sudo nmap -O 192.168.56.101

### 6. Save Scan Results
sudo nmap -sS -sV -O -oN nmap_report.txt 192.168.56.101

## Results

Update this section using your actual Nmap output.

| Port | Protocol | Service | State |
|---|---|---|---|
| Add actual result | TCP/UDP | Add service | Open/Closed |

## Observations

- Active target identification.
- Open port discovery.
- Service identification.
- Operating system detection.

## Conclusion

Nmap helps identify exposed network services and provides information useful for security assessment.
