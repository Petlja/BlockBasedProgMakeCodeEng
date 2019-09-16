Project Task - Happy or Sad
=============================

Until now, all the programs we have created were linear programs, more specifically, these were programs where commands are executed consecutively, one after the other until the end of the program.

Unlike these programs, where every step, i.e. every command, is executed once, in decision-making algorithms, or more precisely, conditional (branch) algorithms some of the commands will be executed, and some won't, which will depend on whether the condition has been fulfilled or not.

We will demonstrate the use of decision-making blocks by creating a program, which will display different images on the EV3 screen, depending on whether the touch sensor is pressed or not. If the sensor is pressed, the EV3 is happy - a smiley face will be displayed on the screen, and if not, a sad face will be displayed on the screen.

In some programs, the execution of the blocks doesn't have to be done in the same order they were placed in the program. The decision-making blocks are used when we need to choose which stack of blocks will run. Which line (branch) will be chosen depends on whether the condition has been fulfilled or not. For the robot, whether or not the condition was fulfilled, depends on the information it receives from the sensor.

To create a program which will display a smiley or a sad face, depending on whether the touch sensor is pressed or not, we need to start a new project.

Into the block |Forever| (located in the category |Loops|) we will drag the block |if..then| from the category |Logic|. Into the condition input field |uslov| we will drag the block |touch|.
Based on the setup of the task, when the sensor is pressed, the program should display the happy (smiley) face. We need to drag the block |show| from the category |Basic| into the branch YES.

.. |forever| image:: ../_images/_imageEV3/46.png
.. |Loops| image:: ../_images/_imageEV3/43.png
.. |if..then| image:: ../_images/_imageEV3/45.png
.. |Logic| image:: ../_images/_imageEV3/44.png
.. |uslov| image:: ../_images/_imageEV3/47.png
.. |touch| image:: ../_images/_imageEV3/48.png
.. |show| image:: ../_images/_imageEV3/50.png
.. |Basic| image:: ../_images/_imageEV3/49.png

The look of the program when the sensor is pressed and the simulation.

.. image:: ../_images/_imageEV3/50_.png
      :align: center

We can see that, even when we release the sensor button, the image of the happy face remains on the EV3 Brick screen. To correct this mistake, we will have to use the block |Clear|.

.. |Clear| image:: ../_images/_imageEV3/54.png

The look of the program when the sensor is pressed.

.. image:: ../_images/_imageEV3/55.png
      :align: center

Based on the setup of the task, there is also the condition which allows a sad face to be displayed on the EV3 Brick screen when the touch sensor is not pressed. To achieve this, we need to add another branch "else" by clicking the sign |Plus|. Within this branch, we will add the block that will display the sad face on the screen.

.. |Plus| image:: ../_images/_imageEV3/56.png

The final look of the code when the touch sensor is pressed or not pressed, and the simulation:

.. image:: ../_images/_imageEV3/57_.png
      :align: center

In this example, the upper line of the code will run if the button is pressed, and the lower line will run if the button is not pressed. 

To illustrate this, we will give one more example: We need to create an application with which the robot is moving forward until it sees an obstacle (the distance should be less than 30cm). When the robot sees the obstacle, it should turn to the right, thus trying to go around it.

Into the block |Forever| (located in the category |Loops|) we will drag the block |if..then| from the category |Logic|. Into the condition input field |uslov| we will drag the block |operacija|, which is a comparison operator. To create the condition where the distance between the robot and the obstacle is less than 30cm, we will assemble the block |manje30|. Based on the setup of the task, when the obstacle is less than 30cm away, the robot will turn right; otherwise, it will move forward (if the condition is not fulfilled, that is, the robot doesn't see the obstacle).

.. |operacija| image:: ../_images/_imageEV3/59.png
.. |manje30| image:: ../_images/_imageEV3/61.png

We will add the block for turning |skreni| and for moving forward |pravo|.

.. |skreni| image:: ../_images/_imageEV3/62.png
.. |pravo| image:: ../_images/_imageEV3/63.png

The look of the final code:

.. image:: ../_images/_imageEV3/60.png
      :align: center

Connect the EV3 Brick to the computer via USB cable and download the .uf2 file to your computer by clicking the button |dugme1|. By dragging the file onto the EV3, it is ready to start working.

.. |dugme1| image:: ../_images/_imageEV3/download.png
        :width: 199px
