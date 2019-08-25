0 - Set startup characteristics
===============================

Feature bit
-----------

Number of the ``Feature`` bit: 0

Set startup characteristics
---------------------------

With this Feature bit, you set the startup characteristics of the function
\blocks, for example, for:

- Motors, valves and controllers
- Channel blocks
- Monitoring blocks, e.g. MonAnL and MonDiL.
- Mathematical and analog logic blocks
- The OpAnL, OpAnS, OpDi01, and OpDi03 block
- The TimeTrg block
- Counter blocks
- The Average block
- The TimeTrig block
- The Trigger block

The default setting is 0.

.. note::
   This Feature bit has no function in the "Out of service" operating mode. The process tag remains in the "Out of service" operating mode after a warm restart of the CPU.

.. note::
   The message classes Alarm, Warning and Tolerance are not valid for user-configured message classes. Please take into consideration the validity of terms for user-configured message classes.

.. note::
   With a Run-Stop-Run transition of the CPU and internally pending messages, non-stuck-through messages with time stamps and auxiliary values beginning with RunUpCycle occur for blocks with the startup characteristic Feature bit  = 0 after expiration of the RunUpCycle counter in the following cases:

   - Alarm, warning or tolerance messages from the operating points (motor, valve, dosing, controller and analog monitoring blocks)
   - Feedback errors (motor and valve blocks)
   - Output signals of digital process tags (MonDiL, MonDi08)
   - Flutter limits violated (MonDiL)

   The restart routines of the blocks reset the following outputs in OB100:
   - Operating point outputs xx_AH_Act, xx_AL_Act, xx_WH_Act, xx_WL_Act, xx_TH_Act, xx_TL_Act or GradHUpAct, GradHDnAct, GradLAct
   - Feedback error outputs MonDynErr and MonStaErr
   - Output binary signals Out, Out1..8 for MonDiL or MonDi08
   - Flutter suppression FlutAct for MonDiL

   This causes an outgoing message when initializing Alarm8_P in OB100 and an incoming message after expiration of the RunUpCycle counter on the cyclic interrupt level.


.. note::
   During a complete download with AS stop, the blocks (with Feature.Bit0 = 1) cannot resume operation in their previous mode and control when restarted.

Set startup characteristics for motors, valves and controllers
--------------------------------------------------------------

**Bit = 0**: Starting the block in manual mode and in neutral position. With controllers, the setpoint is set to (SP_Int) internally. See also the section Neutral position for motors, valves and controllers for more on this.

The controller blocks PIDConL, PIDConS, PIDConR, PIDStepL, ModPreCon, MPC10x10, and the valve block VlvAnL have the additional Feature bit 16, Neutral position manipulated variable takes effect at startup, which specifies whether the neutral position is approached

**Bit = 1**: Starting the block with the last stored values, in other words in the last operating mode set (manual, automatic or local mode) and at the last valid position.

.. note::
   Special note following complete download to the CPU

   Following a complete download to the CPU, the motor protection signal Trip is evaluated during the initial run as good (=1).

   When a motor protection signal is pending, this causes a non-struck-through message with time stamp and auxiliary values beginning with RunUpCycle after the complete download and after expiration of the RunUpCycle counter.

Startup characteristics for the ShrdResS block
----------------------------------------------

**Bit = 0**: The output command interface is reset to 0.

**Bit = 1**: The block leaves the output command interface unchanged.


Defining the startup characteristics for channel blocks
-------------------------------------------------------

**Bit = 0**: The channel block uses either the process value PV_In or the value of SimPV_In as the startup value, depending on the setting of the input parameter SimOn (PV_In = PV_Out or SimPV_In = PV_Out).

**Bit = 1**: The channel block uses the value StartVal as the startup value (StartVal = PV_Out).


Defining the startup characteristics for monitoring blocks
----------------------------------------------------------

**Bit = 0**: The most recently stored values are reset on startup.

**Bit = 1**: The most recently used value at the output parameter Out is output on startup.


Defining the startup characteristics for mathematical, analog logic blocks
--------------------------------------------------------------------------
**Bit = 0**: The Out output parameter is reset to 0 on startup.

**Bit = 1**: The most recently saved value is output at the Out output parameter on startup.


Defining startup characteristics for the OpAnL/OpAnS blocks
-----------------------------------------------------------
**Bit = 0**: The internal setpoint is used for startup.

**Bit = 1**: The most recently saved value is output at the Out output parameter on startup.


Defining startup characteristics for the OpDi01/OpDi03 blocks
-------------------------------------------------------------
**Bit = 0**: The output parameters Out or Out1...Out3 will be reset on startup.

**Bit = 1**: The most recently used value at the output parameter Out or Out1...Out3 is outputted on startup.


Defining the startup characteristics for counter blocks
-------------------------------------------------------
**Bit = 0**: On startup, the counter is stopped and reset to the value specified in the input parameter.

**Bit = 1**: On startup, counting continues with the most recently stored value.

Input parameters for the startup characteristics of the counter blocks:
- Block CountOh: Input parameter PresetTime
- Block CountScL: Input parameter PresetVal
- Block TotalL: Input parameter PresetVal

Messages can be suppressed for a short time after startup. You can set the number of cycles using the input parameter RunUpCyc.

.. note::
   Advanced configuration of the startup characteristics for the counter blocks

   Note that you can further affect the startup characteristics via the Feature Bit 5 as a function of this Feature Bits 0. Refer to the section: Use the last value following a complete download as the current value during startup of the block.


Defining startup characteristics for the Average block
------------------------------------------------------

**Bit = 0**: At startup, averaging begins with the value that is currently at the input parameter (Out = In, NumCycles = 1).

**Bit = 1**: When starting-up, the last Out and NumCycles values saved are used as the last value for averaging (Out ≠ In).


Defining startup characteristics for the TimeTrig block
-------------------------------------------------------

**Bit 0 = 0**: Periodic trigger and single trigger can be shut off. The trigger pulse Trigger is reset.

**Bit 0 = 1**: The activation of the periodic trigger and single trigger as well as the single trigger point are retained.

The InPerTrigOn, InSglTrigOn and InSglTrigDT inputs are applied for this. If you want to use the reset for a complete download, you must read back the marked parameters in addition to the operated and monitored parameters before a complete download.
