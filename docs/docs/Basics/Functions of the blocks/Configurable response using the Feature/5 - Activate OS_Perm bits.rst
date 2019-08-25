5 - Activate OS_Perm bits
=========================

Feature bit
-----------
Number of the ``Feature`` bit: 5


Display only input values that are interconnected in the faceplate
------------------------------------------------------------------
You use this ``Feature`` bit to activate the use of additional ``OS_Perm`` bits in the faceplate.

The default setting is 0.

- **Bit = 0**: ``OS_Perm`` bits XXX inactive
- **Bit = 1**: ``OS_Perm`` bits XXX active

With XXX:

.. list-table::
   :header-rows: 1

   * - Block
     - ``OS_Perm`` bit X
   * - Intlk02
     - 16-17
   * - Intlk04
     - 16-19
   * - Intlk08
     - 16-23
   * - Intlk16
     - 16-31


.. list-table::
   :header-rows: 1

   * - ``OS_Perm`` bit 16
     - ``OS_Perm`` bit 0
     - ``OS_Perm`` bit 1
     - Operation exclusion "Set" ``In01``
     - Operation exclusion "Reset" ``In01``
   * - 0
     - 0
     - 0
     - No
     - No
   * - 0
     - 0
     - 1
     - No
     - Yes
   * - 0
     - 1
     - 0
     - Yes
     - No
   * - 0
     - 1
     - 1
     - Yes
     - Yes
   * - 0
     - X
     - X
     - Yes
     - Yes
