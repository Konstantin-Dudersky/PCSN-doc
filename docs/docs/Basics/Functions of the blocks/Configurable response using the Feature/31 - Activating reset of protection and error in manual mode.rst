31 - Activating reset of protection and error in manual mode
============================================================


Feature bit
-----------
Number of the ``Feature`` bit: 31.


Activating reset of protection and error in manual mode
-------------------------------------------------------

Use this ``Feature`` bit to specify whether a reset is necessary once the "Protection" interlock signal, feedback errors ("Runtime error", "Control deviation"), or "Motor protection" are present again. See also the following section: :doc:`../General information/Resetting the block in case of interlocks or errors`.

The default setting is 0.

- **Bit = 0**: No reset required in manual mode.
- **Bit = 1**: Reset required in manual mode. The reset is performed using the "Reset" button (``RstOp = 1``) or, in CFC, using the input parameter ``RstLi``.

.. note::
   Rapid stop is unlocked for all operating modes using the "Reset" button in the faceplate (``RstOp = 1``); in CFC it is unlocked using the ``RstLi = 1`` input parameter.

.. note::
   The local operating mode does not depend on this ``Feature`` bit and has a separate reset mechanism.

