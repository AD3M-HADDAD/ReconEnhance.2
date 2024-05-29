```bash
nmap -vv --reason -Pn -T4 -sV -sC --version-all -A --osscan-guess -oN "/media/adam/3268e159-c01d-4551-8089-f31f5ad8a3c7/ReconEnhance/results/10.129.148.12/scans/_quick_tcp_nmap.txt" -oX "/media/adam/3268e159-c01d-4551-8089-f31f5ad8a3c7/ReconEnhance/results/10.129.148.12/scans/xml/_quick_tcp_nmap.xml" 10.129.148.12
```

[/media/adam/3268e159-c01d-4551-8089-f31f5ad8a3c7/ReconEnhance/results/10.129.148.12/scans/_quick_tcp_nmap.txt](file:///media/adam/3268e159-c01d-4551-8089-f31f5ad8a3c7/ReconEnhance/results/10.129.148.12/scans/_quick_tcp_nmap.txt):

```
# Nmap 7.94SVN scan initiated Tue May 28 00:01:37 2024 as: nmap -vv --reason -Pn -T4 -sV -sC --version-all -A --osscan-guess -oN /media/adam/3268e159-c01d-4551-8089-f31f5ad8a3c7/ReconEnhance/results/10.129.148.12/scans/_quick_tcp_nmap.txt -oX /media/adam/3268e159-c01d-4551-8089-f31f5ad8a3c7/ReconEnhance/results/10.129.148.12/scans/xml/_quick_tcp_nmap.xml 10.129.148.12
Nmap scan report for 10.129.148.12
Host is up, received user-set (0.069s latency).
Scanned at 2024-05-28 00:01:38 CET for 4s
Not shown: 999 closed tcp ports (conn-refused)
PORT   STATE SERVICE REASON  VERSION
21/tcp open  ftp     syn-ack vsftpd 3.0.3
| ftp-syst: 
|   STAT: 
| FTP server status:
|      Connected to ::ffff:10.10.15.71
|      Logged in as ftp
|      TYPE: ASCII
|      No session bandwidth limit
|      Session timeout in seconds is 300
|      Control connection is plain text
|      Data connections will be plain text
|      At session startup, client count was 4
|      vsFTPd 3.0.3 - secure, fast, stable
|_End of status
| ftp-anon: Anonymous FTP login allowed (FTP code 230)
|_-rw-r--r--    1 0        0              32 Jun 04  2021 flag.txt
Service Info: OS: Unix

Read data files from: /usr/bin/../share/nmap
Service detection performed. Please report any incorrect results at https://nmap.org/submit/ .
# Nmap done at Tue May 28 00:01:42 2024 -- 1 IP address (1 host up) scanned in 4.47 seconds

```
