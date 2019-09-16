Blocks from the Basic Category
===============================

The category |Basic| includes the blocks used for running (starting) programs, as well as blocks for displaying numbers, text or images.

It's time to create a program, which will display the message "Hello!". 

To display the greeting message (on the simulator or on the Micro:bit display), we have to drag the block |showstring| from the category |Basic| to the work surface and insert it into the block |onstart|. We can type in the desired message "Hello!" by clicking on the text input field. 

.. |Basic| image:: ../_images/_imageMicroBit/s2.png
.. |onstart| image:: ../_images/_imageMicroBit/s20.png
.. |showstring| image:: ../_images/_imageMicroBit/p6.png

The final look of the program, which displays the greeting message "Hello!":

.. image:: ../_images/_imageMicroBit/p5.png
      :align: center

We have two options to test the program:

- to run it in the simulator by clicking the |play| button.

- to download it to the Micro:bit device. In order to transfer the program to the Micro:bit device, we need to connect it to the computer by using the USB cable. You download the .hex file to your computer by clicking the |download| button.

.. |play| image:: ../_images/_imageMicroBit/p3.png
.. |download| image:: ../_images/_imageMicroBit/p4.png
      :width: 200px

We will use the simulator to test the program. The running of the program is triggered by clicking on the |play| button, i.e. the greeting message "Hello!" is displayed.

**Task.** Create a program which will display the message "Hello!" an infinite number of times. 
**Little help:** The block |forever| is the block which will repeat the commands inserted in it an infinite number of times. The running of this block will never stop on its own. To stop the running of this block, you need to press the stop button.

You can compare your solution with ours: https://makecode.microbit.org/_9Cw5d6Czda1d


.. |forever| image:: ../_images/_imageMicroBit/s1.png


In the category |Basic| you can also find blocks for displaying defined images |showicons| or for displaying images which the user can create by turning on diodes on the LED screen (|showleds|).


.. |showicons| image:: ../_images/_imageMicroBit/p7.png
.. |showleds| image:: ../_images/_imageMicroBit/s12.png


**Task.** You want to create a program that displays a smiley face on the screen.

You can compare your solution with ours: https://makecode.microbit.org/_CAdaFfKsY46a


.. mchoice:: L1Z1
    :answer_a: Block on start.
    :answer_b: Block forever.
    :feedback_a: The answer is not correct. The onstart block is one of the blocks from the category Basic, and blocks within it are executed only once during the running of the program.
    :feedback_b: Bravo! The forever block is the block within which commands will be executed an infinite number of times. The running of this block will never stop on its own. To stop the running of this block, you need to press the stop button (|stop|).
    :correct: b

    Which block, used for starting a program, will you have to use if you want the images of an empty square and a full square to alternate on the screen? 

Apart from the blocks mentioned above, in the category |Basic|, you can also find the blocks for displaying number values |shownumber|, blocks used to slow down the running of the program |pause|, the time interval code is presented in milliseconds 1000ms is 1 second, as well as the block for clearing the screen |clearall|.

.. |shownumber| image:: ../_images/_imageMicroBit/15.png
.. |pause| image:: ../_images/_imageMicroBit/s39.png
.. |clearall| image:: ../_images/_imageMicroBit/s14.png
.. |stop| image:: ../_images/_imageMicroBit/p2.png

**Task.** Using the example from the question above, about the alternating images of squares, try to slow down the time it takes for the image to change, by two seconds. 
**Little help:** Use the |pause| block.

Check our solution: https://makecode.microbit.org/_F5h5UKD2Vgau

**Additional task.** You need to turn on 3/5 LEDs on the Micro:bit. The display of illuminated LEDs has to be unique!

You can compare your solution with one of the possible solutions: https://makecode.microbit.org/_29YWXrLHg22U
