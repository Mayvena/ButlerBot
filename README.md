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
