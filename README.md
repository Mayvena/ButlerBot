# ButlerBot

## Goals

This project aims to create a home helper robot. Initial goals for this robot's capabilities include:

1. Ability to navigate freely around the home
2. Ability to handle terrain obstacles, such as stairs, doorsteps, various types of flooring/rugs/carpets
3. Ability to dynamically maintain balance in case of collisions with pets or humans
4. Ability to recognise objects
5. Ability to handle objects - a set of at least two manipulators
6. Ability to transport objects while balancing them - for example a plate of soup without spilling

## Design considerations

In order to achieve _Goal 2_, the robot will need to be able to traverse verious obstacles, all while maintaining its stability (_Goal 6_). For this purpose the current design includes a roughly cylindrical chassis similar in size and shape to that of a Roomba. However unlike the said Roomba, ButlerBot will feature 4 spider-like legs, which will allow it to walk over and step on all kinds of stairs, doorsteps or items, misplaced on the floor. In addition to that, to ensure smooth movement, each leg will feature a "foot" that will have 4 separate, individually pivoted tank tracks. When no obstacles are detected, ButlerBot will use these tracks to roll smoothly, and raise its legs when needed to tackle an obstacle larger than the capabilities of the tracks. Generally the tracks should be able to handle a transition between smooth floor and a thick carpet. 

_Goal 1_ will likely require various sensors. Likely there will be a LiDAR underneath the chassis, combined with a set of two ultrasonic sensors in the front and back of every foot that would allow detection of obstacles larger than the threads' capacity. The navigation algorithm will be handled by the software devised in the ___NavBot___ sister project. 

To achieve _Goal 3_ each joint will need to be equipped with an encoder that would return the exact position of the joint in any given moment, and the power consumption of each servo will be measured in real time and cross-referenced with the appendage position. This will allow thhe bot to know if there's excessive strain on one of the joints and compensate accordingly. 

_Goal 4_ will require a machine learning algorithm that would allow the ButlerBot to memorize and recognize various objects it would need to interact with.

The body will be a tall cylinder that will be able to rotate on top of the chassis. In the top end there will be a set of two arms with interchangeable manipulators. On top of the body there will be a head with a camera and two microphones that would allow the ButlerBot to determine the direction of sounds. The "face" of the ButlerBot will be a 7-inch display that will display a stylized face image. The entire head assembly will be mounted on a 2 DOF mount to allow the ButlerBot to rotate and tilt forward and back its head in order to take a better look at objects it has hard time recognising. To keep the center of mass low (thus increasing the static stability of the ButlerBot) while helping with cooling, the RaspberryPi that would handle the local processing and the communication with the actual "brain" in the docking station will likely be housed in the head or the upper back, while allowing the lower part of the ButlerBot's torso to be reserved for the heavier batteries and motors. This will also allow easier access to the RaspberryPi's memory card and USB ports.

To achieve _Goal 6_ the ButlerBot will feature a foldable "plate" in its chest. It would unfold and extend forward, so the bot is able to place the object it transports on it. It is possible to equip the plate with a set of servos that would tilt it to compensate any tilting of the body.

For user-fiendly looks, the body will feature smooth cylindrical shape, coloured in a way that would mimic a stylized image of a tuxedo with a bowtie. Arms will be coloured black with white manipulators at the end, mimicking white gloves. The head will feature a decorative stylized "top hat" and a monocle to finish the butler impression. 

For ease of interaction and movement around the home, the total height of the ButlerBot needs to be somewhere between 170 and 190 cm, its body approximately the width of a normal human torso. Its legs will have the ability to straighten which should allow the ButlerBot to reach the highest shelves and ceilings with its manipulators.
