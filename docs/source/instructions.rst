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

First Fill Procedure (After large plumbing changes)
1. Check all water connections at motor modules for tightness 
2. Turn off all electronics and cover PCBs with plastic bags 
3. Continue with Normal Fill Procedure 

Normal Fill Procedure
1. Close all ball valves on actuators 
2. Ensure fill tank is full 
3. Connect fill, return, and air lines from fill cart 
4. Pressurize tank to 60 psi 
5. Starting with fingers, open glove/gripper ball valve and motor module ball valve 
6. Re-pressurize to 60psi to account for volume change 
7. Start pump and wait for water to flow out of return port (back into tank) 
8. Move large stiff hoses around to ensure all air exits 
9. Rotate and move glove/gripper around to ensure air exits starlite hoses 
10. Move both rotary and linear actuators being filled to remove small trapped bubbles 
11. Stop pump and close one of the two valves (whichever is easier to access) 
12. With two people, move both linear and rotary actuators to middle position and close final valve 
13. Repeat steps 5-12 for remaining DOFs in system (6 for robot, 3 for each exo-arm) 
14. Ensure pressure is at 60 psi 
15. Check all DOFs for proper motion (reach both end stops) 
16. Disconnect air, fill, and return ports 

Water Volume Calibration Procedure
1. Connect fill, return, and air lines 
3. Pressurize fill tank to 60 psi 
4. Starting with fingers, open one valve on linear/rotary pair 
5. With two people, move both linear and rotary actuators to middle position and close final valve 
6. Repeat steps 3 and 4 for all DOFs in system that need calibration 
7. Ensure pressure is at 60 psi 
8. Disconnect air, fill, and return ports 

Flush Procedure 
1. Depressurize system by pressing down on air quick release fitting pin (center of fitting) 
2. Depressurize fill cart by twisting small bleed valve/disconnecting air out push-to-connect 
3. Open tank lid 
4. Connect return to fill port on robot/exo-arm 
5. Ensure system is depressurized 
6. Connect Mikita compressor to return port 
7. Open one set of valves for a linear/rotary pair 
8. Pressurize using compressor to 30-50psi (water will be flowing if pressure is dropping) 
9. Once air is flowing into fill tank (listen for bubbles), continuously pressurize and push air into lines 
10. Move gripper/glove around to dislodge any trapped water in hoses, move large hoses as well 
11. Move rotary an linear actuators to dislodge trapper water in bonnets 
12. Stop pressurizing lines with compressor 
13. Close both valves 
14. Repeat steps 7-13 for all rotary/linear pairs on system (6 for robot, 3 for each exo-arm) 
15. Disconnect compressor and fill cart from system. 
16. NOTE: Small amounts of water can still be trapped in hoses, always turn off all electronics when disconnecting any fittings. Take extra care when doing plumbing maintenance on motor modules, cover PCBs with plastic bags. 
