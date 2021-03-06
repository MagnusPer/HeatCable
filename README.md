# HeatCable

Control system using external temperature sensor (DB18B20) with a configurable temperature treshold (SetTemp) controlling heatcable relay. LCD display (Omilex sheild-LCD16x2) to visualize external(OutTemp) and treshold(SetTemp) with relay status. Pushbutton to increase or decrease the temperature treshold.     

Two versions available **Basic** without any WiFi connection and one using WiFi and **MQTT** topics to publish status. 

<img src="https://github.com/MagnusPer/HeatCable/blob/main/images/LCDdisplay.jpg" width="400">


## Installation
Needed Arduino Libraries to be included in [IDE](https://www.arduino.cc/en/Main/Software). Install them either from GitHub repository directly or within the IDE application itself **Sketch > Import Library** 

| Library                            | Link to GitHub                                      |  Basic  |  MQTT  | 
| ---------------------------------- | --------------------------------------------------- |---------|--------|
| PubSubClient                       |  https://github.com/knolleary/pubsubclient          |         |   X    |     
| OneWire                            |                                                     |   X     |   X    |
| Dallas Temperature                 |                                                     |   X     |   X    |   
| Wire                               |                                                     |   X     |   X    |  
| LCD16x2                            | https://www.olimex.com/Products/Duino/Shields/SHIELD-LCD16x2/open-source-hardware |   X     |   X    |  
| Dallas Temperature                 |                                                     |   X     |   X    |  


## MQTT Topics
MQTT Topics to be published. 

| Topic                              | Description                                         |
| ---------------------------------- | --------------------------------------------------- |
| HeatCable/Status                   |  set topic - Status "online/offline"                |
| HeatCable/RelayStatus              |  set topic - Relay status "activated/deactivated"   |
| HeatCable/OutTemp                  |  set topic - Outdoor temperature                    |
| HeatCable/SetTemp                  |  set topic - Configured temperature                 |


## Wiring
<img src="https://github.com/MagnusPer/HeatCable/blob/main/images/HeatCable.JPG" width="800">


## BOM List
| Part                               | Comment/Link                                        |
| ---------------------------------- | --------------------------------------------------- |
|  Wemos D1 mini                     | https://www.wemos.cc/en/latest/                     |   
|  Omilex sheild-LCD16x2             | https://www.olimex.com/Products/Duino/Shields/SHIELD-LCD16x2/open-source-hardware |
|  Tempsensor DB18B20                |                                                     |  
|  Power Supply HLK-PM03             | http://www.hlktech.net/product_detail.php?ProId=59  |  


