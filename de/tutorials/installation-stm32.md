# Installation STM-Board

Installation zu Arduino siehe [Anleitung Installation Arduino](installation-arduino.md)

Als erstes müssen die Hardware-Files für das STM32-Board unter folgendem
Link heruntergeladen werden:
<https://github.com/rogerclarkmelbourne/Arduino_STM32>

Es erscheint dieses Fenster:

<img src="../../images/STM32/STM32_00_Download_2.png" width="604" height="322" />

Mithilfe des Buttons „Clone or download“ (rot markiert) wird die Datei
Arduino\_STM32-master.zip heruntergeladen.

Nachdem der Ordner „Arduino\_STM32-master“ entpackt wurde, muss dieser
in C:\\Program Files (x86)\\Arduino\\hardware kopiert werden.

Sollte der Ordner „hardware“ noch nicht vorhanden sein, muss dieser
erstellt werden.

<img src="../../images/STM32/STM32_01_Hardware.png" width="604" height="389" />

Als nächstes muss die „install\_drivers.bat“ ausgeführt werden. Diese
findet man unter
C:\\Program Files (x86)\\Arduino\\hardware\\Arduino\_STM32-master\\drivers\\win

<img src="../../images/STM32/STM32_02_Install-driver-bat.png" width="604" height="389" />

Nachdem diese installiert ist, muss Arduino gestartet und der
Boardverwalter geöffnet werden. Diesen erreicht man unter Werkzeuge
Boards Boardverwalter (siehe Bild unten)

<img src="../../images/STM32/STM32_03_Boardverwalter.png" width="604" height="617" />

Über das Suchfeld im Boardverwalter kann nun nach „ARM Cortex M3“
gesucht werden. (rot markiert)

<img src="../../images/STM32/STM32_04_Install-ARM_2.png" width="604" height="370" />

Über den Button „Installieren“ kann ARM nun installiert werden. Ist die
Installation abgeschlossen erscheint daneben „INSTALLED“

<img src="../../images/STM32/STM32_05_Installed-ARM_2.png" width="604" height="340" />

Nun kann das Board eingestellt werden:

Die Einstellungen sind in Arduino unter „Werkzeuge“ zu finden

Für das STM32 Board werden folgende Einstellungen (im Bild untern rot
markiert) benötigt:

***Board*** Generic STM32F103C series;
***Variant*** 128k Flash
***Speed*** 72Mhz
***Upload*** ***Method*** STM32duino Bootloader
***Optimize*** Smallest
***Port*** COMx (x systemabhängig)

<img src="../../images/STM32/STM32_06_Einstellungen_2.png" width="604" height="673" />