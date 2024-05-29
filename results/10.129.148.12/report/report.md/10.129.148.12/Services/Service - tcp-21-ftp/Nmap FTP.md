```bash
nmap -vv --reason -Pn -T4 -sV -p 21 --script="banner,ftp-anon" -oN "/media/adam/3268e159-c01d-4551-8089-f31f5ad8a3c7/ReconEnhance/results/10.129.148.12/scans/tcp21/tcp_21_ftp_nmap.txt" -oX "/media/adam/3268e159-c01d-4551-8089-f31f5ad8a3c7/ReconEnhance/results/10.129.148.12/scans/tcp21/xml/tcp_21_ftp_nmap.xml" 10.129.148.12
```

[/media/adam/3268e159-c01d-4551-8089-f31f5ad8a3c7/ReconEnhance/results/10.129.148.12/scans/tcp21/tcp_21_ftp_nmap.txt](file:///media/adam/3268e159-c01d-4551-8089-f31f5ad8a3c7/ReconEnhance/results/10.129.148.12/scans/tcp21/tcp_21_ftp_nmap.txt):

```
# Nmap 7.94SVN scan initiated Tue May 28 00:01:52 2024 as: nmap -vv --reason -Pn -T4 -sV -p 21 --script=banner,ftp-anon -oN /media/adam/3268e159-c01d-4551-8089-f31f5ad8a3c7/ReconEnhance/results/10.129.148.12/scans/tcp21/tcp_21_ftp_nmap.txt -oX /media/adam/3268e159-c01d-4551-8089-f31f5ad8a3c7/ReconEnhance/results/10.129.148.12/scans/tcp21/xml/tcp_21_ftp_nmap.xml 10.129.148.12
Nmap scan report for 10.129.148.12
Host is up, received user-set (0.071s latency).
Scanned at 2024-05-28 00:01:52 CET for 1s

PORT   STATE SERVICE REASON  VERSION
21/tcp open  ftp     syn-ack vsftpd 3.0.3
| ftp-anon: Anonymous FTP login allowed (FTP code 230)
|_-rw-r--r--    1 0        0              32 Jun 04  2021 flag.txt
|_banner: 220 (vsFTPd 3.0.3)
Service Info: OS: Unix

Read data files from: /usr/bin/../share/nmap
Service detection performed. Please report any incorrect results at https://nmap.org/submit/ .
# Nmap done at Tue May 28 00:01:53 2024 -- 1 IP address (1 host up) scanned in 1.27 seconds

```
