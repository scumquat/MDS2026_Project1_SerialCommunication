# minimum_python_example
 
 This project demonstrates a minimal reproducible example for setting up a Python program with two classes. 

TODO
An intro
Short background with at least 2 references
Build of materials
Images for wiring and a table for connected pins (not ALL pins)
General steps for the experiment process, including where the code was run 
Results when you run the code
Short discussion of the experiment and what it did.
IEEE style references

 
## Table of Contents
* [Requirements](#requirements)
* [Implementation](#implementation)
* [Error Handling](#error-handling)
* [References](#references)

Hardware Serial is a mode of communication that uses hardware such as UART protocols to convey information between nodes.  Arduino boards typically have dedicated pins for software serial, and in the case of the Uno they are pins 0 and 1.  They are labeled Rx and Tx and are able to exchange information at a much faster rate than other means.  Alternatively, software serial is a method of serial communication that sends information across any digital output.  It is possible to communicate through more channels simultaneously but it is limited by a lower maximum baud rate. [1]

A TTL cable (Transistor-Transistor Logic) is a mode of communication that allows for simple serial interfacing with a wide variety of devices.  Some vary in output pins, but most if not all are comprised of a Tx, Rx, GND, and V+ connections.  In this case, we use a TTL-USB cable to interface with the computer and the Arduino board.  The cable used in these projects outputs 5V across the power cable, and produces 3.3V logic signals along the Tx/Rx lines. [2]


## Requirements

This project requires numpy. It was developed using Python 3.12

Use 'pip install -r requirements.txt' to install the following dependencies:

```python
numpy==2.2.2

```

## Implementation

This program can be run through main.py

There are two classes that main.py calls: ClassOne and ClassTwo.  Both classes allow outside function calls to add, clear, and get array values. ClassOne takes no input at initialization. ClassTwo takes an array at initialization.

## Part 1

Flash the Arduino with the serial testing script. This script outputs text over serial on a delay, and also outputs text over software serial with a longer delay.

In order to show data output through two serial ports on a laptop, the TTL-USB cable and a standard USB cable can be used to connect to the Arduino.

Connect the Green Tx line to the port specified in the script.  Connect the white Rx line to the Tx port specified in the script.  These are selected by the user and can be changed as needed, and in this application we will use 3 and 2, respectively.

With both connections made, the serial monitor in arduino can  be used to visualize one data stream while a second serial monitor can be used to visualize the other.

## Part 2

## Error Handling

This project does not have any error handling. 


## References

[1] https://exam.pscnotes.com/difference-between-hardware-serial-and-software-serial-in-arduino/

[2] https://www.adafruit.com/product/954

