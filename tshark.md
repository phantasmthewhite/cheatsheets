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

# Champ "SID" dans une trame vers une URL spécifique (-x data en hexa)
tshark -r HTTP_traffic.pcap -R 'frame contains "/1/batch/1/OE"' -2 -x | grep sid

# Compter le nombre de trames de protocole RTP
tshark -r VoIP_traffic.pcap -z io,phs,rtp -q

# Compter le nombre de trames RTP concernant un SSRC donné
tshark -r VoIP_traffic.pcap -R '(ip.src==192.168.10.15 && ip.dst==208.51.63.146) && (udp.port==48268 && udp.port==19138)' -2
```
