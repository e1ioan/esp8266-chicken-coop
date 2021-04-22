# Chicken Coop Door 
## powered by esp8266

The controller will sync the date/time from a GPS or using a NTP server. If you have a GPS, the controller will get the coordinates of the place to calculate the sunrise and sunset.

The door opens automatically at sunrise and closes one hour after the sunset. 

[Here is the code](https://github.com/e1ioan/esp8266-chicken-coop/blob/master/chicken-coop.ino)


## Code 

If you use a GPS, the coordinates will be updated automatically The coordinates are used to calculate the sunrise/sunset time. If you are not using a gps, replace the values of: 

float latitude = 44.9308;
float longitude = -123.0289;

with your own values. 

At first boot, you'll have to connect to the Access Point created by the esp8266 (go to 192.168.4.1) and configure your wifi network.

After esp8266 connects to your wifi, open in your browser the IP assigned, for the available commands.

![Main Page](http://i.imgur.com/6RE3KER.jpg)

## Wifi 

The code allows the "coop door" to run connected to your wifi, or as stand alone in AP mode.

![Wifi Mode](http://i.imgur.com/mbSJfk7.jpg)

##DynDNS

![DynDNS](http://i.imgur.com/iMRAzJt.jpg)

The esp8266 controller commands ~~a servo modified for continuous rotation to lift and lower a door (with two relays to reverse the rotation direction). The door mechanism is using pulleys (F/3), that way the servo doesn't have to work too hard.~~ a high torque geared motor to lift and lower the door. Please watch the video bellow for more details.

Click on the image below to see a video of the door operating:

[![Coop door video](https://img.youtube.com/vi/U9hd2GVmE3A/0.jpg)](https://www.youtube.com/watch?v=U9hd2GVmE3A)

Everything is powered by a 10 Watt 12 Volt solar panel

![Solar panel](http://i.imgur.com/OjkDhTW.jpg)


TO DO: [Use MQTT](https://learn.adafruit.com/mqtt-adafruit-io-and-you/overview)
