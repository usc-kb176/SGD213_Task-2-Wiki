# Road Runner Escape 

## The Game

Road Runner Escape is a side-scroller with multiple levels based on Super Mario. We believe there is a nostalgia market for such games and our aim is to improve this much-loved classic through the introduction of eye-catching graphics and progressively more difficult levels. 

The player character ("**Road Runner**) moves in jump'n'run style as it navigates each level. Collecting power-ups, defeating enemies [and solving problems] along the way.

Each level consists of a platform, hills and interactive elements such as pickups. To make it more challenging randomly generated enemies will appear which the player will either avoid or destroy.

Destruction of an enemy is achieved by landing on it.

There will be several pickups, [sometimes hidden in destructible
boxes], which will either award points or restore the player character's health.

A level will be comlpeted when a player has accumulated a certain number of points [or completed a number of tasks or a certain time?].

## Specifications

    **Software**        **Purpose**

    Unity2D             Main tool, this will be used for the game engine
    Internet Commons    This will be used for placeholder character art
    Visual Studio Code  Scripting in C#
    [Future Development]Music and audio effects

## Gameplay

The gameplay is movement based side-scroller style. The player controls Road Runner. 

The player character starts with [describe life e.g., 100 points or three hearts etc.] which will reduce when coming in contact with an enemy or similar hazard. The player charcter can defeat the enemy by landing on top of it. 

At this stage of development the game will feature one level. However, additional levels can easily be created by changing the level of difficulty. By increasing the rate enemy objects are spawned, for example.

The goal is for the player objects to accumulate points. This can be achieved by collectiing pickups or destroying enemy objects. Some pickups will also enable a player to restore health.

### Game Progression



### Objectives

### Play Flow

## Mechanics

### Physics - How Does the Physical Universe Relate

### Movement in the Game

The player character will start facing to the right. 

Player movement will be handled by a player input script which, on receiving input from the player (from the keyboard), will feed that input into a player movement script.

Horizontal movement will be handled by applying force to the horizontal vector. Negative numbers will send Road Runner to the laft and positive numbers will send it to the right.

Road runner will be allowed to drift when there is no input from the player. This will allow greater control when attempting to land at specific a specific point, perhaps on a pickup.

Horizontal movement will have a walk and a run speed. With running being twice the speed of walking.

Vertical movement will be handled by applying force to the vertical vector. Force will only be applied in an upwards direction. With Unity's physics engine controlling the Road runner's descent.

When jumping, Road Runner will only be able to do this while on the ground. Jump height will be controlled by repeatedly hitting the control command. A celing will be placed on the number of times a player can use the jump command. Ceiling will be reset once Road Runner is back on the ground.

For example, three uses of the jump command will send Road Runner three times as high as one use. But a fourth use will gain no extra height.

Naturally, the aboce example is subject to review during development.

### Actions

Road Runner will be controlled through the keyboard. 

Moving left or right will be through the arrow keys. The default speed will be walking.

This will be doubled to run speed when the left control key is held down at the same time as an arrow key.

The space bar will be used to get the Road Runner to jump. The more presses the higher it will jump.

### Enemies

These will initiated and stored in an array at the beginning of the game.

At specific time intervals a random object from the array will be spawned. This could be an enemy or a pickup.

We anticpate having three different enemy objects at this stage of development:

* A boulder that is rolled down the hill by a coyote. Road Runner can only evade this object by jumping.
* A stationary coyote that can be destroyed by landinh on it.
* A moving coyote on a rocket which can be evaded or destroyed.

### Pickups

These will also be intiated and stored in the array at the beginning of the game.

At specific intervals these will be generated.

We anticpate having three different enemy objects at this stage of development.

* A basic tresure object that awards a number of points.
* A super trasure object that awards a greater number of points.
* A health pickup that restores lost player health. Up to the maximum health available.

### Collisions

Road Runner will have a ground check and a celing check. These will be created as child objects of the player objects. 

These will be used to detect collisions above or below Road runner. These collisions will not cause damage to Road Runner.

While there is no combat in the game it will be possible to destroy an enemy by landing on top of it.

Rolling boulders will not be able to be destroyed and can only be evaded.

Pickups can be collected by landing on them.

When landing on an enemy or a pickup, they will not be destroyed but be deactivted and used again.

Collisions will be handled by Unity's Collider2D. Enemies will appear in a black list.

If the parent object, and not the child comes into contact with an enemy object theRoad Runner will lose a certain number of health points. The points lost will vary according tot he type of enemy object.


### Economy

### Screen Flow

## Game Options

## Replaying

## Levels

## Interface

### Visual System

## Artificial Intelligence

### Opponent and Enemy AI

## Game Art

This stage of game development operates on the understanding that game artwork will be provided by a third party. We will develop with our own placeholder artwork that can easliy be swapped out.

You only need UML ***images*** in this section.

Justify why you chose it.

## Dummy Heading
Fill this with information.