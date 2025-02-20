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
//192.168.0.224/Movies /mnt/movies cifs credentials=/etc/cifs-credentials 0 0
//192.168.0.224/Shows /mnt/shows cifs credentials=/etc/cifs-credentials 0 0
//192.168.0.224/Music /mnt/music cifs credentials=/etc/cifs-credentials 0 0
```

192.168.0.224 is the current ip for my nas (see [[01192025 boenet]])

also see [[01192025 Plex cifs-credentials]]
