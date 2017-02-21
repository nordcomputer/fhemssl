# fhemssl
SSL Verbindung mit letsencrypt oder anderem Anbieter für FHEM


## Voraussetzung: 
- Apache2 Webserver
- vorhandenes SSL Zertifikat für Domain (im Code als Beispiel: meinedomain.myfritz.net 
- Installiertes Modul mod-proxy-html für Apache

# Installationsanweisungen: 

## Installation von mod-proxy-html unter Debian:
sudo apt-get install libapache2-mod-proxy-html

## Aktivierung des Moduls/der Module:
sudo a2enmod proxy
sudo a2enmod proxy_html
sudo a2enmod proxy_http

## Installation des VHosts:
Die Datei meineDomain.myfritz.net ist lediglich eine Beispieldatei!
Unter Apache liegen die VHosts Dateien üblicherweise unter /etc/Apache2/sites-available/

# fhemssl herunterladen: 
git clone https://github.com/nordcomputer/fhemssl.git

cd fhemssl/

sudo cp meinedomain.myfritz.net /etc/apache2/sites-available/EIGENEDOMAIN.conf 

## Anpassen der Datei:
sudo nano /etc/apache2/sites-available/EIGENEDOMAIN.conf  

## nach der Anpassung Link in der /etc/apache2/sites-enabled/ erstellen:

cd /etc/apache2/sites-enabled/

sudo ln -s /etc/apache2/sites-available/EIGENEDOMAIN.conf EIGENEDOMAIN.conf

## Apache neustarten
sudo /etc/init.d/apache2 restart
