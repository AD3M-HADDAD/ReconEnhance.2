```bash
nmap -vv --reason -Pn -T4 -sV --script vuln -A --osscan-guess -oN "/media/adam/3268e159-c01d-4551-8089-f31f5ad8a3c7/ReconEnhance/results/10.129.148.12/scans/nmap_vuln.txt" -oX "/media/adam/3268e159-c01d-4551-8089-f31f5ad8a3c7/ReconEnhance/results/10.129.148.12/scans/xml/nmap_vuln.xml" 10.129.148.12

nmap -vv --reason -Pn -T4 -sV -sC --version-all -A --osscan-guess -oN "/media/adam/3268e159-c01d-4551-8089-f31f5ad8a3c7/ReconEnhance/results/10.129.148.12/scans/_quick_tcp_nmap.txt" -oX "/media/adam/3268e159-c01d-4551-8089-f31f5ad8a3c7/ReconEnhance/results/10.129.148.12/scans/xml/_quick_tcp_nmap.xml" 10.129.148.12

nmap -vv --reason -Pn -T4 -sV -sC --version-all -A --osscan-guess -p- -oN "/media/adam/3268e159-c01d-4551-8089-f31f5ad8a3c7/ReconEnhance/results/10.129.148.12/scans/_full_tcp_nmap.txt" -oX "/media/adam/3268e159-c01d-4551-8089-f31f5ad8a3c7/ReconEnhance/results/10.129.148.12/scans/xml/_full_tcp_nmap.xml" 10.129.148.12

nmap -vv --reason -Pn -T4 -sV -sC  -p 21 --script="ftp-anon" -oN "/media/adam/3268e159-c01d-4551-8089-f31f5ad8a3c7/ReconEnhance/results/10.129.148.12/scans/tcp21/tcp_21_ftp_anonymousLogin_nmap.txt" -oX "/media/adam/3268e159-c01d-4551-8089-f31f5ad8a3c7/ReconEnhance/results/10.129.148.12/scans/tcp21/xml/tcp_21_ftp_nmap.xml" 10.129.148.12

nmap -vv --reason -Pn -T4 -sV -p 21 --script="banner,ftp-anon" -oN "/media/adam/3268e159-c01d-4551-8089-f31f5ad8a3c7/ReconEnhance/results/10.129.148.12/scans/tcp21/tcp_21_ftp_nmap.txt" -oX "/media/adam/3268e159-c01d-4551-8089-f31f5ad8a3c7/ReconEnhance/results/10.129.148.12/scans/tcp21/xml/tcp_21_ftp_nmap.xml" 10.129.148.12


```