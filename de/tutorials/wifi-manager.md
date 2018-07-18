# Wifi-Manager starten und ausführen

## Wifi-Manager starten

Um den WifiManager verwenden zu können, muss dieser unter dem Link:
<https://github.com/tzapu/WiFiManager> heruntergeladen werden.

Es erscheint folgende Webseite:

<img src="../../images/WiFi-Manager/WiFi-Manager_00_Download-Treiber.png" width="594" height="308" />

Nach Herunterladen der Zip-Datei „WiFiManager-master.zip“ wird Arduino
gestartet.

Zum Einbinden der Bibliothek, muss die Zip-Datei unter *„Sketch
Bibliothek einbinden .ZIP-Bibliothek hinzufügen“* geöffnet werden.

<img src="../../images/WiFi-Manager/WiFi-Manager_01_Bib-einbinden-Menü.png" width="604" height="673" />

## Erstes Testprogramm

Um den WiFi-Manager zu testen, wird ein neues Arduino-File geöffnet
(Menü Datei Neu oder über die Tastenkombination Strg+N)

Das erstes Testprogramm beinhaltet eine setup Funktion und eine loop



```
#include &lt;WiFiManager.h&gt;                                   
void setup() {                                                     
WiFiManager wifiManager;                                           
wifiManager.autoConnect();                                         
}                                                                
void loop(){}   
```

                 
 
<img src="../../images/WiFi-Manager/WiFi-Manager_02_Testprogramm.png" width="259" height="316" /> 


Zum Hochladen des Programms muss der Button mit dem Pfeil geklickt
werden (rot markiert)

<img src="../../images/WiFi-Manager/WiFi-Manager_03_Hochladen2.png" width="486" height="593" />

Nach erfolgreichem Hochladen erscheint im unteren Teil des Fensters die
Meldung „Hochladen abgeschlossen“ (im unteren Bild rot markiert)

<img src="../../images/WiFi-Manager/WiFi-Manager_03_Hochladen-erfolgreich2.png" width="604" height="489" />