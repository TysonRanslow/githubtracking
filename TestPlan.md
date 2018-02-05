# Coffee Maker Quest Test Plan

Tyson Ranslow and John Teeslink

## Introduction
Here you can note any concerns or dfficulties you may have had or anticipate with the testing process. You could also not why you considered certain test cases, how you thought of edge cases, etc.

For our test plan...

## Test Cases
Include all the test cases. You may name or number them any way you wish, but be consistent. Use the format from the lecture or textbook, i.e. Identifier, Description, Preconditions, Input Values, Execution Steps, Output Values, Postconditions (all on separate lines).


Identifier: 1
Description: Test commands N and S for functionality while a door is available
Preconditions: Player must be in beginning room.
Input Values: N, S
Execution Steps: Type N to go through door leading north. Player will be in A Funny room. Type S to go through door leading south.
Output Values: You see a Small room.

It has a quaint sofa.

A Magenta door leads north.
Post conditions: Player should now be in a Small room.

Identifier: 2
Description: Test L functionality
Preconditions: Player must be in the beginning room
Input Values: L
Execution Steps: Type L while in beginning room.
Output Values: There might be something here...
You found some creamy cream!


You see a Small room.

It has a quaint sofa.

A Magenta door leads north.


INSTRUCTIONS (N, S, L, I, D) > 
Post conditions: Player is in beginning Room. 

Identifier: 3
Description: Enter incorrect numeric instructions
Preconditions: Player is in any room, with Instructions listed
Input Values: Any numeric key [0-9]
Execution Steps: When the player is given a list of instructions to choose from, type a numeric value.
Output Values: Program will reply "What?" and give another description of the room the player is in and available instructions.
Post conditions: Player will be in the same room.

Identifier: 4
Description: Enter incorrect letter instructions
Preconditions: Player is in any room, with Instructions listed
Input Values: Any alphabet letter key not listed on the available instructions.
Execution Steps: When the player is given a list of instructions to choose from, type a letter key not listed in the instructions.
Output Values: Program will reply "What?" and give another description of the room the player is in and available instructions.
Post conditions: Player will be in the same room.

Identifier: 5
Description: Enter capitalized letter instructions
Preconditions: Player is in beginning room.
Input Values: 'N'
Execution Steps: In beginning room, type uppercase 'N'.
Output Values: 
You see a Funny room.

It has a sad record player.

A Beige door leads north.

A Massive door leads south.

Post conditions: Player has gone through door, and is in a Funny room.

Identifier: 6
Description: Enter lowercase letter instructions
Preconditions: Player is in beginning room.
Input Values: 'n'
Execution Steps: In beginning room, type lowercase 'n'.
Output Values: 
You see a Funny room.

It has a sad record player.

A Beige door leads north.

A Massive door leads south.

Post conditions: Player has gone through door, and is in a funny room.

Identifier: 7
Description: Test N functionality while a door is available
Preconditions: Player must be in a room and a door to the north must be present.
Input Values: N 
Execution Steps: While in a room with a door to the north, press the N key. Do this until there is no door leading north. Then type N one more time to go north while no door leading north is present.
Output Values: The game will say "You see an 'x' room" and describe it after pressing N.
Post conditions: Player should now be in a different room than before after going through a door that leads north. If a door leading north is not present, the player should be in the same room.

Identifier: 8
Description: Test S functionality while a door is available
Preconditions: Player must be in beginning room.
Input Values: N, S 
Execution Steps: While in beginning room, type N to go north. The game will describe a door going south. Type S to go south. The player should be in the beginning room with no door leading south. Type S one more time to go south while no door leading south is present.
Output Values: The game will say "You see an 'x' room" and describe it after pressing S.
Post conditions: After typing S, the player should be in the beginning room. After typing S a second time the player should still be in the beginning room.

Identifier: 9
Description: Test win functionality with all items collected in order.
Preconditions: Player is in beginning room with no items collected.
Input Values: N, L, D
Execution Steps: In beginning room, type L to collect cream. Type N to go north. Type N to go north. Type L to collect coffee. Type N to go north 3 times until player is in a Rough room. Type L to collect sugar. Type D to drink coffee.
Output Values: You drink the beverage and are ready to study!

You win!

