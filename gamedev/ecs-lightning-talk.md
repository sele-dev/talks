---
title: ECS Lightning Talk
sub_title: 2026-02-09 Cooking Up Games Workmeet
author: "Caleb Currie"
---

<!-- jump_to_middle -->
Administrivia
===
<!-- end_slide -->

ECS - Entities, Components, Systems
===

* Architectural pattern
* Data & Code (logic) separated
* Implementation differs by engine, perspective
* Not new: Scott Bilas 2002 GDC talk
<!-- end_slide -->

What is ECS?
===

* **E**ntity - A unique ID (usually an integer)
* **C**omponent - Just data (position, health, velocity)
* **S**ystem - Logic to process components
<!-- end_slide -->

Why?
===

* Archetype storage -> effective use of cache
* Dependency graph -> parallelize work
* Shared state avoided implicitly
* Organizing your project
* Flexible composition

<!-- end_slide -->
Memory Layout
===

```
AoS (traditional OOP):
[{pos, vel, health}, {pos, vel, health}, ...]

SoA (ECS):
Position: [pos1, pos2, pos3, ...]
Velocity: [vel1, vel2, vel3, ...]
Health:   [hp1,  hp2,  hp3,  ...]
```

<!-- end_slide -->

ECS in the Wild
===
- Hytale
- Tiny Glade - the Bevy ECS for simulation
- Bevy Engine internally: render graph -> systems
- Godot GECS
- Unity DOTS
- Unreal MASS
<!-- end_slide -->

Questions?
===
- Reach out - caleb@sele.dev
- https://this.scottbilas.com/files/pubs/2002/gdc-san-jose/GameObjects.pdf
- https://github.com/bevyengine/bevy/pull/22144
<!-- end_slide -->

License
===
© Caleb Currie
This presentation is licensed under CC BY-SA 4.0.

https://creativecommons.org/licenses/by-sa/4.0/
