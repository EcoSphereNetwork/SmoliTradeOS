# SmoliTradeOS
SmoliTradeOS - Your privat and local, AI powered Crypto Bank operating system

___
#EcoSphere-Networks | #SmoliTrade | #Smolit | #Smolitux-Suite 
___


SmoliTradeOS (STO) ist ein Linux Betriebssystem und basiert auf QubesOS.

# Cloud basiert

SmolituxOS ist ganz einfach im Browser unter https://smolitux.os erreichbar. 
Der User kann oben rechts, in dem Menu auswählen zwischen Login oder Create Account.
Nach einloggen gelangt der User auf seinen SmolituxOS Desktop des SmoliTrade Qubes. Dieser ist live synchronisiert mit dem Smolitux-HomeCenter (MPCPS (MiniPc-PowerStation), oder HSE (HomeServEdition)). Der User kann natürlich einstellen, welche Ordner von seinem Smolitux-HomeCenter synchronisiert werden.

___

### SmoliTradeOS-arm64 on Raspberry PI 

SmoliTradeOS_arm64 basiert auf Raspbian. 
Es ist so konfiguriert, dass nach dem Boot das Dashboard automatisch auf dem montierten Display in den Full Screen Modus startet.
SmoliTradeOS_arm64 ist Touch-Screen kompatible.
Das Dashboard zeigt in der MItte den SmoliTrade Chart, sowie links und recht Sidebars mit Menu Funktion. 
Mehr Info in der Datei [[SmoliTrade GUI]].
Dazu sind die Web-GUIs von SmoliTrade, Freqtrade und OctoBot im Browser erreichbar. Der remote Zugriff auf den Raspberry PI kann ein und aus gestellt werden.
Zudem sind alle Komponente über Telegramm Bots erreichbar.


___

### SmoliTradeOS Konfigurationen on MPCPS (MiniPc-PowerStation) oder  HSE (HomeServEdition):

```
Erklärung:
	c/: = Configuration
	p/: = Program
	d/: = Develop Status
```

- Dom0:
	- nur für Administratoren
	- Updates vom offiziellen Mirror herunterladen
	- lädt auch Updates vom Smolitux-Spiegel herunter
	- vollständig automatisiert mit Skripten und Bots 
- SysNet Qube:
	- AdminNet
		- nur für Dom0
	- BotNet Qube:
		- nur für TradingBots
	- AkademieNet:
		- nur für Moodlebox
	- CloudNet:
		- nur für Freedombox
- SmoliTrade Qube
	- c/:nach dem Starten des PCs und Booten von SmoliTradeOS
		- c/d/:auto Qube starten 
		- c/d/:automatisch Vollbild-Desktop-Modus
	- SmoliTrade Server
		- p/d/:Web-Benutzeroberfläche SmoliTrade 
		- p/:Web-Benutzeroberfläche Freqtrade
		- p/:Web-Benutzeroberfläche OctoBot
	- Firewall
	- Proxy
	- Open-Cloud Qube # Open-Cloud ist die Plattform mit der die Hardware Ressourcen # bereit gestellt werden
	- p/:Freedombox Server
		- p/:Web-Benutzeroberfläche
	- ...
- Freqtrade Qube
	- p/:Freqtrade Server
	- ...
- OctoBot Qube
	- p/:OctoBot Server
	- ...
- Akademie Qube
	- p/:Moodle-Server
		- p/:Web-GUI
	- ...
- Privat-Cloud Qube
	- p/:Freedombox Server
		- p/:Web-GUI
	- ...
