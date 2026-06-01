## Porty v modu Trunk
- Pokud propojíme switche je potřeba, aby switch co odesílá rámce, přidal k těmto rámcům informaci o tom, do jaké VLAN patří.
- Způsoby:
	- IEE 802.1Q (802.1Q, DOT1Q)
	- Cisco ISL - nepoužívá se běžně
- V případě 802.1Q se do hlavičky doplní značka s informací o VLAN, do které patří. Hovoří se pak o **značkovaných rámcích**. Výhoda je, že velikost rámce se zvětší pouze o 4 bajty. Nevýhoda je, že se změnil obsah rámce a musí se přepočítat FCS v patičce.