Zobrazení přehledu VLAN (v enable)
```
show vlan
```
př.: vytvoření VLAN 120, "Leva" = jméno
```
conf t
vlan 120    # vlan číslo VLANU
name Leva   # jméno vlan
```
Potom ping na switch v tty2, abych zjistil zda funguje
```
conf t
interface fastEthernet0/1       # vetsinou leva, fastEthernet0/2 vetsinou prava
switchport mode access          # abysme zrušili dynamic
switchport access vlan 120
```
Vždy před vypnutím vymažu konfiguraci vlan.dat (v enable)
```
del vlan.dat
# Zmáčknout 2x ENTER (RETURN)
dir     # kontrola jestli je stále přítomný vlan.dat
```
Nastavení Access na všechny z Dynamic
```
conf t
interface range
interface range fastEthernet0/1-24
switchport mode access
```
Trunk mode (vice vlan jede pres 1 kabel)
```
conf t
interface range GigabitEthernet 0/1-2
switchport mode trunk
```
Vypnutí upozornění z Gigabit portů (furt kecaj něco)
```
ena
conf t
interface range gigabitEthernet 0/1-2
switchport nonegotiate
```