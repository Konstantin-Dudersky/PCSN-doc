4 - Setting switch or button mode
=================================

Feature bit
-----------

Number of the ``Feature`` bit: 4


Setting switch or button mode (input signal as pulse signal or as static signal)
--------------------------------------------------------------------------------

You can use this Feature bit to determine whether a separate interconnectable 1-active control input has to be used for every automatic command of the block or two automatic commands are assigned to a control input.

The Feature bit affects the following control inputs:

- starting and stopping a motor
- Opening and closing a valve
- switching modes (parameters AutModLi and ManModLi)
- Setpoint specification internal and external (parametersSP_ExtLi and SP_IntLi)

is given in the form of a pulse (pushbutton operation) or a static signal (switching mode).

You can find the commands for controlling the block in the relevant section on block operating modes. They are always the parameters that are used for the automatic operation of a block.

**Bit = 0**: Button mode: Each automatic command is assigned to a control input. This has a latching reaction and is 1-active.

**Example with a motor MotRevL** : In this case, use the interconnectable input parameters.

- FwdAut = 1 for the command "Start forward"
- RevAut = 1 for the command "Start backwards"
- StopAut = 1 for the stop command and
- AutModLi = 1 for setting "Automatic" operating mode
- ManModLi = 1 for setting "Manual" operating mode

**Bit = 1**: Switching mode: two static automatic commands are assigned to a control input.

**Example with a motor MotRevL** : In this case, use the interconnectable input parameters.

- FwdAut = 1 for the command "Start forward"
- RevAut = 1 for the command "Start backwards" and
- FwdAut = 0 and RevAut = 0 for the stop command
- AutModLi = 1 for setting "Automatic" operating mode
- AutModLi = 0 for setting "Manual" operating mode

The StopAut and ManModLi control inputs are irrelevant in this case.
