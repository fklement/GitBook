# Starting and running the Wifi-Manager

## Starting the Wifi-Manager

In order to use the Wifi-Manager, you have to download it under <https://github.com/tzapu/WiFiManager> first.

The following website is shown:

<img src="../../images/WiFi-Manager/WiFi-Manager_00_Download-Treiber.png" width="594" height="308" />

After downloading the zip-file „WiFiManager-master.zip“ you have to open Arduino.

To use the library, you have to import it under *Sketch* --> *Include Library* --> *Add .ZIP Library...*

<img src="../../images/WiFi-Manager/WiFi-Manager_01_Bib-einbinden-Menü.png" width="604" height="673" />

## First test-program

In order to test the Wifi-Manager, a new Arduino-file has to be opened (*File* --> *New* or via shortcut *CTRL* + *N*)

The first test-program includes a setup-function and a loop



```
#include &lt;WiFiManager.h&gt;                                   
void setup() {                                                     
WiFiManager wifiManager;                                           
wifiManager.autoConnect();                                         
}                                                                
void loop(){}   
```

                 
 
<img src="../../images/WiFi-Manager/WiFi-Manager_02_Testprogramm.png" width="259" height="316" /> 

To upload the program, you have to click the button with arrow (marked red)

<img src="../../images/WiFi-Manager/WiFi-Manager_03_Hochladen2.png" width="486" height="593" />

After the upload was successful you will get to see the message "Upload successful" in the lower part of the window (marked red in the lower picture)

<img src="../../images/WiFi-Manager/WiFi-Manager_03_Hochladen-erfolgreich2.png" width="604" height="489" />