# Justification
[//]: # (This section is an example of justifying your design and development decisions.)

## Overview

### Brief
[//]: # (What was the client's brief?)
Hello! I’m looking for a simple 2D/3D sidescroller platformer game (2D sprites or 3D models - Must be sidescrolling). I want to focus on the art and I’m not so good with programming. I would need the game to be laid out in a way I could make levels, and enemies, control a player, and create pickups. 

I would like the player to be able to walk, run, jump, and be damaged. This would be very similar to the old-school Mario games! However, I want to put my art spin on it.


### Communication
* When do you need this prototype by?
> I need the prototype by Friday Week 13.

* What kind of games do you think are good?
> Platform games appear to be simple enough to develop and can move reasonable units if done well.

* Since you only need a prototype, are you happy for us to focus on gameplay and use based geometry for art assets?
> Yes perfect, the prototype is a proof of concept, please don't waste time on creating art assets; if the game is fun with simple art assets, that is perfect. At least change the colour palette to be aesthetically pleasing though.

* Do you need a menu system?
> Well since I want you to make a proof of concept to show investors, I currently do not need a menu system but keep it in the back of your mind so we can add it futher down the line.

* Are there any themes you think are popular or you would like to see in your game?
> Hmm... not really. I do like Looney Tunes though! I think silly games catch people's eyes?

---

## Project Understanding

### Requirements
[//]: # (What are the requirements of the finished project?)
* Delivery within 5 weeks.
* Implementation of 2D platformer mechanics.
* Player actions: walking, running, jumping, and taking damage.
* Resemblance to classic Mario games.
* Ability for the client to create levels.

### Expectations
[//]: # (What are the client's expectations?)
* Timely delivery.
* Regular progress updates.
* Transparent project management and communication.
* No requirement for audio or high-quality art assets.

### Assumptions
[//]: # (What are you assuming based on client responses)
* Basic Unity UI sprites for UI art.
* Focus on gameplay functionality over complex features.
* Limited scope with only one level for initial demonstration.
* Accessibility for the client to incorporate their own art assets.

---
## Risks

### Risks
[//]: # (What are the risks of this project)
* Imperfections in Unity and C#.
* Communication challenges within remote teams.
* Potential technical issues such as computer malfunctions or GitHub problems.

### Risk Management
[//]: # (How are you managing the mentioned risks)
* Designing code with extensibility in mind.
* Implementing thorough testing throughout development.
* Using source control we will ensure our code is safe and usable at all times
* Maintaining constant communication within the team and addressing any issues promptly.

---

## Constraints

### Constraints
[//]: # (What are the constraints of this project)
* Tight timeframe necessitates quick decision-making.
* Remote team dynamics may impact response times.
* Specific Unity version compatibility must be ensured.

---

## Justification
Given the client's preferences for simplicity, market appeal, and Looney Tunes-inspired whimsy, we've proposed "Road Runner's Escape" as the game concept. This title encapsulates the fast-paced platforming action reminiscent of classic Mario games, while also appealing to the client's affinity for Looney Tunes characters. The concept allows for a straightforward yet engaging gameplay experience, aligning with the project's objectives and constraints.

The client, having little experience with writing code, needs a game design that allows new game objects and levels to be easily created or modified. For this reason our game architecture will rely heavily on inheritance. 

This way the more complex and critical code can be hidden in the parent class where it cannot be amended by mistake. The child classes will have intuitively named variables which the client can access in Unity to change attributes of enemies and pickups. This design will also allow the client to easily swap out artwork and best fits client expectations.

## Contents
[//]: # (You need to populate these pages, they are part of your grades)
* [Architectural Options](../Architecture/options.md)
* [Architecture Index](../Architecture/index.md)
* [Chosen Architecture](../Architecture/architecture.md)
* [Home](../README.md)