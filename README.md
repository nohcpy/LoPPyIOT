# LoPPyIOT

The overall goal of this project is to document the creation of simple Low Power Python IOT devices that meet the following criteria. 

* Low power consumption. 
* MicroPython and/or CircuitPython controlled.  
* Easily sourced and inexpensive hardware.  
* Agnostic to specific hubs, gateways, and other projects as possible.
* Easy to configure and as self contained as possible.

# Background

I have devoted many hours over the past few years to experimenting with various IoT devices, home automation solutions, sensors, light, you name it.  I went from solely DIY to fully off the shelf and somewhere in between.  I love playing with DIY stuff but most microtrollers are coded in C/C++.  I realize why this is and it's not that I find it overly difficult, I just don’t enjoy coding in it that much and it takes some of the fun out of it for me.  I tried more of the off the shelf stuff for a while (hub and sensors).  It was nice for a while but plenty of its own issues.  I have experienced updates that break the entire setup, APIs shutdown for various reasons, etc.  I had one device where the company went out of business and shut down their servers so their device completely stopped working and I had no idea for months.  Anyways, this recently led me to researching low power MicroPython projects which I had only briefly experimented with a while back.  The cost of the boards and lack of libraries turned me away initially but I was happy to see what Adafruit was doing with CircuitPython and thus the experimenting began.

# Finding a suitable board

I already own or have recently purchased several dev boards capable of running CircuitPython and/or MicroPython.  I knew the first step was going to be finding a suitable board that can meet the criteria of low power, inexpensive, and readily available.  To try and put some numbers to those: I define low power as a board that consumes less than 25µA in deep sleep, including all the components needed to support the processor itself.  Other factors will come into play I am sure but that is where I am starting.  Inexpensive to me is between $5-$20 for the board depending on what is included at that price.  Most commercial home automation devices that I have been willing to purchase are around 20-35 bucks so I want to stay in that range for the total cost of the board, sensors, battery, etc.  Readily available means you can order it from a reputable source constantly.  I realize that most dev boards are not going to be low power friendly and another option would be to design a board to meet my needs.  That may happen on down the road but I have hopes of finding something I can just buy and expand for now.

## RFM69 and SAMD21 M0
I initially set out with the goal of using CircuitPython as that project has so much support including working RFM69 and RFM9x libraries. I have some experience with the RFM69 radio modules and own several Moteinos from Lowpowerlabs.  They are great boards and I really like everything about what Felix has created.  I highly suggest you check them out.  RFM69s are great for low power as they have a very low sleep current and short time needed to transmit data.  I believe the SAMD21 M0 can make a great low power python board and I am working on getting that setup working.  Will keep you posted.  The most suitable board I have found is the Moteino M0.  It already has low power friendly components and the radio module is on the board.  I think it's just a matter of getting the processor to sleep and making sure the pins are pulled to the right state.  

## ESP8266
I did some testing with the ESP8266 and it could work.  I have several Wemos D1 minis and they can be modified to run at pretty low power when sleeping.  Right now I like the ESP32 much better though so not sure I am going to pursue this route.  

## ESP32-S1

The ESP32-S1 is looking very promising at this point.  I was able to hunt down some awesome boards from Ezsbc that are super low power, have a ton of features, and are available in the feather board layout.  Wifi is of course built in which is great but it eats a lot of power during transmission and I don’t think it's a great candidate for sending sensor data too often.  I was able to port the CircuitPython RFMx libraries to work with MicroPython (thanks to some help) to test with.  It's a work in progress but having that option with the ability to still use wifi for configuration, or direct alering for certain events could be a real winner.  

## The ESP32-S2

The ESP32-S2 looks very promising but it's still very new.  I don’t have any dev boards yet and there are no low power production dev boards that I know of yet.  I do know of one in the works so we will see.

# Technology and Project Resources 

To be updated….
