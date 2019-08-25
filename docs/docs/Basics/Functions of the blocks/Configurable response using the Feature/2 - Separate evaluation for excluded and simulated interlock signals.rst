2 - Separate evaluation for excluded and simulated interlock signals
====================================================================

Feature bit
-----------

Number of the ``Feature`` bit: 2


Separate evaluation for excluded and simulated interlock signals
----------------------------------------------------------------

You can use this Feature bit to set the reaction of the block to an interlock signal of an interlock block that is excluded or simulated.

The default setting is 0.

**Bit = 0**: Switch-relevant excluded and simulated interlock signals are processed with the status 16#60 and are displayed as simulated or excluded, depending on the interlock status.

**Bit = 1**: Excluded and simulated interlock signals are evaluated separately. All excluded interlock signals in a sequence of interlock blocks are displayed as excluded. Switch-relevant simulated interlock signals are processed with the status 16#60 and displayed as simulated.

.. note::
   If the ``Feature`` Bit is enabled, the signal cannot be inverted via CFC during interconnections at the inputs, as, otherwise, the bypass display would not update.

   The interlocking inputs of the following blocks are affected:

   - **Intlk02 , Intlk04, Intlk08, Intlk16**: ``In01``, ``In02``, …
   - **DoseL, MotL, MotSpdL, MotSpdCL, VlvL, Vlv2WayL, VlvAnL**: ``Permit``, ``Interlock``, ``Protect``
   - **MotRevL** : ``Permit``, ``Interlock``, ``Protect``, ``PermRev``, ``IntlRev``, ``ProtRev``
   - **VlvMotL , VlvPosL**: ``Permit``, ``Interlock``, ``Protect``, ``PermCls``, ``IntlCls``, ``ProtCls``
   - **MotS , VlvS, OpDi01, OpDi03, PIDConL, PIDConR**: ``Interlock``

   The inversion of the interlocking signals occurs via the ``InvIn01``, ``InvIn02``, … inputs on the interlocking blocks.
