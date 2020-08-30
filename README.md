# LoPPyIOT

The goal of this project is to document the creation of simple Low Power Python IOT devices.

#Criteria

* Low power consumption. 
* MicroPython and/or CircuitPython controlled.
* Easily sourcable and inexpensive hardware.
* Agnostic to specific hubs, gateways, and other projects as possible.
* Easy to configure and as self contained as possible.

#Background

I have devoted many hours over the past few years to experimenting with various IoT devices, home automation solutions, sensors, light, you name it.  I went from soley DIY to fully off the shelf and somewhere in between.  I love playing with DIY stuff but I don't enjoy coding in C/C++.  I even less enjoy fixing something I already have made that 6 months ago and having to relearn what I did.  The off the shelf stuff can be easier for a bit but I have experiened updates that break the entire setup, APIs shutdown for various reasons, etc.  I had one device where the company went out of business and shutdown their servers so their device completely stopped working.  Anyways, this recently led me to researching MicroPython which I had only breifly experimented with a while back.  The cost of the boards and lack of libraries turned me away initially but I was happy to see what Adafruit was doing with CircuitPython and thus the experimenting began.

#Technology and Project Resources

#Experiments

RFM69 and SAMD21 M0
I initially set out with the goal of using CircuitPython as that project has so much support including a working RFM69 library. I have some experience with that radio module and own several Moteinos from Lowpowerlabs.  They are great boards and I really like everything about what Felix has created.  I highly suggest you check them out.  RFM69s are great for low power as they have a very low sleep current and short time needed to transmit data than wifi (depends).  They also should draw less current than a wifi transmisison.  I believe the SAMD21 M0 can make a great low power python board and I working on getting that setup working.  Will keep you posted.  The most suitable board I have found is the Moteino M0.  I think its just a matter of getting the processor to sleep and making sure the pins are pulled to the right state.  

ES8266

ESP32-S1

ESP32-S2

