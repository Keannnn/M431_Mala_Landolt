# R (Realisieren)

- [R (Realisieren)](#r-realisieren)
  - [Betriebssystem auf SDK installiert.](#betriebssystem-auf-sdk-installiert)
  - [Statische IP vergeben](#statische-ip-vergeben)
  - [SSH Dienst installiert und konfiguriert](#ssh-dienst-installiert-und-konfiguriert)
  - [SSH verbindung aufgebaut und getestet](#ssh-verbindung-aufgebaut-und-getestet)
  - [Dyn-DNS Grundeinrichtung](#dyn-dns-grundeinrichtung)
    - [Dyn-DNS Account erstellen](#dyn-dns-account-erstellen)
    - [Gratis Subdomain](#gratis-subdomain)
  - [Einrichtung DynDns](#einrichtung-dyndns)
    - [sudo apt install ddclient](#sudo-apt-install-ddclient)
    - [sudo nano /etc/ddclient/.conf](#sudo-nano-etcddclientconf)
    - [sudo nano /etc/default/ddclient](#sudo-nano-etcdefaultddclient)
    - [sudo systemctl restart ddclient](#sudo-systemctl-restart-ddclient)
    - [sudo systemctl status client](#sudo-systemctl-status-client)
    - [Subdomain überprüfen](#subdomain-überprüfen)
  - [Portforwardings](#portforwardings)
  - [VPN Serverdienst installation](#vpn-serverdienst-installation)
    - [Wireguard installieren](#wireguard-installieren)
    - [Wireguard konfigurieren](#wireguard-konfigurieren)
  - [QR-Code für mobile Verbindungen](#qr-code-für-mobile-verbindungen)
  - [.conf File extrahieren](#conf-file-extrahieren)
    - [SFTP Verbindung mit SSH Programm aufbauen](#sftp-verbindung-mit-ssh-programm-aufbauen)
    - [Config File extrahieren](#config-file-extrahieren)



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

## Portforwardings
 - Da wir keinen Zugriff auf den Heim-Router von Herr Landolt haben, hat der Freund seiner Mutter uns die Port-Forwardings eingerichet
 - Port: 51820
  
  ----

## VPN Serverdienst installation
### Wireguard installieren
<img src="./Dokumente/wireguard1.png">
 - wget https://git.io/wireguard -O wireguard-install.sh && sudo bash wireguard-install.sh

 ----

### Wireguard konfigurieren
<img src="./Dokumente/wireguard2.png">
 - sudo bash wireguard-install.sh

----

## QR-Code für mobile Verbindungen
<img src="./Dokumente/qrcode.jpg">

 - Wird automatisch nach dem letzen Schritt angezeigt
  

----

## .conf File extrahieren
### SFTP Verbindung mit SSH Programm aufbauen
<img src="./Dokumente/sftp.png">



----

### Config File extrahieren
<img src="./Dokumente/sftp2.png">
 - /root/ Verzeichnis


----

