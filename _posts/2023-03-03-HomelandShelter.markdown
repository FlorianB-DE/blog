---
layout: post
title: Homeland Shelter – A Java Roguelike from Scratch
date: 2023-03-03
tags:
  - gamedev
  - roguelike
  - procedural-generation
  - java
---

## The Beginning

In 2020, some friends ([@bautim](https://github.com/bautim) and [@melvinmotion](https://www.instagram.com/melvinmotion/)) and I decided to take on a challenge: building a game completely from scratch using **Java** and the respective **standard library only**. 
The idea was to learn by doing, to gain hands-on experience with the foundations of game engines and mechanics, and to push our programming and design skills forward.

## What We Built

![starting material](/assets/images/002/random_dungeon.webp)

The result was **Homeland Shelter**, a dungeon-style roguelike that brings together several core gameplay systems we implemented ourselves:

- **Procedural dungeon generation** for dynamic level layouts  
- A flexible **item and inventory system** with equipment management  
- **Enemy spawning and combat mechanics** built from the ground up  
- Integration of the **A\*** pathfinding algorithm  
- **Custom sprite work** created specifically for the game  

Everything you see in the project was created without the aid of external libraries or engines — a deliberate choice that forced us to really understand the low-level mechanics behind games and engines.

![starting material](/assets/images/002/items_and_enemies.webp)

In this picture you can see some changes to the starting position.
First up, the tall grass is "breakable" and loot can be generated via a loottable.
Also an enemy spotted me and began to move to my position.
The fire is a placeholder texture for GIF-based animations.


Changing the metadata file for the items, the texture is easily swapable and collectable. Collected items can be access via an inventory.
<div style="display: grid;">
  <div style="display: flex; gap: 1rem; margin: auto;">
    <img src="/assets/images/002/sword.webp" height="200px">
    <img src="/assets/images/002/inventory.webp" height="200px">
  </div>
</div>

## Collaboration and Contributions

This project was a team effort:  
- **Tim Bauer** ([@bautim](https://github.com/bautim)) contributed the A\* algorithm and gameplay improvements.  
- **Melvin Lannatewitz** ([MelvinMotion](https://www.instagram.com/melvinmotion/)) designed and drew the sprites that brought our world to life.  

Working together, we not only improved as individual developers but also learned a lot about teamwork, version control, and project planning.

## Key Takeaways

What I’m most proud of with *Homeland Shelter* is how much it taught me about **game architecture, algorithm design, and procedural generation techniques**. 
It also reinforced the importance of balancing creativity with maintainable code. 
While I’ve since explored engines like Unity to scale projects further, this experience gave me a solid foundation in the **fundamentals of game development**.

## Try It Yourselves
The project is available on GitHub for anyone who’d like to explore the code or try it out:  
[Homeland Shelter on GitHub](https://github.com/FlorianB-DE/HomelandShelter)

---

*Homeland Shelter* remains an important milestone in my portfolio — a project that demonstrates persistence, technical curiosity, and a passion for building games from the ground up.