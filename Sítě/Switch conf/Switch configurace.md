Před vstupem do Switche
```
ifconfig eth0 192.168.1.40
//Přepojit žlutý kabel do bílý rack
microcom /dev/ttyS1
no
```
automaticky udělám v terminálu switche
```
enable
conf t
hostname Switch_4B
```
**CTRL + Z** = se dostanu o úroveň "víš" (blíž k "rootu")
HESLO do ENABLE!!! (dělá se v conf t)
```
enable password cisco
```
Heslo do ENABLE šifrované (Hash)
```
enable secret cisco
```
Zrušení hesla
```
no enable password
```
Zobrazení aktuální konfigurace(musím být v "root" switche)
```
show run
```
V conf t nastavení ip adresa switche
```
interface vlan 1
ip address 192.168.1.72 255.255.255.0 #to 72 je moje číslo 40 + 32
no shutdown
```
Vypnutí mačkat CTRL+Z nebo psát exit nakonec CTRL+X => přesun do terminálu
Nastavení portů na portů na protected - 2 protected porty spolu nemůžou komunikovat
```
conf t
interface fastEthernet0/1
switchport protected
```