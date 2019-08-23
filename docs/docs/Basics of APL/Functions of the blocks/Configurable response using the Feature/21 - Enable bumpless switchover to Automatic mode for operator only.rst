21 - Enable bumpless switchover to Automatic mode for operator only
=====================================================================

Feature bit
-----------
Number of the Feature bit: 21

Enable bumpless switchover to automatic mode for operator only
--------------------------------------------------------------

You can use this Feature bit to specify whether bumpless switchover to automatic mode for valves, motors and dosing unit should be enabled only if switching via the faceplate is in effect, or whether switching using interconnectable inputs AutModLi and ManModLi (ModLiOp = 1) is also possible.

The default setting is 0

**Bit = 0**: The function "Bumpless switchover to automatic mode for valves, motors and dosers" works when switching via the faceplate and switching using interconnectable inputs AutModLi and ManModLi (ModLiOp = 1).

**Bit = 1**: The "Bumpless switchover in automatic mode for valves, motors and dosers" function only works for switching via the faceplate. Bumping switchover can be activated via the inputs AutModLi and ManModLi (ModLiOp = 1).
