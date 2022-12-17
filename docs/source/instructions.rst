Instructions
============


.. _control-instructions:

How to start control
--------------------

.. _video-instructions-avatar:

How to start the video (avatar side)
------------------------------------
Open the terminal with predefined layout, this will pop up a terminal with 6 panels, it doesn't matter which terminal you 
run the following commands, only the order matters:

.. code-block:: console

   $ terminator -l avatar

**Main Camera:** In terminal 1, start main camera sender by running

.. code-block:: console

   $ send_main

**Peripheral Camera:** In terminal 2, start peripheral camera sender by running

.. code-block:: console

   $ send_left

**Operator Camera:** We use :code:`obs` to receive operator view (due to my code not able to receive cropped 
video properly somehow..). In terminal 3, run 

.. code-block:: console

   $ obs

In obs you should be able to see only one source, right click and select **project to fullscreen**.
**(Add a picture or gif here)**. You might adjust the webcam on top of the camera to center the operator face.

.. _video-instructions-operator:

How to start the video (operator side)
--------------------------------------

Open the terminal with predefined layout, this will pop up a terminal with 8 panels, it doesn't matter which terminal you 
run the following commands, only the order matters:

.. code-block:: console

   $ terminator -l avatar

**Discovery center:** In terminal 1, start discovery by running 

.. code-block:: console

   $ discovery

**Main Camera:** In terminal 2, start main camera receiver by running

.. code-block:: console

   $ recv_main_node

The program will start listening to the main camera feed, once you started the sender, the main camera view will show up 
automatically.  
If you encountered an error saying *cannot connect to ROS master*, that means the ROS core is not started yet.
Please refer to :ref:`control-instructions`.

**Operator camera:** In terminal 3, start operator view sender by running

.. code-block:: console

   $ send_operator_video

**Peripheral Camera:** To receive peripheral view is a bit more complicated (don't worry, it's only two more steps).
First open :code:`obs` in terminal 4 by running

.. code-block:: console

   $ obs

If you have followed :ref:`video-instructions-avatar`, you should be able to see the wide angle camera view. Right click it and
project it onto the Sumsung monitor. **(Add a picture or gif here)**

.. _audio-instructions-avatar:

How to start the audio (avatar side)
--------------------------------------


.. _audio-instructions-operator:

How to start the audio (operator side)
--------------------------------------

.. _bleed-system:

How to bleed the system
-----------------------
First of all, you need to get up at 6am!