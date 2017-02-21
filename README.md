# fhemssl
SSL Verbindung mit letsencrypt für FHEM


# Voraussetzung: 
- Apache2 Webserver
- vorhandenes SSL Zertifikat für Domain (im Code als Beispiel: meinedomain.myfritz.net 
- Installiertes Modul mod-proxy-html für Apache

# Installation von mod-proxy-html unter Debian:
sudo apt-get install libapache2-mod-proxy-html

# Aktivierung des Moduls/der Module:
sudo a2enmod proxy
sudo a2enmod proxy_html
sudo a2enmod proxy_http

# Installation des VHosts:
Die Datei meineDomain.myfritz.net ist lediglich eine Beispieldatei!
Unter Apache liegen die VHosts Dateien üblicherweise unter /etc/Apache2/sites-available/


