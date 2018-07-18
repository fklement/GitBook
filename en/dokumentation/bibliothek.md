# Summary

 Members                        | Descriptions                                
--------------------------------|---------------------------------------------
`define `[`SENSORTYPE`](#_brightness_sensor_8cpp_1a509736813096e8cbc106b117fad43ccc)            | 
`enum `[`Status`](#devices_2_status_device_8h_1a67a0db04d321a74b7e7fcfd3f1a3f70b)            | 
`class `[`BrightnessSensor`](#class_brightness_sensor) | 
`class `[`EmptyEEPROM`](#class_empty_e_e_p_r_o_m) | 
`class `[`EmptyTestRadioDevice`](#class_empty_test_radio_device) | 
`class `[`PullUpSetupButtonDevice`](#class_pull_up_setup_button_device) | 
`class `[`RadioDevice`](#class_radio_device) | 
`class `[`SensorBoardDevice`](#class_sensor_board_device) | 
`class `[`SensorDevice`](#class_sensor_device) | 
`class `[`SetupButtonDevice`](#class_setup_button_device) | 
`class `[`SingleLedStatusDevice`](#class_single_led_status_device) | 
`class `[`StatusDevice`](#class_status_device) | 
`class `[`Stm32EEPROM`](#class_stm32_e_e_p_r_o_m) | 
`class `[`STM32SensorBoard`](#class_s_t_m32_sensor_board) | 
`class `[`StorageDevice`](#class_storage_device) | 

## Members

#### `define `[`SENSORTYPE`](#_brightness_sensor_8cpp_1a509736813096e8cbc106b117fad43ccc) 

#### `enum `[`Status`](#devices_2_status_device_8h_1a67a0db04d321a74b7e7fcfd3f1a3f70b) 

 Values                         | Descriptions                                
--------------------------------|---------------------------------------------
OK            | 
SETUP_MODE            | 
LINKING            | 
ERROR            | 
SEND_MQTT_MESSAGE            | 
EMPTY            | 

# class `BrightnessSensor` 

```
class BrightnessSensor
  : public SensorDevice
```  

## Summary

 Members                        | Descriptions                                
--------------------------------|---------------------------------------------
`public virtual bool `[`begin`](#class_brightness_sensor_1a94ca31afa0684433c478c50174214598)`()` | Initialization of the sensor and determination of the output-mode.
`public virtual bool `[`loop`](#class_brightness_sensor_1abf8151307016a0496dbbb50401888ee7)`()` | Is called for every run.
`public virtual JsonObject & `[`getValueToSendAsJson`](#class_brightness_sensor_1a5ae67cd276bf69e784638420084ce34e)`(DynamicJsonBuffer & buffer)` | Returns the current value of the sensor as Json-object.
`public virtual JsonArray & `[`getTypeAsJson`](#class_brightness_sensor_1a28c4bc9b3b1be31118d1412474b730d0)`(DynamicJsonBuffer & buffer)` | Returns the type of the sensor as Json-object.

## Members

#### `public virtual bool `[`begin`](#class_brightness_sensor_1a94ca31afa0684433c478c50174214598)`()` 

Initialization of the sensor and determination of the output-mode.

#### Parameters
* `TRUE` Successful initialization 

* `FALSE` Sensor could not be initialized

#### `public virtual bool `[`loop`](#class_brightness_sensor_1abf8151307016a0496dbbb50401888ee7)`()` 

Is called for every run.

#### `public virtual JsonObject & `[`getValueToSendAsJson`](#class_brightness_sensor_1a5ae67cd276bf69e784638420084ce34e)`(DynamicJsonBuffer & buffer)` 

Returns the current value of the sensor as Json-object.

#### Returns
Current value as Json-object

#### `public virtual JsonArray & `[`getTypeAsJson`](#class_brightness_sensor_1a28c4bc9b3b1be31118d1412474b730d0)`(DynamicJsonBuffer & buffer)` 

Returns the type of the sensor as Json-object.

#### Returns
Type as Json-object

# class `EmptyEEPROM` 

```
class EmptyEEPROM
  : public StorageDevice
```  

## Summary

 Members                        | Descriptions                                
--------------------------------|---------------------------------------------
`public virtual String `[`readFromStorage`](#class_empty_e_e_p_r_o_m_1adbdb3b8539e4766a5284bae596809668)`(String key)` | Returns the value to the associated key from memory.
`public virtual bool `[`writeInStorage`](#class_empty_e_e_p_r_o_m_1a5afd5223d1f70c94ef05bf453a9a88c7)`(String key,String value)` | Permanently saves the value with the associated key in memory.
`public virtual bool `[`removeFromStorage`](#class_empty_e_e_p_r_o_m_1af3278e04e9789a971e58b7284ea26a73)`(String key)` | Removes the value from the memory.

## Members

#### `public virtual String `[`readFromStorage`](#class_empty_e_e_p_r_o_m_1adbdb3b8539e4766a5284bae596809668)`(String key)` 

Returns the value to the associated key from memory.

#### Parameters
* `key` key of the value

#### Returns
value

#### `public virtual bool `[`writeInStorage`](#class_empty_e_e_p_r_o_m_1a5afd5223d1f70c94ef05bf453a9a88c7)`(String key,String value)` 

Permanently saves the value with the associated key in memory.

#### Parameters
* `TRUE` Value saved successfully 

* `FALSE` Value could't be saved

#### `public virtual bool `[`removeFromStorage`](#class_empty_e_e_p_r_o_m_1af3278e04e9789a971e58b7284ea26a73)`(String key)` 

Removes the value from the memory.

#### Parameters
* `TRUE` Value removed successfully 

* `FALSE` Value could't be removed

# class `EmptyTestRadioDevice` 

```
class EmptyTestRadioDevice
  : public RadioDevice
```  

## Summary

 Members                        | Descriptions                                
--------------------------------|---------------------------------------------
`public  `[`EmptyTestRadioDevice`](#class_empty_test_radio_device_1ab39f21ebdb35be0918b137de98e98c6f)`()` | 
`public virtual bool `[`begin`](#class_empty_test_radio_device_1a9a874586b844a91223470fb6e6608ec2)`()` | Initialization of radio module.
`public virtual bool `[`loop`](#class_empty_test_radio_device_1a98a08ed433cec505a45bb882a1d0d9e2)`()` | Is called for every run.
`public virtual bool `[`startRadioDevice`](#class_empty_test_radio_device_1a67db1c0970bfd913b064e22577c6d7e8)`()` | Radio module is started.
`public virtual bool `[`stopRadioDevice`](#class_empty_test_radio_device_1ad11dfdcc424b2865e2254dd31ef0c19e)`()` | Radio module is stopped.
`public virtual int `[`getMaxMessageLength`](#class_empty_test_radio_device_1a57daf3518e814ba4e7714f03d73a5d75)`()` | Returns the maximum length of the messages that can be sent by the radio module.
`public virtual JsonVariant `[`getTypeAsJson`](#class_empty_test_radio_device_1abd125f3a2350973f8c0345518df3d1ec)`(DynamicJsonBuffer & buffer)` | Returns the type of the radio module as Json-object.
`public virtual JsonObject & `[`getConfigAsJson`](#class_empty_test_radio_device_1a645990d6ac6170c5ee46ea7002cd8c24)`(DynamicJsonBuffer & buffer)` | Returns the configuration of the radio module as Json-object.
`public virtual void `[`setServerConfig`](#class_empty_test_radio_device_1ac881fd9c520e7fdbbafc5ea93183bc5f)`(JsonObject & jsonConfig)` | Sets the configuration of the radio module.
`public virtual bool `[`sendMessage`](#class_empty_test_radio_device_1a794d81287c993992da19f0d30cd0bc21)`(String & buffer)` | Sends the message to the server.
`public virtual bool `[`connect`](#class_empty_test_radio_device_1af64367b0c7ab1c3cfcc63498942aef05)`()` | The connection to the server is being established.

## Members

#### `public  `[`EmptyTestRadioDevice`](#class_empty_test_radio_device_1ab39f21ebdb35be0918b137de98e98c6f)`()` 

#### `public virtual bool `[`begin`](#class_empty_test_radio_device_1a9a874586b844a91223470fb6e6608ec2)`()` 

Initialization of radio module.

#### Parameters
* `TRUE` Successful initialization 

* `FALSE` Radio module could not be initialized

#### `public virtual bool `[`loop`](#class_empty_test_radio_device_1a98a08ed433cec505a45bb882a1d0d9e2)`()` 

Is called for every run.

#### `public virtual bool `[`startRadioDevice`](#class_empty_test_radio_device_1a67db1c0970bfd913b064e22577c6d7e8)`()` 

Radio module is started.

#### Parameters
* `TRUE` Successful start 

* `FALSE` Radio module could not be started

#### `public virtual bool `[`stopRadioDevice`](#class_empty_test_radio_device_1ad11dfdcc424b2865e2254dd31ef0c19e)`()` 

Radio module is stopped.

#### Parameters
* `TRUE` Successful Stop 

* `FALSE` Radio module could not be stopped

#### `public virtual int `[`getMaxMessageLength`](#class_empty_test_radio_device_1a57daf3518e814ba4e7714f03d73a5d75)`()` 

Returns the maximum length of the messages that can be sent by the radio module.

#### Returns
maximum message-length

#### `public virtual JsonVariant `[`getTypeAsJson`](#class_empty_test_radio_device_1abd125f3a2350973f8c0345518df3d1ec)`(DynamicJsonBuffer & buffer)` 

Returns the type of the radio module as Json-object.

#### Returns
type as Json-object

#### `public virtual JsonObject & `[`getConfigAsJson`](#class_empty_test_radio_device_1a645990d6ac6170c5ee46ea7002cd8c24)`(DynamicJsonBuffer & buffer)` 

Returns the configuration of the radio module as Json-object.

#### Returns
configuration as Json-object

#### `public virtual void `[`setServerConfig`](#class_empty_test_radio_device_1ac881fd9c520e7fdbbafc5ea93183bc5f)`(JsonObject & jsonConfig)` 

Sets the configuration of the radio module.

#### Parameters
* `jsonConfig` configuration of the radio module

#### `public virtual bool `[`sendMessage`](#class_empty_test_radio_device_1a794d81287c993992da19f0d30cd0bc21)`(String & buffer)` 

Sends the message to the server.

#### Parameters
* `buffer` the sending message

#### Parameters
* `TRUE` Message sent successfully 

* `FALSE` Message could not be sent

#### `public virtual bool `[`connect`](#class_empty_test_radio_device_1af64367b0c7ab1c3cfcc63498942aef05)`()` 

The connection to the server is being established.

#### Parameters
* `TRUE` Connection is established successfully 

* `FALSE` Connection could not be established

# class `PullUpSetupButtonDevice` 

```
class PullUpSetupButtonDevice
  : public SetupButtonDevice
```  

## Summary

 Members                        | Descriptions                                
--------------------------------|---------------------------------------------
`public  `[`PullUpSetupButtonDevice`](#class_pull_up_setup_button_device_1aa1e30733894315fefa7bba84d16fedbc)`(int buttonPin)` | 
`public virtual bool `[`begin`](#class_pull_up_setup_button_device_1abd2aefc45ae40f2143cdf2b139faccf6)`()` | Initialization of the button and determination of the input-mode for the button.
`public virtual bool `[`loop`](#class_pull_up_setup_button_device_1a931aa8ae66d7eafd6ba5b2bb99eef72b)`()` | Is called for every run.
`public virtual bool `[`isPressed`](#class_pull_up_setup_button_device_1aa3d426fdca29cd8adddd3f26fe77d10f)`()` | Returns, if the button is pressed.

## Members

#### `public  `[`PullUpSetupButtonDevice`](#class_pull_up_setup_button_device_1aa1e30733894315fefa7bba84d16fedbc)`(int buttonPin)` 

#### `public virtual bool `[`begin`](#class_pull_up_setup_button_device_1abd2aefc45ae40f2143cdf2b139faccf6)`()` 

Initialization of the button and determination of the input-mode for the button.

#### Parameters
* `TRUE` Initialization successful 

* `FALSE` Button could not be initialized

#### `public virtual bool `[`loop`](#class_pull_up_setup_button_device_1a931aa8ae66d7eafd6ba5b2bb99eef72b)`()` 

Is called for every run.

#### `public virtual bool `[`isPressed`](#class_pull_up_setup_button_device_1aa3d426fdca29cd8adddd3f26fe77d10f)`()` 

Returns, if the button is pressed.

#### Parameters
* `TRUE` Button is pressed 

* `FALSE` Button is not pressed

# class `RadioDevice` 

## Summary

 Members                        | Descriptions                                
--------------------------------|---------------------------------------------
`public bool `[`begin`](#class_radio_device_1a1e3bae05174cefd126dfd0865fc6a13e)`()` | Initialization of radio module.
`public bool `[`loop`](#class_radio_device_1a22a76a4a896062be9d963268fc5816d8)`()` | Is called for every run.
`public bool `[`startRadioDevice`](#class_radio_device_1ac1654b3214d754e9016ec5030f1ab961)`()` | Radio module is started.
`public bool `[`stopRadioDevice`](#class_radio_device_1a724270c4a49bf55305d1f12466a48262)`()` | Radio module is stopped.
`public int `[`getMaxMessageLength`](#class_radio_device_1a2315c9fdb81eaf7f56a85fe32ec4aa31)`()` | Returns the maximum length of the messages that can be sent by the radio module.
`public JsonVariant `[`getTypeAsJson`](#class_radio_device_1a50c3e62cee6eb1100e2d88d7c702a147)`(DynamicJsonBuffer & buffer)` | Returns the type of the radio module as Json-object.
`public JsonObject & `[`getConfigAsJson`](#class_radio_device_1a5fdacca976595a90eb33a562b066d71a)`(DynamicJsonBuffer & buffer)` | Returns the configuration of the radio module as Json-object.
`public void `[`setServerConfig`](#class_radio_device_1a33a7a185cac8dac9e7493a0af653ef7f)`(JsonObject & jsonConfig)` | Sets the configuration of the radio module.
`public bool `[`sendMessage`](#class_radio_device_1afe5ba95def57de345db6e615622d7a70)`(String & buffer)` | Sends the message to the server.
`public bool `[`connect`](#class_radio_device_1af6d0252a2ac8cba533c3ec4d07f2b6ee)`()` | The connection to the server is being established.

## Members

#### `public bool `[`begin`](#class_radio_device_1a1e3bae05174cefd126dfd0865fc6a13e)`()` 

Initialization of radio module.

#### Parameters
* `TRUE` Successful initialization 

* `FALSE` Radio module could not be initialized

#### `public bool `[`loop`](#class_radio_device_1a22a76a4a896062be9d963268fc5816d8)`()` 

Is called for every run.

#### `public bool `[`startRadioDevice`](#class_radio_device_1ac1654b3214d754e9016ec5030f1ab961)`()` 

Radio module is started.

#### Parameters
* `TRUE` Successful start 

* `FALSE` Radio module could not be started

#### `public bool `[`stopRadioDevice`](#class_radio_device_1a724270c4a49bf55305d1f12466a48262)`()` 

Radio module is stopped.

#### Parameters
* `TRUE` Successful Stop 

* `FALSE` Radio module could not be stopped

#### `public int `[`getMaxMessageLength`](#class_radio_device_1a2315c9fdb81eaf7f56a85fe32ec4aa31)`()` 

Returns the maximum length of the messages that can be sent by the radio module.

#### Returns
maximum message-length

#### `public JsonVariant `[`getTypeAsJson`](#class_radio_device_1a50c3e62cee6eb1100e2d88d7c702a147)`(DynamicJsonBuffer & buffer)` 

Returns the type of the radio module as Json-object.

#### Returns
type as Json-object

#### `public JsonObject & `[`getConfigAsJson`](#class_radio_device_1a5fdacca976595a90eb33a562b066d71a)`(DynamicJsonBuffer & buffer)` 

Returns the configuration of the radio module as Json-object.

#### Returns
configuration as Json-object

#### `public void `[`setServerConfig`](#class_radio_device_1a33a7a185cac8dac9e7493a0af653ef7f)`(JsonObject & jsonConfig)` 

Sets the configuration of the radio module.

#### Parameters
* `jsonConfig` configuration of the radio module

#### `public bool `[`sendMessage`](#class_radio_device_1afe5ba95def57de345db6e615622d7a70)`(String & buffer)` 

Sends the message to the server.

#### Parameters
* `buffer` the sending message

#### Parameters
* `TRUE` Message sent successfully 

* `FALSE` Message could not be sent

#### `public bool `[`connect`](#class_radio_device_1af6d0252a2ac8cba533c3ec4d07f2b6ee)`()` 

The connection to the server is being established.

#### Parameters
* `TRUE` Connection is established successfully 

* `FALSE` Connection could not be established

# class `SensorBoardDevice` 

## Summary

 Members                        | Descriptions                                
--------------------------------|---------------------------------------------
`public  `[`SensorBoardDevice`](#class_sensor_board_device_1aed29a5ead2c20121a463abf678bd72e6)`()` | 
`public  `[`~SensorBoardDevice`](#class_sensor_board_device_1a2461e83ff54b733be3fbfff0adf57f35)`()` | 
`public bool `[`begin`](#class_sensor_board_device_1aadc6109fc3cc1268b44a1ad3f5405081)`()` | Initialization of the sensor-board.
`public bool `[`loop`](#class_sensor_board_device_1a3e9a1fa2396d7614ba447899c396947a)`()` | This method is run through in every loop in the ino-file.
`public bool `[`sendMessage`](#class_sensor_board_device_1a65113b0c8d7ddc6f3285eaa0991c19a3)`(String & buffer)` | Sending a message via the radio-module.
`public `[`StatusDevice`](#class_status_device)` & `[`getStatus`](#class_sensor_board_device_1af1c97a8320f2d9e074e929ab6c30d90b)`()` | Returns the device for the output of the status.
`public void `[`setStatus`](#class_sensor_board_device_1a606ea9015e0a7205bff0e4a8ef1f5426)`(`[`StatusDevice`](#class_status_device)` & status)` | Sets the device for the output of the status.
`public `[`SetupButtonDevice`](#class_setup_button_device)` & `[`getSetupButton`](#class_sensor_board_device_1af163ed6e25f79cd82af36787811351a0)`()` | Returns the button that starts the setup-mode.
`public void `[`setSetupButton`](#class_sensor_board_device_1a356f384d05a3158503760f618d15bd6b)`(`[`SetupButtonDevice`](#class_setup_button_device)` & setupButton)` | Sets the button that starts the setup-mode.
`public `[`RadioDevice`](#class_radio_device)` & `[`getRadioModul`](#class_sensor_board_device_1a353ded8f9cf7cd12f561f286f6544ecc)`()` | Returns the radio-module that is used for the connection to the bridge.
`public void `[`setRadioModul`](#class_sensor_board_device_1a716638c39981b8cda8dd18ab7bcb41dd)`(`[`RadioDevice`](#class_radio_device)` & radioModul)` | Sets the radio-module that is used for the connection to the bridge.
`public `[`SensorDevice`](#class_sensor_device)` & `[`getSensor`](#class_sensor_board_device_1a5412ce2d788d9aa26971da3e59c343da)`()` | Returns the sensor that is installed on the sensor-board.
`public void `[`setSensor`](#class_sensor_board_device_1aaba25337f0109e0fc3228a5aa26e0db3)`(`[`SensorDevice`](#class_sensor_device)` & sensor)` | Sets the sensor that is installed on the sensor-board.
`public `[`StorageDevice`](#class_storage_device)` & `[`getStorageDevice`](#class_sensor_board_device_1af6412dd5d7323e050e50bfa4d5337ab1)`()` | Returns the memory, which stored the data permanently.
`public void `[`setStorageDevice`](#class_sensor_board_device_1a3969a2ee2b9f8fb2e84c4ce4bbaeb512)`(`[`StorageDevice`](#class_storage_device)` & storage)` | Sets the memory, which stored the data permanently.
`public Stream & `[`getConnectionStream`](#class_sensor_board_device_1a78ba85d90380d254bd66221c6c1e08f4)`()` | Returns the http-connection that is used for the connection to the gateway.
`public void `[`setConnectionStream`](#class_sensor_board_device_1a9ba2c32c49766be3172e37400e5d9070)`(Stream * stream)` | Sets the http-connection that is used for the connection to the gateway.
`public int `[`getSetupModePressTime`](#class_sensor_board_device_1abf8050ddf0756a62d8d38625c474ec69)`()` | Returns the amount of seconds that the button needs to be pressed to enter the setup-mode.
`public void `[`setSetupModePressTime`](#class_sensor_board_device_1a08120fe8e8167e510a02abac14308510)`(int pressTime)` | Sets the amount of seconds that the button needs to be pressed to enter the setup-mode. Therefore the time for the setup-mode needs to be shorter than the time for the reset-mode.
`public int `[`getResetPressTime`](#class_sensor_board_device_1a8a51b4bf5f9e2b73e91df9fd4a547ca7)`()` | Returns the amount of seconds that the button needs to be pressed to enter the reset-mode.
`public void `[`setResetPressTime`](#class_sensor_board_device_1a6fbdab18c9632c922babeeaffeb07451)`(int pressTime)` | Sets the amount of seconds that the button needs to be pressed to enter the reset-mode. Therefore the time for the reset-mode needs to be longer than the time for the setup-mode.
`public char * `[`getUuid`](#class_sensor_board_device_1ac7d49c4beb4ed5c6b351bbc893d0453f)`()` | Returns the UUID of the device.
`public void `[`setUuid`](#class_sensor_board_device_1a5eb7d8ad1f07ebce6119b9c3456082c6)`(const char * uuid)` | Sets the UUID of the device.
`public bool `[`isInSetupMode`](#class_sensor_board_device_1ae967d4afac88276cffc83df9e9ceb911)`()` | Indicating if the sensor-board is in setup-mode.
`public JsonObject & `[`getContextAsJson`](#class_sensor_board_device_1a9148df5b440136454eb416b7c16a0098)`(JsonBuffer & buffer)` | Returns the JsonLD-context of the Sensor-Board.

## Members

#### `public  `[`SensorBoardDevice`](#class_sensor_board_device_1aed29a5ead2c20121a463abf678bd72e6)`()` 

#### `public  `[`~SensorBoardDevice`](#class_sensor_board_device_1a2461e83ff54b733be3fbfff0adf57f35)`()` 

#### `public bool `[`begin`](#class_sensor_board_device_1aadc6109fc3cc1268b44a1ad3f5405081)`()` 

Initialization of the sensor-board.

#### Parameters
* `TRUE` Successful initialization 

* `FALSE` Sensor-Board could not be initialized

#### `public bool `[`loop`](#class_sensor_board_device_1a3e9a1fa2396d7614ba447899c396947a)`()` 

This method is run through in every loop in the ino-file.

#### Parameters
* `TRUE` Method ran through successfully 

* `FALSE` Method failed to run through

#### `public bool `[`sendMessage`](#class_sensor_board_device_1a65113b0c8d7ddc6f3285eaa0991c19a3)`(String & buffer)` 

Sending a message via the radio-module.

#### Parameters
* `buffer` The message to be sent 

#### Parameters
* `TRUE` Message was sent successfully 

* `FALSE` Message could not be sent

#### `public `[`StatusDevice`](#class_status_device)` & `[`getStatus`](#class_sensor_board_device_1af1c97a8320f2d9e074e929ab6c30d90b)`()` 

Returns the device for the output of the status.

#### Returns
statusDevice

#### `public void `[`setStatus`](#class_sensor_board_device_1a606ea9015e0a7205bff0e4a8ef1f5426)`(`[`StatusDevice`](#class_status_device)` & status)` 

Sets the device for the output of the status.

#### Parameters
* `status` [StatusDevice](#class_status_device) to be set

#### `public `[`SetupButtonDevice`](#class_setup_button_device)` & `[`getSetupButton`](#class_sensor_board_device_1af163ed6e25f79cd82af36787811351a0)`()` 

Returns the button that starts the setup-mode.

#### Returns
setupButton

#### `public void `[`setSetupButton`](#class_sensor_board_device_1a356f384d05a3158503760f618d15bd6b)`(`[`SetupButtonDevice`](#class_setup_button_device)` & setupButton)` 

Sets the button that starts the setup-mode.

#### Parameters
* `setupButton` SetupButton to be set

#### `public `[`RadioDevice`](#class_radio_device)` & `[`getRadioModul`](#class_sensor_board_device_1a353ded8f9cf7cd12f561f286f6544ecc)`()` 

Returns the radio-module that is used for the connection to the bridge.

#### Returns
radioModul

#### `public void `[`setRadioModul`](#class_sensor_board_device_1a716638c39981b8cda8dd18ab7bcb41dd)`(`[`RadioDevice`](#class_radio_device)` & radioModul)` 

Sets the radio-module that is used for the connection to the bridge.

#### Parameters
* `radioModul` Radio-module to be set

#### `public `[`SensorDevice`](#class_sensor_device)` & `[`getSensor`](#class_sensor_board_device_1a5412ce2d788d9aa26971da3e59c343da)`()` 

Returns the sensor that is installed on the sensor-board.

#### Returns
sensor

#### `public void `[`setSensor`](#class_sensor_board_device_1aaba25337f0109e0fc3228a5aa26e0db3)`(`[`SensorDevice`](#class_sensor_device)` & sensor)` 

Sets the sensor that is installed on the sensor-board.

#### Parameters
* `sensor` Sensor to be set

#### `public `[`StorageDevice`](#class_storage_device)` & `[`getStorageDevice`](#class_sensor_board_device_1af6412dd5d7323e050e50bfa4d5337ab1)`()` 

Returns the memory, which stored the data permanently.

#### Returns
storage

#### `public void `[`setStorageDevice`](#class_sensor_board_device_1a3969a2ee2b9f8fb2e84c4ce4bbaeb512)`(`[`StorageDevice`](#class_storage_device)` & storage)` 

Sets the memory, which stored the data permanently.

#### Parameters
* `storage` to be set

#### `public Stream & `[`getConnectionStream`](#class_sensor_board_device_1a78ba85d90380d254bd66221c6c1e08f4)`()` 

Returns the http-connection that is used for the connection to the gateway.

#### Returns
connection

#### `public void `[`setConnectionStream`](#class_sensor_board_device_1a9ba2c32c49766be3172e37400e5d9070)`(Stream * stream)` 

Sets the http-connection that is used for the connection to the gateway.

#### Parameters
* `connection` HttpConnection to be set

#### `public int `[`getSetupModePressTime`](#class_sensor_board_device_1abf8050ddf0756a62d8d38625c474ec69)`()` 

Returns the amount of seconds that the button needs to be pressed to enter the setup-mode.

#### Returns
Time in seconds

#### `public void `[`setSetupModePressTime`](#class_sensor_board_device_1a08120fe8e8167e510a02abac14308510)`(int pressTime)` 

Sets the amount of seconds that the button needs to be pressed to enter the setup-mode. Therefore the time for the setup-mode needs to be shorter than the time for the reset-mode.

#### Parameters
* `pressTime` Time in seconds

#### `public int `[`getResetPressTime`](#class_sensor_board_device_1a8a51b4bf5f9e2b73e91df9fd4a547ca7)`()` 

Returns the amount of seconds that the button needs to be pressed to enter the reset-mode.

#### Returns
Time in seconds

#### `public void `[`setResetPressTime`](#class_sensor_board_device_1a6fbdab18c9632c922babeeaffeb07451)`(int pressTime)` 

Sets the amount of seconds that the button needs to be pressed to enter the reset-mode. Therefore the time for the reset-mode needs to be longer than the time for the setup-mode.

#### Parameters
* `pressTime` Time in seconds

#### `public char * `[`getUuid`](#class_sensor_board_device_1ac7d49c4beb4ed5c6b351bbc893d0453f)`()` 

Returns the UUID of the device.

#### Returns
uuid

#### `public void `[`setUuid`](#class_sensor_board_device_1a5eb7d8ad1f07ebce6119b9c3456082c6)`(const char * uuid)` 

Sets the UUID of the device.

#### Parameters
* `uuid` UUID to be set

#### `public bool `[`isInSetupMode`](#class_sensor_board_device_1ae967d4afac88276cffc83df9e9ceb911)`()` 

Indicating if the sensor-board is in setup-mode.

#### Parameters
* `TRUE` Sensor-Board is in setup-mode 

* `FALSE` Sensor-Board is not in setup-mode

#### `public JsonObject & `[`getContextAsJson`](#class_sensor_board_device_1a9148df5b440136454eb416b7c16a0098)`(JsonBuffer & buffer)` 

Returns the JsonLD-context of the Sensor-Board.

#### Returns
context as JsonObject

# class `SensorDevice` 

## Summary

 Members                        | Descriptions                                
--------------------------------|---------------------------------------------
`public bool `[`begin`](#class_sensor_device_1a29c391a719518b19e6d987d4749a862c)`()` | Initialization of the sensor and determination of the output-mode.
`public bool `[`loop`](#class_sensor_device_1ac066ec48feb52acb1b3d958baababbcc)`()` | Is called for every run.
`public JsonObject & `[`getValueToSendAsJson`](#class_sensor_device_1a8c6c45f047b5240d2092f2b7aa0a01dd)`(DynamicJsonBuffer & buffer)` | Returns the current value of the sensor as Json-object.
`public JsonArray & `[`getTypeAsJson`](#class_sensor_device_1abb24672fbd44c8613bd9667a5d3bbf60)`(DynamicJsonBuffer & buffer)` | Returns the type of the sensor as Json-object.

## Members

#### `public bool `[`begin`](#class_sensor_device_1a29c391a719518b19e6d987d4749a862c)`()` 

Initialization of the sensor and determination of the output-mode.

#### Parameters
* `TRUE` Successful initialization 

* `FALSE` Sensor could not be initialized

#### `public bool `[`loop`](#class_sensor_device_1ac066ec48feb52acb1b3d958baababbcc)`()` 

Is called for every run.

#### `public JsonObject & `[`getValueToSendAsJson`](#class_sensor_device_1a8c6c45f047b5240d2092f2b7aa0a01dd)`(DynamicJsonBuffer & buffer)` 

Returns the current value of the sensor as Json-object.

#### Returns
Current value as Json-object

#### `public JsonArray & `[`getTypeAsJson`](#class_sensor_device_1abb24672fbd44c8613bd9667a5d3bbf60)`(DynamicJsonBuffer & buffer)` 

Returns the type of the sensor as Json-object.

#### Returns
Type as Json-object

# class `SetupButtonDevice` 

## Summary

 Members                        | Descriptions                                
--------------------------------|---------------------------------------------
`public bool `[`begin`](#class_setup_button_device_1a86323ee22cd39fe44d42df34d387be3b)`()` | Initialization of the button and determination of the input-mode for the button.
`public bool `[`loop`](#class_setup_button_device_1a392f1bb810e188de00c5dbcab5ca0b72)`()` | Is called for every run.
`public bool `[`isPressed`](#class_setup_button_device_1aef9c55947fefa01e4a26d12dae8f9d1a)`()` | Returns, if the button is pressed.

## Members

#### `public bool `[`begin`](#class_setup_button_device_1a86323ee22cd39fe44d42df34d387be3b)`()` 

Initialization of the button and determination of the input-mode for the button.

#### Parameters
* `TRUE` Initialization successful 

* `FALSE` Button could not be initialized

#### `public bool `[`loop`](#class_setup_button_device_1a392f1bb810e188de00c5dbcab5ca0b72)`()` 

Is called for every run.

#### `public bool `[`isPressed`](#class_setup_button_device_1aef9c55947fefa01e4a26d12dae8f9d1a)`()` 

Returns, if the button is pressed.

#### Parameters
* `TRUE` Button is pressed 

* `FALSE` Button is not pressed

# class `SingleLedStatusDevice` 

```
class SingleLedStatusDevice
  : public StatusDevice
```  

## Summary

 Members                        | Descriptions                                
--------------------------------|---------------------------------------------
`public  `[`SingleLedStatusDevice`](#class_single_led_status_device_1af1a9e00aac3600455149106bee2898ec)`(int ledPin)` | 
`public virtual bool `[`begin`](#class_single_led_status_device_1a80e2a06ab3abab6d609f5461a2cb105f)`()` | Initialization of the status and definition of the output-mode.
`public virtual bool `[`loop`](#class_single_led_status_device_1ac59bd53277cbba0ba4769ac109829efe)`()` | Is called in every turn and returns the current status.

## Members

#### `public  `[`SingleLedStatusDevice`](#class_single_led_status_device_1af1a9e00aac3600455149106bee2898ec)`(int ledPin)` 

#### `public virtual bool `[`begin`](#class_single_led_status_device_1a80e2a06ab3abab6d609f5461a2cb105f)`()` 

Initialization of the status and definition of the output-mode.

#### Parameters
* `TRUE` Successful initialization 

* `FALSE` Status could not be initialized

#### `public virtual bool `[`loop`](#class_single_led_status_device_1ac59bd53277cbba0ba4769ac109829efe)`()` 

Is called in every turn and returns the current status.

# class `StatusDevice` 

## Summary

 Members                        | Descriptions                                
--------------------------------|---------------------------------------------
`public `[`Status`](#devices_2_status_device_8h_1a67a0db04d321a74b7e7fcfd3f1a3f70b)` `[`currentStatus`](#class_status_device_1a3a3ff51f5f629f02ed733b818ae84707) | 
`public bool `[`begin`](#class_status_device_1ab09ed46fdc035c93082de606b19ed26a)`()` | Initialization of the status and definition of the output-mode.
`public bool `[`loop`](#class_status_device_1aabbe19c4710f7156867c857661fd9b28)`()` | Is called in every turn and returns the current status.
`public void `[`setStatus`](#class_status_device_1a6beca177e2bf31bf4dd55e3d137f7555)`(`[`Status`](#devices_2_status_device_8h_1a67a0db04d321a74b7e7fcfd3f1a3f70b)` status)` | Sets the status.

## Members

#### `public `[`Status`](#devices_2_status_device_8h_1a67a0db04d321a74b7e7fcfd3f1a3f70b)` `[`currentStatus`](#class_status_device_1a3a3ff51f5f629f02ed733b818ae84707) 

#### `public bool `[`begin`](#class_status_device_1ab09ed46fdc035c93082de606b19ed26a)`()` 

Initialization of the status and definition of the output-mode.

#### Parameters
* `TRUE` Successful initialization 

* `FALSE` Status could not be initialized

#### `public bool `[`loop`](#class_status_device_1aabbe19c4710f7156867c857661fd9b28)`()` 

Is called in every turn and returns the current status.

#### `public void `[`setStatus`](#class_status_device_1a6beca177e2bf31bf4dd55e3d137f7555)`(`[`Status`](#devices_2_status_device_8h_1a67a0db04d321a74b7e7fcfd3f1a3f70b)` status)` 

Sets the status.

#### Parameters
* `status` -> the status to be set

# class `Stm32EEPROM` 

```
class Stm32EEPROM
  : public StorageDevice
```  

## Summary

 Members                        | Descriptions                                
--------------------------------|---------------------------------------------
`public virtual String `[`readFromStorage`](#class_stm32_e_e_p_r_o_m_1a836784b1c20eacb203ec9bfb5a247b49)`(String key)` | Returns the value to the associated key from memory.
`public virtual bool `[`writeInStorage`](#class_stm32_e_e_p_r_o_m_1add207fb78f912a15ccbb7231807ae6ca)`(String key,String value)` | Permanently saves the value with the associated key in memory.
`public virtual bool `[`removeFromStorage`](#class_stm32_e_e_p_r_o_m_1a7f3280ceba3e2d710bebf8221d1f49c0)`(String key)` | Removes the value from the memory.

## Members

#### `public virtual String `[`readFromStorage`](#class_stm32_e_e_p_r_o_m_1a836784b1c20eacb203ec9bfb5a247b49)`(String key)` 

Returns the value to the associated key from memory.

#### Parameters
* `key` key of the value

#### Returns
value

#### `public virtual bool `[`writeInStorage`](#class_stm32_e_e_p_r_o_m_1add207fb78f912a15ccbb7231807ae6ca)`(String key,String value)` 

Permanently saves the value with the associated key in memory.

#### Parameters
* `TRUE` Value saved successfully 

* `FALSE` Value could't be saved

#### `public virtual bool `[`removeFromStorage`](#class_stm32_e_e_p_r_o_m_1a7f3280ceba3e2d710bebf8221d1f49c0)`(String key)` 

Removes the value from the memory.

#### Parameters
* `TRUE` Value removed successfully 

* `FALSE` Value could't be removed

# class `STM32SensorBoard` 

```
class STM32SensorBoard
  : public SensorBoardDevice
```  

## Summary

 Members                        | Descriptions                                
--------------------------------|---------------------------------------------

## Members

# class `StorageDevice` 

## Summary

 Members                        | Descriptions                                
--------------------------------|---------------------------------------------
`public String `[`readFromStorage`](#class_storage_device_1a2028faad93235394a2327bcdd4630a17)`(String key)` | Returns the value to the associated key from memory.
`public bool `[`writeInStorage`](#class_storage_device_1aa1ffcf1c7187cc6f33eacd9642346e36)`(String key,String value)` | Permanently saves the value with the associated key in memory.
`public bool `[`removeFromStorage`](#class_storage_device_1aba00c01142203a082d17cae760c36332)`(String key)` | Removes the value from the memory.

## Members

#### `public String `[`readFromStorage`](#class_storage_device_1a2028faad93235394a2327bcdd4630a17)`(String key)` 

Returns the value to the associated key from memory.

#### Parameters
* `key` key of the value

#### Returns
value

#### `public bool `[`writeInStorage`](#class_storage_device_1aa1ffcf1c7187cc6f33eacd9642346e36)`(String key,String value)` 

Permanently saves the value with the associated key in memory.

#### Parameters
* `TRUE` Value saved successfully 

* `FALSE` Value could't be saved

#### `public bool `[`removeFromStorage`](#class_storage_device_1aba00c01142203a082d17cae760c36332)`(String key)` 

Removes the value from the memory.

#### Parameters
* `TRUE` Value removed successfully 

* `FALSE` Value could't be removed

Generated by [Moxygen](https://sourcey.com/moxygen)