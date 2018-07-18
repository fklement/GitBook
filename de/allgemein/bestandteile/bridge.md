# Bridge

## Technisch

### Bestandteile
* Netzwerkfähiger Microcontroller
    * ESP8266
* Gleiches Funkmodul muss erhalten sein, wie auf dem Sensor-Board-Node
    * RFM69 Funkmodul
    


<img src="../../../images/bestandteile/bridge.jpg" width="456" height="401" />



### Funktionsweise
Die Bridge erhält über das Funkmodul die Daten des Sensor-Boards. Dabei wird die UUID des Boards und die aktuellen Messwerte des Sensors im JSON-LD Format übermittelt. Anschließend baut die Bridge eine Verbindung zum Gateway auf und fordert dort die verknüpften RDF-Daten zur passenden UUID an. Anhand dieser RDF-Daten wird die MQTT URI gebildet. 
Anschließend published die Bridge über das jeweilige Topic an den MQTT Broker den Wert.  


### Beispiel Platinenlayout
<img src="../../../images/bestandteile/fritzing_bridge.PNG" width="455" height="341" />  
 
Hier sehen Sie ein mögliches Layoutdesign der Bridge.
Als Funkmodul wurde das RFM69 verwendet und als Microcontroller ein ESP8266.
