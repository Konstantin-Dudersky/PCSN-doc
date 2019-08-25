Resetting the block in case of interlocks or errors
===================================================

Resetting the block
-------------------

The block must be reset when an interlock has been set via the ``Protect`` input ("Protection"), ``Trip`` ("Protection") or an error has occurred ("Runtime" or "Control", external error ``FaultExt`` or ``CSF`` with ``Feature`` Bit 18).

.. note::
   "Small" blocks do not feature protection (``Protect``).

The ``RdyToReset`` output signals when a reset can be carried out via the ``RstLi`` input parameter or the automatic commands.

There are different ways to reset the block:

- Reset by interconnection (input ``RstLi``).
- Reset by the operator using a button in the faceplate (input ``RstOp``).
- Reset with a 0-1 edge transition in the corresponding automatic or local signal (except with motor protection). Refer to the following sections for more information.

.. note::
   The reset via input ``RstLi`` or ``RstOp`` does not depend on the selected operating mode.

The operator must have the appropriate authorization to use the reset function in the faceplate (``OS_Perm``). After a reset, the output parameter ``P_Rst`` is set for a cycle.


Resetting monitoring errors and interlocks in manual and automatic mode
-----------------------------------------------------------------------

You can influence the reaction using the following ``Feature`` Bits:

- ``Feature`` Bit 9: :doc:`../Configurable response using the Feature/9 - Resetting via input signals in the event of interlocking (Protection) or errors`
- ``Feature`` Bit 30: :doc:`../Configurable response using the Feature/30 - Set reset depending on the operating mode or the LiOp parameter`
- ``Feature`` Bit 31: :doc:`../Configurable response using the Feature/31 - Activating recording of the first signal`

.. note::
   The following applies for valves:

   With ``MonSafePos = 0``, no reset is required; the valve can be moved in spite of the response fault.


Resetting monitoring errors, external errors and interlocks in local mode
-------------------------------------------------------------------------

The monitoring error can occur in local mode if you have set 1, 3 or 5 for the input parameter ``LocalSetting`` (see :doc:`../Operating modes of the blocks/Local mode`). When ``LocalSetting`` is set to 2 or 4, a monitoring error can only occur when a rapid stop is triggered.

The following applies with ``LocalSetting`` 1 or 3:

- The monitoring error, the external error and the interlocks cannot be reset when the control and feedback signals do not match.
- When the control and feedback signals match, the monitoring error, external error and the interlocks are reset by stopping (``StopLocal = 1``) the drive.
- With Vlv2WayL in the ``MonSafePos = 1`` setting, a monitoring error is reset by Pos0Local = 1.
- With VlvL, VlvMotL in the ``MonSafePos = 1`` setting, a monitoring error is reset with the local command, which moves the valve to the neutral position.
- With Vlv2WayL, VlvMotL and VlvL in the ``MonSafePos = 0`` setting, no reset of the monitoring error is required. The currently pending control is in effect.
- With Vlv2WayL, VlvL and VlvMotL, an external error is reset with the local command, which moves the valve to the neutral position
- With DoseL, you must acknowledge the protection (``Protect``) and flow alarms with a positive edge at the ``CancelLocal`` or ``PauseLocal`` output parameter.

The following applies with LocalSetting 2, 4 or 5:

- No reset required.


Resetting motor protection (``Trip``) in local mode
---------------------------------------------------

In local mode, the "Motor protection" display is reset in the faceplate and not using the Reset button available there. The display disappears as soon as ``Trip = 1``, the activation signals and feedback match and a command for stopping the drive has been issued.

.. note::
   A motor protection signal (Trip parameter) with signal status 16#00 or 16#28 is used to activate motor protection. This is indicated by "Motor protection" in the standard view of the faceplates.


Resetting monitoring errors, external errors and interlocks using the "Forcing operating states" function
---------------------------------------------------------------------------------------------------------

With "Forcing operating states", monitoring errors, external errors, interlocks or the motor protection function are reset under the following conditions and a reset pulse is output at the ``P_Rst`` output:

- The block is in an operating mode in which a reset is necessary and
- a monitoring error, an external error, a "Protection" interlock or the motor protection function is ready to be reset. This can be seen in the faceplate with the reset button or with the Request 0/1 indicator in the faceplate. When ``Feature`` Bit 19 = 1, the block is ready to reset as soon as the protection (``Protect = 0``) or motor protection (``Trip = 0``) interlock is set, whereby enabled motor protection prevents the motor from starting.

See also the following chapter: :doc:`Forcing operating modes`.


Tabular overview for resetting for interlocks and errors
--------------------------------------------------------

