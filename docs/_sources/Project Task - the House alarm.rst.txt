===============================
Project Task - the House Alarm
===============================

Alarms are devices that communicate with the central control unit via an electronic network and send signals about possible movements and changes, which are detected by sensors.

A typical home alarm system contains the following components:

- The control panel, which is actually the central control unit of the alarm system

- Sensors on doors, windows or some pieces of furniture

- Motion sensors, internal and external

- A very loud siren or alarm.

The principle of operation is very simple: alarm systems secure entry points, i.e. places that allow access to a home, apartment or workspace, by using sensors, which communicate with the main control unit. Sensors are usually located on doors or windows, but also on other openings that allow access inside.

The House Alarm device should detect motion, as well as temperature and light level changes in the given room. If the door opens and the room temperature or the light intensity rises, the device will make a sound.

To make the House Alarm, we will need:

- 3 Micro:bits

- adhesive tape

- speaker or headphones

- Crocodile clips

To create the House Alarm device, first, we will have to make the actual (physical) device composed of the Micro:bit, which will serve as a motion sensor, the Micro:bit which will detect the change in room temperature and light level, and the Micro:bit which will make a sound when changes are detected (the Micro:bit connected to speakers or headphones must be placed about 10 meters from the sensor). 

Now that we have made the House Alarm device, we need to create programs for each Micro:bit.

We need to program each Micro:bit separately:

­1. The first has to detect movement.
2. The second detects changes in temperature and light level.
3. The third produces a sound when movement, changes in temperature or light level are detected in the room.

**Step 1**

Go to https://makecode.microbit.org/.

First, we will program the Micro:bit that serves as the motion detector.

**Step 2**

Create a new project.

Now, we want to program motion detection; more specifically, we want to register motion using the Micro:bit.

When we want to establish communication (to use radio communication) between Micro:bits, all included Micro:bits must belong to the same group, i.e. the must use the same group ID.

**Step 3**

By creating the group ID, we actually create a space where the devices will communicate.

To create an ID group, we need to drag the block |radioset| from the category |Radio| into the block |onstart| from the category |Basic|. Into the space |ID| we type the desired number for the group ID. This can be any number. We will leave the number 1. This way, we have created the group with the ID 1 in which all Micro:bits will communicate.

.. |Radio| image:: ../_images/_imageMicroBit/s21.png
.. |radioset| image:: ../_images/_imageMicroBit/s22.png
.. |Basic| image:: ../_images/_imageMicroBit/s2.png
.. |ID| image:: ../_images/_imageMicroBit/s23.png
.. |onstart| image:: ../_images/_imageMicroBit/onstart.png

The part of the code, which creates the group for communication:

.. image:: ../_images/_imageMicroBit/s24.png
      :align: center

**Step 4**

Drag the block |if..then| from the category |Logic| into the block |forever|, located in the category |Basic|.

.. |forever| image:: ../_images/_imageMicroBit/s1.png
.. |if..then| image:: ../_images/_imageMicroBit/s3.png
.. |Logic| image:: ../_images/_imageMicroBit/s4.png

Into the condition input field |uslov| drag the block |uslov1| (located in the category |Input|).

.. |uslov| image:: ../_images/_imageMicroBit/s5.png
.. |Input| image:: ../_images/_imageMicroBit/s6.png
.. |uslov1| image:: ../_images/_imageMicroBit/s7.png

From the drop-down list of the block |uslov1|:

.. image:: ../_images/_imageMicroBit/s8.png
      :align: center

choose the option |shake|. This option detects movements.

.. |shake| image:: ../_images/_imageMicroBit/s9.png

.. image:: ../_images/_imageMicroBit/s10.png
      :align: center

Based on the setup of the task, when a movement is registered (or in our case when the conditions are fulfilled), the Micro:bit will send a certain value by using the block |radiosend|.

We will put the number 5 into the input field |broj| (any value can be entered). For the sensor to react, i.e. detect movement, we need to set it so it takes a certain amount of time, let's put 3 seconds (or 3000 milliseconds). For this, we will use the block |time| from the category |Basic|. Into the input field |vreme| we will put 3000ms, which will be the sensor response time, with regard to the change that has occurred.

.. |broj| image:: ../_images/_imageMicroBit/s32.png
.. |vreme| image:: ../_images/_imageMicroBit/s40.png
.. |time| image:: ../_images/_imageMicroBit/s39.png
.. |radiosend| image:: ../_images/_imageMicroBit/s30.png

.. image:: ../_images/_imageMicroBit/s48.png
      :align: center

**Step 5**

Download the .hex file to your computer by clicking on the button |dugme1| or button |dugme2|. The Micro:bit will be ready to start working once you have dragged the file onto it.

.. |dugme1| image:: ../_images/_imageMicroBit/s49.png
.. |dugme2| image:: ../_images/_imageMicroBit/29.png
      :width: 199px

**Step 6**

