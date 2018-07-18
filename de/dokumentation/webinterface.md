# WebInterface

## Installation

Run `npm run webinterface` in `/Code/WebInterface/` to install all the dependencies.

### Server

Run `npm start` in folder `/Code/WebInterface/` for installing the server dependencies.

### Go on With the Angular DevMode
Run `npm run angulardev` to start the DevMode for the WebApp.

## Anwendung

<img src="../../images/Webinterface/picture_1.png" width="600" height="318" />

Das WebInterface besteht aus zwei Teilen, dem **Device** und dem **Radio** .


### Device
Wenn keine Devices (SensorBoards) angeschlossen sind wird sieht man folgendes Fenster:

<img src="../../images/Webinterface/picture_2.png" width="600" height="318" />

Durch das Klicken des Buttons _Show Device_ werden alle [[zugelassenen Geräte]] aufgelistet. 

Jedes **Device** wird mit folgenden Informationen aufgelistet 

* ID
* Manufacturer
* ProductID
* VendorID
* LocationID
* …

<img src="../../images/Webinterface/picture_3.png" width="600" height="318" />

Von jedem einzelnen **Device** kann man sich die Informationen holen lassen um zu schauen um welchen Typ von Sensor es sich hierbei handelt. 

<img src="../../images/Webinterface/picture_4.png" width="500" height="500" />

Des Weiteren wird beim Aufrufen der Informationen die _UUID_ vergeben, falls keine vorhanden. 

<img src="../../images/Webinterface/picture_5.png" width="500" height="500" />

Das Anlegen der _UUID_ wird mit einer FlashMessage gekennzeichnet.

Im weitern Schritt wird eine vorhandene **RadioConfig** ausgewählt, die auf das Board gesendet werden soll. Nach dem der Button _Initialize_ gedrückt wurde, wird die Konfiguration am Board gespeichert.

<img src="../../images/Webinterface/picture_6.png" width="600" height="391" />

### Radio
Unter dem Tab **Radio** findet man die ganzen RadioHead Konfigurationen, die angelegt wurden. Diese kann man bearbeiten oder auch löschen.

<img src="../../images/Webinterface/picture_7.png" width="600" height="318" />
