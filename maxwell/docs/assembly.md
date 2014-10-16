# Maxwell Assembly Notes

## Part Modifications

The BaneBots hubs are only available in Metric, the motor shafts however are
English. The 6mm bore on the hubs will need to be slightly enlarged to a 1/4"
bore.

The 20" track-style linear actuator has no feedback. Feedback has been added
by putting an optical flag on the threaded rod, providing a low resolution
encoder. The flag is 3D printed, as is the mount for the photointerrupter.

## Wiring

The power switch is wired up so that in one position, it conducts from the battery
to the power board, and in the other position it will conduct from the power jack
to the power board. This allows users to plug the power supply in and then switch
to external power without turning the robot off.

The Etherbotix supports split power supplies for logic and motors/servos.
The power board routes 12V directly to the Etherbotix logic supply, while the
motor/servo power is passed through the runstop. The auxillary power output
on the Etherbotix (which is connected to motor/servo power) is routed to the
motor driver board which controls the base motors. The torso lift motor driver
is connected to a servo header for power.

# Attaching


# Assembling the Power Board

TODO: convert links to final branch name
![Power Board 1](https://raw.github.com/mikeferguson/maxwell/doc/maxwell/doc/power_board_1.jpg)
![Power Board 2](https://raw.github.com/mikeferguson/maxwell/doc/maxwell/doc/power_board_2.jpg)

