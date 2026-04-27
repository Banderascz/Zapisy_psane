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
interface fastEthernet0/1
switchport mode access          # abysme zrušili dynamic
switchport access vlan 120
```
Vždy před vypnutím vymažu konfiguraci vlan.dat (v enable)
```
del vlan.dat
# Zmáčknout 2x ENTER (RETURN)
dir     # kontrola jestli je stále přítomný vlan.dat
```
