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


## Download
Use git to download the software from github.com:

    $ cd projects   { or wherever you put downloads }
    $ git clone https://github.com/wryan67/lcd101rpi_lib.git


## Install

To compile this library, navigate into the src folder and use the make utility to compile 
and install the library.  Don't forget the **sudo** on the last make step as the insall 
process will copy the library to the system folders.

    $ cd lcd101rpi_lib
    $ cd src
    $ sudo make install
    
    
## Compiling
Complie your applications using these command line arguments:
    -lwiringPi -lwiringPiDev -lwiringPiLCD101rpi


## Examples
In the example folder, there is a sample program that you can compile and run.  Use the "gpio i2cd" 
command to determine what address your LCD16xx device is using.

    $ cd [project folder]
    $ cd example
    $ make
    $ ./lcd1602 -a 0x23
    Raspberry Pi LCD test program

