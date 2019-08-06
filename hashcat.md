### MD5 (bruteforce)
* -a 3 = brute-force
* -m 0 = hash MD5
* -1   = le char set qu'on veut utiliser
* ?1   = le nombre de char du PW + le charset qu'on veut utiliser tel que défini par le -1 d'avant

Soit :

`hashcat -a 3 -m 0 -1 ab123 digest.txt ?1?1?1?1?1`
