### airodump-ng
Capture raw 802.11 frames

```
airodump-ng -r WEP-Cracking.cap
```

Gives us an SSID and a MAC address, which we can use in aircrack-ng.

### aircrack-ng
802.11 WEP and WPA/WPA2-PSK key cracking program

```
aircrack-ng -b 00:21:91:d2:8e:25 WEP-Cracking.cap
```
```
aircrack-ng -w 1000000-password-seclists.txt -b 00:21:91:d2:8e:25  WPA-PSK.pcap
```
