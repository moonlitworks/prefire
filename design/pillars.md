# Pillars

### The players must feel reactive to their environment

There shouldn't be surprises in what happens to the character that is
not the result of oversight. The player should see ahead of time if
there is an incoming damage.

### Each round of battle state would roughly correspond to one second

### The player should be able to use the cards that enemies can use

### Every enemy type must have its own attack pattern

### All enemies should be defeatable by any weapon

This allows for challenges like full stealth where the player can
finish the game entirely using MOVE and SLASH cards.

### Enemy drop should correspond to their type

An enemy who uses grenades should have a high chance of dropping a
grenade, etc.

### Some world state may transfer across saves

To enforce the idea of Feryth being able to see into the future, or
rather time travelling, we will be leveraging the save and load
functionality to support that. Some states in one save file can affect
the world in another save file. For example, if in one save file, a
door was opened far into the game, the game that takes place will have
that detail until the save file is deleted. Similarly, if the player
closes said door in the current playthrough, the save files that have
it open will now have it closed. To further support this, the part
where Feryth's Eegris breaks, the save files will not be usable.

### Enemy actions must not be atomic

Aside from the influences of their attack preferences, the enemies
should move as random as possible so that each playthrough will be a
fresh challenge.