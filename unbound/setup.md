# Unbound Installation

1. Installera Unbound:

```bash
sudo apt install unbound
```

2. Kopiera pi-hole.conf till /etc/unbound/unbound.conf.d/

3. Starta och testa tjänsten:
``` 
sudo service unbound restart    # Startar unbound

dig pi-hole.net @127.0.0.1 -p 5335  # Testar att unbound är uppe

dig fail01.dnssec.works @127.0.0.1 -p 5335 # Ska ge timeout första gången och SERVFAIL andra gången 

dig +ad dnssec.works @127.0.0.1 -p 5335 # Ska ge no error

```

4. Starta om enheten:
```
reboot now
```
