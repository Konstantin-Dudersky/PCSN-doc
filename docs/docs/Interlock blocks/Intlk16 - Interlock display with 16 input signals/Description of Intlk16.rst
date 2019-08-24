Description of Intlk16
======================

Object name (type + number) and family
--------------------------------------

Type + number: FB 1827

Family: Interlck


Area of application for Intlk16
-------------------------------

The block is used for the following applications:

- Standardized interlock with display


How it works
------------

The block is used to calculate a standardized interlock that can be displayed on the OS. A maximum of 16 input signals can be supplied to the block. They are linked using selectable binary logic. The signal status of the output signal is also determined. You can assign an analog value with the signal status and unit to each input value for display in the faceplate.

The current state is displayed at the Out output parameter:

- ``Out = 0``: Interlock
- ``Out = 1``: "Good" state


Configuration
-------------

Use the CFC editor to install the block in a cyclic interrupt OB (OB30 to OB38).

For the Intlk02 (Intlk16) block, the Advanced Process Library contains templates for process tag types as examples with various application scenarios for this block.

Refer to Description of Intlk02 for more information.


Startup characteristics
-----------------------

The block does not have any startup characteristics.


Status word allocation for ``Status1`` parameter
------------------------------------------------

You can find a description for each parameter in section :doc:`Intlk16 IOs`.

.. list-table::
   :header-rows: 1
   :widths: 5 95

   * - Status bit
     - Parameter
   * - 0
     - 1 = ``Logic = OR``
   * - 1
     - 1 = ``Logic = AND``
   * - 2
     - Not used
   * - 3
     - Result of logic operation ``Out.Value``
   * - 4
     - 1 = At least one input value is excluded. See the section Excluding input values in Intlk16 functions
   * - 5
     - All input values are excluded
   * - 6
     - 1 = No input value is interconnected or ``NotUsed.Value``
   * - 7
     - Status display for simulation
   * - 8
     - Status display for not interlocked
   * - 9
     - Status display for interlocked
   * - 10
     - Not used
   * - 11
     - ``Feature`` bit 2: Separate evaluation for excluded and simulated interlock signals
   * - 12
     - Not used
   * - 13
     - Not used
   * - 14
     - Not used
   * - 15
     - Not used
   * - 16
     - Not used
   * - 17
     - Not used
   * - 18
     - Not used
   * - 19
     - Not used
   * - 20
     - Not used
   * - 21
     - Not used
   * - 22
     - Not used
   * - 23
     - Not used
   * - 24
     - Not used
   * - 25
     - Not used
   * - 26
     - Not used
   * - 27
     - Not used
   * - 28
     - Not used
   * - 29
     - Not used
   * - 30
     - Occupied
   * - 31
     - BatchEn


Status word allocation for ``Status2`` parameter
------------------------------------------------

.. list-table::
   :header-rows: 1
   :widths: 5 95

   * - Status bit
     - Parameter
   * - 0
     - ``In01.Value``
   * - 1
     - ``In02.Value``
   * - 2
     - ``In03.Value``
   * - 3
     - ``In04.Value``
   * - 4
     - ``In05.Value``
   * - 5
     - ``In06.Value``
   * - 6
     - ``In07.Value``
   * - 7
     - ``In08.Value``
   * - 8
     - ``In09.Value``
   * - 9
     - ``In10.Value``
   * - 10
     - ``In11.Value``
   * - 11
     - ``In12.Value``
   * - 12
     - ``In13.Value``
   * - 13
     - ``In14.Value``
   * - 14
     - ``In15.Value``
   * - 15
     - ``In16.Value``
   * - 16
     - Not used
   * - 17
     - Not used
   * - 18
     - Not used
   * - 19
     - Not used
   * - 20
     - Not used
   * - 21
     - Not used
   * - 22
     - Not used
   * - 23
     - Not used
   * - 24
     - Not used
   * - 25
     - Not used
   * - 26
     - Not used
   * - 27
     - Not used
   * - 28
     - Not used
   * - 29
     - Not used
   * - 30
     - Not used
   * - 31
     - Not used


