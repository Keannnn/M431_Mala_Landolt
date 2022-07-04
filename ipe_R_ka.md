# R (Realisieren)
## Betriebssystem auf SDK installiert.
- Hardware: Raspberry Pi 3 Model B Rev 1.2
- Betriebsystem: Raspberry Pi OS Lite
- Image mit rufus auf SD-Karte geladen.

## Statische IP vergeben
 - sudo nano /etc/dhcpcd.conf
<img src="./Dokumente/staticip.png">


## SSH Dienst installiert und konfiguriert
 - sudo apt install openssh-server -y
<img src="./Dokumente/sshstatus.png">


## SSH verbindung aufgebaut und getestet
 - ssh lama@192.168.1.200 (Raspberry PI)
<img src="./Dokumente/sshconnection.png"> 


## Account erstellen DynDNS
 - freedns.afraid.org
<img src="./Dokumente/freedns.png">
 - Gratis Subdomain
<img src="./Dokumente/subdomain.png">


## Einrichtung DynDns
 - sudo apt install ddclient
<img src="./Dokumente/package.png">


## VPN Serverdienst installation (Wireguard)
 - wget https://git.io/wireguard -O wireguard-install.sh && sudo bash wireguard-install.sh
<img src="./Dokumente/wireguard1.png">
