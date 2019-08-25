21 - First-in detection response to deactivation
================================================

Feature bit
-----------
Number of the ``Feature`` Bit: 21

First-in detection response to deactivation
-------------------------------------------
You can use this ``Feature`` Bit to define the first-in detection response of the interlock blocks depending on the ``FirstInEn = 0`` input parameter.

The default setting is 0.

- **Bit = 0**: When first-in detection is deactivated via ``FirstInEn = 0``, the output parameter ``FirstIn`` is reset.
- **Bit = 1**: When first-in detection is deactivated via ``FirstInEn = 0``, the output parameter ``FirstIn`` is maintained. When first-in detection is activated for the first time by an edge change of ``FirstInEn 0 -> 1``, the output parameter ``FirstIn`` is reset.