Status word allocation for ``Status3`` parameter
------------------------------------------------

.. list-table::
   :header-rows: 1
   :widths: 5 95

   * - Status bit
     - Parameter
   * - 0
     - ``InvIn01``
   * - 1
     - ``InvIn02``
   * - 2
     - ``InvIn01``
   * - 3
     - ``InvIn04``
   * - 4
     - ``InvIn05``
   * - 5
     - ``InvIn06``
   * - 6
     - ``InvIn07``
   * - 7
     - ``InvIn08``
   * - 8
     - ``InvIn09``
   * - 9
     - ``InvIn10``
   * - 10
     - ``InvIn11``
   * - 11
     - ``InvIn2``
   * - 12
     - ``InvIn13``
   * - 13
     - ``InvIn14``
   * - 14
     - ``InvIn15``
   * - 15
     - ``InvIn16``
   * - 16
     - Not used
   * - 17
     - Not used
   * - 18
     - Not used
   * - 19
     - Not used
   * - 20
     - Not used
   * - 21
     - Not used
   * - 22
     - Not used
   * - 23
     - Not used
   * - 24
     - Not used
   * - 25
     - Not used
   * - 26
     - Not used
   * - 27
     - Not used
   * - 28
     - Not used
   * - 29
     - Not used
   * - 30
     - Not used
   * - 31
     - Not used


Status word allocation for ``Status4`` parameter
------------------------------------------------

.. list-table::
   :header-rows: 1
   :widths: 5 95

   * - Status bit
     - Parameter
   * - 0
     - ``In01`` with inversion
   * - 1
     - ``In02`` with inversion
   * - 2
     - ``In03`` with inversion
   * - 3
     - ``In04`` with inversion
   * - 4
     - ``In05`` with inversion
   * - 5
     - ``In06`` with inversion
   * - 6
     - ``In07`` with inversion
   * - 7
     - ``In08`` with inversion
   * - 8
     - ``In09`` with inversion
   * - 9
     - ``In10`` with inversion
   * - 10
     - ``In11`` with inversion
   * - 11
     - ``In12`` with inversion
   * - 12
     - ``In13`` with inversion
   * - 13
     - ``In14`` with inversion
   * - 14
     - ``In15`` with inversion
   * - 15
     - ``In16`` with inversion
   * - 16
     - Bypass ``In01`` (via interconnection)
   * - 17
     - Bypass ``In02`` (via interconnection)
   * - 18
     - Bypass ``In03`` (via interconnection)
   * - 19
     - Bypass ``In04`` (via interconnection)
   * - 20
     - Bypass ``In05`` (via interconnection)
   * - 21
     - Bypass ``In06`` (via interconnection)
   * - 22
     - Bypass ``In07`` (via interconnection)
   * - 23
     - Bypass ``In08`` (via interconnection)
   * - 24
     - Bypass ``In09`` (via interconnection)
   * - 25
     - Bypass ``In10`` (via interconnection)
   * - 26
     - Bypass ``In11`` (via interconnection)
   * - 27
     - Bypass ``In12`` (via interconnection)
   * - 28
     - Bypass ``In13`` (via interconnection)
   * - 29
     - Bypass ``In14`` (via interconnection)
   * - 30
     - Bypass ``In15`` (via interconnection)
   * - 31
     - Bypass ``In16`` (via interconnection)


Status word allocation for ``Status5`` parameter
------------------------------------------------

