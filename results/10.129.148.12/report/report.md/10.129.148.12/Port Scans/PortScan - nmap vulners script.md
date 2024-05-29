```bash
nmap -vv --reason -Pn -T4 -sV --script vuln -A --osscan-guess -oN "/media/adam/3268e159-c01d-4551-8089-f31f5ad8a3c7/ReconEnhance/results/10.129.148.12/scans/nmap_vuln.txt" -oX "/media/adam/3268e159-c01d-4551-8089-f31f5ad8a3c7/ReconEnhance/results/10.129.148.12/scans/xml/nmap_vuln.xml" 10.129.148.12
```

[/media/adam/3268e159-c01d-4551-8089-f31f5ad8a3c7/ReconEnhance/results/10.129.148.12/scans/nmap_vuln.txt](file:///media/adam/3268e159-c01d-4551-8089-f31f5ad8a3c7/ReconEnhance/results/10.129.148.12/scans/nmap_vuln.txt):

```
# Nmap 7.94SVN scan initiated Tue May 28 00:01:30 2024 as: nmap -vv --reason -Pn -T4 -sV --script vuln -A --osscan-guess -oN /media/adam/3268e159-c01d-4551-8089-f31f5ad8a3c7/ReconEnhance/results/10.129.148.12/scans/nmap_vuln.txt -oX /media/adam/3268e159-c01d-4551-8089-f31f5ad8a3c7/ReconEnhance/results/10.129.148.12/scans/xml/nmap_vuln.xml 10.129.148.12
Nmap scan report for 10.129.148.12
Host is up, received user-set (0.070s latency).
Scanned at 2024-05-28 00:01:41 CET for 4s
Not shown: 999 closed tcp ports (conn-refused)
PORT   STATE SERVICE REASON  VERSION
21/tcp open  ftp     syn-ack vsftpd 3.0.3
| vulners: 
|   cpe:/a:vsftpd:vsftpd:3.0.3: 
|     	PRION:CVE-2021-3618	5.8	https://vulners.com/prion/PRION:CVE-2021-3618
|_    	PRION:CVE-2021-30047	5.0	https://vulners.com/prion/PRION:CVE-2021-30047
Service Info: OS: Unix

Read data files from: /usr/bin/../share/nmap
Service detection performed. Please report any incorrect results at https://nmap.org/submit/ .
# Nmap done at Tue May 28 00:01:45 2024 -- 1 IP address (1 host up) scanned in 14.89 seconds

```
