Vytvoření usera
```
enable
conf t
username Petr secret 12345
#jmeno a heslo je jedno
```

Připojení k doméně (conf t)
```
ip domain-name sps-jia.cz
crypto key gen
2048
```

v tty2 ssh
```
ssh -l Petr 192.168.1.72
#pokud bude potřeba tak povolení kex...
ssh -l Petr 192.168.1.72 -o kexalgorithms=diffie-hellman-group1-sha1
#to kex... je nastavení menšího zabezpečení(šifrování) sha1 :D
yes
```
