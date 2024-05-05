![alt text](../Proposal/Logo.png)

## Table of Contents
[//]: # (You need to populate these pages, they are part of your grades)
* [Proposal](../Proposal/proposal.md)
* [Justification](../Proposal/project_justification.md)
* [Home](../README.md)

# Architecture Options

Architectural decisions play a crucial role in shaping the structure, scalability, and maintainability of a game project.

Typically, projects such as yours focus on one of three different architecture options as the backbone for its architecture:
- Inheritance
- Interfaces
- Component Pattern

Each approach offers unique advantages and challenges. And while it is possible to use more than one option, based on the following analysis, we recommend that you adopt Inheritance as the foundation for your project.

## Inheritance
Inheritance is a fundamental concept in object-oriented programming (OOP) whereby a sub class is created by inheriting data fields and methods from a parent class. A good way to think about it is an apple being a sub class of fruit. An apple shares properties with other fruit but also has its own unique characteristics.

Similarly, inheritance can be utilized to create a hierarchy of game objects with shared characteristics.

#### For Example:
```
  Bird (Base Class)        |    Animal
    ↑                      |      ↑ **Inherits**
    ↑ **Inherits**         |     Bird
    ↑                      |      ↑ **Inherits**
  Pigeon (Derived Class)   |    Pigeon
```

### Reasons for Our Recommendation

#### Code Reusability
By defining common attributes in a parent class these properties and methods can be used multiple times across different sub classes. For example, applying this concept to pickups in your side-scrolling game, each pickup shares common features such as spawning and being collected. These features are inherited by specific pickup types. But these specific pickups would also have their own unique features such as awarding points in the case of a treasure pickup or restoring player health in the case of a health pickup.

#### Organised Code Structure
Inheritance promotes a structured approach to your project, making it easier to maintain and provides scalability. By providing an inheritance hierarchy, you can easily identify and understand relationships between different game objects.

The benefit to you from this approach is that it lays the code out in a manner that makes it easier to add levels, create new pickups and enemies and, of course, change the artwork.

Naturally, variables and classes will be labelled in a manner that make such amendments intuitive.

We have provided the following UML diagrams which illustrate how these classes interact and the ease with which they can be amended, or new objects created.

**Enemy Object UML**

![alt text](<UML Enemy.png>)

**Pickup Object UML**

![alt text](<UML Pickup.png>)

#### Data Hiding

The other benefit is that critical game components will be hidden. What this means is that they cannot be accidentally accessed resulting in a game that crashes.

Consequently, you can be confident that any changes you apply in making new levels or game objects are not going to cause the game to no longer run.

#### Decreased Execution Speed

One of the challenges with using inheritances is that it can take longer to execute things which can cause lag. Though this usually only occurs with poor program design. Therefore, are not of the view that this challenge outweighs the advantage inheritance offers for your particular application.

Plus, we can deal with this issue in designing your game. All game objects will be created at the beginning of the game and reused. Freeing up resources for other tasks.

## Interfaces
Interfaces are analogous to a contract for classes. They specify a set of methods that implementing classes must adopt. However, unlike inheritance, they provide no implementation. Each class must have its own code for these methods. 

Interfaces area good way to provide a common set of behaviours across multiple game objects while allowing for differences in behaviour.

### Reasons for Using Interfaces

#### Flexibility
Interfaces provide the freedom to define behaviours independently of class hierarchies, providing greater flexibility when creating game systems.

While this certainly would allow you the freedom to create further objects and levels it would require you to write the code for each new object. Making implementation more difficult than if you went with inheritance.

#### Loose Coupling
Interfaces by nature promote loose coupling between components, improving modularity and maintainability of your project. By programming interfaces instead of concrete classes, you can easily swap out or extended functionality without impacting other parts of the system.

As mentioned previously, the downside of this is that it requires more code to be written.

## Component Pattern
The component pattern advocates building complex objects by composing them into smaller & reusable components.

#### For Example
```
 Player Object
    /      \              
Movement  Input 
```
Rather than having everything within the player object, this architecture breaks the player object into smaller components. It is implemented by attaching a movement & input script to the player game object.

### Reasons for Using Component Pattern

#### Modularity
The component pattern encourages a modular approach to game development, where each component encapsulates a specific functionality (See above diagram).

#### Dynamic Composition
The component pattern allows for dynamic composition of game objects at runtime. This enables developers to create customizable systems, where components can be added, removed, or replaced to achieve different behaviours.

We will adopt this type of architecture for things like player movement. Note: This will not impact on your ability to easily add new objects and levels using inheritance.

