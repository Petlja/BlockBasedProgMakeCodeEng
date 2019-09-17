Project Task - Pillar
========================

Similar to how it is in nature (change of seasons, water circulation, day and night, the rise and fall of sea level, etc.), in programming we can repeat certain steps multiple times. As in nature, in programming, it is necessary to run parts of a program several times to complete certain tasks. For these types of programs, we say that they contain repetitions, and these repetitions are called **loops**.

We will demonstrate repetition by creating a square-shaped pillar, the base of which is a square with sides of 5 blocks in length and 10 in height.
In Minecraft, we can also use an **agent** for performing certain actions, such as planting and harvesting, mining, cutting down trees and building objects. The blocks which relate to the agent are located in the category |Agent|:

.. |Agent| image:: ../_images/_imageMinecraft/s2.png
              :width: 100px

.. image:: ../_images/_imageMinecraft/s5.png
      :align: center

**Stage 1.**

Thinking about the task: Moving forward 5 blocks and turning left and right (at a 90-degree angle) creates a square-shaped base. Moving on the z-axis allows the construction of the 10 blocks high tower. 

**Stage 2**

Open ``Code Builder`` (by pressing the key ``C``); an editor window will appear where you can stack blocks.

We will divide this task into three parts:

- We place the agent in a specific position in the world and give it tools for building the desired object,

- creating the square base of the pillar,

- creating the vertical side of the pillar.

To place the agent where we want it, we will use the block |chat|. Entering the word **come** becomes the trigger for placing the agent in the desired spot. We use the block |teleport| form the category |Agent| to place the agent in the desired spot. We will place the agent in the position of our character (player) moved two blocks (steps) to the left. To achieve this, we will use the variable **position**, which stores the current value of the character's (player's) position. 

.. |chat| image:: ../_images/_imageMinecraft/s7.png
.. |teleport| image:: ../_images/_imageMinecraft/s6.png
              :width: 450px

We will create the variable **position** in the category ``Variables``:

.. image:: ../_images/_imageMinecraft/61.png
      :align: center

In the beginning, the value of the variable **position** is the current position of the character in the world moved two blocks to the left. 
We will define the initial value with the block |start|. This means that each time program starts, Minecraft sets the value of the position to the desired spot (the agent is moved two blocks to the left from the character (player)), and we can start building the square base of the pillar.

From the category ``Variables`` we drag the block |set|, into which we will insert the block that gives us the current position of the player moved two blocks to the left.

.. |set| image:: ../_images/_imageMinecraft/s8.png

.. |start| image:: ../_images/_imageMinecraft/28.png
          :width: 150px

.. |Position| image:: ../_images/_imageMinecraft/0.png
            :width: 100px

This can be achieved in the following manner, by using the block:

.. image:: ../_images/_imageMinecraft/62.png
      :align: center

from the category |Position|.

Into the upper part of the block, we will drag the block |world|, which gives the current position of the character (player) from the category |Player|. In the lower part of the block, in the x coordinate input field, we will put number 2.

.. |world| image:: ../_images/_imageMinecraft/28.png

.. |Player| image:: ../_images/_imageMinecraft/42_.png
            :width: 150px

The look of the ``on start`` block:

.. image:: ../_images/_imageMinecraft/63.png
      :align: center

To place the agent in the desired spot, we will use the block agent |teleport| from the category |Agent|. We will put the variable **position** into the first argument block, and in the second argument block, we will choose **East (positive X)** from the drop-down list.

The look of the code:

.. image:: ../_images/_imageMinecraft/65.png
      :align: center


**Stage 3.**

We test the program by clicking the button |Play|:

.. |Play| image:: ../_images/_imageMinecraft/15.png
          :width: 40px

.. image:: ../_images/_imageMinecraft/64.png
          :align: center

In order for the agent to be able to set up blocks, we need to ensure that it has everything it needs for building pillars in its inventory. For this, we will use the block |setagent| from the category |Agent|:

.. |setagent| image:: ../_images/_imageMinecraft/s14.png
          :width: 350px

.. image:: ../_images/_imageMinecraft/70.png
          :align: center

**Important:** The inventory, which is opened by pressing the key ``E``, is used by the player to manage the items it owns (carries). It consists of slots 1 to 9 in which it can "store" items it needs to create different objects.
Now we need to create the square-shaped base of the pillar. In order for the agent to be able to create the square base, we need some kind of a "trigger" for that event. For this, we will use the chat and the word square.

To place the block into a square shape, with the length of 5 blocks, we will use the block |repeat| from the category |Loops|.

.. |repeat| image:: ../_images/_imageMinecraft/s10.png
.. |Loops| image:: ../_images/_imageMinecraft/2_.png
          :width: 100px

A square is a geometric figure made up of four sides of equal length, with opposite sides parallel and angles between adjacent sides 90 degrees. The square has four sides, so we will enter the number ``4`` into the repetition block:

.. image:: ../_images/_imageMinecraft/66.png
          :align: center

To enable the agent to place blocks by moving around in the world, we need to use the block |placeagent| from the category |Agent|.

For it to be able to perform the action, we need to set the second argument block to ``true``:

.. |placeagent| image:: ../_images/_imageMinecraft/s11.png

.. image:: ../_images/_imageMinecraft/67.png
          :align: center

The length of the side, which is 5 blocks, will be defined with the block |move| from the category |Agent|:

.. |move| image:: ../_images/_imageMinecraft/s12.png

.. image:: ../_images/_imageMinecraft/68.png
          :align: center

The angles in a square are 90 degrees, we will achieve this by using the block |turn| from the category |Agent|:

.. |turn| image:: ../_images/_imageMinecraft/s13.png

.. image:: ../_images/_imageMinecraft/69.png
          :align: center

We can test the program by clicking the button |Play|.

.. image:: ../_images/_imageMinecraft/71.png
          :align: center

After the testing is complete, we can see that the agent did not construct the entire square.

To achieve this, we need to move the agent. We can do this by introducing the block |move| and choosing the option ``up`` from the drop-down list. We move the agent for one block, which is why we need to put ``1`` as the value of the third parameter:

.. image:: ../_images/_imageMinecraft/73.png
          :align: center

Now we will test the program again, and this time we will receive a square:

.. image:: ../_images/_imageMinecraft/72.png
          :align: center

Based on the code above, we can see that the agent is not in the position, which is one block above the initial position. To place the agent in the desired position we will introduce two blocks |turn| and |move|:

.. image:: ../_images/_imageMinecraft/74.png
          :align: center

During the testing of the program, we can see that the agent leaves the block after the movement is complete. We don't want this to happen. This is why we introduce two blocks, which will put the agent without the block into the position for building the wall:

.. image:: ../_images/_imageMinecraft/75.png
          :align: center

What remains for us to do is to create the program for building the pillar, which will be 10 blocks high.

We can do this by introducing a new loop where we will insert the already completed loop (which creates the square). We will introduce the block |repeat| and set the value of the counter to ``10``:

Placing one loop inside the body of another loop is called **nesting**.

.. image:: ../_images/_imageMinecraft/77.png
          :align: center

The final look of the code, which will enable the construction of a pillar which is 10 blocks high and has a 5x5 square base:

.. image:: ../_images/_imageMinecraft/78.png
          :align: center

**Stage 3**

Testing the program.
Click the button |Play|.

.. image:: ../_images/_imageMinecraft/76.png
          :align: center

This way, we have created a pillar which is 10 blocks high and has a 5x5 square base.
