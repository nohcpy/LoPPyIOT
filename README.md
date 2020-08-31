# LoPPyIOT

The goal of this project is to document the creation of simple Low Power Python IOT devices.

## Criteria

* Low power consumption. 
* MicroPython and/or CircuitPython controlled.  
* Easily sourced and inexpensive hardware.  
* Agnostic to specific hubs, gateways, and other projects as possible.
* Easy to configure and as self contained as possible.

## Background

I have devoted many hours over the past few years to experimenting with various IoT devices, home automation solutions, sensors, light, you name it.  I went from solely DIY to fully off the shelf and somewhere in between.  I love playing with DIY stuff but I don't enjoy coding in C/C++.  I even less enjoy fixing something I already have made 6 months ago and having to relearn what I did.  The off the shelf stuff can be easier for a bit but I have experienced updates that break the entire setup, APIs shutdown for various reasons, etc.  I had one device where the company went out of business and shut down their servers so their device completely stopped working.  Anyways, this recently led me to researching MicroPython which I had only briefly experimented with a while back.  The cost of the boards and lack of libraries turned me away initially but I was happy to see what Adafruit was doing with CircuitPython and thus the experimenting began.

## Testing Status

### RFM69 and SAMD21 M0
I initially set out with the goal of using CircuitPython as that project has so much support including working RFM69 and RFM9x libraries. I have some experience with the RFM69 radio modules and own several Moteinos from Lowpowerlabs.  They are great boards and I really like everything about what Felix has created.  I highly suggest you check them out.  RFM69s are great for low power as they have a very low sleep current and short time needed to transmit data.  I believe the SAMD21 M0 can make a great low power python board and I am working on getting that setup working.  Will keep you posted.  The most suitable board I have found is the Moteino M0.  It already has low power friendly components and the radio module is on the board.  I think it's just a matter of getting the processor to sleep and making sure the pins are pulled to the right state.  
https://github.com/BitKnitting/wakey_circuitpython/wiki

### ESP8266
I did some testing with the ESP8266 and it could work.  I have several Wemos D1 minis and they can be modified to run at pretty low power when sleeping.  Right now I like the ESP32 much better though so not sure I am going to pursue this route.  

### ESP32-S1

The ESP32-S1 is the most promising by far at this point.  I was able to hunt down some awesome boards from Ezsbc that are super low power, have a ton of features, and are available in the feather board layout.  This meets all the requirements from a hardware perspective and I am definitely going to build from this design first.

### The ESP32-S2

The ESP32-S2 looks very promising but it's still very new.  I don’t have any dev boards yet and there are no low power production dev boards that I know of yet.  

## Technology and Project Resources 

To be updated….
