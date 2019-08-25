Intlk16 functions
=================


Functions of Intlk16
--------------------
The functions for this block are listed below.


Logic operators
---------------
Use the ``Logic`` input to specify the logic operator that the block should employ when determining the interlock state. Make the following settings:

- ``Logic = 0``: OR
- ``Logic = 1``: AND


Inversion of logic signals
--------------------------
You can invert the input signals by setting the input parameter ``InvInx`` for the input concerned to ``Inx = 1``, e.g. for input ``In01`` set the I/O ``InvIn01``.

The inversion is displayed in the faceplate. If you invert signals using any other method, this is not shown in the faceplate.


Bypass
------

.. note::
   Bypassing the interlock means that the interlock signal (input signal) is excluded from the logic of the interlock block, in other words, this signal is ignored in the logic operation.

This function can only be executed in the faceplate with "high-level operating permission".

You can bypass interlock signals as follows:

- From operator over faceplate (``BypInx = 1``):

  Independent ``BypLix`` is connected or not, the operator can bypass the input signal.

- By connecting ``BypLix`` in CFC (``BypLix.Value = 1``, ``BypLix.ST <> 16#FF``)

  Follow this if interlock signals are connected to parameters, which has no bypass information bit for bypass. Refer to sectionBypassing signals.

- By connected interlock signal ``Inx``. For this the corresponding enable bit (``BypEn.Inx = 1``) and ``Feature`` Bit2 :doc:`Separate evaluation for excluded and simulated interlock signals <../../Basics/Functions of the blocks/Configurable response using the Feature/2 - Separate evaluation for excluded and simulated interlock signals>`  have to be set. Follow this if the interlock signals are all connected to parameters which has the bypass information. Refer to sectionBypassing signals.

The bypassed interlock signal is shown in the faceplate as the symbol below:



You can reset all the bypass of interlock signals as follows:

- From operator over faceplate (``RstBypOp = 0 -> 1``)
- Over CFC linkable parameter (``RstBypLi = 0 -> 1``)

**Special situation**: If all input parameters are bypassed, the output value is defined using the ``DefaultOut`` parameter.

Depending on the configuration of the ``Feature`` bit :doc:`../../Basics/Functions of the blocks/Configurable response using the Feature/2 - Separate evaluation for excluded and simulated interlock signals`, the output ``BypAct`` is formed and the bypass signal/information is set at the output ``Out``.

Feature Bit2 = 0:
^^^^^^^^^^^^^^^^^
If one of the interlock inputs is bypassed by the operator or by connected ``BypLix``, then the output ``BypAct`` is set. The bypass signal/information at the output ``Out`` is always reset.

- ``BypAct.Value = BypIn01 OR BypLi01 OR BypInx OR BypLix``

  The calculation is simplified and described.

- ``Out.Bit1 = 0``

A bypassed interlock signal, that is switch-relevant, sets the status of ``Out`` to Simulation.

Feature Bit2 = 1:
^^^^^^^^^^^^^^^^^
If one of the interlock inputs is bypassed or the block which is connected to interlock signal is in bypass (signal is set at an interlock input ``In01...Inx``), the output ``BypAct`` is set. The bypass informataion in the signal at the input ``In01...Inx`` can be read from the upstream interlock block at the output ``BypAct`` or from the upstream technical block with bypass functionallity (MonDiL, MonAnL, TotalL, PIDConL, PIDConR, PIDStepL) at the output ``BypassAct``.

The bypass signal information at the outputOutis set to the value of ``BypAct``.

- ``BypAct.Value = BypIn01 OR BypLi01 OR In01.Bit1 OR BypInx OR BypLix OR In01.Bitx OR In01.Bit1 OR Inx.Bit1``

  The calculation is simplified and described.

- ``Out.Bit1 = BypAct.Value``

An bypassed interlock input has no influence on the status of ``Out``.

.. note::
   Do **not** connect the input ``BypLix`` with the output ``BypAct`` from an interlock block because ``BypAct`` is calculated from the bypass signal information.


Handling non-connected inputs
-----------------------------
Inputs which are not interconnected are not evaluated. They are not displayed in the faceplate either.

**Special situation**: If no inputs are connected, the output value is defined using the ``DefaultOut`` parameter. The signal status is set to 16#FF.


Opening additional faceplates
-----------------------------
This block provides the standard function Opening additional faceplates. However, only one additional faceplate can be called up using ``SelFp1 = 1``.


First-in detection for interlock blocks
---------------------------------------
This block provides the standard function Recording the first signal for interlock blocks. Note that a signal status change only has an effect on the first-in detection when the ``Feature`` Bit :doc:`../../Basics/Functions of the blocks/Configurable response using the Feature/23 - Evaluation of signal status` and the input ``FirstInEn`` is set.

The response to deactivation via the ``FirstInEn`` input can be influenced by Feature bit :doc:`../../Basics/Functions of the blocks/Configurable response using the Feature/23 - Evaluation of signal status`.

.. note::
   This function can only be executed in the faceplate with "process control" operating permission.


Forming the signal status for blocks
------------------------------------
This block provides the standard function Forming and outputting the signal status for interlock blocks.

The worst signal status ``ST_Worst`` for the block is formed from the following parameter:

- ``OUT.ST``


Operating permissions
---------------------
This block provides the standard function Operator control permissions.

The block has the following permissions for the OS_Perm parameter:

.. list-table::
   :header-rows: 1
   :widths: 5 95

   * - Bit
     - Function
   * - 0
     - 1 = Operator can exclude values
   * - 1
     - 1 = Operator can reset the exclusion of input values
   * - 2
     - 1 = Operator can reset the recording of the first signal
   * - 3
     - Not used
   * - 4
     - Not used
   * - 5
     - Not used
   * - 6
     - Not used
   * - 7
     - Not used
   * - 8
     - Not used
   * - 9
     - Not used
   * - 10
     - Not used
   * - 11
     - Not used
   * - 12
     - Not used
   * - 13
     - Not used
   * - 14
     - Not used
   * - 15
     - Not used
   * - 16
     - 1 = Operator can set or reset the exclusion of input value ``In01``
   * - 17
     - 1 = Operator can set or reset the exclusion of input value ``In02``
   * - 18
     - 1 = Operator can set or reset the exclusion of input value ``In03``
   * - 19
     - 1 = Operator can set or reset the exclusion of input value ``In04``
   * - 20
     - 1 = Operator can set or reset the exclusion of input value ``In05``
   * - 21
     - 1 = Operator can set or reset the exclusion of input value ``In06``
   * - 22
     - 1 = Operator can set or reset the exclusion of input value ``In07``
   * - 23
     - 1 = Operator can set or reset the exclusion of input value ``In08``
   * - 24
     - 1 = Operator can set or reset the exclusion of input value ``In09``
   * - 25
     - 1 = Operator can set or reset the exclusion of input value ``In10``
   * - 26
     - 1 = Operator can set or reset the exclusion of input value ``In11``
   * - 27
     - 1 = Operator can set or reset the exclusion of input value ``In12``
   * - 28
     - 1 = Operator can set or reset the exclusion of input value ``In13``
   * - 29
     - 1 = Operator can set or reset the exclusion of input value ``In14``
   * - 30
     - 1 = Operator can set or reset the exclusion of input value ``In15``
   * - 31
     - 1 = Operator can set or reset the exclusion of input value ``In16``

.. note::
   If you interconnect a parameter that is also listed in ``OS_Perm`` as a parameter, you have to reset the corresponding ``OS_Perm`` bit.


Configurable reactions using the Feature parameter
--------------------------------------------------
You can find an overview of all reactions provided by the Feature parameter in the chapter Configurable functions using the Feature I/O. The following functionality is available for this block at the relevant bits:

.. list-table::
   :header-rows: 1
   :widths: 5 95

   * - Bit
     - Function
   * - 2
     - :doc:`../../Basics/Functions of the blocks/Configurable response using the Feature/2 - Separate evaluation for excluded and simulated interlock signals`
   * - 5
     - :doc:`../../Basics/Functions of the blocks/Configurable response using the Feature/5 - Activate OS_Perm bits`

       - 0 = OS_Perm bits 16...17 inactive (evaluation only in faceplate)
       - 1 = OS_Perm bits 16...17 active (evaluation only in faceplate)

   * - 21
     - :doc:`../../Basics/Functions of the blocks/Configurable response using the Feature/21 - First-in detection response to deactivation`
   * - 23
     - :doc:`../../Basics/Functions of the blocks/Configurable response using the Feature/23 - Evaluation of signal status`
   * - 24
     - :doc:`../../Basics/Functions of the blocks/Configurable response using the Feature/24 - Enabling local operator authorization`
   * - 31
     - :doc:`../../Basics/Functions of the blocks/Configurable response using the Feature/31 - Activating recording of the first signal`


SIMATIC BATCH functionality
---------------------------
This block provides the standard function SIMATIC BATCH functionality.
