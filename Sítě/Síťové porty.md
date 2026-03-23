Adresy na transportní vrstvě
Slouží pro rozlišení služeb na serverech a k rozlišení aplikací/relací

Porty:
- známé porty 
	- rozsah 0-1023
	- vyhrazené pro nejběžnější služby
	- může spouštět pouze privilegovaný uživatel
- registrované porty
	- rozsah 1024-49151
	- použití portu se musí registrovat u ICANN
- dynamické porty
	- rozsah 49151-65535
	- vyhrazené pro dynamické přidělování a soukromé použití
	- nejsou pevně přiděleny žádné aplikaci

Nejběžnější porty:

| Číslo portu | Aplikační protokol popis                                                                                      |
| :---------: | :------------------------------------------------------------------------------------------------------------ |
|   80/tcp    | HTTP, pro World Wide Web (WWW)                                                                                |
|   443/tcp   | HTTPS pro šifrovaný WWW, TLS/SSL certifikáty                                                                  |
|   53/udp    | DNS, UDP pro překlad adresa-jméno, TCP pro zónové                                                             |
|   53/tcp    | přenosy mezi DNS servery nebo překlad v případě použití DNSSEC                                                |
|   67/udp    | DHCP server                                                                                                   |
|   68/udp    | DHCP client                                                                                                   |
|   23/tcp    | Telnet - vzdálená konzola. Nešifrovaný přenos včetně přihlašovacích údajů!                                    |
|   22/tcp    | SSH, šifrovaná náhrada Telnetu                                                                                |
|   21/tcp    | FTP, příkazový kanál                                                                                          |
|   20/tcp    | FTP, datový kanál pro aktivní ftp                                                                             |
|   25/tcp    | Simple Mail Transfer Protocol (SMTP),                                                                         |
|   110/tcp   | POP3 (Post Office Protocol). pro prohlížení e-mailů, Možnost označit zprávu jako přečtenou na více zařízeních |
|   143/tcp   | Internet Message Access Protocol (IMAP4). Pro práci s e-maily na serverech                                    |
|   993/tcp   | IMAP4 over TLS/SSL. Šifrovaná varianta IMAP4                                                                  |
|   123/udp   | Network Time Protocol (NTP). Pro synchronizaci času                                                           |
|   161/tcp   | Simple Network Management Protocol (SNMP)                                                                     |
|   162/tcp   | SNMP traps                                                                                                    |
|  3389/tcp   | Remote Desktop Protocol. Pro vzdálenou plochu                                                                 |
|  1433/tcp   | MSSQL                                                                                                         |
|  3306/tcp   | MySQL                                                                                                         |