Now, we have to program the second Micro:bit to detect the changes in temperature and light level, and to send that information to the Micro:bit, which will react to this by making a sound. 
In order for the Micro:bits to communicate, they have to belong to the same ID group.

We have already created the group with the ID 1 where all of our Micro:bits will communicate:

.. image:: ../_images/_imageMicroBit/s24.png
      :align: center

Drag the block |if..then| form the category |Logic| into the block |forever|. We also need to drag the blocks that define the conditions into the condition input field |uslov|. One condition will be that the temperature is higher than 30 degrees, and the other condition will be that the light level is higher than 150.

Conditions can be complex (created by connecting simple conditions).

In our case, the simple conditions are that the temperature is higher than 30, or that the light level is higher than 150.

.. |poredjenje| image:: ../_images/_imageMicroBit/s53.png

We define our simple conditions with the block |poredjenje|.

In our case, we define the conditions as follows:

- temperature |temperatura| higher than 30: |vece30|.

- light level |intenzitet| higher than 150: |vece150|.

.. |temperatura| image:: ../_images/_imageMicroBit/s55.png
.. |intenzitet| image:: ../_images/_imageMicroBit/s54.png
.. |vece30| image:: ../_images/_imageMicroBit/s56.png
.. |vece150| image:: ../_images/_imageMicroBit/s57.png

You use logical (boolean) operators to connect simple conditions (AND, OR, NOT).

In MakeCode, logical (boolean) operators are represented as follows:

|and| - Connects two conditions, and it returns True as the result only if both conditions are True.

|or| - Connects two conditions, and it returns True as the result if at least one condition is True.

|not| - It is placed in front of one condition, and it returns True as the result in case the condition is not fulfilled.

.. |and| image:: ../_images/_imageMicroBit/s50.png
.. |or| image:: ../_images/_imageMicroBit/s51.png
.. |not| image:: ../_images/_imageMicroBit/s52.png

The condition, which checks whether there has been a change in temperature or light level, is defined by the following block:

.. image:: ../_images/_imageMicroBit/s58.png
      :align: center

The look of the conditional block:

.. image:: ../_images/_imageMicroBit/s60.png
      :align: center

Based on the setup of the task, when the change in temperature or light level has been registered, the Micro:bit will send a certain value by using the block |radiosend|. We will put number 10 into the input field |broj| (any value can be entered). For the sensor to react, i.e. detect changes, we need to set it so it takes a certain amount of time, let's put 3 seconds (or 3000 milliseconds). For this, we will use the block |time| from the category |Basic|. Into the input field |vreme| we will put 3000ms, which will be the sensor response time, with regard to the change which has occurred.

The look of the program when a change in temperature or light level is detected:

.. image:: ../_images/_imageMicroBit/s59.png
      :align: center

**Step 7**

Download the .hex file to your computer by clicking on the button |dugme1| or button |dugme2|. The Micro:bit will be ready to start working once you have dragged the file onto it.

.. |dugme11| image:: ../_images/_imageMicroBit/s61.png
.. |dugme21| image:: ../_images/_imageMicroBit/29.png
      :width: 199px

**Step 8**

Finally, we need to program the third Micro:bit. This Micro:bit will make a loud sound when it receives certain information from the other two Micro:bits.

We will create a group with ID 1:

.. image:: ../_images/_imageMicroBit/s24.png
      :align: center

The next step is for this Micro:bit to receive information (in our case a number) on the basis of which it will "respond" by making a sound. To achieve this, we will drag the following block from the category |Radio|:

.. image:: ../_images/_imageMicroBit/s30.png
      :align: center

Into it, we will drag the block |if..then|. Into the condition input field |uslov| we need to drag the condition, which will check the numbers (5, 10) received from the other two Micro:bits.

Using the |plus| sign, we will introduce one more condition. Into the branch with the condition |uslov5| and into the branch with the condition |uslov10|, we will drag the block |melodija| (from the drop-down list of this block we will choose the melody ``ringtone``) from the category |Music|, which is used for producing sound.
In addition to this block, we will also add a time interval of one second.

.. |plus| image:: ../_images/_imageMicroBit/s15.png
.. |uslov5| image:: ../_images/_imageMicroBit/s63.png
.. |uslov10| image:: ../_images/_imageMicroBit/s64.png
.. |melodija| image:: ../_images/_imageMicroBit/s65.png
.. |Music| image:: ../_images/_imageMicroBit/s66.png

The final look of the code:

.. image:: ../_images/_imageMicroBit/s67.png
      :align: center

**Note**: The Micro:bit has to be connected to speakers or headphones, as shown in the figure below, for the sound to be reproduced:

.. image:: ../_images/_imageMicroBit/34.png
      :align: center

**Step 9**

Download the .hex file to your computer by clicking on the button |dugme1| or button |dugme2|. The Micro:bit will be ready to start working once you have dragged the file onto it.

.. |dugme01| image:: ../_images/_imageMicroBit/s62.png
.. |dugme02| image:: ../_images/_imageMicroBit/29.png
      :width: 199px
