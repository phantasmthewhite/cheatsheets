Updated script list: https://nmap.org/nsedoc/

### Scann complet avec version des services 
`nmap -sS -sV -p- -T4 -v <IP>`

### DNS
`nmap -R -sL --dns-servers <IP> -Pn <IP RANGE> | grep "("`
