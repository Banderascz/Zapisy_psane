Připojení ke switchy pomocí Telnetu
Ve switchy
```
enable
conf t
line vty 0 15
#napojeni na seriovou linku asi
password 12345 
#heslo může být cokoli, hlavně něco ať to je něco jednoduchého
exit
```

Heslo do ENABLE šifrované (Hash)
```
enable secret cisco
```

V terminálu tty2
```
telnet 192.168.1.72 
#to je ip adresa switche
```

Pokud chci aby se šifrovaly hesla pomocí password příkazu (musí být v "conf t")
```
service password-encryption
```

Pokud to chci zrušit
```
no service password-encryption
```
