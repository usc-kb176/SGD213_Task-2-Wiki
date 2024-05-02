# Road Runner Escape 

## The Game

Road Runner Escape is a side-scroller with multiple levels based on Super Mario. We believe there is a nostalgia market for such games and our aim is to improve this much-loved classic through the introduction of eye-catching graphics and progressively more difficult levels. 

The player character ("**Road Runner**") moves in jump'n'run style as it navigates each level. Collecting power-ups, defeating enemies [and solving problems] along the way.

Each level consists of a platform, hills and interactive elements such as pickups. To make it more challenging randomly generated enemies will appear which Road Runner will either evade or destroy.

Destruction of an enemy is achieved by landing on top of it.

There will be several pickups, [sometimes hidden in destructible
boxes], which will either award points or restore the player character's health.

A level will be comlpeted when a player has accumulated a certain number of points [or completed a number of tasks or a certain time?].

## Specifications
Software | Purpose
---|---
Unity2D | Main tool, this will be used as the game engine
Internet Commons | This will be the source of  placeholder character art
Visual Studio Code | Scriting in C#
Future Development | Music and audio effects


## Gameplay

The gameplay is movement based side-scroller style. The player controls Road Runner. 

Road Runner starts with three health units. An appropriate graphic will be chosen to represent these. Health units will be deducted on contact with an enemy or similar hazard.  

At this stage of development the game will feature one level. However, additional levels can easily be created by changing the level of difficulty. By increasing the rate enemy objects are spawned, for example.

The game will have the flexibility to allow enemy objects to take damage. Though that feature may be reserved for more difficult levels.

The goal is for the player objects to accumulate points. This can be achieved by collectiing pickups or destroying enemy objects by landing on them. Some pickups will  enable a player to restore health.

### Game Progression



### Objectives

### Play Flow

## Mechanics

### Physics - How Does the Physical Universe Relate

### Movement in the Game

Road Runner will start facing to the right. 

Movement will be handled by a player input script which, on receiving input from the keyboard, will trigger forces in a player movement script.

Horizontal movement will be implemented by applying force to the horizontal vector. Negative numbers will send Road Runner to the laft and positive numbers will send it to the right.

Road Runner will be allowed to drift when there is no input from the player. This will allow greater control when attempting to land at specific point, perhaps to collect a pickup.

Horizontal movement will have a walk and a run speed. 

Vertical movement will be handled by applying force to the vertical vector. Force will only be applied in an upwards direction. With Unity's physics engine controlling Road Runner's descent.

When jumping, Road Runner will only be able to initiate this while on the ground. Jump height will be controlled by repeatedly hitting the control command. A maximum will be placed on the number of times a player can use the jump command to increase height. This cap will be reset once Road Runner is back on the ground.

A cool down period will be implemented whereby Road Runner will not return to its full abilities during this time. Pickups can be collected which reduce this cool down.

For example, three uses of the jump command will send Road Runner three times as high as one press (though testing may necessiate introducing diminishing returns per key press). Notwithstanding, a fourth key press will gain no additional height.

Naturally, the aboce example is subject to review during development.

### Actions

Road Runner will be controlled through the keyboard. 

Moving left or right will be through the arrow keys. The default speed will be walking.

This will increase to run speed when the left control key is held down at the same time as an arrow key. Note: development testing will reveal the optimal incremental speed to be applied to running.

The space bar will be used to get the Road Runner to jump. As indicated, the more presses the higher it will jump.

### Enemies

These will initiated and stored in an array at the beginning of the game.

At specific time intervals a random enemy object will be spawned. 

We anticpate having three different enemy objects at this stage of development:

* A boulder that is rolled down the hill by a coyote. Road Runner can evade or destroy this object. 
* A stationary coyote that can be destroyed by landing on it.
* A moving coyote on a rocket which can be either evaded or destroyed.

### Pickups

These will be intiated and stored in a separate array at the beginning of the game.

At specific intervals a random pickup will be spawned.

We anticpate having three different pickup objects at this stage of development.

* A basic tresure object that awards a number of points.
* A super trasure object that awards a greater number of points.
* A health pickup that restores lost player health. Up to the maximum health available.
* Reduce jump restoration cool down time.

### Collisions

Road Runner will have a ground check and a celing check. At this stage of development it is anticipated that these will be created as child objects of the player object. 

These will be used to detect collisions above or below Road Runner. These collisions will not cause damage to Road Runner. The ground check will be used as the trigger to destroy an enemy or collect a pickup.

During development, if Unity's ray or box colliders prove to be a better approach method may be implemented instead.

When landing on an enemy or a pickup, the memory object will not be destroyed. Instead it will be deactivated and remain in the array for future use.

Collisions will be handled by Unity's Collider2D. Enemies will appear in a black list.

If the parent object, and not the child comes into contact with an enemy object theRoad Runner will lose a certain number of health points. The points lost will vary according tot he type of enemy object.


### Scoring

A score field will appear on the screen. This will be updated as a player earns points from collecting a pickup or destryoing an enemy.

Differnt points will be awarded according to the level of the enemy or the pickup.

### Screen Flow

Once Road Runner arrives at, or near, the middle of the screen the side-scroller will be activated. It will deactive when Road Runner moves to the left.

## Game Options

A player will be able to save and load games.

## Levels

As mentioned, no additional levels will be provided at this stage of development. However, the game will be flexible enough to easily add these.

To facilitate this Serialised Fields (a feature in Unity) will be implemented. This will allow parameters to be easily changed to adjust difficulty levels.

## Interface

### Visual System

## Artificial Intelligence

### Opponent and Enemy AI

## Game Art

This stage of game development operates on the understanding that game artwork will be provided by a third party. We will develop with our own placeholder artwork that can easliy be swapped out.

Attached below is a simple sketch of the game.

[Insert image here].