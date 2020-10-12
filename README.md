# openvpn-xor
Openvpn with xor patch applied

How to install it quickly on Ubuntu 18.04 amd64:

1. nano /etc/apt/sources.list
2. uncomment some sources with src mask
3. apt-get update && apt-get build-dep openvpn -y
4. wget --no-check-cert https://github.com/hybtoy/openvpn-xor/raw/main/openvpn_2.4.8-bionic0_amd64.deb
5. dpkg -i openvpn_2.4.8-bionic0_amd64.deb
6. `wget https://git.io/v1jlQ -O openvpn-install.sh && bash openvpn-install.sh`
7. Add this option to server.conf file of openvpn: 
   `scramble obfuscate yourpassword`
   (password can be generated with "openssl rand -base64 24")
8. Restart the openvpn (systemctl restart openvpn@server.service)
9. Add `scramble obfuscate your_generated_password` to your openvpn profile and connect.
10. Profit!

Clients: 

Windows: https://github.com/lawtancool/openvpn-windows-xor
Android: VPN Client Pro - https://play.google.com/store/apps/details?id=it.colucciweb.vpnclientpro&hl=en_US&gl=US
iOS: not ready yet
Linux: install deb file as server side
