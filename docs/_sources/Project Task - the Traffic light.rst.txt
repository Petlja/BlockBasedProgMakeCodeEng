=================================
Project Task - the Traffic Light
=================================

A traffic light is a light signal device, and it has an important role in controlling traffic. Traffic lights are usually installed at intersections.

.. image:: ../_images/_imageMicroBit/semafor.jpg
      :align: center

The first traffic light was installed on 10 December 1868 in London; it was designed by John Peake Knight. This traffic light was operated manually by a police officer. The first interconnected traffic lights were installed in Salt Lake City. The first automatic control traffic light was introduced in the United States of America, in Huston, in 1922, and in 1927 in England. The first traffic light in Serbia was installed in Belgrade, at the intersection of King Alexander Street, King Ferdinand Street (currently Kneza Miloša Street), and Takovska street, on 4 December 1939.    

The color, shape and the size of light signals on a traffic light are determined by international standards:
­
- stop – red

- prepare to proceed – red and yellow at the same time

- proceed – green

- announces that the signal is about to change to red – yellow.


The colors turn on and off in a specific order, or more precisely, at certain time intervals.


Using a Micro:bit we will build a traffic light with red, yellow and green lights turning on and off at certain intervals, just like a real traffic light.

To make a traffic light, we will need:

-	1 Micro:bit

-	protoboard

-	styrodur

-	3 diodes (red, green and yellow)

-	3 resistors

-	4 crocodile clips

-	4 wires of different lengths.

Before we start connecting the Micro:bit to the diodes, we should remember that a Micro:bit has 25 pins, five big pins - 0, 1, 2, 3V and GND. The remaining 20 pins can be used for connecting the Micro:bit to other devices.

.. image:: ../_images/_imageMicroBit/67.png
      :align: center
 
By using wires/crocodile clips, we will connect the Micro:bit via GND to any of the pins on the protoboard, so we can connect it to the GND diode.

The operation of the diode requires power; we will limit the power supply by using resistors (they provide some resistance that limits the flow of current and controls the voltage in the circuit).

The figure below shows the connection of the Micro:bit to one of the LEDs:

.. image:: ../_images/_imageMicroBit/semafor1.png
      :align: center

We connect the Micro:bit via pin P0 and one of the pins on the protoboard on the left side of the resistors (figure below). We will connect the longer part (+) of the light diode to the P0 pin using crocodile clips, and the shorter one, also using crocodile clips, to the GND pin (look at the picture below). 

We will connect the other two LEDs the same way.

.. image:: ../_images/_imageMicroBit/semafor2.png
      :align: center

We will use this connection logic to physically make a traffic light out of styrodur.

**Programming**

We need to create a program, which allows the LEDs to turn on and off.

**Step 1**

Go to https://makecode.microbit.org/.

**Step 2**

Create a new project.

Now, we want to program the diodes to turn on and off.

**Step 3**

To create a code, which will allow the LEDs to turn on and off, we need to drag the block |digital| from the category ``Advanced - Pins`` into the block |forever| from the category |Basic|.

.. |forever| image:: ../_images/_imageMicroBit/s1.png
.. |Basic| image:: ../_images/_imageMicroBit/s2.png
.. |digital| image:: ../_images/_imageMicroBit/s37.png


In order for the light to turn on, we need to put the number 1 into the space |blokcic|. If the value has been set to 0, the light will turn off. 

.. |blokcic| image:: ../_images/_imageMicroBit/s38.png

.. image:: ../_images/_imageMicroBit/s41.png
      :align: center

With regard to the light turning on and off, we also need to set a time interval within which these changes will occur.
We will set that the light stays turned on for 4 seconds, an off for 2 seconds. To achieve this, we will use the block |b1| from the ``Basic`` category. Into the field |b2| we will put 4000ms (which is 4 seconds) for the light to stay on, and 2000 for the light to stay off.

.. |b1| image:: ../_images/_imageMicroBit/s39.png
.. |b2| image:: ../_images/_imageMicroBit/s40.png

The final look of the traffic light code:

.. image:: ../_images/_imageMicroBit/s42.png
      :align: center

Download the .hex file to your computer by clicking on the button |dugme1| or button |dugme2|. The Micro:bit will be ready to start working once you have dragged the file onto it.

.. |dugme1| image:: ../_images/_imageMicroBit/s43.png
.. |dugme2| image:: ../_images/_imageMicroBit/29.png
      :width: 199px
