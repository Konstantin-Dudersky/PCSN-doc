Local mode
==========

Areas of application for local mode
-----------------------------------

This operating mode is used for motors, valves and dosing units. The control settings are made directly or via a control station that is located "locally". In addition, you can set different control strategies with the parameter LocalSetting.

With LocalSetting = 0, you prevent a change to "local mode".

.. note::
   Differences between "Large" and "Small" blocks

   The operating mode described here is valid for "Large" blocks. For "Small" blocks, LocalSetting can be configured only on a limited basis. For more information, refer to the respective description for the operating modes of the blocks.


Changing to local mode
----------------------

Changing to local mode is only possible from the manual and automatic operating modes. The change to this mode is initiated by:

- An operation on the faceplate (input parameter LocalOp = 1, valid if LocalSetting = 3 or LocalSetting = 4 and ModLiOp = 0) or
- The interconnected input parameter (LocalLi = 1, valid if LocalSetting = 1 or LocalSetting = 2).


Exiting local mode
------------------

You leave local mode using:

- An operation on the faceplate (LocalSetting = 3 or LocalSetting = 4 and ModLiOp = 0) or
- the interconnected input parameter (LocalSetting = 1 or LocalSetting = 2).

In order to exit local mode via the interconnected input parameter, you can configure various reactions using a Feature bit Exiting local mode.


Operator input in "local mode" using a faceplate
------------------------------------------------

You are not permitted to functionally operate the block in local mode. You can only use the faceplate to exit local mode if you have also activated "local mode" using the faceplate. The rules you specified for exiting "local mode" apply here.


Input in "local mode" via interconnected inputs
-----------------------------------------------

In "local mode", the way the block functions is influenced via interconnected input parameters according to the settings of the LocalSetting parameter. You have the following options:

- LocalSetting = 1 and LocalSetting = 3

  - The control settings for the block are adjusted (tracking) via an interconnected input parameter. The interconnected input parameter includes the control signal for the local operator station on the system.
  - The runtime monitoring of the block is effective in accordance with your configuration.
  - The interlocking functions of the block are activated in accordance with input parameter BypProt = 0 or deactivated (BypProt = 1).

  .. note::

     The block VlvAnL does not support LocalSetting = 1/3.

- LocalSetting = 2 and LocalSetting = 4

  - The control settings for the block are made based on internal adjustment of the feedback value.
  - Runtime monitoring of the block is active only with rapid stop, external fault, motor protection, and if both feedback signals are set (discrepancy).

  An exception is VlvMotL:

  .. note::

     **VlvMotL**

     The motor and valve feedback signals are monitored if the motor feedback signlas exist and are connected with FbkOpening and FbkClosing (Feature bit 12 = 0). The motor feedback signals are only monitored in the end positions of the valve and in discrepancy. For example, if the valve is in end position FbkOpen =1 and the motor feedback FbkOpening =1 is pending, an error message is generated upon expiration of the monitoring time. If there are no motor feedback signals (Feature bit 12 = 1), monitoring of the valve and motor feedback signals does not take place.


     **VlvAnL**: The auxiliary valve is controlled via internal tracking of the feedback signals FbkAuxVCloseOut and FbkAuxVOpenOut. The control of the main valve via the feedback value Rbk is not affected by this.

The texts for labeling the command buttons in the faceplates of the motor and valve blocks can now be assigned for each specific instance.
The configuration of the texts is performed with the "Text 1" property of the respective control inputs of the motor and valve blocks in the CFC.

If no instance-specific text is configured, the previous default texts are used and displayed in the faceplate.

The following table shows the assignment of the command buttons to the corresponding block input:

The interlock functions of the block are deactivated.

.. list-table:: Overview of behavior in local mode
   :header-rows: 1

   * - LocalSetting =
     - 0
     - 1
     - 2
     - 3
     - 4
     - 5 (VlvS only)
   * - Switch on operating mode
     - Cannot be set
     - CFC/SFC
     - CFC/SFC
     - Faceplate
     - Faceplate
     - CFC
   * - Changing the operating mode: Local mode/to manual mode only (Feature = 0)
     - \-
     - CFC/SFC
     - CFC/SFC
     - \-
     - \-
     - CFC/SFC
   * - Changing the operating mode: Local mode/previous mode (Feature = 1)
     - \-
     - CFC/SFC
     - CFC/SFC
     - \-
     - \-
     - CFC/SFC
   * - Operating in the faceplate
     - \-
     - Only rapid stop and resetting of rapid stop
     - Only rapid stop and resetting of rapid stop (only for "Large" blocks)
     - Only switching of operating mode, rapid stop, internal/external setpoint switchover and resetting of rapid stop
     - Only switching of operating mode, rapid stop, and resetting of rapid stop
     - \-
   * - Executing local commands
     - \-
     - Yes
     - No
     - Yes
     - No
     - No
   * - Reaction of the block
     - \-
     - Monitoring the feedbacks
     - Tracking of feedback, monitoring feedback during rapid stop, external errors, motor protection or discrepancy
     - Monitoring the feedbacks
     - Tracking of feedback, monitoring feedback during rapid stop, external errors, motor protection or discrepancy
     - Monitoring the feedbacks
   * - Interlock activated
     - \-
     - Yes: (BypProt = 0) No: (BypProt = 1)
     - only at output LockAct with Feature Bit 27 = 1 and BypProt = 0
     - Yes: (BypProt = 0) No: (BypProt = 1)
     - only at output LockAct with Feature Bit 27 = 1 and BypProt = 0
     - only at output LockAct with Feature Bit 27 = 1 and BypProt = 0






