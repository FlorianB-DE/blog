---
layout: post
title: "OOM Project – Modeling a Game Engine: Concepts, Complexity, and Lessons"
date: 2020-08-31
tags:
  - software-design
  - uml
  - oop
  - game-development
---

## Project Overview

This project is an academic exploration of how object-oriented modeling and UML can guide the design of a small, interactive game engine prototype. The goal was to explore the concepts of production engines, and to capture core ideas like rendering, input, collisions, camera behavior, and persistence in a clean, teachable architecture. It bridges rigorous modeling with a pragmatic, working prototype suitable for demonstrating design thinking.

## Scope and Intent

The primary aim of this project was to translate UML-driven concepts into a compact, engine-like prototype. Rather than remaining purely theoretical, the outcome was designed to be a playable sandbox that demonstrates movement, interaction, simple item usage, basic collision handling, smooth camera following, and the ability to save and load game state. In this way, the project connects abstract modeling with a tangible implementation that highlights how design decisions shape the player’s experience.

## What I Built (Conceptually)

![generated world](/assets/images/003/generated_world.webp)

- A lightweight render-update loop that draws a 2D world and entities.
- An input layer that turns user intent into movement and interactions.
- A simple collision/trigger mechanism for proximity-based actions.
- A camera that follows play while respecting screen edges for a smooth feel.
- A minimal persistence path to save and restore session state.
- A component-oriented approach to assembling game objects, favoring composition and clear responsibilities.

## Complexity I Tackled

One of the core challenges was mapping high-level UML artifacts into concrete, cohesive code structures while still adhering to the set out preplanned structure. The diagrams provided clarity on responsibilities, but the real test came in ensuring that the resulting code preserved this separation while still feeling natural to work with during implementation.

Another area of focus was managing interactive items with lifecycle constraints and sensible feedback. Items needed to behave consistently—appearing, being used, and disappearing in ways that respected both the underlying design and the player’s expectations—while still leaving room for extensibility.

I also worked on keeping rendering concerns distinct from input handling, lightweight physics checks, and overall game state management. This separation was critical for maintaining clean boundaries between systems, reducing coupling, and ensuring that changes in one area (like input) did not ripple unpredictably into others.

Finally, I designed a minimal yet extensible save/load system. The emphasis was on capturing and restoring session state reliably.

## How It Compares to a Real Game Engine

What this prototype includes:
- Core gameplay loop with input → update → render.
- Basic camera logic.
- simple collision/trigger interactions.
- Elementary state persistence and a modest world layout.

What full engines typically add (beyond this project’s scope):
- Advanced physics (continuous collision, rigid bodies, constraints).
- Robust asset pipeline, animation systems, and editor tooling.
- Scene graph/ECS with high scalability and data-driven workflows.
- Cross-platform rendering backends, multithreading, and job systems.
- Memory/resource management, streaming, and hot-reload.
- Networking, replay systems, automated testing, and profiling suites.

This project purposefully concentrates on conceptual clarity rather than breadth, making it ideal for illustrating architectural thinking in a portfolio/personal experience context.

## Key Learnings

- Modeling to Code: Good diagrams accelerate implementation by clarifying roles.
- Abstractions Matter: Clean interfaces reduce coupling and ease iteration.
- Scope Discipline: A focused slice of engine functionality tells a stronger story than a shallow attempt at “everything.”
- Player Feel: Small decisions (camera thresholds, input smoothing) impact overall experience.

## Closing Thoughts

This project showcases the path from disciplined modeling to a concise, working engine slice. It’s intentionally scoped to highlight architectural judgment, composability, and player-facing feel—qualities that I hope to transfer to professional software and game development environments.