# WebInterface

## Installation

Run `npm run webinterface` in `/Code/WebInterface/` to install all the dependencies.

### Server
Run `npm start` for the server.

### Go on With the Angular DevMode
Run `npm run angulardev` to start the DevMode for the WebApp.

## Application

<img src="../../images/Webinterface/picture_1.png" width="600" height="318" />

The web interface consists of two parts, the **device** and the **radio** .


### Device
If there are no devices (sensor boards) connected, you will get to see the following window:

<img src="../../images/Webinterface/picture_2.png" width="600" height="318" />

By clicking on the button _Show Device_ all [approved devices] will be listed.  

Each **device** is listed with the following information: 

* ID
* Manufacturer
* ProductID
* VendorID
* LocationID
* …

<img src="../../images/Webinterface/picture_3.png" width="600" height="318" />

You can get the information of each single **device** to check which type of sensor it is.

<img src="../../images/Webinterface/picture_4.png" width="500" height="500" />

Furthermore the _UUID_ is assigned when checking the information, if there is none existing. 

<img src="../../images/Webinterface/picture_5.png" width="500" height="500" />

Generating the _UUID_ is marked with a flash message.

The existing **radio module** config is selected in the next stept, which will be sent to the board. After pressing the button _Initialize_, the board is saving the configuration.

<img src="../../images/Webinterface/picture_6.png" width="600" height="391" />

### Radio
You can find all the generated RadioHead configurations when selecting **Radio**. They can be edited or also deleted.

<img src="../../images/Webinterface/picture_7.png" width="600" height="318" />
