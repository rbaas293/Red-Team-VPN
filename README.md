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
#### Run the following to set which virtual machine and port you want to use:
```
cd /etc/openvpn
sudo nano client.conf
```
* Find the following line of code in the `client.conf` file:
    ```
    ca /etc/openvpn/credentials/ca.crt
    cert /etc/openvpn/credentials/red-04.crt
    key /etc/openvpn/credentials/red-04.key
     ```
    and replace all instances of `red-00` with your corrisponding assigned virtual machine.

* Scroll to the bottom of the file and find:
    ```
    # Choose your port
    socks-proxy 127.0.0.1 <your-port>
    ```
    and replace `<your-port>` with any port between 1-66000.

## Connecting vpn:
* Fill in the following with your information:
    ```
    ssh -N -f -C -D <your-port> <your-UC-6+2>@ucfilespace.uc.edu
    sudo openvpn client.conf
    ```



