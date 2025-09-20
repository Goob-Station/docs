```admonish warning "Attention: WIP!"
This doc is actively under development and is not fully complete. Things may change!
```

# Shuttles
| Designers                      | Implemented | GitHub Links |
|--------------------------------|---|---|
| Rouden | :warning: Partially | TBD |

## Overview
This proposal tries to explain and fix major issues related to shuttles. They are a major, yet very dangerous mechanic for core SS14 design. Probably this rework, when implemented, can have unpredictable impact on the main game, since we are changing the core idea of Space Station.

## The Main Problem
**Shuttles ARE NOT Space Station.** This is shuttles biggest flaw - they are independent from the station, and can even be separate stations on practice.

Shuttles from the very beggining violate the first **"What is Space Station 14"** question. Quote from Wizden docs:
> _"Spacestation 14 is a game where disasters, enemies, and incompetence conspire to make each shift aboard the **station** a unique and hellish experience."_

Well, this is it - Space Station is a game about one specific station, that goes into a cascade of chaotic events. And shuttles with their mobility completely break this rule.

So, there are 2 final possible outcomes for SS14 shuttles:

 1. Shuttles are completely removed as a mechanic in favor for the game;
 2. We redesign the game to be able to support shuttles.

This is probably **THE MOST** uneasy decision to make in general, but for now we will assume the second variant as the right one.

Why? Because Shuttles has great potential to expand the limits of the game significantly.

We can't predict what will happen, but we always can just try. It will noticeably change how SS14 is played, and only we can decide if it's for the better or the worse.

## Learning from Frontier
Frontier servers are a great example of how shuttles can be made useful by making a _game about shuttles_.
But right here we're making a game about shuttles AND stations, so comparing it to the main game will be useful only in some cases.

Lets look at Frontier's flaws and how can we avoid them in our main game:
* Shuttles have a couple of possibilities, but they're usually aren't enough. You can salvage, make buisnesses, do space combat, do science, or other space station stuff, but only on your own shuttle.
* This leads to lack of player's agency, since there are not enough choices you can make for gameplay to be especially fun.
* And when you're stck on your shuttle, you rarely talk with people, so you basically starting to play your own sigleplayer game.

As you can see, even a complete rethinking of the game isn't safe from violting core principles of SS14. So we **MUST** reinforce these design pillars At All Costs.

# Shuttle Content

This part of the proposal will suggest more specific ideas for shuttles that should be added eventually, if we want to make them good and not just remove them forever.

## Space Transportation
The main purpose for shuttles will always be transportation. It doesn't matter if it's some cargo or weapons on board, any object can be transported quickly.

The problem is, currently in space there are only 3 living objects: ATS, the Station and Cargo shuttle.

If we want to make shuttles a part of the game, we should not just add more shuttles, but also think about new destinations to explore and content that will be available for them.

## Space Combat
Shuttle combat can be a fun mechanic as we know from other games. But adapting it properly to a sandbox real-time multiplayer RP game is a very non-trivial task.

Space combat can be a counterpart for normal PvP with much higher bets.

But, it's almost impossible to balance shuttle combat without touching already existing foundations of Space Stations.
For example, lets look at theoretical statistics if we just add shuttle combat without changing all stations:

| Ship Type: | Speed (m/s) | Size (tiles) | Weapons (amount)|
|---------|------|----|---|
| Station | 0 | A lot | 0 |
| Shuttle | 0-60 | 300 & lower | ~0-15 |

So, just attaching weapons to shuttles without also changing stations is a bad idea. Space combat needs to be added EXTREMELY thoughtfully, otherwise it WILL break the meta.
It will require a separate proposal for sure.

## FTL Rework
Currently all shuttles by defaul can FTL anywhere in fixed 256 tile radius. Mostly it used for escapes or to travel between maps.

All shuttles being with the same stat is BORING, so lets fix that by adding **Bluespace drives**.

They consume power and allow for shuttle to be able to FTL. And without it, you can't do FTL jumps at all.
Cooldowns and range also now depend based on what type of bluespace drive you have installed.

This will have some major mapping issues, expecially with gamerule-spawned shuttles, so this should be implemented smoothly in PR that is made out of 2 parts.

## Space Archeology
What if science experiments were available not just in RnD department, but also in deep cold space? Potentially we can add something like science ship equipment that gives tons of points for researching different space ruins or anomalies with huge shuttle scanners.

Science will be interested in building their own ship to get even more points, and this will lead to a lot of interactions between departments, which will be healthy for smooth gameplay.

## Space Gamerules
**More unique gamerules** related to something happening in deep space near the station is also needed to keep the sector and deep space alive. When you fly far away from the station, _you shouldn't be saved from chaos coming from your docking ports_.

For example, carp migration can occur near your shuttle, and then some of them may end up entering your shuttle.

Meteors also can be reworked to spawn passively, but be not as destructive, meaning that all shuttles will require constant repairs and therefore be more dependent on stations.

## Salvage Rework
Salvage is currently the only department that is constantly interacting with space enviroment. They already have a strong foundation of content, but it needs a lot of work to be fully done.

From the side of shuttles, to make them even more useful for salvage:
* **Lavaland** should be available for an FTL jump at any spot that is clear from structures.
* **Expeditions** also should be readded in reworked form eventually, but this mostly depends on wizden.
* **More Procedural space ruins** will help salvage to never be too bored and to make space salvaging even useful. This will require a separate proposal for Goobstation's rework of all salvage and lavaland.

## Split Stations
Game maps actually support multiple grids or even stations on one single map. Split stations will not only provide unique experience for high-pop, but also will make deep space more alive in general.

More stations means more shuttles means more fun!

And we don't have to make multiple split stations, we can just make one station that has a satellite for Science as an example. There are many possibilities, and mappers can brainstorm even more crazy ideas for split stations.

## Security shuttle
After space becomes chaotic, some source of stability should be added. Security shuttle will add even more interactions between departments (shuttle needs repairs) and antagonists.

If there are huge meteors on the way, security can undock and try to shoot these down, or they can detect nukies before they arrive to the station and engage into the fight right from space. The possibilities are endless.

The problem is that another role will be required for security to pilot this shuttle. Something like security technitian that would have engineering access to fix and pilot the shuttle can be a bit controversial idea.

## ATS Rework
Having just one ATS for cargo is too boring. I propose adding 3 or 4 trade stations that have diffirent selling prices, meaning that its better to sell something on one station, while bying something on another will be cheaper.

QM can have a special console to pick between different supplier companies that offer diffirent pricing on buying/selling, and all of them have their own ATS stations. Many mechanics can revolve around this idea, and it also should be detailed in it's own design document.

# Conclusion
All ideas from previus chapter still can't guarantee the absence of "Meta", because how good shuttles will play will depend only on implementation and not the ideas. But making small steps, at the end we may end up finishing a great project that will improve SS14's gameplay.
