# Sensor-Board-Node

## Technological

### Components
* Microcontroller
    * STM32
* Radio module
    * RFM69
* Sensor
    * Brightness-sensor, temperature-sensor etc.
* Setup-button
* Status-display

<img src="../../../images/bestandteile/sensor_node.jpg" width="455" height="387" />





    
### Functionality
The sensor-board is transferred in the setup-mode by the setup- button.
The initialization of the board is run during the setup-mode, in which a UUID (Unique unified ID) is being generated respectively obtained from the gateway. Furthermore the RDF-data are transferred to the gateway (for other boards this is also possible via MAC-address).
The sensor-board is receiving the valid bridge configuration as response from the gateway, which is used to build the connection to the bridge afterwards. To save these data permanently, also when there is no electrical power, they are saved in the EEPROM.
The node is receiving a UUID from the gateway.


### Example of the circuit boards’ layout
<img src="../../../images/bestandteile/fritzing_sensor_board.PNG" width="455" height="313" />

This picture is showing a possible layout of the sensor board.
The RFM69 was used as radio module and the TSL2561 as brightness-sensor.

