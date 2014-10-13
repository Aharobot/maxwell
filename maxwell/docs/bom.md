# Maxwell Parts List

## Purchased Components

Qty | Description                        | Est. Cost | Notes
----|------------------------------------|-----------|-------
1   | [Drive wheels, casters, encoder cables.](http://www.zagrosrobotics.com/shop/item.aspx?itemid=529) | $309.95 | Only the motors, encoders, and casters are used. Be sure to select the 2X speed option and also add the HEDS5500 encoder cables.
2   | http://banebots.com/c/WHB-HS4-498 | $6.80 ea. | Any of the three colors will do.
2   | http://banebots.com/pc/WHB-HM-HS4-M6/T40H-SM62 | $4.50 ea. | These are 6mm and will need to be bored out to 1/4" to match motors above.
20  | Digikey P/N 621K-ND | $6 total | These are used to assemble the base.
1   | UB1280 12V 8AH SLA | $20 | Available from Amazon among others.
2   | 8020 1010x36 T Slot Aluminum Extrusion | ~$10 ea. | The 8020 Ebay store can be a good place to buy this and other 8020 components.
2   | 8020 Corner Bracket P/N 4108 | $2.75 ea. | Used to hold torso upright.
1   | 8020 Joining Strip P/N 4117 | $5 | Attaches upper and lower 8020 setions.
1   | 8020 3/8" Screws, T Nuts (25) P/N 3386 | $11.50 | (2) for corner bracket upright portion, (4) for joining plate.
1   | 8020 1/2" Screws, T Nuts (25) P/N 3321 | $12.50 | (4) for estop, 
6   | 1/4-20 x 5/8" Screw | ??? | (4) for head, (2) for base

1   | Linear actuator
2   | Actuator Mounts

5   | Ax-12
5   | MX-64T

2   | Bioloid F1 | $1.49 ea. | Used in gripper
1   | Bioloid F2
7   | Bioloid F3 | $1.49 ea. | (2) used to attach head pan servo to neck brackets, (1) used to attach pan and tilt servos, (4) used in gripper
2   | Bioloid F6 | $1.49 ea. | Used in gripper
2   | Bioloid F9 | $1.49 ea. | Used in gripper
2   | Bioloid F11 | $1.49 ea. | Used in gripper

1   | FR07-H101K | $27.90 | Hinge kit used for wrist flex
2   | HN07-I101 Idler | $14.10 | Needed for upper arm MX-64 servos
3   | FR07-S101K Side Frame | $11.90 | Used for arm pan


1   | Power switch RS 275-666
1   | 12V snap in blue bulb RS 272-335
1   | Charge inlet
1   | Power inlet

standoffs for etherbotix, power board, motor driver
estop standoff
mounting hardware for 
8020 bearings 

1   | http://www.pololu.com/product/708 | $59.95 | Motor driver plugs into Etherbotix.
1   | http://www.pololu.com/product/2468 | $19.95 | IMU, plugs into Etherbotix.
1   | http://www.pololu.com/product/705 | $27.95 | Used for torso lift.

Optional components (or use your own wiring):

1   | http://www.pololu.com/product/1700 | $12.49 | Recommended way of easily connecting torso lift motor controller to Etherbotix.
??  | Digikey A99257-ND | $0.28 ea. | Recommended for terminating wires into terminal blocks.

16ga white, black
long dynamixel wires (lenght is?)

## Custom Components

The Etherbotix is not currently available from retailers, but is entirely open source.
Cost of parts is approximately $60 plus PCB.

Similarly, the power board is not currently retailed, but is open source. It is very easy
to assemble. The PCB is less than 5x5cm, meeting the requirements for the cheapest
board options at Seeedstudio and others. Parts list for the power board is:

Qty | Description                        | Est. Cost | Notes
----|------------------------------------|-----------|-------
1   | Maxwell Power Board                | 5.00      | Bare PCB
1   | Terminal Block 2P, Orange          | 0.55      | Digikey 281-2888-ND
1   | Terminal Block 2P, Black           | 0.55      | Digikey 281-1882-ND
1   | Terminal Block 3P, Orange          | 0.77      | Digikey 281-2882-ND
1   | Terminal Block 3P, Black           | 0.77      | Digikey 281-1883-ND 
1   | (optional) 19V regulator for NUC   | $16.95    | http://www.pololu.com/product/2571

Finally, there are a number of laser cut and 3d printed components. The 3d printed
components include:

Qty | Description           | Filename or link
----|-----------------------|-------------------
1   | Upper arm bracket 1   |
1   | Upper arm bracket 2   |
1   | Head sensor mount     |
1   | Torso lift optical interrupter |

Laser cut components are split into 3 sheets, one each in 1/8", 3/16" and 1/4"
thickness, which should all be cut from ABS.

The 1/8" sheet contains:
 * 1 - Left neck side
 * 1 - Right neck side
 * 1 - Left runstop side
 * 1 - Right runstop side
 * 2 - Runstop spacer
 * 1 - Runstop mount plate
 * 2 - Forearm side panel
 * 2 - Gripper joining plate
 * 2 - Arm lift spacer

The 3/16" sheet contains:
 * 2 - Arm lift mounting plate
 * 2 - Arm lift servo mounting plate
 * 1 - Base front panel
 * 1 - Base left side
 * 1 - Base right side
 * 1 - Base rear panel

The 1/4" sheet contains:
 * 1 - Left neck spacer
 * 1 - Right neck spacer
 * 1 - Base top plate
 * 1 - Base upright holder



Todo:
 Confirm lengths on T-slot
 Screws for assembling base?

