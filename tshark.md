```
# Afficher les 100 premiers paquets d'une capture
tshark -r HTTP_traffic.pcap -c 100

# Afficher 10 paquets à partir du 100ème
tshark -r <file> -x -c 10 -R frame.number>=100

# Afficher les paquets avec hiérarchie
tshark -r HTTP_traffic.pcap -z io,phs -q

# Afficher les BSSID uniques d'une capture
tshark -r WiFi_traffic.pcap -Tfields -e wlan.bssid | sort -u

# HTTP GET
tshark -r HTTP_traffic.pcap -z "io,stat,0,COUNT(http.request.method)http.request.method=="GET""

# HTTP "200 OK"
tshark -r HTTP_traffic.pcap -R 'frame contains "HTTP/1.1 200 OK"' -2

# URL
tshark -r HTTP_traffic.pcap -R "http.host==www.alexa.com" -2
```
