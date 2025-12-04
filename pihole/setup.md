# Pi-hole Installation

1. Installera Pi-hole:

```bash
curl -sSL https://install.pi-hole.net | bash
```

2. Ställ in lösenord för web:
```
pihole setpassword 

reboot now
```

3. VÄlj unbound till DNS

I web UI: Gåt till Settings -> DNS, custom DNS: 127.0.0.1#5335
