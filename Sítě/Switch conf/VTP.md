- Sharování [[Sítě/Switch conf/VLAN|VLAN]] konfigurací (Tabulek) mezi switchema
Zobrazeni info o VTP
```
ena
show vtp status
```
VTP nastaveni na Client - nemůže vytvářet VLAN, přijímá tabulky od serveru
```
conf t
vtp mode client
```
VTP přepnutí na verzi 2
```
conf t
vtp version 2
```
