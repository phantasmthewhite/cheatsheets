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

### asleap
Actively recover LEAP/PPTP passwords

```
asleap -W 1000000-password-seclists.txt -C c9:db:48:a9:7b:0e:e9:04 -R bb:c9:cf:16:27:bc:ee:16:7e:21:3a:59:4c:1c:97:d1:25:10:af:d7:81:6e:88:87
```

Ou `-C` est le challenge, et `-R` la réponse.
