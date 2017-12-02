# Red-Team-VPN
how to connect to red team vpn 
sudo apt-get install openvpn bridge-utils

Change the last line to the port you want
Commands needed:
ssh -N -f -C -D 42000 <your-username-on-ucfilespace>@ucfilespace.uc.edu
openvpn client.conf
