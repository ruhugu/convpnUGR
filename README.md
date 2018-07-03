# convpnUGR
Bash script to connect to the University of Granada (UGR) VPN server. It retrieves the temporary VPN password automatically, making the connection process quicker and easier.

## Configuration
Before using the script the VPN connection must be set up. Instructions can be found at the [CSIRC webpage](https://csirc.ugr.es/informatica/RedUGR/VPN/ConfVPN/VPN-Linux.html).

Make sure that you enable password storage, as shown in the picture.

![Password storage settings](https://github.com/ruhugu/convpnUGR/blob/master/storepassword.png)

Once the connection is created, the script must be configured. Open convpnUGR file and, in EMAILADDRESS and VPNID variables, specify your email address and the name that you gave to the VPN connection:
```
# VPN name in NetworkManager
VPNID="UGR"
# UGR email address
EMAILADDRESS="example@correo.ugr.es"
```

After this, you should be able to connect to the VPN by running the script:
```console
foo@bar:~$ ./convpnUGR
UGR email password:  
VPN password: m_cz=45cnWxW
VPN connection successfully activated (D-Bus active path: /org/freedesktop/NetworkManager/ActiveConnection/150)
```

If you want to be able to run the script from anywhere (not just the script folder), copy it to "/usr/local/bin/". Then you will be able to connect to the vpn using:
```console
foo@bar:~$ convpnUGR
```
