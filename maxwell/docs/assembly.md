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

The power jack is located directly below the power switch, while the charge plug
is located on the other side of the robot. The image below shows how the switch
is wired:

![Power Switch](https://raw.githubusercontent.com/mikeferguson/maxwell/doc/maxwell/docs/power_switch.jpg)

Most of the wiring can be installed while only the base is assembled. When the
panel of the base is flipped down, it will look something like:

![Wiring Diagram](https://raw.githubusercontent.com/mikeferguson/maxwell/doc/maxwell/docs/wiring_view.jpg)

In this picture, the power board is on the left, the Etherbotix with motor
driver is in the center, and the torso lift motor driver is on the right.
The power cables coming from the power switch in the back of the robot are
wired into the 2-pin black header on the power board.

The Etherbotix supports split power supplies for logic and motors/servos.
A single ground wire runs from the power board to the Etherbotix.
The power board routes 12V directly to the Etherbotix logic supply, while the
motor/servo power is passed through the runstop. The auxillary power output
on the Etherbotix (which is connected to motor/servo power) is routed to the
motor driver board which controls the base motors. The torso lift motor driver
is connected to a servo header for power.

In the image above, the 19V power cable is not installed in the 2-pin orange
terminal block on the power board.

In this configuration, measured currents include:

 * Servo Current - measures the current used by all servos, as well as the
   torso lift.
 * Auxilary Current - measures the current used by the base motors.

## Assembly

The mobile base is constructed of several lasercut ABS panels, held together
with 4-40 screws and right angle brackets (Digikey 621K-ND). Note that the
brackets are not symmetrical, check that they are installed correctly (the
holes in the laser cut components are made asymmetrical to match the bracket
installation direction). 1/4" long screws are used everywhere except for holding
the top down, where we use 3/8" long screws.
 
![Base Top View](https://raw.githubusercontent.com/mikeferguson/maxwell/doc/maxwell/docs/top_view.jpg)

The "upright holder" piece is used as a retaining socket for the 8020 upright.
This piece is bolted to the bottom of the base using 1/2" long 4-40 screws.

The caster is attached to the top plate of the base using 1/4-20 standoffs,
and pan head bolts (these are actually extras from the bag of 8020 components,
but have a large head and the black finish matches the ABS).

TODO: assembling the torso lift

TODO: assembling the arm

TODO: assembling the neck and head

## ASUS Xtion Configuration

Depending on the age of the ASUS Xtion and the computer you are using, you may have
to update the firmware on the Xtion. To test the Xtion, do the following:

    sudo apt-get install ros-indigo-openni2-launch
    (plug in the xtion now -- or reboot if already plugged in so that
     udev rules are definately up to date)
    roslaunch openni2_launch openni2.launch

If you see something like the following, there is probably an issue:

```
[ INFO] [1413707372.756294067]: No matching device found.... waiting for devices. Reason: openni2_wrapper::OpenNI2Device::OpenNI2Device(const string&) @ /tmp/buildd/ros-indigo-openni2-camera-0.2.1-0trusty-20140921-1358/src/openni2_device.cpp @ 74 : Initialize failed
	Could not open "1d27/0601@2/11": USB transfer timeout!
```

Next, check the dmesg for these lines:

```
[   42.301532] usb 2-2: new high-speed USB device number 6 using xhci_hcd
[   42.321448] usb 2-2: New USB device found, idVendor=1d27, idProduct=0600
[   42.321453] usb 2-2: New USB device strings: Mfr=2, Product=1, SerialNumber=0
[   42.321455] usb 2-2: Product: PrimeSense Device
[   42.321457] usb 2-2: Manufacturer: PrimeSense
[   42.321767] usb 2-2: Not enough bandwidth for new device state.
[   42.321775] usb 2-2: can't set config #1, error -28
```

If you see the "can't set config #1, error -28" line, you almost certainly need
to update the firmware. To do this, you will need a Windows machine. Install
the [Openni2 SDK](http://structure.io/openni) and then grab the updated
[firmware from ASUS](http://www.asus.com/Multimedia/Xtion_PRO_LIVE/HelpDesk_Download/).
Extract the firmware update, and run the program as administrator. After the
update, you should notice that idProduct will now be 0601.
