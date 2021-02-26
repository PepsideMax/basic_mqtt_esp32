# basic_mqtt_etp32

This is a basic mqtt client on the esp32 used for turning a led on and off, using a physical and online method and sending temperature and humidity data. 

A short warning: this is not a secure way of working with mqtt please do not use this in an actual application this is purely for educational purposes
to make this project yourself you will need:
- esp32
- dht11/22
- led (+ optional resistance is preferred but not necessary for this test setup)
- button
- mqtt host server 

First install node-red red on your laptop or pc and install the dashboard module https://flows.nodered.org/node/node-red-dashboard.
Then start node red and import the noderedmqtt.json flow. 

Then download the basc_mqtt_esp32.ino file open it in your prefered arduino code editor and create a file named wifi.h in the same folder in which you put the following: 
#define ssid “the ssid of your wifi network”
#define password “the password of your wifi network”
const char* mqtt_server = "the ip address of your mqtt server";

To see the pins used for this project check the led_pin, butt_pin and dhtpin constants.

To connect the node red to your own mqtt server go to one of the mqtt modules and change the server to hove your own server IP after deploying this you should be able to go to localhost:1880/ui to see your data in an interface.
