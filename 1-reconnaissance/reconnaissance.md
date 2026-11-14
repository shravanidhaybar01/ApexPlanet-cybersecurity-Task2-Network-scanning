# Reconnaissance

## Objective
To understand how information about a target can be collected before network security testing.

## Tools
- WHOIS
- Nslookup
- Google Dorking
- Shodan
- Ping
- Netcat

## Commands

### WHOIS
whois example.com

### DNS Lookup
nslookup example.com

### Ping
ping -c 4 192.168.56.101

### Host Discovery
nmap -sn 192.168.56.0/24

### Netcat Banner Grabbing
nc -nv 192.168.56.101 21

## Observations

Record the information collected during reconnaissance.

- Domain information:
- DNS information:
- Active hosts:
- Identified service banners:

## Conclusion

Reconnaissance helps understand the target environment and provides useful information before performing detailed network scanning.
