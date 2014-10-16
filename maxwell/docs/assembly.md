# Maxwell Assembly Notes

TODO: convert links to final branch name

## Part Modifications

The BaneBots hubs are only available in Metric, the motor shafts however are
English. The 6mm bore on the hubs will need to be slightly enlarged to a 1/4"
bore.

The 20" track-style linear actuator has no feedback. Feedback has been added
by putting an optical flag on the threaded rod, providing a low resolution
encoder. The flag is 3D printed, as is the mount for the photointerrupter.

TODO: add pictures of linear actuator encoder.

# Assembling the Power Board

The first step in assembling the power board is to install 0.1" headers. Cut
off 5-pin lengths of header, removing every other pin so that there are only
3 pins. Solder the headers in:
![Power Board 1](https://raw.githubusercontent.com/mikeferguson/maxwell/doc/maxwell/docs/power_board_1.jpg)

The second step is to install the terminal blocks:
![Power Board 2](https://raw.githubusercontent.com/mikeferguson/maxwell/doc/maxwell/docs/power_board_2.jpg)

A schematic of the power board can be downloaded as a
[PDF](https://raw.githubusercontent.com/mikeferguson/maxwell/doc/maxwell/docs/powerboard.pdf).

## Wiring

The following diagram is a complete view of the wiring in Maxwell:

![Wiring Diagram](https://raw.githubusercontent.com/mikeferguson/maxwell/doc/maxwell/docs/wiring_diagram.png)

The above wiring diagram can also be downloaded as a
[PDF](https://raw.githubusercontent.com/mikeferguson/maxwell/doc/maxwell/docs/wiring.pdf).

The power switch is wired up so that in one position, it conducts from the battery
to the power board, and in the other position it will conduct from the power jack
to the power board. This allows users to plug the power supply in and then switch
to external power without turning the robot off.

![Wiring Diagram](https://raw.githubusercontent.com/mikeferguson/maxwell/doc/maxwell/docs/wiring_diagram.png)

The Etherbotix supports split power supplies for logic and motors/servos.
The power board routes 12V directly to the Etherbotix logic supply, while the
motor/servo power is passed through the runstop. The auxillary power output
on the Etherbotix (which is connected to motor/servo power) is routed to the
motor driver board which controls the base motors. The torso lift motor driver
is connected to a servo header for power.

![Power Switch](https://raw.githubusercontent.com/mikeferguson/maxwell/doc/maxwell/docs/power_switch.jpg)
