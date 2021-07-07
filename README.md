# ButlerBot

## Goals

This project aims to create a home helper robot. Initial goals for this robot's capabilities include:

1. Ability to navigate freely around the home
2. Ability to handle terrain obstacles, such as stairs, doorsteps, various types of flooring/rugs/carpets
3. Ability to dynamically maintain balance in case of collisions
4. Ability to recognise objects
5. Ability to handle objects - a set of at least two manipulators
6. Ability to transport objects while balancing them - for example a plate of soup without spilling

## Design considerations

In order to achieve _Goal 2_, the robot will need to be able to traverse verious obstacles, all while maintaining its stability (_Goal 6_). For this purpose the current design includes a roughly cylindrical chassis similar in size and shape to that of a Roomba. However unlike the said Roomba, ButlerBot will feature 4 spider-like legs, which will allow it to walk over and step on all kinds of stairs, doorsteps or items, misplaced on the floor. In addition to that, to ensure smooth movement, each leg will feature a "foot" that will have 4 separate, individually pivoted tank tracks. When no obstacles are detected, ButlerBot will use these tracks to roll smoothly, and raise its legs when needed to tackle an obstacle larger than the capabilities of the tracks. Generally the tracks should be able to handle a transition between smooth floor and a thick carpet. 

The body will be a tall cylinder that will be able to rotate on top of the chassis. In the top end there will be a set of two arms with interchangeable manipulators. On top of the body there will be a head with a camera and two microphones that would allow the ButlerBot to determine the direction of sounds. The "face" of the ButlerBot will be a 7-inch display that will display a stylized face image. The entire head assembly will be mounted on a 2 DOF mount to allow the ButlerBot to rotate and tilt forward and back its head in order to take a better look at objects it has hard time recognising.

For user-fiendly looks, the body will feature smooth cylindrical shape, coloured in a way that would mimic a stylized image of a tuxedo with a bowtie. Arms will be coloured black with white manipulators at the end, mimicking white gloves. The head will feature a decorative stylized "top hat" and a monocle to finish the butler impression. 
