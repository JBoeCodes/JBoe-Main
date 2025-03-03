---
Date: 2025-01-19T14:21:00
tags:
  - plex
  - proxmox
  - linux
  - server
---
/etc/fstab for plex server network drives:

```
//NAS.IP/Movies /mnt/movies cifs credentials=/etc/cifs-credentials 0 0
//NAS.IP/Shows /mnt/shows cifs credentials=/etc/cifs-credentials 0 0
//NAS.IP/Music /mnt/music cifs credentials=/etc/cifs-credentials 0 0
```

NAS.IP is the current ip for my nas (see [[01192025 boenet]])

also see [[01192025 Plex cifs-credentials]]
