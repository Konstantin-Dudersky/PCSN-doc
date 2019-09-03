30 - Set reset depending on the operating mode or the LiOp parameter
====================================================================

Feature bit
-----------
Number of the ``Feature`` Bit: 30.


Set reset depending on the operating mode (motor, valve and dosing blocks)
--------------------------------------------------------------------------
When the "Protection" interlock, feedback error ("Status error", "Control error") or "Motor protection" signal is present again, use this ``Feature`` bit to specify if a reset can be made depending on the mode only by the operator in manual mode or only by the automatic I/Os in automatic mode.

Resetting to manual mode is enabled with ``Feature`` bit :doc:`31 - Activating reset of protection and error in manual mode`. Also refer to :doc:`../General information/Resetting the block in case of interlocks or errors`.

The default setting is 0.

- **Bit = 0**: Reset does not depend on the operating mode
- **Bit = 1**: In manual mode, manual reset by the operator is only possible if ``Feature`` bit 31 is set, otherwise no reset is required in manual mode.

In automatic mode, reset can only be made with automatic I/Os, regardless of ``Feature`` bit 31. This is performed either with a 0-1 edge transition at the ``RstLi`` input or, when ``Feature`` bit 9 is set, with a 0-1 edge transition at the automatic inputs, for example ``OpenAut``, ``CloseAut``.

.. note::
   Rapid stop is unlocked for all operating modes using the "Reset" button in the faceplate (``RstOp = 1``); in CFC it is unlocked using the ``RstLi = 1`` input parameter.

.. note::
   The local operating mode does not depend on this ``Feature`` bit and has a separate reset mechanism.



Resetting the dosing mode depending on the operating mode (dosing blocks)
-------------------------------------------------------------------------

You can also use this feature bit to set whether or not the reset of the dosing quantity is dependent on the operating mode.

The default setting is 0.

- **Bit = 0**: Reset does not depend on the operating mode
- **Bit = 1**: In manual mode, only a manual reset by the operator is possible at the input ``RstDQ_Op``. In automatic mode, a reset is only possible by a 0-1 edge transition at the input ``RstDQ_Li``.

.. note::
   The operating mode Local is independent of this feature bit. The dosing quantity can be reset by the operator at the input ``RstDQ_Op`` or via a 0-1 edge transition at the input ``RstDQ_Li``.


Set reset depending on the LiOp parameter (counter blocks)
----------------------------------------------------------
You can use this ``Feature`` bit to determine whether the setting or resetting to a default value should be made dependent on the ``LiOp`` parameter.

The default setting is 0.

- **Bit = 0**: Setting or resetting to a default value does not depend on the ``LiOp`` parameter.
- **Bit = 1**: Setting or resetting to a default value depends on the ``LiOp`` parameter.

  - ``LiOp = 0``: Setting or resetting to a default value can only be made via the faceplate or at the parameter for the faceplate.
  - ``LiOp = 1``: Setting or resetting to a default value can only be made at the parameter for interconnections.
