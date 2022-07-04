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


## Dyn-DNS Grundeinrichtung

----

### Dyn-DNS Account erstellen
<img src="./Dokumente/freedns.png">

----

### Gratis Subdomain
- http://freedns.afraid.org/subdomain/
<img src="./Dokumente/subdomain.png">

----


## Einrichtung DynDns
### sudo apt install ddclient
<img src="./Dokumente/package.png">
 - Enter drücken, bis das Programm sich schliesst.

----

### sudo nano /etc/ddclient/.conf
<img src="./Dokumente/ddclient.png">
 - Muss mit den Login-Daten des DynDNS übereinstimmen.

----

### sudo nano /etc/default/ddclient
<img src="./Dokumente/daemon.png">
 - Daemon Einstellungen übernehmen

----

### sudo systemctl restart ddclient
### sudo systemctl status client
<img src="./Dokumente/restart.png">
 - Dyn-DNS Client neu starten und den Status anzeigen

----

### Subdomain überprüfen
 - http://freedns.afraid.org/subdomain/


<img src="./Dokumente/wanip.png">
 - Subdomain wird nun WAN-IP anzeigen
  
----


## VPN Serverdienst installation (Wireguard)
 - wget https://git.io/wireguard -O wireguard-install.sh && sudo bash wireguard-install.sh
<img src="./Dokumente/wireguard1.png">
