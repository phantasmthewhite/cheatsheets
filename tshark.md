```
# Afficher les 100 premiers paquets d'une capture
tshark -r HTTP_traffic.pcap -c 100
# Afficher les paquets avec hiérarchie
tshark -r HTTP_traffic.pcap -z io,phs -q
# Afficher les BSSID uniques d'une capture
tshark -r WiFi_traffic.pcap -Tfields -e wlan.bssid | sort -u
```
