

#### A side note
This is not the same type of 'AI' that is getting more popular today. It can't write essays for you, and is not a neural network. It's much more dumb than that. Anyways, onto explaining everything


## Enemy Sight

Every AI will have a predetermined sight and field of view, which will detect if the player enters it's sight. Once the player is in sight, It will trigger the Enemy Navigation script or the Enemy Attack script, depending on how far away the player is. The sight will behave like human eyes; it won't be able to see behind itself.
## Enemy Navigation

While the player is not in sight, there will be an option in the script for it to walk around (Or "Patrol") certain predetermined points on the map. When the player is in sight however, it will break the patrol cycle and navigate towards the player. If the player goes out of sight of the AI, it will go to the last point it did see the player and look for them again. If the player is nowhere to be seen again, it will wait around for a few seconds before resuming the patrol phase. However, if the AI manages to get close enough to the player, It will begin to attack them as well as navigate towards them.
## Enemy Attack

When the player is in sight and is in range of attack, the enemy attack script will fire either a Raycast (an invisible line that detects collisions) or a Sphere cast (An invisible sphere that detects collisions) towards the player. This will most likely always hit the player, so I will add on some randomness to the shot so the AI has a chance to miss the player (like a D20 roll). The enemy will be able to continue to move whilst attacking, and will stop once the player goes out of range and goes back to the follow phase in Enemy Navigation.

## Enemy Health

A basic script that stores a value that represents the health of the enemy (can be any positive number). The script includes functions to make the enemy take damage of a fixed or random amount, and destroys the Enemy when its health reaches zero. 