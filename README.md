# feeder
# work in progress
documentation and template set still incomplete

## English
*feeder (small container ship)* is an IoT Appliance with MQTT broker, controller, analytics, monitoring and docker administration based on
the latest hypriot-os and portainer.io container management.

*feeder* comes with a ready to deploy Raspberry Pi SD-Image file (standard hypriot-os - to be downloaded from hypriot original git-repro -  with custom cloud-init file from here), you can be deploy it manually with etcher and put the cloud-init file on the /boot partition of the sd-card or download the image automated and deploy everything automated with hypriot flash tool (linux and mac) with included scripts.

During the installation routine feeder will use hypriot-os build-in cloud-init feature.
You are able to modify username, password, wlan access (activation, ssid, credentials) and hostname before the first start.
feeders default is a ethernet connection with dhcp. default username/password: feeder/raspberry, portainer credentials are generated after the installation.

2nd day deployment is template driven, you can pick and select features to install within portainers *App Template* menu. 
[Documentation in English and German can be found in the wiki pages](https://github.com/holgerimbery/feeder/wiki)


## Deutsch: 
*feeder (kleines Transportschiff zum Containertransport)* ist eine IoT Appliance mit MQTT broker, controller, analytics, monitoring und docker Administration basierend auf der aktuellen hypriot-os Version sowie auf portainer.io Management

*feeder* kommt als fertiges SD-Image für RaspberryPi (Download aus dem hypriot-os Repository mit cloud-init Skript von hier), installation mit etcher und kopieren des cloud-init Files auf die /boot Partition der SD-Karte oder Skript gestützter Download und Installationsprozess mit hypriot flash tool in einem Schritt (linux und Mac). Während des 
Installationprozesses werden die in hypriot-os vorhandenen cloud-init Routinen genutzt.
Vor dem ersten Start können Benutzername, Passwort, WLan Zugangsdaten (Aktivierung, ssid, credentials) und Host Name verändert werden.
Standartmässig ist feeder auf dhcp via ethernet eingestellt. Standard Benutzername/Password: feeder/raspberry, die Zugangsdaten für portainer können nach der Installation festgelegt werden.

Weitere Funktionen können Template gesteuert über das *App Template* Menü von Portainer nach installiert werden.
[Die Dokumentation in Deutsch und Englisch wird über die wiki-Seiten zur Verfügung gestellt](https://github.com/holgerimbery/feeder/wiki)

## Security
feeder does not modify hypriot-os or portainer.io. Feeder installs portainer.io as a GUI to hypriot-os via cloud-init - [user-data](https://raw.githubusercontent.com/holgerimbery/feeder/master/user-data) - and make use of a own app template set - [templates.json](https://raw.githubusercontent.com/holgerimbery/feeder/master/templates.json) - to deploy addons to hypriot-os. Both files are available as plain-text files. Some add-ons will use custom created docker container, please find there source within the linked git-repro of the respective container.


