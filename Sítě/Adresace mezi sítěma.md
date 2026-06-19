řeší se na síťové vrstvě
zařizuje komunikaci mezi sítěmi
síťové adresy jsou, protože z MAC adresy není poznat, zda je zařízení v naší síti
protokol IP = Internetová adresa(IPv4/IPv6), Internetová = mezi síť
**IPv4** = 32 bitů, informace do jaké sítě patříte, DHCP server ji nastavuje nebo uživatel, zapisuje se v desítkové soustavě po 8 bitech, oddělovače ".", nedůležité 0 se vypouštějí, při konfiguraci je **nutné zadat i masku**
**Maska** = př.: 255.255.255.0, nemusí mít nutně 24 bitů(nejčastěji 24 bitů), u masky se musí vždy dát 0b1111000..., **nikdy** 0b1010101...
IP adresa je složena z NETID a HOSTID
11000000.10101000.11011010.00100001 = 192.168.218.33 = IPv4
11111111.11111111.11111111.00000000 = 255.255.255.0 = maska
NetID
11000000.10101000.11011010 = 192.168.218
HostID
0010000 = 33

Poslední adresa v síti je tzv. **Broadcast**(př.: 192.168.1.255) vysílání určeno všem => v HostID je všechno = 1
Počet adres celkem = 255 (256 když počítáme broadcast)
Počet použitelných adres = 254

192.168.0.1/24 = 255.255.255.0 (ta maska je to /24 a i to 255 rovnají se)

př.: 192.168.1.33/25
11111111.11111111.11111111.10000000

---
Prehistorické doby:
Maska pro Třída A
255.0.0.0
16 milionů adres
Privatní IP
- 10.0.0.0 - 10.255.255.255
- hostů: 16 777 214
- Sítí: 126

Maska pro Třídu B
255.255.0.0
16 tisíc adres
Privatní IP
- 176.16.0.0 - 171.31.255.255
- hostů: 65 535
- Sítí: 16 382

Maska pro Třídu C
255.255.255.0
256 adres
Privatní IP
- 192.168.0.0 - 192.168.255.255
- hostů: 256
- Sítí: 2 000 000 cca.

A-C = pro unicast

Další třídy: D(pro multi-cast),E

Dnes:
Už se neřeší třídy
Dělá to router

0.0.0.0 = Nedefinovaná adresa