### Bruteforce (MD5)
* -a 3 = brute-force
* -m 0 = hash MD5
* -1   = le char set qu'on veut utiliser
* ?1   = le nombre de char du PW + le charset qu'on veut utiliser tel que défini par le -1 d'avant

Soit :

`hashcat -a 3 -m 0 -1 ab123 digest.txt ?1?1?1?1?1`

### Straight (Salted MD5)
* -a 0 = straight attack
* -m 10 = salted MD5

Soit:

`hashcat -a 0 -m 10 hash.txt 1000000-password-seclists.txt`
