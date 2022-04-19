# Million Monkeys Game Engine

> If you had a million monkeys working on a million games for a million years, eventually, maybe one would create a fun game...

The Million Monkeys game engine is a C++ game engine designed with three core goals in mind:

1. It should be easy to use and extend
2. It should do what it can to support smart NPC's through flexible Game AI systems
3. It should do what it can to support dynamic storytelling

To that end, it is designed around the idea that game events and NPC interactions occur dynamically and independently of the player, in a simulated world.

Some key features:

* Core engine is written in C++17
* Game-specific logic is written in Lua scripts (executed through LuaJIT)
* Data and configuration is stored in human-editable TOML files
* Game entities are managed through an EnTT-based Entity-Component-System
* Entities and systems communicate through an event system
* Multithreaded task-based systems
* PhysX-based physics system (Not yet implemented)
* A wide set of AI building blocks:
  * Hierarchical Task Network
  * Goal Oriented Action Planning (Not yet implemented)
  * Utility System (Not yet implemented)
  * Pathfinding (A* and perhaps Recast/Detour navmeshes) (Not yet implemented)
  * Steering (Not yet implemented)
  * RETE-based inference (Not yet implemented)
* A web-based editor: (work in progress)
  * Live access to entities
  * Visualisation of game data
  * Map events to Lua script functions
  * Create NPC AI data:
    * HTN networks
    * GOAP actions
    * Scripted Actions
    * Utility curves
    * Inference rules
  * Create story templates:
    * Condition-based templates for story beats which the dynamic storyteller can use to generate larger story arcs
* OpenGL 4.6 renderer with: (Not yet implemented)
  * Physically-based material system
  * Deferred shading light system (the plan it to try Deferred-texturing based renderer first):
    * https://mynameismjp.wordpress.com/2016/03/25/bindless-texturing-for-deferred-rendering-and-decals/
    * https://www.reedbeta.com/blog/deferred-texturing/
  * Maybe switch to bgfx later

Currently the engine is only built and tested on Linux. In the future, prebuilt binaries for both Linux and Windows will be provided and an OS X port is planned (once a compatible renderer is written, since OS X does not support versions of OpenGL newer than 4.1, this is the primary blocker for an OS X port).
