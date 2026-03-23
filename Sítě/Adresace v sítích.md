adresy se řeší na linkové vrstvě => linkové adresy
MAC je uložena na síťovém rozhraní
MAC/EA(Ethernet address) adresa příklad: 5e:49:2c:d0:11:e3
celková velikost 48 bitů(6 bajtů) 
rozděluje se to po 1 bajtu(8 bitů), rozdělovače adresy můžou být: :, ., -, ,nic
písmena můžou být velké i malé
zápis je v Hex

	5 0
0101    0000
	    ||
		||...0 - unicast
		||...1 - multicast
		|....0 - globálně jedinečná
		|....1 - lokálně jedinečná

Adresa ff:ff:ff:ff:ff:ff = broadcast = vysílání které je dostupné všem
u globálně jedinečné je: OUI - 3 bajtový identifikátor(OUI = Organizationally unique identifier) 

Spolehlivost = Data přijdou, ve správném pořadí, není tam ani méně ani více paketů
Bezchybnost =  -||-  , i data jsou bez chyby, Latence je větší než u spolehlivé, př.: stream videa, zvuku...
