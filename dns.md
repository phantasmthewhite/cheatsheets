```
dig -t AXFR <URL> @<DNS SERVER IP> (Zone transfert)
dig -t RRSIG <URL> @<DNS SERVER IP> (DNSSEC)
dig -t NSEC3PARAM <URL> @<DNS SERVER IP> (Salt)
dig -t DNSKEY <URL> @<DNS SERVER IP> (DNS Key)
nmap -R -sL --dns-servers <IP> -Pn <IP RANGE> | grep "("
```
