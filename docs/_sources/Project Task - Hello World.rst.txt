Project Task - Hello World
===============================================

Let this be a simple example, where the message "Hello, World!" will appear in Minecraft.

The procedure for solving any task (problem) involves going through each of the following stages:

  Stage 1: Think about the task and write or draw an algorithm (steps) to solve it.

  Stage 2: Enter commands so that the program runs according to the algorithm.

  Stage 3: Test the program and correct mistakes (if there are any).

We will go through all of the stages together, and we will create a program in which the Minecraft environment (created world) says hello.

**Stage 1**

**Thinking about the task:** We need to display the greeting "Hello, World!" in the created world.

**Stage 2**

Open ``Code Builder`` (by pressing the key ``C``); an editor window will appear where you can stack blocks.

Based on the algorithm, we need to display the desired message (text: "Hello, World!").

To display the message we have to use the block |print| from the category |Blocks|.

.. |print| image:: ../_images/_imageMinecraft/33.png

.. |Blocks| image:: ../_images/_imageMinecraft/33_.png

This block has four parameters, which define how and where the message will be displayed (written) in the Minecraft world:

- In the text input field of the block ``print``, we will type the desired text. In our case, this will be the message ``Hello, World!``.

- In the field ``of``, we can choose the type of block that will be used to create the text.

- In the field ``at``, we will define the position, or more precisely the coordinates where we want the text to be displayed in our world.  Minecraft is a three-dimensional world defined by three coordinates (X, Y, Z):

    •	X – coordinate east/west

    •	Y – coordinate up/down (how far up or down the block is positioned in relation to the base)

    •	Z – coordinate south/north

- In the field ``along``, we can define the orientation, or more specifically, the axis along which the text is displayed (printed).

Into the block ``on start`` we will drag the block ``print`` where will put the following:

	In the text input field ``Hello, World!``

	In the field ``of``, we will choose ``Block of Diamond`` from the list, this will be the "material" which we will use to write the message.

.. image:: ../_images/_imageMinecraft/35.png
      :align: center
      :width: 350px

	In the field ``at``, in the x coordinate input field, we will put the value 1.

	We will define the field ``along`` by choosing the option ``East (positive X)`` from the drop-down list.

.. image:: ../_images/_imageMinecraft/36.png
      :align: center

After all the changes, the program which will display the greeting will look like this:

.. image:: ../_images/_imageMinecraft/37.png
      :align: center

**Stage 3**

Testing the program.
Click on the button |Play|.

.. |Play| image:: ../_images/_imageMinecraft/15.png
          :width: 40px

"Hello, World!" is displayed in the Minecraft world:

.. image:: ../_images/_imageMinecraft/38.png
      :align: center

Once we have tested the program, we can conclude that it did what we wanted. Our greeting is displayed when we open our Minecraft world.
