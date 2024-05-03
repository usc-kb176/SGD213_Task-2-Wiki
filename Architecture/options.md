# Architecture Options

Architectural decisions play a crucial role in shaping the structure, scalability, and maintainability of a game project.

In this section, we will explore three different architecture options...
- Inheritance
- Interfaces
- Component Pattern

Each approach offers unique advantages and considerations, ultimately influencing how game systems are designed, implemented, and extended.

## Inheritance
Inheritance is a fundamental concept in object-oriented programming (OOP) where a new class is created by inheriting properties and behaviours from an existing class. Inheritance can be utilized to create a hierarchy of game objects with shared characteristics.

#### For example:
```
  Bird (Base Class)        |    Animal
    ↑                      |      ↑ **Inherits**
    ↑ **Inherits**         |     Bird
    ↑                      |      ↑ **Inherits**
  Pigeon (Derived Class)   |    Pigeon
```

### Justification

#### Code Reusability
Inheritance allows you to define common functionalities in a base class and reuse them across multiple derived classes. For example you can have a 'weapon' base class that have common functions like `shoot()` or `reload()`. Then create specific weapon types like machine gun or sniper rifle that can inherit all the functions from the weapon base class and adjust to suit the weapon type.

#### Organised Code Structure
Inheritance promotes a structured approach to your programming project, making it easier to maintain and provides scalability. By providing a inheritance hierarchy, you can easily identify and understand relationships between different game objects.

## Interfaces
Interfaces define a contract for classes, specifying a set of methods that implementing classes must adhere to. 

#### For Example
```
public interface IHealth
{
    // Get the amount of health this health component currently has
    int CurrentHealth { get; }

    // Get the maximum health of this health component
    int MaxHealth { get; }

    void TakeDamage(int damageAmount);

    void Heal(int healingAmount);

    void Die();
}
```
If any class was to use this interface then they must have each one of the functions mentioned above or Unity will report an error. This provides a good way to ensure that objects with interfaces will all react in the same way.

### Justification

#### Flexibility
Interfaces provide the freedom to define behaviours independently of class hierarchies, providing greater flexibility when created game systems.

#### Loose Coupling
Interfaces by nature promote loose coupling between components, improving modularity and maintainability of your project. By programming interfaces instead of concrete classes, you can easily swap out or extended functionality without impacting other parts of the system.

## Component Pattern
The component pattern advocates building complex objects by composing them into smaller & reusable components.

#### For Example
```
 Player Object
    /      \              
Movement  Input 
```
Rather than having everything within the player object, break up the player object into smaller components like a movement & input script and place them onto the player.

### Justification

#### Modularity
The component pattern encourages a modular approach to game development, where each component encapsulates a specific functionality (See For Example).

#### Dynamic Composition
The component pattern allows for dynamic composition of game objects at runtime. This enables developers to create customizable systems, where components can be added, removed, or replaced to achieve different behaviours.


## Contents
[//]: # (You need to populate these pages, they are part of your grades)
* [Chosen Architecture](architecture.md)
* [Home](../README.md)