1 - Reaction to the out of service mode
=======================================

Feature bit
-----------

Number of the Feature bit: 1

Reaction to the out of service mode
-----------------------------------

You can use this Feature bit to define the reaction of the technologic block based on the interconnectable input parameter OosLi = 1.

The default setting is 0.

**Bit = 0**: The symbol for the "In progress" status (see below) appears in the block icon and in the faceplate of the assigned technologic block. A 0-1 edge transition at the input parameter OosLi has no further influence on the reaction of the technological block; the previous status is retained. No switch to the "Out of service" mode is performed.

**Bit = 1**: The mode switches to "Out of service" assuming that the block is "On" or "Manual" mode. If this is not the case, the mode does not change. The symbol for the "In progress" (see below) status also appears in the block icon and in the faceplate of the assigned technologic block regardless of the mode change. No message is output to indicate whether or not the mode change took place.

The status display for "In progress" appears as follows:

A 1-0 edge transition at the input parameter OosLi has no influence on the reaction of the technologic block, the previous status is retained.

See also the section Release for maintenance for more on this.
