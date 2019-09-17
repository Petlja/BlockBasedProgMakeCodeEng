Project Task - Planting Trees
===================================

Events are occurrences, which are usually results of something the user did (clicking the mouse, pressing keys on the keyboard, drag and drop, etc.). An event causes a reaction. An event in computer science is an action detected (performed) by a computer. For example, by clicking the mouse, we open an application, when it starts raining people open umbrellas. 
In programming, an event handler is the part of the program (function) which is activated as a result of some event. In MakeCode event handlers are blocks which usually start with the word **on**:

.. image:: ../_images/_imageMinecraft/31.png
      :align: center

We will use an event to simulate planting trees and displaying the current position of the character in the Minecraft world, by adding the command **position**.

**Stage 1.**

**Thinking about the task:** The character interacts with the world by moving around, i.e. trees are planted. The character plants trees by moving around the Minecraft world. Sending a message (through chat) displays the current position of the character.

**Stage 2**

Open ``Code Builder`` (by pressing the key ``C``); an editor window will appear where you can stack blocks.

To start the chat, or more specifically, to trigger an event which will display character's current position, we need to drag the block |onchat| from the category |Basic| to the work surface, and then type the word **position** into the input field of this block.

.. |onchat| image:: ../_images/_imageMinecraft/40.png
              :width: 250px

.. |Basic| image:: ../_images/_imageMinecraft/40_.png

Within this block, we need to add blocks that will say the current position. To say any message (e.g. My current position is:) we need to use the block |say| from the category |Player|.

The character's (player's) position is stored in the block |position| from the category |Player|. Since we want to display the position of the player in chat, we need to use the block |string| form the category |Pozicija|. Instead of the option ``position``, we will insert the block |position| into the field:

.. |say| image:: ../_images/_imageMinecraft/27.png
.. |Player| image:: ../_images/_imageMinecraft/27_.png
.. |position| image:: ../_images/_imageMinecraft/42_.png
.. |string| image:: ../_images/_imageMinecraft/41_.png
.. |Pozicija| image:: ../_images/_imageMinecraft/0.png

.. image:: ../_images/_imageMinecraft/41.png
      :align: center
      :width: 350px

Let's test this part of the code by clicking the button |Play|.

After testing the program, we can see that we got what we wanted. When the user presses the key ``T``, opens the chat and types in the message **position**, player's current position in the world will be displayed.

.. |Play| image:: ../_images/_imageMinecraft/15.png
          :width: 40px

.. image:: ../_images/_imageMinecraft/43.png
          :align: center

.. image:: ../_images/_imageMinecraft/42.png
          :align: center

Now we need to create an event for the character, which will enable it to plant trees in the Minecraft world with its movement. This will be achieved with the block |walk|. From the drop-down list of this block we will choose the option ``walk``:

.. |walk| image:: ../_images/_imageMinecraft/1_.png

.. image:: ../_images/_imageMinecraft/44.png
          :align: center


And finally, we need to place the block |place| from the category |Blocks| within this block. We use this block to place (or in our case plant) a tree. From the drop-down list of this block we will choose the block which represents a tree:

.. |place| image:: ../_images/_imageMinecraft/45.png
              :width: 350px

.. |Blocks| image:: ../_images/_imageMinecraft/33_.png

.. image:: ../_images/_imageMinecraft/46.png
          :align: center
          :width: 450px

In the ``at`` part of the block, where we need to define the position of the block we want to place in the world, we will leave all three values to be 0 |nula|. This will allow the trees to be planted in the same plane the character is located.

After all the changes, the part of the code for planting trees is presented in the figure below:

.. |nula| image:: ../_images/_imageMinecraft/47.png

.. image:: ../_images/_imageMinecraft/49.png
          :align: center

**Stage 3**

Testing the program.
Click on the button |Play|.

.. image:: ../_images/_imageMinecraft/48.png
          :align: center

Once we have tested the program, we can conclude that it did what we wanted. The character is planting trees by moving around.
