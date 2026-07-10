# Nmap Command Cheat Sheet

A quick reference guide for common Nmap commands used in network scanning and penetration testing.

---

## Basic Scan

```bash
nmap <target>
```

Example:

```bash
nmap 192.168.1.1
```

---

## Scan Specific Ports

```bash
nmap -p 22,80,443 <target>
```

---

## Scan All Ports

```bash
nmap -p- <target>
```

---

## Service Version Detection

```bash
nmap -sV <target>
```

---

## Default Script Scan

```bash
nmap -sC <target>
```

---

## Aggressive Scan

```bash
nmap -A <target>
```

---

## SYN Scan (Stealth)

```bash
sudo nmap -sS <target>
```

---

## UDP Scan

```bash
sudo nmap -sU <target>
```

---

## OS Detection

```bash
sudo nmap -O <target>
```

---

## Ping Scan (Host Discovery)

```bash
nmap -sn <target>
```

---

## Scan Multiple Targets

```bash
nmap 192.168.1.1 192.168.1.2
```

---

## Scan an Entire Subnet

```bash
nmap 192.168.1.0/24
```

---

## Save Results

Normal output

```bash
nmap -oN scan.txt <target>
```

XML output

```bash
nmap -oX scan.xml <target>
```

All formats

```bash
nmap -oA scan <target>
```

---

## Increase Scan Speed

```bash
nmap -T4 <target>
```

---

## Verbose Mode

```bash
nmap -v <target>
```

Very Verbose

```bash
nmap -vv <target>
```

---

## Disable Ping

```bash
nmap -Pn <target>
```

---

## Common Enumeration Command

```bash
nmap -sC -sV <target>
```

---

## Full TCP Scan

```bash
nmap -p- -sC -sV <target>
```

---

## Useful NSE Scripts

SMB

```bash
nmap --script smb-enum-shares <target>
```

FTP Anonymous Login

```bash
nmap --script ftp-anon <target>
```

HTTP Title

```bash
nmap --script http-title <target>
```

HTTP Enumeration

```bash
nmap --script http-enum <target>
```

SSH Algorithms

```bash
nmap --script ssh2-enum-algos <target>
```

---

## Useful Commands for HTB & TryHackMe

```bash
nmap -sC -sV <target>

nmap -p- --min-rate 1000 <target>

nmap -A <target>

nmap -Pn -sC -sV <target>

sudo nmap -sS -sV -O <target>
```

---

## Author

**Amaljith A S**

Learning Cyber Security through:
- Hack The Box
- TryHackMe
- PortSwigger Labs
