## Co přesně je služba?

Služba (v Linuxu _daemon_, v Windows _service_) je proces, který:

- běží automaticky po startu systému, nebo když je potřeba
    
- nemá grafické rozhraní
    
- stará se o nějakou konkrétní funkci
    
- běží často stále na pozadí


---

## 🖥️ Příklady služeb podle typu OS

### **Linux (systemd, daemony)**

- `NetworkManager` – spravuje připojení k síti
    
- `sshd` – umožňuje vzdálené přihlášení přes SSH
    
- `cups` – tiskové služby
    
- `fstrim.timer` – pravidelné TRIM pro SSD
    
- `bluetooth.service` – správa Bluetooth