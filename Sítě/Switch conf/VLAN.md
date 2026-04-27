Zobrazení přehledu VLAN (v enable)
```
show vlan
```
př.: vytvoření VLAN 120, "Leva" = jméno
```
conf t
vlan 120
name Leva
```
Potom ping na switch v tty2, abych zjistil zda funguje
```
conf t
interface fastEthernet0/1
switchport mode access
switchport access vlan 120
```