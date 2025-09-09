---
layout: post
title: Forest Warrior – Indirect-Control Game in Unity (Games in C#)
date: 2021-04-18
tags:
  - gamedev
  - unity
  - csharp
  - game-jam
  - portfolio
---

## The Concept

This project was built for the “Games in C#” university course mimiking a small, jam‑style competition. The theme was: **"You control the game, not the player."**

So instead of steering the hero, you set the stage. You place enemies, play cards, and even buff enemies to raise the loot rewards, at the risk of making your hero’s life. It’s a bit like being a slightly mischievous dungeon master on a budget.

## What We Built

![Forest Warrior menu](/assets/images/004/menu.webp)

Forest Warrior is a Unity project (C#) where your inputs nudge systems more than characters. A few concrete bits:
- Menus you can actually use: start the run, and hop right in.
- A simple “cards” panel to pick what to spawn or modify during play.
- Buffs you can apply to enemies to bump loot values—fun for you, less so for the hero.
- A small upgrade flow woven into the loop so choices matter without turning into a spreadsheet (Leveling Attackspeed is OP 😉 !).

![Village](/assets/images/004/village.webp)

The core gameplay:
- Rougelike with persistent upgrades and runs that start from scratch.
- Unlock content as you go.
- Different playstyles with different weapons.
- The main loop is time based so you can multiple quick runs in succession.

![Main Stage](/assets/images/004/stage.webp)

## My Role and Team

- Me — gameplay code, the “you poke systems, not the hero” bits
- Lars S. — menus, in‑game UI, and the upgrade choices
- Felix v. R. — art and visual style

We scoped small, shipped something playable, and learned a couple of tricks on the way and most importantly, how to manage time crunch.

## My Engineering Highlight: Fast "closest enemy" lookup

I’m quietly happy with how the game finds the nearest enemy. The short version: we keep enemies in a min-heap (priority queue) keyed by squared distance to the hero. Asking “who’s closest right now?” is O(1) via Peek. We only reshuffle when something actually changes order—like when one enemy overtakes another. Most frames, nothing changes and it stays O(1).

Why it works nicely here:
- We avoid computing the square root by comparing squared distances.
- Enemies mark themselves “dirty” only when they move enough to matter (or on a small cadence).
- Only the dirty ones pay O(log n) to update their position in the heap.


Is this the only way to do it? Nope. Is it the most efficient? I try to think so but probably not... But for this project’s size it was simple, predictable, and kept the main loop tidy and efficient.

## What I Took Away

- Indirect control is fun if the feedback is clear. If players don’t see what their card or buff did, they assume it did nothing or the game is broken.
- The priority queue is overengineed² but it was fun having an "eureka" moment and telling myself that my computer science degree is worth something... I don't think it matters performance-wise but saving resources is a good thing in any case.
- In a jam, “good enough and readable” beats “clever but fragile” every time. That's cause all our enemies have a slime sprite...

## Try It Yourself

- Repo: https://github.com/FlorianB-DE/Games-in-CSharp
- How to run:
  1. Clone the repo
  2. Open in Unity (2020.3+; tested with 2022.3.62f1)
  3. Press Play
  4. Set resolution to Full HD (1920×1080) for best results