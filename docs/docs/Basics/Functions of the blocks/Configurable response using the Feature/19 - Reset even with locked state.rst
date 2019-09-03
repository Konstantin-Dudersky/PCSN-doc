19 - Reset even with locked state
=================================

Feature bit
-----------
Number of the ``Feature`` bit: 19


Reset even with locked state
----------------------------
With this ``Feature`` bit, you specify if it is possible to perform a reset with an active "Protection" or "Motor protection" type interlock. This can be used, for example, to reset hardware interlocks.

The default setting is 0.

- **Bit = 0**: No reset is possible with a "Protection" type interlock or with active motor protection.

- **Bit = 1**: Reset is possible with a "Protection" type interlock or with active motor protection.
