9 - Resetting via input signals in the event of interlocking (Protection) or errors
===================================================================================


Feature bit
-----------
Number of the Feature bit: 9.


Resetting via input signals in the event of interlocking (Protection) or errors
-------------------------------------------------------------------------------
With this ``Feature`` bit, you define how automatic control is to be re-enabled after an active interlock.

The default setting is 0.

- **Bit = 0**: After an interlock (only Protection: Input parameter ``Protect``) or errors, the system can only be restarted using a reset command. Reset is initiated either by operator input in the faceplate or via the interconnectable input parameter (``RstLi = 1``) in the block. Thereafter, the currently pending command takes effect in automatic mode.
- **Bit = 1**: It is also possible to reset with a 0-1 edge change in the control signal in automatic mode.
