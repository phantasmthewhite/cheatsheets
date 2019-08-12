### setuid

find /bin -perm -4000

find / -user root -perm -4000 -exec ls -ldb {} \;

Eventually `strings` on the said SUID file to see its interactions with other files and modify those files instead.