Post conditions: Program exits with error code 0.

Identifier: 10
Description: Test win functionality with all items collected out of order.
Preconditions: Player is in beginning room with no items collected.
Input Values: N, L, S, D
Execution Steps: Type N to go north. Type N to go north. Type L to collect coffee. Type N to go north 3 times until player is in a Rough room. Type L to collect sugar. Type S to go south 5 times until you are back in the Small Room. Type L to collect cream. Type D to drink coffee.
Output Values: You drink the beverage and are ready to study!

You win!

Post conditions: Program exits with error code 0.

Identifier: 11
Description: Test lose functionality with only 2 items.
Preconditions: Player is in beginning room with no items collected.
Input Values: N, L, D
Execution Steps: In beginning room, type L to collect cream. Type N to go north. Type N to go north. Type L to collect coffee. Type D to drink coffee.
Output Values: Without sugar, the coffee is too bitter.   You cannot study.
You lose!
Post conditions: Program exits with error code 1.

Identifier: 12
Description: Test lose functionality with no items
Preconditions: Player is in beginning room with no items collected.
Input Values: D
Execution Steps: Type D to drink.
Output Values: The air is invigorating, but not invigorating enough.  You cannot study.

You lose!
Post conditions: Program exits with error code 1.

Identifier: 13
Description: Test Inventory functionality with no items
Preconditions: Player should be in beginning room with no items collected.
Input Values: I
Execution Steps: Type I with no items collected.
Output Values: YOU HAVE NO COFFEE!
YOU HAVE NO CREAM!
YOU HAVE NO SUGAR!
Post conditions: Player will be in same room with no items collected.

Identifier: 14
Description: Test Inventory functionality after collecting item
Preconditions: Player should be in beginning room with no items collected.
Input Values: L, I
Execution Steps: Type L to collect cream. Type I to check inventory.
Output Values: YOU HAVE NO COFFEE!
You have some fresh cream.
YOU HAVE NO SUGAR!
Post conditions: Player will be in same room with cream collected.

Identifier: 15
Description: Test Look in a room with no collectable items.
Preconditions: Player is in beginning room.
Input Values: N, L
Execution Steps: Type N to go north. Type L to look for items
Output Values:
You don't see anything out of the ordinary.


You see a Funny room.

It has a sad record player.

A Beige door leads north.

A Massive door leads south.
Post conditions: Player is in a Funny room with no items collected.

Identifier: 16
Description: Test Look in a room with a collectable item.
Preconditions: Player is in beginning room.
Input Values: L
Execution Steps: Type L to look for items
Output Values:
There might be something here...

You found some creamy cream!


You see a Small room.

It has a quaint sofa.

A Magenta door leads north.
Post conditions: Player is in a Small room with cream collected.

Identifier: 17
Description: Test Help functionality in beginning room.
Preconditions: Player is in beginning room.
Input Values: H
Execution Steps: Type H
Output Values: Program will show a listing of possible commands and what their effects are.
Post conditions: Player is in the same room, with a help list displayed.

Identifier: 18
Description: Test Help functionality after collecting cream and moving North.
Preconditions: Player is in beginning room.
Input Values: L, N, H
Execution Steps: Type L to collect cream. Type N to move north. Type H to display help menu.
Output Values: Program will show a listing of possible commands and what their effects are.
Post conditions: Player is in the funny room, with cream collected, and help list displayed.

Identifier: 19
Description: Test Unique Room adjectives moving north.
Preconditions: Player is in beginning room.
Input Values: N
Execution Steps: Player starts out in a small room. Type N to go to a funny room. Type N to go to a Refinanced Room, type N to go to a dumb room. Type N to go to a bloodthirsty room. Type N to go to a rough room.
Output Values: While moving north, the program will describe the rooms. All the room descriptions should be different.
Post conditions: Player is in the rough room.

Identifier: 20
Description: Test Unique Room adjectives moving south
Preconditions: Player is in beginning room. Type N 5 times to go to the Rough Room
Input Values: S
Execution Steps: type S to go to the bloodthirsty room. Type S to go to the dumb room. Type S to go to the Refinanced Room. Type S to go to the Funny room. Type S to go to the small room.
Output Values: While moving south, the program will describe the rooms. All the room descriptions should be different.
Post conditions: Player is in the small room.