.. list-table::
   :header-rows: 1

   * -
     - Permit
     - Interlock
     - Protect
   * - Meaning
     - Activation enable ("Permission")
     - Interlock without reset ("Interlock")
     - Interlock with reset ("Protection")
   * - Description
     - The activation enable (input ``Permit = 1``) makes it possible to leave the neutral position of the block in response to operator input or a command from the program (CFC/SFC). The activation enable has no effect if the block is not in the neutral position.
     - A pending interlock condition brings the block to the neutral position (input ``Intlock = 0``).
     - A pending interlock condition brings the block to the neutral position (input ``Protect = 0``).
   * - Automatic mode
     - Takes effect if block is in the neutral position.

       After the interlock condition has gone, the currently pending control function becomes active again.

     - After the interlock condition has gone, the currently pending control function becomes active again.

     - - **Feature Bit 9 and 30 = 0**: Reset via faceplate or ``RstLi = 1``

       - **Feature Bit 9 = 1 and 30 = 0**: Reset via faceplate or ``RstLi = 1`` or a 0-1 edge transition in the control

       - **Feature Bit 9 = 0 and 30 = 1**: Reset via ``RstLi = 1``

       - **Feature Bit 9 and 30 = 1**: Reset via ``RstLi = 1`` or a 0-1 edge transition in the control = 1 or 0-1 edge transition in the control

   * - Local mode
     - Takes effect if block is in the neutral position.

       After the interlock condition has gone, the currently pending control function becomes active again.

     - After the interlock condition has gone, the currently pending control function becomes active again.

     - The following applies with ``LocalSetting`` = 1 or 3:

       - **Generally**: When the control and feedback signals match, reset via ``StopLocal = 1``.

       - **Vlv2WayL , VlvMotL und VlvL**: Reset via local command, which moves the valve into the neutral position.

       - **DoseL** : Reset via a positive edge at ``CancelLocal`` or ``PauseLocal``.

       The following applies with ``LocalSetting`` = 2,4 or 5:

       - No reset required

   * - Manual mode
     - Takes effect if block is in the neutral position.

       It is possible to leave the neutral position with an operation in the faceplate.

     - The faceplate can be operated again after the interlock condition has gone.

     - - **Feature Bit 30 and 31 = 0**: Resetting not necessary

       - **Feature Bit 30 = 1 and 31 = 0**: Resetting not necessary

       - **Feature Bit 30 = 0 and 31 = 1**: Reset via faceplate or RstLi = 1

       - **Feature Bit 30 and 31 = 1**: Reset via faceplate


.. list-table::
   :header-rows: 1

   * -
     - Trip
     - Error
     - Rapid stop

   * - Meaning
     - Motor protection
     - Monitoring errors and external errors
     - Rapid stop

   * - Description
     - The motor protection function is used to switch off the motor when there is a heat overload (input ``Trip = 0``).
     - - Monitoring the startup and stop characteristics for motors or the runtime of valves
       - Monitoring the operation of motors or the maintenance of the position of valves
       - External error FaultExt: Block goes to error state without a message being output.
       - External control system fault CSF with set Feature Bit 18: block reports an external control system fault and goes to error state.
     - A rapid stop stops the drive immediately.

   * - Automatic mode

     - - **Feature Bit 9 and 30 = 0**: Reset via faceplate or ``RstLi = 1``
       - **Feature Bit 9 = 1 and 30 = 0**: Reset via faceplate or ``RstLi = 1`` or a 0-1 edge transition in the control
       - **Feature Bit 9 = 0 and 30 = 1**: Reset via ``RstLi = 1``
       - **Feature Bit 9 and 30 = 1**: Reset via ``RstLi = 1`` or a 0-1 edge transition in the control = 1 or 0-1 edge transition in the control

     - - **Feature Bit 9 and 30 = 0**: Reset via faceplate or ``RstLi = 1``
       - **Feature Bit 9 = 1 and 30 = 0**: Reset via faceplate or ``RstLi = 1`` or a 0-1 edge transition in the control
       - **Feature Bit 9 = 0 and 30 = 1**: Reset via ``RstLi = 1``
       - **Feature Bit 9 and 30 = 1**: Reset via ``RstLi = 1`` or a 0-1 edge transition in the control = 1 or 0-1 edge transition in the control

     - - **Feature Bit 9 = 0**: Reset via faceplate or ``RstLi = 1``
       - **Feature Bit 9 = 1**: Reset via faceplate or ``RstLi = 1`` or a 0-1 edge transition in the control

   * - Local mode

     - The following applies with ``LocalSetting`` = 1 or 3:

       - When the control and feedback signals of the drive match, reset via ``StopLocal = 1``.

       The following applies with ``LocalSetting`` = 2, 4 or 5:

       - No reset required.

     - The following applies with ``LocalSetting`` = 1 or 3:

       - When the control and feedback signals of the drive match, reset via ``StopLocal = 1``.

       - With Vlv2WayL, VlvMotL and VlvL

         - **Monitoring error** with ``MonSafePos = 1``: Reset via the local command, which moves the valve into the neutral position.

         - **Monitoring error** with ``MonSafePos = 0``: No resetting required; the currently pending control function is active.

         - **External error**: Reset via the local command, which moves the valve into the neutral position.

       - With DoseL, resetting via a positive edge at ``CancelLocal`` or ``PauseLocal``.

       The following applies with ``LocalSetting`` = 2, 4 or 5:

       - No reset required.

     - The rapid stop function is unlocked in the faceplate via the "Reset" button (``RstOp = 1``). In CFC, unlocking is carried out using the input parameter ``RstLi = 1``

   * - Manual mode

     - - **Feature Bit 30 and 31 = 0**: Resetting not necessary
       - **Feature Bit 30 = 1 and 31 = 0**: Resetting not necessary
       - **Feature Bit 30 = 0 and 31 = 1**: Reset via faceplate or ``RstLi = 1``
       - **Feature Bit 30 and 31 = 1**: Reset via faceplate

     - - **Feature Bit 30 and 31 = 0**: Resetting not necessary
       - **Feature Bit 30 = 1 and 31 = 0**: Resetting not necessary
       - **Feature Bit 30 = 0 and 31 = 1**: Reset via faceplate or ``RstLi = 1``
       - **Feature Bit 30 and 31 = 1**: Reset via faceplate

     - The rapid stop function is unlocked in the faceplate via the "Reset" button (``RstOp = 1``). In CFC, unlocking is carried out using the input parameter ``RstLi = 1``

