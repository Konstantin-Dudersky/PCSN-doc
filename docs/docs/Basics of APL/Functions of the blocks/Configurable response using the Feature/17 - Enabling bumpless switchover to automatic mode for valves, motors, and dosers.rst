17 - Enabling bumpless switchover to automatic mode for valves, motors, and dosers
==================================================================================

Feature bit
-----------
Number of the Feature bit: 17

Bumpless switchover
-------------------
You can use this Feature bit to enable the bumpless switchover from local/manual mode to automatic mode.

Default setting is 0

**Bit = 0**: Bumpless switchover is disabled. You can switch from local/manual mode to automatic mode at any time.

**Bit = 1**: Bumpless switchover from local/manual mode to automatic mode is enabled. A switchover from local/manual mode to automatic mode is only possible if the control settings of the local/manual mode and automatic modes match. If switchover occurs at a different point in time, this is indicated in the faceplate with the text "Switchover error".

Refer to the Manual and automatic mode for motors, valves and dosers section for more on this.

A second feature bit is used to specify if bumpless switchover to automatic mode is only possible via the faceplate or if switching is also possible via the interconnectable parameters AutModLi and ManModLi (ModLiOp = 1).

Refer to the section :doc:`21 - Enable bumpless switchover to Automatic mode for operator only`.
