[^1]Pozor na žlutý a jedem!

---

**Žlutá** (lokální) - "*ifconfig eth0 192.168.1.40*"
**Černá** (globální) - "*ifconfig eth1 192.168.218.40*"
			- "*vi /etc/resolve.conf*"  : do toho napsat DNS server = "*nameserver 8.8.8.8*"
			- "*route add default gw 192.168.218.1*": nastaví default gateway

Adresa 0.0.0.0 - prázdná adresa,nechá zaplé rozhraní, ale je bez adresy

"*ifconfig eth0 down*" - vypne rozhraní eth0

**Alias na síť** - "*ifconfig eth0:2 192:168:2.40*" - odvolávám se na rozhraní eth0, ale s jinou adresou

[^1]: Citace: Rostislav Sítějičný