Identifier: 21
Description: Test unique room furnishing going north
Preconditions: Player is in the beginning room.
Input Values: N
Execution Steps: Player starts out in a small room. It has a quaint sofa. Type N to go to a funny room. It should have a sad record player. Type N to go to a Refinanced Room. It has a tight pizza. Type N to go to a dumb room. It has flat energy drink. Type N to go to a bloodthirsty room. It has a beautiful bag of money. Type N to go to a rough room. It has a perfect air hockey table.
Output Values: Program will describe the rooms and furnishing when moving room to room. The rooms and furnishing should be unique.
Post conditions: Player is in the rough room. It has a perfect air hockey table.

Identifier: 22
Description: Test Unique Room furnishing moving south
Preconditions: Player is in beginning room. Type N 5 times to go to the Rough Room
Input Values: S
Execution Steps: Player starts out in the rough room. It has a perfect air hockey table. Type S to go to the bloodthirsty room. It has a beautiful bag of money. Type S to go to the dumb room. It has a flat energy drink. Type S to go to the Refinanced Room. It has a tight pizza. Type S to go to the Funny room. It has a sad record player. Type S to go to the small room. It has a quaint sofa.
Output Values: While moving south, the program will describe the rooms. All the room descriptions should be different.
Post conditions: Player is in the small room. It has a quaint sofa.

These are the requirements for the test case:

FUN-ITERATION - At each iteration of the game, the user shall be able enter one of six commands - "N" to go North, "S" to go South, "L" to Look for items, "I" for Inventory, "H" for Help, or "D" to Drink.


FUN-UNKNOWN-COMMAND - If a player enters a command not specified by FUN-ITERATION, the system shall respond with the phrase "What?".


FUN-INPUT-CAPS - The system shall be case-insensitive in regards to input values; that is, it shall accept capital and lower-case letters and treat them as equivalent.


FUN-MOVE - The system shall allow a player to move North only if a door exists going North, and South only if a door exists going South.


FUN-WIN - The player shall win the game if and only if Coffee, Sugar, and Cream have been collected by the player and then drunk.


FUN-LOSE - The player shall lose the game if and only if the player Drinks but has not collected all of the items (Coffee, Sugar, and Cream).


FUN-INVENTORY - Upon entering "I" for inventory, the player shall be informed of the items that he/she has collected (consisting of Coffee, Sugar, and Cream).


FUN-LOOK - Upon entering "L" for Look, the player shall collect any items in the room and those items will be added to the player's inventory.


FUN-HELP - Upon entering "H" for Help, the player shall be shown a listing of possible commands and what their effects are.


FUN-UNIQ-ROOM - Each room in the house shall have a unique adjective describing it.


FUN-UNIQ-ROOM-FURNISHING - Each room in the house shall have one and only one unique furnishing visible to the user upon entering the room.


## Traceability Matrix
Include a traceability matrix which maps the test cases and their associated requirements. Remember that all requirements should map to AT LEAST ONE test case, and all test cases should map to EXACTLY ONE requirement.


FUN-ITERATION
FUN-UNKNOWN-COMMAND
FUN-INPUT-CAPS
FUN-MOVE
FUN-WIN
FUN-LOSE
FUN-INVENTORY
FUN-LOOK
FUN-HELP
FUN-UNIQ-ROOM
FUN-UNIQ-ROOM-FURNISHING

## Defects Found
List at least three defects found. The defects should follow the following defect reporting style: Identifier, Description, Reproduction Steps, Expected Behavior, Observed Behavior (all on separate lines).


Going all the way north and it will loop threw and going south it will keep saying that you are in a magical land. 

n doesnt work with all of the other lower case letters. 


Defect 1: Lower case n

Indentifier: FUN-INPUT-CAPS

Description: If you try to go north using a lower case 'n', you will not 

Reproduction Steps: 

Expected Behavior:

Observed Behavior:

Defect 2: There is no H option.

Indentifier: FUN-HELP

Description:

Reproduction Steps:

Expected Behavior:

Observed Behavior:

Defect 3: Maigcal Land?

Indentifier:

Description:

Reproduction Steps:

Expected Behavior:

Observed Behavior:

