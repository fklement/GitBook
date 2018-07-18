# Gateway

## Technisch

### Bestandteile
* Netzwerkfähiger Microcontroller
    * RaspberryPi

    
### Funktionsweise
Das Gateway ist dafür zuständig, die UUID's mit dem dazugehörigen RDF-Schema zu verknüpfen und zu speichern. Dabei werden die einzelnen Sensor-Boards zu Beginn, mit dem Gateway per USB-Kabel verbunden. Wenn sich das Sensor-Board im Setupmodus befindet, wird dieses auf dem Webinterface aufgelistet um anschließend die Initialisierung zu starten.

**Initialisierung:**
Bei der Initialisierung wird zu Beginn überprüft, ob das angeschlossene Sensor-Board über eine UUID verfügt. Ist dies nicht der Fall, wird diese vom Gateway generiert und an das Sensor-Board übermittelt. Als nächstes wird das RDF-Schema vom Sensor-Board angefordert und auf dem Gateway mit der UUID verknüpft und gespeichert. Das Gateway übermittelt anschließend eine gültige Bridge-Konfiguration an das angeschlossene Sensor-Board.

**Datentransfer**
Die Bridge fordert vom Gateway kontinuierlich das verknüpfte RDF-Schema zur UUID an.
