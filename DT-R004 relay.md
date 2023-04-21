# ESPHome configuration for DT-R004 relay from Dingtian-Tech  
![DT-R004](https://user-images.githubusercontent.com/25821291/233686194-241baaf3-6a28-4ef3-8ac7-0f8dcd39579b.png)

NB: ESP32-WROOM comes with vendorlock. Flashing EspHome will brick the chip. Either request "Development" board from vendor, or solid new chip ESP32-WROOM chip.

GPIO settings for the ESPHome

```yaml
binary_sensor:
 - platform: gpio
   pin:
     number: GPIO39
     inverted: true 
   name: ${devicename}_DI4
 - platform: gpio
   pin:
     number: GPIO36
     inverted: true 
   name: ${devicename}_DI3
 - platform: gpio
   pin:
     number: GPIO35
     inverted: true 
   name: ${devicename}_DI1
 - platform: gpio
   pin:
     inverted: true    
     number: GPIO33
   name: ${devicename}_DI2
   
switch:
  - platform: gpio
    id: "relay2"
    name: ${devicename}_relay2
    pin: GPIO2
  - platform: gpio
    id: "relay1"
    name: ${devicename}_relay1
    pin: GPIO16
  - platform: gpio
    id: "relay3"
    name: ${devicename}_relay3
    pin: GPIO32
  - platform: gpio
    id: "relay4"
    name: ${devicename}_relay4
    pin: GPIO12
```
