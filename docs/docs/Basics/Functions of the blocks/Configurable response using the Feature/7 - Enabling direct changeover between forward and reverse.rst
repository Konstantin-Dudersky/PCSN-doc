7 - Enabling direct changeover between forward and reverse
==========================================================

Feature bit
-----------
Number of the ``Feature`` bit: 7


Direct changeover between forward and reverse
---------------------------------------------

With this ``Feature`` bit, you can enable direct reversal of the direction of motors.

The default setting is 0.

- **Bit = 0**: Direct reversal of the direction is disabled.

  You can only change the direction of the motor by first stopping and starting the motor again in the required direction. The motor can only be started again after the time set in the IdleTime parameter has elapsed.

- **Bit = 1**: Direct changeover is enabled.

  You can reverse the motor direction directly. The motor block reverses the direction automatically. The motor is stopped and is started in the other direction when the time set in the IdleTime parameter has elapsed.
