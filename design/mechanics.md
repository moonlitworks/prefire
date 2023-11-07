# Mechanics


## Initialize

Character starts with a knife and pistol equipped; a deck of cards
containing STEP, KNIFE, and 12 BULLETs; 3 Insight, 3 Mobility, and 3
Reactivity.

Each battle round, a certain number of cards will be drawn from the
player's deck. This number is based on their Reactivity stats which
starts at 3. The player can choose a certain number of action cards
from these drawn cards. This number is based on their Mobility stats
which starts at 3. The player will also see a certain number of
enemies' action cards per enemy. This number is based on their Insight
which starts at 3.

The goal is for the player to kill all the enemies within the map while
avoiding getting hit by their attacks. Beginning enemies will choose
3 action cards each round.

When an enemy dies, they can drop the weapon they are using, a random
card or a random stat increase.

## Prototype

The map will be a flat-top hexagonal grid with a radius of 6. The
player and 6 enemies will be randomly placed in cells without overlap
and start the first round. A new round will start until all enemies are
defeated.


## Card Effects

### STEP

STEP card is an infinite card. This allows the player to take three
steps. The player will choose three consecutive neighboring cells as
the target action.

### SLASH

SLASH card is an infinite card and only usable when the player has a
knife equipped. The player will choose a neighboring cell to attack.

### BULLET

BULLET card is a finite card and only usable when the player has a
pistol or rifle equipped. The player will choose a neighboring cell to
attack as a direction with an infinite range until it hits something.

### GRENADE

GRENADE card is a finite card. The player will choose any cell within
the range of 3. It will damage fully at its cell and neighboring cell
with a range of 1.

### SCOPE

SCOPE card is a finite card and only usable when the player has a rifle
equipped. The player will choose any cell within the entire map and
will fully damage at its cell.


## Undoing Action Cards

Chosen cards can be undone from the last selected only. That means if
the player wishes to change their first card, they will have to undo
all their selected cards. This is to prevent lingering invalid actions.


## Stats

## Reactivity

Min: 1
Max: 10

This dictates the number of cards drawn from the player's deck each
round. Player starts with 3.

### Mobility

Min: 1
Max: 10

This dictates the number of action cards that the player can choose
each round. Player starts with 3.

### Insight

Min: 0
Max: 10

This dictates the number of enemy action cards the player can see each
round per enemy. Player starts with 3. This also serves as the player's
HP. Each time the player gets hit, this stat decreases. When this is at
0, the player gets a debuff in their card effects and will die the next
time they get hit.