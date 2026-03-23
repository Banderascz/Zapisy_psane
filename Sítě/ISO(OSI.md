- Nikdy nebyl použit v praxi
- [^1]Hierarchický  vrstevní model nebo referenční model
- **Vrstvy** - Složitý problém rozdělen do vrstev(menších problémů)
	1. *Fyzická vrstva* - médium(kabely...), signál, binární přenos, DATA - Bity
	2. *Spojová/Linková vrstva* - [^2]fyzické adresování, komunikace v jedné síti, [^3]**DATA - Rámce** = blok dat, řeší se bezchybnost(MAC) a spolehlivost(LLC)
	3. *Síťová vrstva* - komunikace mezi sítěmi, určování cesty a logické adresování (IP), **Data - Pakety**
	4. *Transportní  vrstva* - SPOLEHLIVOST, End-to-End spojení, **Data - segmenty**
	5. *Relační vrstva* - komunikace mezi hostitely, udržuje spojení, více spojení může být i v jednom(rychlé swapování), ukončuje spojení, **Data - Data**
	6. [^4]*Prezentační vrstva* - Mění přijatá a odeslaná data, aby měli stejný význam, pro obě strany, **Data - Data**
	7. *Aplikační vrstva* - Poskytuje rozhraní pro uživatelské aplikace k síťovým službám, protokoly jako HTTP, FTP, ...., **Data - Data**

[^1]: Vztah mezi vrstvami mezi podřízeností a nadřízeností, každá vrstva má 1 podřazený a 1 nadřazený.

[^2]: Podvrstvy: MAC(media-access-control)/(Každej KKT si to značí jinak, MAC = fyzická adresa = hw adresa) má **48 bitů**, je zobrazovaná v hex soustavě a LLC(Logical-link-control)

[^3]: Hlavička-adresa odkud kam ,data ,patička - kontrola dat FCS = Frame(rámec)-Control(kontrola)-Sequence(sekvence)

[^4]: Příklad: kódování jazyků čeština windows 1250 vs UTF-8 atd., i mezi dos a moderními systémy třeba txt

