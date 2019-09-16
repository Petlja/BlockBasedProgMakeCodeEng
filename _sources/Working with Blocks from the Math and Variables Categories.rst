Working with Blocks from the Math and Variables Categories
===========================================================

MakeCode supports four basic arithmetic operations:
- addition ( + ),
- subtraction ( - ),
- multiplication ( * ) and
- division ( / ).

The blocks that enable computation are called arithmetic operators. They are located in the category |Math|.

.. |Math| image:: ../_images/_imageMicroBit/p41.png

Arithmetic operators return a **NUMBER** (the result of an arithmetic operation).

.. image:: ../_images/_imageMicroBit/p40.png
      :align: center

You can use the result (number) returned by an arithmetic operator as an input value for blocks, which accept numbers. This can be clearly seen in the figure above. The show number ... block accepts a number as an input and displays it on the screen.

We put before you a more complex arithmetic expression: ( 2 + 1 ) * ( 12 - 10 ). In MakeCode, calculating the result might look like this:

.. image:: ../_images/_imageMicroBit/p42.png
      :align: center

By analyzing the complex expression, we can conclude that it consists of smaller units - interim results.

The sum of (2 + 1) is one interim result. The difference of (12-10) is the second interim result. We will get the result of the whole expression when we multiply the sum and the difference (sum * difference).

In programming, it is convenient to use the interim results (interim values), which we call **variables**. You can think of variables as spaces in computer memory, similar to boxes, in which the interim results are stored. Variables have names. 

When you want to use the value of a specific variable in a program, it is enough just to indicate its name.

In MakeCode, you create variables in the category |Variables|.

.. |Variables| image:: ../_images/_imageMicroBit/p43.png

We create variables by clicking on the Make a variable button (2) in the Variable category (1), entering the name of the variable (3), in our case the name Counter, and then click on the OK button (4).

.. image:: ../_images/_imageMicroBit/11.png
      :align: center

Clearly, you can present our (2 + 1) * (12 - 10) expression differently. By creating two variables: |Zbir| and |Razlika|.

.. |Zbir| image:: ../_images/_imageMicroBit/p45.png

.. |Razlika| image:: ../_images/_imageMicroBit/p44.png

We will set the initial value of the ``Counter`` variable to be 0. This can be done by dragging the block |set| from the category |Variables| into the block |onstart|.

.. |onstart| image:: ../_images/_imageMicroBit/s20.png

.. |set| image:: ../_images/_imageMicroBit/p47.png

The final look of the code:

.. image:: ../_images/_imageMicroBit/p46.png
      :align: center

.. mchoice:: L5Z1
    :answer_a: 2.
    :answer_b: 10.
    :answer_c: 4.
    :feedback_a: The answer is correct!
    :feedback_b: The answer is not correct!
    :feedback_c: The answer is not correct!
    :correct: a

    Create a program, which has two variables: x and y. The set value of the variable x should be 2 (x = 2), and the set value of the variable y should be 4 (y = 4).
    When the program runs the block shown in the figure below, the result will be:

    .. image:: ../_images/_imageMicroBit/p48.png
          :align: center


Let's use arithmetic operators and variables to create a program, which calculates the perimeter and area of ​​a square.

To calculate the area of ​​a square, it is necessary to define the length of the side ``a``, whose value will change randomly, each time the user presses button ``A``, and when button ``B`` is pressed, the program will calculate the perimeter and the area of the given square.

At the very beginning, we need to create the variables ``a``, ``P`` and ``A``, which represent the side, the perimeter and the area of the square, respectively.

The random change of the value of the variable will be defined by the use of the block |pickrandom|.

.. |pickrandom| image:: ../_images/_imageMicroBit/p49.png

The look of the code when the initial value is defined and set in the block |onbutton| is shown below:

.. |onbutton| image:: ../_images/_imageMicroBit/p18.png


.. image:: ../_images/_imageMicroBit/p50.png
      :align: center

To see the value of the length of the side ``a``, we can drag the display block |shownumber|.


.. |shownumber| image:: ../_images/_imageMicroBit/15.png

The look of the block:

.. image:: ../_images/_imageMicroBit/p51.png
      :align: center

To calculate the perimeter and the area of ​​a square, we must remind ourselves that the perimeter of a square is 4*the length of the side (``4*a``) and that the area of a square is the product of the length of its sides (``a*a``). We use multiplication for calculating this. The look of the block for calculating the perimeter and the area of a square is:

.. image:: ../_images/_imageMicroBit/p52.png
      :align: center

To test the program, we will run it in the simulator by clicking the |play| button.

.. |play| image:: ../_images/_imageMicroBit/p3.png

.. mchoice:: L5Z2
    :answer_a: Any value from the interval 0 to 15, not including 0.
    :answer_b: Any value from the interval 0 to 15, including those values.
    :answer_c: Any value from the interval 0 to 15, not including 15.
    :correct: b
    :feedback_a: The answer is not correct!
    :feedback_b: The answer is correct!
    :feedback_c: The answer is not correct!

    Study the block carefully:

    .. image:: ../_images/_imageMicroBit/p53.png
          :align: center

    What will be the value of the Counter variable when a movement is made (shake)?
