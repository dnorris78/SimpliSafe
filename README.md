# SimpliSafe
This is a modification of the original SmartThings device handler for SimpliSafe
 *  Original Copyright 2015 Felix Gorodishter
 *  Modifications by Scott Silence
 *	Modifications by Toby Harris - 2/10/2018
 *  Modifications by David A. Norris 9/8/2018

I have made a few changes to the device handler that I will share with the group.  I have only tested with SS3 as I do not own SS2 any longer

1) For SS3 the states reported from the SS API are in upper case.  I changed the attributeState in the tiles to reflect want the API is sending
2) Added code in the setState method where alState == "away" - Immediately refreshes the away pending state and obtains the exitDelay value
3) In the poll method, I added code to display the exitDelay value
4) Work in progress - going to display nest ambient temperature if a user has nest integration enabled.
