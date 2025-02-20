---
Date: 2025-01-19T18:54:00
tags:
  - linux
  - network
  - plex
  - server
---
Distro: Ubuntu Server
notes: Install OpenSSH
dependencies: nano, cifs-utils, Plex, OpenSSH
See also: [[01192025 Auto Mount Network Drives in Linux]], [[01192025 Plex cifs-credentials]], [[01192025 Plex fstab]]

1. Add Plex to the repo:
```
echo deb [https://downloads.plex.tv/repo/deb](https://downloads.plex.tv/repo/deb) public main | sudo tee /etc/apt/sources.list.d/plexmediaserver.list
```

```
curl [https://downloads.plex.tv/plex-keys/PlexSign.key](https://downloads.plex.tv/plex-keys/PlexSign.key) | sudo apt-key add -
```

2. Update the repo
```
sudo apt update
```

3. Install Plex
```
sudo apt install plexmediaserver
```

4. Auto start Plex
```
sudo systemctl enable plexmediaserver.service
```

5. Connect to the web server:
ip.address:32400/web

6. Connect your files
If you have not added network shares to your plex machine, see [[01192025 Auto Mount Network Drives in Linux]]
