Raspberry Pi LCD library
------------------------

This library will easily allow you to control an LCD1062 or LCD2004 display using the PCF8574 module

Copyright (c) 2019 Wade Ryan



## Requirements
On your Raspberry Pi, please use the raspi-config program to enable the I2C interface.
Then use the gpio command to make sure your i2c devices can be found.  .  

	$ sudo raspi-config
	$ gpio i2cd


## Prerequisites

This Library is based on [WiringPi](http://wiringpi.com/), so, you'll need make sure you 
have WiringPi installed before you can succesfully compile this library.  


## Install

To compile this library, navigate into the src folder and use the make utility to compile 
and install the library.

    $ cd [project folder]
    $ cd src
    $ make && sudo make install
    
    
## Compiling
Complie your applications using these command line arguments: -lwiringPi -lwiringPiDev -lwiringPiLCD101rpi


## Examples
In the example folder, there is a sample program that you can compile and run like this:

    $ cd [project folder]
    $ cd example
    $ gcc lcd1602.c -lwiringPi -lwiringPiLCD101rpi -o lcd1602
    $ ./lcd1602 -a 0x23
    Raspberry Pi LCD test program

