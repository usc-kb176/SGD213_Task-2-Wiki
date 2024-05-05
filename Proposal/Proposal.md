
![alt text](Logo.png)

## Pages
[//]: # (You need to populate these pages, they are part of your grades)
* [Architecture](../Architecture/Architecture%20Options.md)
* [Justification](../Proposal/project_justification.md)
* [Home](../README.md)

## Table of Contents
* [The Game](#the-game)
* [Specifications](#specifications)
* [Justification](#justification)
* [Gameplay](#gameplay)
  * [Game Progression](#game-progression)
* [Mechanics](#mechanics)
  * [Movement in the Game](#movement-in-the-game)
  * [Actions](#actions)
  * [Enemies](#enemies)
  * [Pickups](#pickups)
  * [Collisions](#collisions)
  * [Scoring](#scoring)
  * [Screen Flow](#screen-flow)
* [Game Options](#game-options)
* [Levels](#levels)
* [Artificial Intelligence](#artificial-intelligence)
  * [Opponent and Enemy AI](#opponent-and-enemy-ai)
* [Game Art](#game-art)
* [Anticipated Completion Schedule](#anticipated-completion-schedule)
* [Agreement](#agreement)

# Road Runner Escape 
## The Game

Road Runner Escape is a side-scroller with multiple levels based on Super Mario. We believe there is a nostalgia market for such games and our aim is to improve this much-loved classic through the introduction of eye-catching graphics and progressively more difficult levels. 

The player character ("**Road Runner**") moves in jump 'n' run style as it navigates each level. Collecting pickups and defeating enemies along the way.

Each level consists of a platform, hills, and interactive elements such as pickups. To make it more challenging randomly generated enemies will appear which Road Runner will either evade or destroy.

Destruction of an enemy is achieved by landing on top of it.

There will be several pickups, which will either award points or restore the player character's health.

A level will be completed when a player has accumulated a certain number of points. Though, should you prefer, we can include an option to complete after a certain number of task have been completed. A timer will be used to determine if these thresholds have been met in time to complete the level.

## Specifications
Software | Purpose
---|---
Unity2D | Main tool, this will be used as the game engine
Internet Commons | This will be the source of placeholder character art
Visual Studio Code | Scripting in C#
Future Development | Music and audio effects

The game architecture will rely heavily on inheritance. See discussion in [Architecture Options](<../Architecture/Architecture Options.md>)

## Gameplay

Gameplay adopts side-scroller movement style. The player controls Road Runner through the keyboard. 

Road Runner starts with three health units. An appropriate graphic will be chosen to represent these. Health units will be deducted on contact with an enemy or similar hazard. We will include an option to vary the number of starting and maximum health units according to the level. 

At this stage of development, the game will feature one level. However, additional levels can easily be created by changing the level of difficulty. By increasing the rate enemy objects are spawned, for example.

The goal is for Road Runner to accumulate points. This can be achieved by collecting pickups or destroying enemy objects by landing on them. Some pickups will enable a player to restore health or receive jump benefits.

### Game Progression

This will be achieved by completing levels of increasing difficulty. We will provide a number of ways to adjust difficulty. While no means exhaustive such tweaks will include:

* Change starting health of player.
* Change the rate pickups a re-spawned.
* Change the rate enemies are spawned.
* Allow more than one enemy to be on the screen at once.
* Introduce enemy characters of increased difficulty. Such as faster movement and more damage to player.

## Mechanics

### Movement in the Game

Road Runner will start facing to the right. 

Movement will be handled by a player input script which, on receiving input from the keyboard, will trigger forces in a player movement script.

Horizontal movement will be implemented by applying force to the horizontal vector. Negative numbers will send Road Runner to the left and positive numbers will send it to the right.

Road Runner will be allowed to drift when there is no input from the player. This will allow greater control when attempting to land at specific point, perhaps to collect a pickup.

Horizontal movement will have a walk and a run speed. 

Vertical movement will be handled by applying force to the vertical vector. Force will only be applied in an upwards direction. With Unity's physics engine controlling Road Runner's descent.

When jumping, Road Runner will only be able to initiate this while on the ground. Jump height will be controlled by repeatedly hitting the control command. A maximum will be placed on the number of times a player can use the jump command to increase height. This cap will be reset once Road Runner is back on the ground.

A cool down period will be implemented whereby Road Runner will not return to its full abilities during this time. Pickups can be collected which reduce this cool down or add jump height.

For example, three uses of the jump command will send Road Runner three times as high as one press (though testing may necessitate introducing diminishing returns per key press). Notwithstanding, a fourth key press will gain no additional height.

Naturally, the above example is subject to review during development.

### Actions

Road Runner will be controlled through the keyboard. 

Moving left or right will be through the arrow keys. The default speed will be walking.

This will increase to run speed when the left control key is held down at the same time as an arrow key. Note: development testing will reveal the optimal incremental speed to be applied to running.

The space bar will be used to get the Road Runner to jump. As indicated, the more presses the higher it will jump.

### Enemies

These will be initiated and stored in an array at the beginning of the game.

At specific time intervals a random enemy object will be spawned. 

We anticipate having three different enemy objects at this stage of development:

* A boulder that is rolled down the hill by a coyote. Road Runner can evade or destroy this object. 
* A stationary coyote that can be destroyed by landing on it.
* A moving coyote on a rocket which can be either evaded or destroyed.

### Pickups

These will be initiated and stored in a separate array at the beginning of the game.

At specific intervals a random pickup will be spawned.

We anticipate having three different pickup objects at this stage of development.

* A basic treasure object that awards a number of points.
* A super treasure object that awards a greater number of points.
* A health pickup that restores lost player health. Up to the maximum health available.
* A timed pickup that will either reduce jump restoration cool down time or increase jump height.

### Collisions

Road Runner will have a ground check and a ceiling check. At this stage of development, it is anticipated that these will be created as child objects of the player object. 

These will be used to detect collisions above or below Road Runner. These collisions will not cause damage to Road Runner. The ground check will be used as the trigger to destroy an enemy or collect a pickup.

During development, if Unity's ray or box colliders prove to be a better approach, this method may be implemented instead.

When landing on an enemy or a pickup, the game object will not be destroyed. Instead, it will be deactivated and remain in the array for future use.

Collisions will be handled by Unity's Collider2D. Enemies will appear in a black list.

If the parent object, and not the child comes into contact with an enemy object Road Runner will lose a certain number of health points. The points lost will vary according to the type of enemy object.

### Scoring

A score field will appear on the screen. This will be updated as a player earns points from collecting a pickup or destroying an enemy.

Different points will be awarded according to the level of the enemy or the pickup.

### Screen Flow

Once Road Runner arrives at, or near, the middle of the screen the side-scroller will be activated. It will deactivate when Road Runner moves to the left.

## Game Options

A player will be able to save and load games. High scores will be recorded and displayed.

## Levels

As mentioned, no additional levels will be provided at this stage of development. However, the game will be flexible enough to easily add these.

To facilitate this, Serialised Fields (a feature in Unity) will be implemented. This will allow parameters to be easily changed to adjust difficulty levels.

## Artificial Intelligence

### Opponent and Enemy AI

Enemies will be instantiated and will move in one direction. There will be the option to have enemies change direction for more difficult levels.

## Game Art

This stage of game development operates on the understanding that game artwork will be provided by a third party. We will develop with our own placeholder artwork that can easily be swapped out.

The game design will look as follows:

![alt text](<Game Layout.png>)

## Anticipated Completion Schedule

Deadline | Task
---|---
Week 10 | Moveable game character
Week 11 | Scrollable background and scenery
Week 12 | Enemies and pickups
Week 13 | Scoring, menus, loading and saving game

Naturally, we will advise if it looks like this schedule requires revision. Notwithstanding any such revision Week 13 remains a firm date for completion.

## Agreement

By accepting this proposal, you agree to enter into a contract with Roadrunner Gaming, Inc for the development of the above game. 

Such contract will be governed by our standard terms and conditions (available on our website or on request). The "Product" referred to in these terms and conditions is the game described in this document.



