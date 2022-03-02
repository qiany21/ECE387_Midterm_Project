20x04 I2C LCD Library
==================================================
:Author: Yicheng Qian
:Course: ECE387
:Project: Midterm Project

This library provides a set of functions for interfacing the I2C LCD with ATmega 328P and a sample program for guiding you to start using it. Note the original authors of this library is Davide Gironi(Enable I2C on LCD) and Peter Fleury(LCD Driver). The library has almost all the functions that we normally use except for clear a specific line and print integer on the LCD. I have added those two functions into the library so that we can use it like what we did in our LCD lab.


Installation
------------
You can install the I2C LCD library:

::

    git clone git@github.com:qiany21/ECE387_Midterm_Project.git

Note you also need a complete avr-gcc toolchain to make it work:

::

    sudo apt-get update
    sudo apt-get upgrade all
    sudo apt-get install gcc-avr binutils-avr avr-libc
    sudo apt-get install gdb-avr
    sudo apt-get install avrdude
    
Now you are all set! To compile the sample program(I borrowed the python script from Dr.Peter Jamieson):

::

    python ./compile_script.py 4 com3

where the number 4 indicates the level of compilation(there are a total of 4 levels) and com3 indicates the port used by Arduino(This can be different in your case, make sure you have the correct port number and change both the command line arguments and the setting in the script).
  
Hardware Overview
-----------------

What is an I2C LCD?
~~~~~~~~~~~~~~~~~~~

An I2C LCD is a LCD display screen with I2C interface. It can be used to display a range of sizes. There are usually two typical sizes: 16x02 and 20x04(16 characters on 2 lines or 20 characters on 4 lines). The reason we need such a LCD with I2C is a normal LCD would need over 10 wires to connect to an Arduino while an I2C LCD would only use 4 wires to connect to an Arduino. 2 data pins are used to control the LCD. Addding an I2C interface reduces complexity and difficulty. In addition, more port resources are saved. An I2C LCD is maade up with a PCF8574T port expander and a HD44780 LCD. We will have a brief review of these two components.

HD44780 LCD
~~~~~~~~~~~





