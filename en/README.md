# Linked IoT

### Aim:
-   	By using Linked-Data and the web-standard semantic interoperability should be achieved
-   	The goal is to demonstrate how already existing standards of the Linked-Data can be used for IoT
-   	To reach the largest possible target audience, everything should be easily implemented (and as cheap as possible)
-   	Throughout a modular setting it should be possible for everybody to use their own components
-   	An extensive documentation should make it as easy as possible for the target audience to get started


### Problem:
-   	Linked Data has already proven its feasibility as instrument for connection and integration of data in the web
-   	With Linked Data it is possible to semantically combine structured data in order to describe their relationship
-   	At the moment it is difficult to bundle the different ways of broadcasting of each sensor and connect them with each other
-  	The different sensors can be addressed only with great effort but it’s impossible at the moment to process unknown structures and types of sensor independently 
-	With the use of Constrained Devices their individual limitation has to be considered 

### Approach of solution:
-       To make the modular setting possible, a library with abstract classes was built which can imported in the own project and run in Arduino 
-       The context which is used in the JSON-LD, is saved on the gateway
-       The bridge is working as operator in order to use the consistent web-standards for the broadcast
-       With a web interface the sensor’s initialisation and broadcasting-configuration is enabled
-       The linking between sensor and gateway is implemented throughout a web standard
-   	The bandwidth of the original payload (broadcast of the sensor’s data) is reduced through the transfer of the context at the linking
-   	The bridge is requesting the needed context at the gateway when broadcasting the sensor-data und is publishing the sensor’s value to the topic
