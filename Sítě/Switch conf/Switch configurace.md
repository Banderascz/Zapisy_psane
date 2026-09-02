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
Pro vypnutí protected
```
conf t
interface fastEthernet0/1
no switchport protected
```
Portsecurity - povolení je nějakých MAC adres (whitelist) - sticky učící mód (default)
```
conf t
interface fastEthernet0/1
switchport port-security mac-address sticky
```
nastavení maximum 5 adres na naučení
```
conf t
interface fastEthernet0/1
switchport port-security mac-address maximum 5
```
nastavení **violation** - protect=zahodí rámec, restrict=pošle zprávu správci, shutdown=schodí rámec pro port pro všechny, dokud ho někdo nezapne. 
```
conf t
interface fastEthernet0/1
switchport port-security violation protect
```
nastavení **aging** - jak dlouho si switch pamatuje MAC adresy
```
conf t
interface fastEthernet0/1
switchport port-security aging type absolute
```
- aging :
	- static - whitelist zůstane navždy
	- time - na jak dlouho si tě to pamatuje (čas)
	- type:
		- absolute - učení od zapnutí
		- inactivity - učení podle času
Spadlý port Errorem zapnu:
```
conf t
interface fastEthernet0/1
no switchport port-security
shutdown
no shutdown
```
Nastavení errordisable - zjistit co to dělá
```
conf t
errordisable ?
```