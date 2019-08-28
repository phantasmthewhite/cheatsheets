### Scan de serveurs DNS
`nmap -R -sL --dns-servers <IP> -Pn <IP RANGE> | grep "("`
  
### Transfert de zone
`dig -t AXFR <URL> @<DNS SERVER IP>`

### DNSSEC
`dig -t RRSIG <URL> @<DNS SERVER IP> (DNSSEC)`

### Salt NSEC3
`dig -t NSEC3PARAM <URL> @<DNS SERVER IP> (Salt)`

### DNS Key
`dig -t DNSKEY <URL> @<DNS SERVER IP> (DNS Key)`

`dig @10.13.37.10 hostname.bind txt chaos`

`dig @10.13.37.10 version.bind txt chaos`

### Requête inverse (reverse lookup)
`dig -x 10.13.37.10 @10.13.37.10`

