# paragliding-flight-computer
Open Hardware vario/flight computer.

This is a long term project to make an open source / hardware flight computer for paragliding. The licenses will probably be MIT for software and 
the CERN OHL for hardware. The long term goal of this project is to make a vario that fuses the data from a GPS unit, a barometric pressure sensor, and 
a 9-axis IMU to provide a fast response to altitude changes for freeflight use. Most commercial varios are slow, using barometric pressure to detect altitude. 
There are some that use IMUs, but they're expensive and proprietary. My goal is to have this vario cost about $150 at most in terms of hardware.
This project is in the incredibly early stages because sensor fusion is really hard, as it turns out. This will log position information to an SD card, 
and I hope to have it be certified for use in paragliding competitions eventually.

My first prototype uses the Adafruit Feather Sense MCU, but it gets easily bogged down in all the calculations and timing requirements of managing sensors and 
writing to the SD card. I'm planning to switch to a Teensy MCU, probably the 4.1, to have a really high ceiling of processing power. I'm probably going to
use the Bosch BNO055 or BNO085 IMU as the primary sensor. I'm also currently using the Adafruit Ultimate GPS Featherwing for GPS, but may explore switching
to a u-Blox module. I'm using the Sharp Memory display from Adafruit for easy daylight readability and low power consumption.

Eventually this will all be on a custom PCB, but right now it's a giant stack of Featherwing modules. I also plan to develop something like a pitot tube for
true airspeed measurement for this flight computer, but that's even further in the future. 
