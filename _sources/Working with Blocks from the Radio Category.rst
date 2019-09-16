Working with Blocks from the Radio Category
=============================================

In this lesson, we will get to know the blocks from the category |Radio|, i.e. the blocks which are used for establishing a connection and communication between two or more Micro:bit devices. As in this case we will not use Micro:bits, in the simulator screen there will be two Micro:bits displayed.
In the simulator, all created codes will work on both virtual Micro:bits.

.. |Radio| image:: ../_images/_imageMicroBit/s21.png

Create a program which, when button A is pressed, sends a random number from the interval 0 to 100. When this information is received, a light appears in the middle of the screen, forming a 3x3 square if the received number is even; otherwise, the value of that number is displayed.

By creating an ID group, we actually create a space where the devices will communicate.

To create an ID group, we need to drag the block |radioset| from the category |Radio| into the block |onstart|. Into the input field for numbers and text, we can enter the desired number for the ID group, which can be any number. We will leave it to be 1. This way we created the ID 1 group, where both Micro:bits can communicate.

.. |onstart| image:: ../_images/_imageMicroBit/s20.png

.. |radioset| image:: ../_images/_imageMicroBit/s22.png

.. image:: ../_images/_imageMicroBit/s24.png
      :align: center

NOTE: When we use the blocks from the category ``Radio`` there will be two Micro:bits displayed in the simulator.

The variable ``Counter`` stores the value obtained from using the block |pickrandom|, or more precisely, the variable ``Counter`` receives one of the random values from the interval 0 to 100.
When button A is pressed, the Micro:bit sends the value of the variable ``Counter`` by using the block |send| from the category |Radio|.

The look of the code:

.. |pickrandom| image:: ../_images/_imageMicroBit/p49.png
.. |send| image:: ../_images/_imageMicroBit/s30.png

.. image:: ../_images/_imageMicroBit/p73.png
      :align: center

When the information is sent (in our case Counter), this information has to be received. Based on this information, the execution of the program is determined (the square will be displayed if the received number is even; otherwise, the value of the received number will be displayed). For this, we will drag a block from the |Radio| category:

.. image:: ../_images/_imageMicroBit/p73.png
      :align: center

Into this block, we will drag the block which defines the variable ``Remainder``, which stores the value for integer division of the ``Counter`` by 2:

.. image:: ../_images/_imageMicroBit/p64.png
      :align: center

This is followed by the block |ifthen|. In the part |uslov| we will check if there is a remainder after the integer division of the Counter by 2. If this is true, a 3x3 square will be displayed. Otherwise, if the condition has not been fulfilled, which means that the remainder is not 0, the value of the variable ``Counter`` will be displayed:

.. image:: ../_images/_imageMicroBit/p75.png
      :align: center

.. |ifthen| image:: ../_images/_imageMicroBit/s3.png
.. |uslov| image:: ../_images/_imageMicroBit/s5.png

The final look of the code:

.. image:: ../_images/_imageMicroBit/p76.png
      :align: center

Link for the code: https://makecode.microbit.org/_f31EfHcv6Kpy

To test the program, we will run it in the simulator by clicking the |play| button.

.. |play| image:: ../_images/_imageMicroBit/p3.png

.. mchoice:: L8Z1
    :answer_a: When the data is received, nothing will be displayed.
    :answer_b: When the data is received, the LED with coordinates (2,2) will be turned on.
    :answer_c: When the data is received, the message "Hello" will be displayed.
    :feedback_a: The answer is correct!
    :feedback_b: The answer is not correct!
    :feedback_c: The answer is not correct!
    :correct: a

    Study the blocks carefully.

    .. image:: ../_images/_imageMicroBit/p77.png
          :align: center

    What will be displayed after the execution of the blocks above?

**Task.** Arrange the blocks so that they simulate the operation of a Telegraph, more precisely when the signal (number) is sent, LEDs are turned on in randomly chosen locations. 

**Little help:** The values of the coordinates x and y are from the interval 0 to 4.

Compare your solution with one of our solutions: https://makecode.microbit.org/_JgFC5vRpudkq
