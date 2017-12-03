# Red-Team-VPN
how to connect to red team vpn.
See the following in Markdown format [here](https://github.com/rbaas293/Red-Team-VPN)
## Install Openvpn (if needed)
`sudo apt-get install openvpn bridge-utils`

## Configure vpn:
```
git clone https://github.com/rbaas293/Red-Team-VPN.git
cd Red-Team-VPN
cp client.cof /etc/openvpn
cp -r credentials /etc/openvpn
```
## Connecting vpn:
Change the last line to the port you want:
```
ssh -N -f -C -D <your-port> <your-UC-6+2>@ucfilespace.uc.edu`
sudo openvpn client.conf
```



