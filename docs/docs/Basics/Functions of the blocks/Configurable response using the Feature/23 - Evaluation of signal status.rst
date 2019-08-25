23 - Evaluation of signal status
================================

Feature bit
-----------
Number of the ``Feature`` bit: 23

Evaluation of signal status
---------------------------
You can use the ``Feature`` bit to specify if the signal status of the inputs is to be checked for the values 16#00 or 16#28. The signal status of the inputs itself remains unchanged here.

The default setting is 0.

**Bit = 0**: No evaluation of the signal status for 16#00 or 16#28.

**Bit = 1**: the signal status is determined, an input with ST = 16#00 or 16#28 is forwarded with value = 0. The "Negate signal" function at the input of the block has no influence on the reaction in this case.