.. list-table::
   :header-rows: 1
   :widths: 5 95

   * - Status bit
     - Parameter
   * - 0
     - ``BypIn01``
   * - 1
     - ``BypIn02``
   * - 2
     - ``BypIn03``
   * - 3
     - ``BypIn04``
   * - 4
     - ``BypIn05``
   * - 5
     - ``BypIn06``
   * - 6
     - ``BypIn07``
   * - 7
     - ``BypIn08``
   * - 8
     - ``BypIn09``
   * - 9
     - ``BypIn10``
   * - 10
     - ``BypIn11``
   * - 11
     - ``BypIn12``
   * - 12
     - ``BypIn13``
   * - 13
     - ``BypIn14``
   * - 14
     - ``BypIn15``
   * - 15
     - ``BypIn16``
   * - 16
     - ``In01`` hidden bypass information
   * - 17
     - ``In02`` hidden bypass information
   * - 18
     - ``In03`` hidden bypass information
   * - 19
     - ``In04`` hidden bypass information
   * - 20
     - ``In05`` hidden bypass information
   * - 21
     - ``In06`` hidden bypass information
   * - 22
     - ``In07`` hidden bypass information
   * - 23
     - ``In08`` hidden bypass information
   * - 24
     - ``In09`` hidden bypass information
   * - 25
     - ``In10`` hidden bypass information
   * - 26
     - ``In11`` hidden bypass information
   * - 27
     - ``In12`` hidden bypass information
   * - 28
     - ``In13`` hidden bypass information
   * - 29
     - ``In14`` hidden bypass information
   * - 30
     - ``In15`` hidden bypass information
   * - 31
     - ``In16`` hidden bypass information


Status word allocation for ``Status6`` parameter
------------------------------------------------

.. list-table::
   :header-rows: 1
   :widths: 5 95

   * - Status bit
     - Parameter
   * - 0
     - ``In01`` not connected
   * - 1
     - ``In02`` not connected
   * - 2
     - ``In03`` not connected
   * - 3
     - ``In04`` not connected
   * - 4
     - ``In05`` not connected
   * - 5
     - ``In06`` not connected
   * - 6
     - ``In07`` not connected
   * - 7
     - ``In08`` not connected
   * - 8
     - ``In09`` not connected
   * - 9
     - ``In10`` not connected
   * - 10
     - ``In11`` not connected
   * - 11
     - ``In12`` not connected
   * - 12
     - ``In13`` not connected
   * - 13
     - ``In14`` not connected
   * - 14
     - ``In15`` not connected
   * - 15
     - ``In16`` not connected
   * - 16
     - Not used
   * - 17
     - Not used
   * - 18
     - Not used
   * - 19
     - Not used
   * - 20
     - Not used
   * - 21
     - Not used
   * - 22
     - Not used
   * - 23
     - Not used
   * - 24
     - Not used
   * - 25
     - Not used
   * - 26
     - Not used
   * - 27
     - Not used
   * - 28
     - Not used
   * - 29
     - Not used
   * - 30
     - Not used
   * - 31
     - Not used


Status word allocation for ``Status7`` parameter
------------------------------------------------

.. list-table::
   :header-rows: 1
   :widths: 5 95

   * - Status bit
     - Parameter
   * - 0
     - ``AV01`` not connected
   * - 1
     - ``AV02`` not connected
   * - 2
     - ``AV03`` not connected
   * - 3
     - ``AV04`` not connected
   * - 4
     - ``AV05`` not connected
   * - 5
     - ``AV06`` not connected
   * - 6
     - ``AV07`` not connected
   * - 7
     - ``AV08`` not connected
   * - 8
     - ``AV09`` not connected
   * - 9
     - ``AV10`` not connected
   * - 10
     - ``AV11`` not connected
   * - 11
     - ``AV12`` not connected
   * - 12
     - ``AV13`` not connected
   * - 13
     - ``AV14`` not connected
   * - 14
     - ``AV15`` not connected
   * - 15
     - ``AV16`` not connected
   * - 16
     - Not used
   * - 17
     - Not used
   * - 18
     - Not used
   * - 19
     - Not used
   * - 20
     - Not used
   * - 21
     - Not used
   * - 22
     - Not used
   * - 23
     - Not used
   * - 24
     - Not used
   * - 25
     - Not used
   * - 26
     - Not used
   * - 27
     - Not used
   * - 28
     - Not used
   * - 29
     - Not used
   * - 30
     - Not used
   * - 31
     - Not used


Status word allocation for ``Status8`` parameter
------------------------------------------------

Identical to ``FirstIn``.
