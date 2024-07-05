# openvpn-xor
Openvpn with Tunnelblick's xor patch applied

Ubuntu 22.04 / Debian 11

1. Install OpenVPN via Angristan's script
```
wget https://git.io/v1jlQ -O openvpn-install.sh && bash openvpn-install.sh
```

2. Remove openvpn package
```
apt remove openvpn -y
```

3. Install Openvpn (2.5.9) with xor patch applied
```
wget https://raw.githubusercontent.com/x0r2d2/openvpn-xor/main/openvpn_xor_install.sh -O openvpn_xor_install.sh && bash openvpn_xor_install.sh
```
4. Add/remove clients via Angristan's script (openvpn-install.sh)
```
bash openvpn-install.sh
```

Clients: 

1. Windows: https://github.com/lawtancool/openvpn-windows-xor
2. Android: VPN Client Pro - https://play.google.com/store/apps/details?id=it.colucciweb.vpnclientpro&hl=en_US&gl=US
3. iOS: not available yet
4. Linux: install deb file as server side
