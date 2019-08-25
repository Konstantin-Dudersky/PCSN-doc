Forcing operating modes
=======================

Forcing operating modes
-----------------------
The "forcing of operating modes" function lets you set the function block into a different operating mode using interconnectable input parameters, regardless of the currently active control. This can, for example, be:

- Forces tracking for closed-loop controllers and control valves
- Enabling and disabling at motors
- Opening and closing of valves

It is only possible to force operating modes with "Large" blocks in the following operating modes:

- Manual mode
- Automatic mode
- Local mode (only if ``Feature2.Bit8 = 1``)

Forcing operating modes has the highest priority over all three operating modes.

.. note::
   It is not possible to force operating modes in local mode.


Forcing operating modes at closed-loop controllers
--------------------------------------------------
In control engineering, this procedure is also known as forced tracking of values. Refer to the :doc:`../Functions for controllers/Tracking and limiting a manipulated variable` section for more on this.


Forcing operating modes at motors and valves
--------------------------------------------
The input parameter ``xxxxForce = 1`` (for example ``OpenForce`` and ``CloseForce`` at a valve) is used for forced controlling of the function block and thus an intervention in the function of the block, irrespective of currently active controls, interlock conditions and monitoring errors. If the input parameters are inconsistent (for example ``OpenForce = 1`` and ``CloseForce = 1`` at valves), an :doc:`error number <../Error handling/Error handling2>` is output at the parameter ``ErrorNum`` and the control remains unchanged.

.. note::
   If you have set the parameters for the advance warning time ``WarnTiMan`` and the idle time ``IdleTime`` to values higher than 0, the control will only take effect once the set times have elapsed.

.. note::
   With block VlvAnL, the warning time is ignored in tracking ``MV_TrkOn = 1`` and in forced tracking ``MV_ForOn``.

The ``Feature`` bit :doc:`../Configurable response using the Feature/7 - Enabling direct changeover between forward and reverse` has no effect when forcing the operating modes of the MotRevL and MotSpdCL blocks. Direct switchover between forward and reverse is always possible.


Display in the faceplate and in the block icon
----------------------------------------------

If an operating mode is forced, this is displayed in the block icon and in the standard view of the faceplate:

**Block icon**: In the block icon, the display for motors, valves and dosers involves the use of a red F and a crossed-out padlock.

There is no display for closed-loop controllers.

**Faceplate**: An information text on the forced operating mode is displayed in the standard view of the faceplate, for example, "Forced stop" for motors. This is also indicated by a crossed-out padlock:

.. todo::
   Insert pucture

Messaging
---------

No messages are assigned to the forcing of operating modes. However, if you want to have corresponding messages, you can use the freely interconnectable input parameters to generate the messages. Refer also to the :doc:`../Messaging/Generating instance-specific messages` section for more on this.
