Working with Blocks from the Loops Category
================================================

There are processes in nature that are repeated constantly or from time to time. As in nature, in programming, sometimes it is necessary to repeat certain parts of the program several times. We have already mentioned that repeating one or more commands (blocks) is a powerful concept in programming. When some of the program commands are repeated several times, we say that the program contains loops. We have used this concept several times before.  

Repeating commands is a very common occurrence in programming.

.. |stop| image:: ../_images/_imageMicroBit/p2.png


MakeCode has three types of blocks into which other blocks, whose execution needs to be repeated, can be inserted. Blocks can be repeated:

  - a certain number of times:

  .. image:: ../_images/_imageMicroBit/p68.png
        :align: center

  We should use this block when we know the exact number of repetitions in advance (they are also called iterations).

  - an infinite number of times (continuously, until the user stops the program):

  .. image:: ../_images/_imageMicroBit/s1.png
        :align: center

  This is one of the most frequently used blocks. The running of this block is stopped when the user clicks the stop button (|stop|).

  - until a certain condition is fulfilled:

  .. image:: ../_images/_imageMicroBit/p68.png
          :align: center

  We should use this block when we do not know how many times blocks inserted into the repetition block should be executed, and therefore, we want them to run until a certain condition is fulfilled.
  Blocks, which need to be repeated, are dragged and inserted into repetition blocks.

The block, which will repeat other blocks an exact number of times, can be used to reproduce the tone C three times.

The look of the code:

.. image:: ../_images/_imageMicroBit/p70.png
      :align: center

The block for repeating commands will be executed an infinite number of times. The running will never stop on its own. We can stop the running by clicking on the stop button (|stop|).

We used the blocks for repeating in our previous lessons when we displayed the animation of a square.

.. mchoice:: L7Z1
    :answer_a: New blocks can be inserted into the block itself, so there is no need to continue the script.
    :answer_b: It is a bug in MakeCode. The block that repeats commands an infinite number of times must have the option to continue stacking the script.
    :answer_c: Adding further blocks would be pointless since they would never be executed.    :feedback_a: The answer is correct!
    :correct: a
    :feedback_b: The answer is not correct!
    :feedback_c: The answer is not correct!
    
    Analyze the look of the blocks. You can see that the forever block used for repeating commands indefinitely does not have the option for connecting to other blocks, other blocks cannot be added onto it. Why?

The block which repeats other blocks (commands) runs until a specific condition is fulfilled. The blocks within this block are executed based on checking whether the condition is fulfilled or not. We use this block when we do not know how many times we need to repeat the commands inside it, and we want them to run until a specific condition is fulfilled. 

.. mchoice:: L7Z2
    :answer_a: The block that repeats commands a certain number of times.
    :answer_b: The block that repeats commands an infinite number of times.
    :answer_c: The block that repeats commands until a certain condition is fulfilled.
    :correct: c
    :feedback_a: The answer is not correct!
    :feedback_b: The answer is not correct!
    :feedback_c: The answer is correct!
    

    You want to create a program, which continuously turns on the LED on the screen with coordinates (2,2) until the light level drops below a certain value. Which blocks will you use for repeating commands?

We will demonstrate the use of this block by creating a program that plays a tune as long as the light level is lower than 120.

.. |svetlost| image:: ../_images/_imageMicroBit/p71.png

For the purposes of this program, we will define the variable |svetlost|, which will store the value of the light level reading. As long as the light level value is less than 120, a sound signal will be emitted.
In the figure below you can find our suggestion for the code, along with comments which explain it. Programmers consider commenting on scripts and explaining what each block does to be useful. Commenting makes it easier for other programmers to understand and upgrade programs we created. 
You can add a comment by right-clicking on the script and selecting the option **Add comment**. 
 

.. image:: ../_images/_imageMicroBit/p72.png
      :align: center

To test the program, we will run it in the simulator by clicking the |play| button.

.. |play| image:: ../_images/_imageMicroBit/p3.png
