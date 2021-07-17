# openvpn-xor
Openvpn with Tunnelblick's xor patch applied

How to install it quickly on Ubuntu 18.04 amd64:
1. 
```
nano /etc/apt/sources.list
```
uncomment first 2-3 sources with src mask

2. 
```
apt-get update && apt-get build-dep openvpn -y
```

Ubuntu 18.04
```
wget --no-check-cert https://github.com/R2D2me/openvpn-xor/raw/main/openvpn_2.4.8-bionic0_amd64.deb
```

```
dpkg -i openvpn_2.4.8-bionic0_amd64.deb
```

Debian 10

```
wget --no-check-cert https://github.com/R2D2me/openvpn-xor/raw/main/openvpn_2.4.8-buster0_amd64.deb
```
```
dpkg -i openvpn_2.4.8-buster0_amd64.deb
```

3. Install openvpn

```
wget https://git.io/v1jlQ -O openvpn-install.sh && bash openvpn-install.sh
```

4. Add this option to server.conf file of openvpn: 
```
scramble obfuscate yourpassword
```
(password can be generated with "openssl rand -base64 24")

5. Restart the openvpn 

```
systemctl restart openvpn@server.service
```

Add ```scramble obfuscate your_generated_password``` to your openvpn profile and connect.


Clients: 

1. Windows: https://github.com/lawtancool/openvpn-windows-xor
2. Android: VPN Client Pro - https://play.google.com/store/apps/details?id=it.colucciweb.vpnclientpro&hl=en_US&gl=US
3. iOS: not available yet
4. Linux: install deb file as server side
