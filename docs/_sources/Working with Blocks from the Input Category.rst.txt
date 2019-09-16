Working with Blocks from the Input Category
============================================

The computer processes the data it receives from the input (from the user (pressing a button,...) or the environment (values obtained by sensor readings)). In MakeCode, there is a category of blocks which enables working with input data, more specifically a block category that allows a program to "perform certain actions" based on the information it receives from the user or the environment.

The |input| category contains blocks (commands), which process data obtained from users (by clicking buttons) or the environment (by reading sensory data).

.. image:: ../_images/_imageMicroBit/p8.png
      :align: center

The input data can be obtained from pressing the button ``A``, ``B`` or ``A+B``, as well as from reading the values ​​of the sensors for light, temperature, and the accelerometer.

.. |input| image:: ../_images/_imageMicroBit/s26.png

We want to create a program which displays the temperature (in degrees Celsius) when button ``A`` is pressed.

.. |onstart| image:: ../_images/_imageMicroBit/s20.png

.. |forever| image:: ../_images/_imageMicroBit/s1.png

.. mchoice:: L2Z1
    :answer_a: once.
    :answer_b: an infinite number of times.
    :feedback_a: Bravo! The onstart block is one of the blocks from the Basic category, and blocks within it are executed only once during the running of the program.
    :feedback_b: The forever block is the block within which commands will be executed an infinite number of times. The running of this block will never stop on its own. To stop the running of this block, you need to press the stop button (|stop|).
    :correct: a

    How many times will the blocks inside of the |onstart| block be executed?


As we have already seen in the examples from the previous lesson, how the program starts and runs depends on which block was applied, |onstart| or |forever|.

In order to enable data entry, that is, to use button ``A`` to start or run the program, we need to select the |onbutton| from the |input| category, and from its drop-down list we need to choose the button A.

.. |onbutton| image:: ../_images/_imageMicroBit/p9.png

The block |onbutton| starts the program and all blocks included in it are executed.

We drag the ``on button ... pressed`` block onto the work surface, and then we insert in it the block which will allow us to display the value of the temperature.

For displaying the temperature, we will use the block |shownumber| from the category |Basic|.

.. |shownumber| image:: ../_images/_imageMicroBit/15.png

.. |Basic| image:: ../_images/_imageMicroBit/s2.png

After connecting these two blocks, we will select the block |temperatura| from the Input category, which we will drag into the input field of the show number command. The block |temperatura| stores the value received from reading the temperature sensor, which is displayed in degrees Celsius.

.. |temperatura| image:: ../_images/_imageMicroBit/s55.png

The final look of the program:

.. image:: ../_images/_imageMicroBit/p10.png
      :align: center

We will use the simulator to test the program. The program will run after the |play| button is clicked.

.. |play| image:: ../_images/_imageMicroBit/p3.png


.. mchoice:: L2Z2
    :answer_a: When button A is pressed, the value of the light level will be displayed.
    :answer_b: When button B is pressed, the value of the light level will be displayed.
    :answer_c: When A and B are pressed at the same time, the value of the light level will be displayed.
    :feedback_a: Bravo! Pressing button A will display the value of the light level.
    :feedback_b: The answer is not correct! Pressing button A will display the value of the light level.
    :feedback_c: The answer is not correct! Pressing button A will display the value of the light level.
    :correct: a

    What will be the trigger for displaying the light level:

    .. image:: ../_images/_imageMicroBit/p11.png
          :align: center

    Little help: The block |level| stores the value received from the light sensor located on the display (LEDs play the role of the light sensor).

.. |level| image:: ../_images/_imageMicroBit/s54.png

.. mchoice:: L2Z3
    :answer_a: Block A.
    :answer_b: Block B.
    :answer_c: Block C.
    :answer_d: Block D.
    :feedback_a: The answer is not correct!
    :feedback_b: The answer is not correct!
    :feedback_c: The answer is correct.
    :feedback_d: The answer is not correct!
    :correct: c

    Look carefully at the blocks. Which of the blocks represents a program that will draw a flower when a movement is made (shake)?

    .. image:: ../_images/_imageMicroBit/p16.png
          :align: center

.. mchoice:: L2Z4
    :answer_a: When button A is pressed, the direction will be displayed.
    :answer_b: When button B is pressed, the direction will be displayed.
    :answer_c: When A and B are pressed at the same time, the direction will be displayed.
    :feedback_a: The answer is not correct!
    :feedback_b: The answer is not correct!
    :feedback_c: The answer is correct.
    :correct: c

    Look carefully at the block. What will be the trigger (input) for displaying the direction of the placement of the device:

    .. image:: ../_images/_imageMicroBit/p17.png
          :align: center

**Task.** Create a program, which should display a Smiley face (by using |showleds|) when button A is pressed, when button B is pressed it should show your names, and when A and B are pressed together, it should display how old you are.

You can compare your solution with ours: https://makecode.microbit.org/_86uV0j7mt0hU

.. |showleds| image:: ../_images/_imageMicroBit/s12.png
    :width: 100px
