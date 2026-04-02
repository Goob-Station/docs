
# Minor Pest Overview:

Added a new midround nuisance antag: Doodon.
Added many doodon buildings and units.



An antag inspired by Colony Sim games and ants, the Doodons are meant to be a nuisance antag. They are supposed to put a material strain on the station, taking food, steel, and glass to turn it into a resource only they can use: Doodon Resin.
Fragile in combat, the doodons have alternate means to secure a spot on the station. Doodons can use resin to make valuable gems and Moodons that can produce omnizine. They can trade these goods to the crew to try and buy their safety.
If peace does not work, doodons do have means to defend themselves. The warrior caste of doodon can be deadly in large numbers and can be armed with doodon swords and doodon shields. Every non-player-controlled doodon goes feral upon the papa's death, as well as having group retaliation, forcing crew to think strategically about taking out the doodons.



# Details: 

## Village Housing System:
For doodon buildings to be able to work, they must be connected/in range of a town hall. When a doodon house building (dwelling, warrior hut, pasture) is placed, it is connected to the nearby town hall. Each doodon house building increases the housing limit for the "village". Essentially, the doodon units cannot be greater than the housing limit. Each unit has its own housing limit. You can check these housing limits by inspecting the town hall. You can spend doodon resin to spawn a unit at a doodon house.
Ex: A doodon dwelling is built within the range of a town hall. That dwelling increases the housing limit for workers by 2, and spawns a worker doodon. The housing available for worker doodons is 1, since that spawned worker is taking up 1 unit of housing.

## Doodon Items:
### Doodon Resin:
A resource completely useless to anyone who isn't doodon. An omni-material used by doodons to build structures, respawn units, and craft doodon items.
### Doodon Shield:
Same as wooden buckler
### Doodon Sword: 
A good armament for warriors
### Doodon Gem:
Good to trade with cargo.

##  Doodon Units:
### Papa Doodon:
The entity that spawns when the gamerule event is triggered. Responsible for placing the Doodon Town Hall, building doodon structures, and commanding the doodons. Has antag goals to build X amount of buildings and to keep Y amount of workers alive. 
### Worker Doodons:
Responsible for making doodon resin and building doodon structures. Not meant for combat, but can defend themselves if needed. Must listen to the Papa doodon, and not start fights.
### Warrior Doodons:
AI-controlled warriors that only listen to papa, meant for combat. Can be equiped with weapons. Use Rat King command logic.
### Moodons:
Cattle of the doodon village. A small cow that produces omnizine. Uses housing, but does not count towards overall population.

## Doodon Town Hall:
The Center of the doodon village. Keeps track of population and housing. Doodon structures stop working without a town hall. Only one can be placed.

## Doodon Housing Buildings: Increases housing. Spends resin to make more units
### Doodon Dwelling:
Increases housing for workers by 2, and spawns 1 doodon worker. Resin can be spent here to spawn more worker doodons, so long as there is housing.
### Doodon Warrior's Hut:
Increases housing for warriors by 1, and spawns 1 doodon warrior. Resin can be spent here to spawn more warrior doodons, so long as there is housing.
### Doodon Pasture:
Increases housing for Moodons by 3, and spawns 1 moodon. Resin can be spent here to spawn more moodons, so long as there is housing.

## Doodon Workshop Buildings: Spends resin to produce items
### Doodon Gem Cutter:
Spends resin to make a doodon gem. Gem is valuable, and should be traded to cargo
### Doodon Shieldsmith:
Spends resin to make a doodon shield. Same as wooden buckler
### Doodon Swordsmith:
Spends resin to make a doodon sword. 10 slash damage

## Doodon Refinery Buildings: Spend material to make resin
### Doodon Glass Refiner:
Glass -> Resin
### Doodon Metal Refiner:
Metal -> Resin

# Why / Balance
Would be a nice way to generate ghost roles without being too destructive.  Has potential for some good RP moments if crew decides to interact positively with the doodons. 
The doodon swords could make sec not want to keep the doodons around, as they pose a security risk.
Doodons are essentially Rat King, but stationary.

# Design Philosophy
The doodons were created to answer the question, "What would it be like to have an ant infestation in space?" "What would it look like?"
As a result, the doodons take a lot of inspiration from ants. They are meant to impose a resource strain on the station, and in the future, should avoid having buildings that produce food or any other material that can be turned into resin.
To encourage RP, they should have equal ways to help the station and harm it.



