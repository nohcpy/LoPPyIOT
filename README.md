# LoPPyIOT

The overall goal of this project is to document the creation of simple Low Power Python IOT devices that meet the following criteria. 

* Low power consumption. 
* MicroPython and/or CircuitPython controlled.  
* Easily sourced and inexpensive hardware.  
* Agnostic to specific hubs, gateways, and other projects as possible.
* Easy to configure and as self contained as possible.

# Background

I have devoted many hours over the past few years to experimenting with various IoT devices, home automation solutions, sensors, light, you name it.  I went from solely DIY to fully off the shelf and somewhere in between.  I love playing with DIY stuff but most microtrollers are coded in C/C++.  I realize why this is and it's not that I find it overly difficult, I just don’t enjoy coding in it that much and it takes some of the fun out of it for me.  I tried more of the off the shelf stuff for a while (hub and sensors).  It was nice for a while but plenty of its own issues.  I have experienced updates that break the entire setup, APIs shutdown for various reasons, etc.  I had one device where the company went out of business and shut down their servers so their device completely stopped working and I had no idea for months.  Anyways, this recently led me to researching low power MicroPython projects which I had only briefly experimented with a while back.  The cost of the boards and lack of libraries turned me away initially but I was happy to see what Adafruit was doing with CircuitPython and thus the experimenting began.

# Finding a Suitable Board

I already own or have recently purchased several dev boards capable of running CircuitPython and/or MicroPython.  I knew the first step was going to be finding a suitable board that can meet the criteria of low power, inexpensive, and readily available.  To try and put some numbers to those: I define low power as a board that consumes less than 25µA in deep sleep, including all the components needed to support the processor itself.  Other factors will come into play I am sure but that is where I am starting.  Inexpensive to me is between $5-$20 for the board depending on what is included at that price.  Most commercial home automation devices that I have been willing to purchase are around 20-35 bucks so I want to stay in that range for the total cost of the board, sensors, battery, etc.  Readily available means you can order it from a reputable source constantly.  I realize that most dev boards are not going to be low power friendly and another option would be to design a board to meet my needs.  That may happen down the road but I have hopes of finding something I can just buy and expand for now.

## A Note on Data Transmission 

I really like RFM69 modules and I am messing around with RFM9x modules as well.  They are very low power and perfect for sensor data.  I don’t really like wifi for several reasons: power hungry, more likely to need reconfiguration in my household, range, etc.  

## ESP32-S1

The ESP32-S1 is looking very promising at this point.  I have found some inexpensive dev boards in the feather format and are able to sleep in the very low µA range.  Pairing the board with an RFM69 or RFM9x module could be a winner.

## The ESP32-S2

The ESP32-S2 looks very promising but it's still very new.  I don’t have any dev boards yet and there are no low power production dev boards that I know of yet.  I do know of one in the works so we will see.

## SAMD21 M0
The M0 can run CircuitPython but I don’t think putting the processor to sleep is natively supported.  There are a couple of boards that come with RFM modules which is nice.  More testing to come on this.

## ESP8266
I did some testing with the ESP8266 and it could work.  I have several Wemos D1 minis and they can be modified to run at pretty low power when sleeping.  It also works fine with a radio module.  That being said, right now I like the ESP32 much better though so not sure I am going to pursue this route.  

# Technology and Project Resources 

To be updated….


