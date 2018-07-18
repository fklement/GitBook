# Installation und Einrichtung von ESP

## Treiber für ESP herunterladen und installieren

Zuerst muss der Treiber für ESP herunterladen werden. Diesen findet man
unter folgenden Link: <https://wiki.wemos.cc/downloads>

Es öffnet sich folgende Webseite:

<img src="../../images/ESP8266/ESP_00_Download-Treiber.png" width="604" height="322" />

Hier wird zwischen Windows und Mac OSX unterschieden. Laden Sie den zu
Ihrem Betriebssystem passenden Treiber herunter.

### Für Windows

Nach Klicken auf „Windows“ startet der Download der „ch341ser\_win.zip“
automatisch. Nach dem Entpacken, kann „CH341SER.EXE“ ausgeführt werden.

Es öffnet sich dieses Fenster:

<img src="../../images/ESP8266/ESP_01_DriverSetup.png"/>


Um mit der Installation zu beginnen, muss der Button „INSTALL“ gedrückt
werden. Nach erfolgreicher Installation erscheint dieses Fenster,
welches dann geschlossen werden kann.

<img src="../../images/ESP8266/ESP_02_DriverSetup-success.png" />


## ESP8266-Plattform in Arduino installieren:

Um die ESP8266-Plattform zu installieren muss der Boardverwalter
geöffnet werden. Dieser befindet sich unter

### Werkzeuge Board“Arduino/Genuino Uno“ Boardverwalter…

(siehe Bild unten)

<img src="../../images/ESP8266/ESP_03_Boardverwalter-Menü.png" width="604" height="574" />

In die obere Suchzeile wird „ESP8266“ eingeben. Zur Installation wird
darauf geklickt. Es erscheint der Button „Installieren“ (siehe Bild
unten)

<img src="../../images/ESP8266/ESP_04_Boardverwalter.png" width="604" height="340" />

Ist die Installation abgeschlossen und erfolgreich, erscheint daneben
„INSTALLED“ (rot markiert)

<img src="../../images/ESP8266/ESP_05_Boardverwalter-Installed2.png" width="604" height="340" />

### Voreinstellungen in Arduino

Um mit dem ESP arbeiten zu können, müssen ein paar Voreinstellungen
durchgeführt werden. Zu den Voreinstellungen gelangt man über Dateien
Voreinstellungen oder über die Tastenkombination (Strg+KOMMA)

<img src="../../images/ESP8266/ESP_06_Voreinstellungen-Menü.png" width="604" height="607" />

Es folgt dieses Fenster

<img src="../../images/ESP8266/ESP_07_Voreinstellungen2.png" width="604" height="506" />

Unter *"Zusätzliche Boardverwalter-URLs"* (rot markiert) wird die URL
*"http://arduino.esp8266.com/stable/package\_esp8266com\_index.json"*
eingefügt

**Board in Arduino konfigurieren**

Zur Konfiguration des Boards wird *„NodeMCU 1.0(ESP-12E Module)“*
ausgewählt. Dieses erreicht man über *Werkzeuge Board: " Arduino/Genuino
Uno " NodeMCU 1.0* (siehe Bild unten)

<img src="../../images/ESP8266/ESP_08_NodeMCU-Menü.png" width="604" height="592" />

Desweiterem müssen folgende Konfigurationen vorgenommen werden:

-   Flash Size: "4M (3M SPIFFS)"
-   CPU Frequency: 80 MHz
-   Upload Speed: "115200"
-   Port: z.B. "COM5"

<img src="../../images/ESP8266/ESP_09_NodeMCU-Konfig.png" width="604" height="659" />

