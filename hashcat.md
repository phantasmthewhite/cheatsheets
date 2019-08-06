### Bruteforce (-a 3)
## MD5
* -1   = le char set qu'on veut utiliser
* ?1   = le nombre de char du PW + le charset qu'on veut utiliser tel que défini par le -1 d'avant

`hashcat -a 3 -m 0 -1 ab123 digest.txt ?1?1?1?1?1`

## NTLM
`hashcat -a 3 -m 1000 digest.txt`

### Straight (-a 0)
## Salted MD5
`hashcat -a 0 -m 10 hash.txt 1000000-password-seclists.txt`
