Blocks from the Music Category
===============================

The category |Music| contains blocks which reproduce tones/melodies, the block that serves as a "trigger" for activating the program when a melody is played, as well as the block for storing the values of basic tones and their duration in milliseconds.

.. |Music| image:: ../_images/_imageMicroBit/s66.png

Let's create a program which plays the tone D for 1/4 beat when button A is pressed.

We will have to drag the block |onpress| from the category |Input| onto the work surface, and then we insert the block |playtone| into it.

.. |onpress| image:: ../_images/_imageMicroBit/p18.png
.. |Input| image:: ../_images/_imageMicroBit/s6.png
.. |playtone| image:: ../_images/_imageMicroBit/p19.png

From the drop-down lists of the given block, we will choose the tone and its duration in milliseconds.

.. image:: ../_images/_imageMicroBit/p20.png
      :align: center

**Note:** Sound is heard through speakers or headphones connected to the computer.

The final look of the code:

.. image:: ../_images/_imageMicroBit/p21.png
      :align: center

.. |play| image:: ../_images/_imageMicroBit/p3.png

To test the program, we can run it in the simulator by clicking on the |play| button.

**Task.** Create a program, which will play the melody of the song "London Bridge".

You should use these notes:

•	g, a, g, f, e, f, g

•	d, e, f, e, f, g

•	g, a, g, f, e, f, g

•	d, g, e, c.

You can compare your solution with ours: https://makecode.microbit.org/_LW3UUKAzocbo

If we want to play a melody (a series of notes lasting a certain amount of time, and played one after the other) we use the block |playmelody|, from the drop-down list of this block we will choose the melody and how long it will last (whether it will be played once, forever, ...)

The final look of the code:

.. image:: ../_images/_imageMicroBit/p23.png
      :align: center

.. |playmelody| image:: ../_images/_imageMicroBit/p22.png

To test the program, we can run it in the simulator by clicking on the |play| button.
