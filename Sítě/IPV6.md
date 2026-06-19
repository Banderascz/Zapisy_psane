- celková velikost 128 bitů
- nástupce IPv4 protokolu
- Vysoký počet adres umožňuje hierarchické uspořádání, což zjednodušuje směrování a přečíslování
- nemá broadcast => nahrazuje se multicastem
- Velikost prefixu vždy 64 bitů
- Možnost řetězení hlaviček za sebe pro speciální funkce

## Zápisy adres
- Standardním způsobem jejího zápisu je osm skupin po čtyřech číslicích šestnáctkové soustavy (tj. 16 bitů dlouhých) navzájem oddělených dvojtečkami. Písmena jsou malá.
- Př.: fedc:ba98:7654:3210:fedc:ba98:7654:3210
- můžeme vypouštět nepotřebné nuly
	- 0123:0000:0000:0000:fedc:ba98:7654:3210
	- => 123:0:0:0:fedc:ba98:7654:3210
	- nebo **i skupiny 0 (může se jen 1 skupina pomocí : : )** => 123::fedc:ba98:7654:3210
	- 123 ve čtveřici znamená 0123 a nelze to udělat místo 1230 (**nelze zaměnit**)
### Kanonický tvar
- jednoznačný tvar zápisu adresy
- pokud jsou stejné skupiny tak se vypouští pomocí "::" pouze nejvýznamnější skupiny
- Př.: 123::4567:0:0:0

## Adresace
- **Individuální (unicast)** - jsou staré známé krotké adresy. Každá z nich identifikuje 1 síťové rozhraní a data mají být dopravena právě jemu
- **Skupinové (multicast)** - slouží k adresování skupin počítačů či jiných zařízení. Pokud někdo odešle data na tuto adresu, musí být doručena všem členům skupiny
- **Výběrové (anycast)** - také výběrové adresy označují skupinu, data se však doručí **jen jedinému nejbližšímu členovi** 

## Adresy v IPv6

|  prefix   | význam                        |
|:---------:|:----------------------------- |
|  ::/128   | nedefinovaná adresa           |
|  ::1/128  | smyčka (loopback)             |
| fc00::/7  | unikátní individuální lokální |
| fe80::/10 | unikátní lokálové linkové     |
| ff00::/8  | skupinové adresy              |
|  ostatní  | individuální globální         |

| známé prefixy  | význam                                   |
|:--------------:| ---------------------------------------- |
|  64:ff9b::/96  | adresy s vloženým IPv4                   |
| 64:ff9b:1::/48 | lokální adresy pro přechodové mechanismy |
|   2001::/32    | Teredo                                   |
| 2001:db8::/32  | adresy pro příklady v dokumentech        |
|   2002::/16    | 6to4                                     |

### Prefix

|  3  |            45             |          16           |
| :-: | :-----------------------: | :-------------------: |
| 001 | Globální směřovací prefix | Identifikátor podsítě |
|     |     veřejná topologie     |   místní topologie    |
|     |                           |                       |
|     |          64 bitů          |                       |
|     |  Identifikátor rozhraní   |                       |
