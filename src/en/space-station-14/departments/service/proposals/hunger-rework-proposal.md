# Proposed changes to hunger system

| Designers | Implemented | GitHub Links |
|---|---|---|
| BombasterDS | :x: No | TBD |

## Current problems
Current hunger system have a big issue - emergency and cargo food have the same OR even more effectiveness as chef's food. There is some reasons for this:
-   There is no penalty for overfeeding. That means you can eat enough food to last you the rest of the round.
-   Junk and emergency food are operate with same attributes as kitchen food. Several junk food will be equal to one soup in kitchen and it's much easier to find junk or emergency food.

These problems make chefs job useless. For most players it's much easier to find some food in maints or order pizzas for whole department.

## Overview
To solve the problems described above, the current starvation system needs to be changed. New hunger system should operate with new variables - **Saturation** and **Food groups**

**Saturation** works as hunger shield.  Whenever hunger system need to decrease hunger amount of entity it decrease saturation first. It works only if your current hunger state is NOT overfed or well-fed. In most cases, saturation cannot be stacked, only overwritten by higher saturation. Only few rare or hard-to-make food should be able to stack saturation to it max level.

Saturation's sources, in most cases, are cooked food. Junk and emergency food won't give any saturation and cargo pizza will be cheap analog of chef's pizza that not gives any saturation.
Saturation main purpose to separate *cheap* food from good cooked food to reward players that made this food and players that come to kitchen to get this food.

**Food groups** are several dietical food groups for each person that should be balanced in the round. Each humanoid entity have their own value of each food group with minimum at 0 and maximum at 100. When humanoid player spawn values of each group sets on 50 +- 25. Value of food groups can be seen with special scanner that spawns in chef or medical vendors. Having less than 10 on food group will apply debuff on player depending on food group. There will be some food groups in game:
-   Dietary fibers - only work on species that can eat vegetables - can be get from most vegetables and fruits. Having less than 10 value decreases blood level regeneration by 25% and increase bloodloss amount.
-   Proteins - only works on species that can eat meat - can be get from most meat food. Having less than 10 makes your melee attacks make 25% less damage and get you more brute damage by 10%. 
-   Sugars - only works on species that can eat sweet food - can be get from berries, sugar and other sweet food/drinks. Having less than 10 makes you and your doafters 25% slow. Having more than 90 makes you get poison damage each time you lose hunger.
-   Fibers - MOTH ONLY - works both as proteins and dietary fibers.

Having more than 80 value on every group player have will give him buff than slightly increase his doafter speed and health regeneration.

Each group value is decreasing when hunger (not saturation) decreases by (hunger decrease amount / food groups amount). 

Food groups will encourage people to eat different food without making it more harder. In rounds it should be enough for players to eat two different types of food OR order pizza box from cargo if there is not enough chefs or botanists. This will also encourage chefs to make different food types and look for crew dietas.

## New penalties
In addition to the food group penalties there also new debuffs for overfeeding. 

**Vomit change** - vomit will massively decrease person hunger and completely zero out his saturation. Vomit will cause debuff that won't allow person to eat anything by himself in next minute.

**Well fed** is new state that comes after normal fed station. When entity is well fed they passive regeneration damage threshold increased from 20 to 35.

**Overfed** is state that comes if you eat more food after **Well fed**. Player get 15% slow debuff, but his passive regeneration damage threshold increased from 35 to 40. In addition person can't eat anything else in this state by himself, but he still can be force fed. Forcing feeding person is this state will cause him to vomit. 

**Hungry** - in addition to speed debuff person also decreases his passive regeneration damage threshold from 20 to 10.

**Super hungry** - in addition to speed debuff person also stops his passive regeneration, he get dizzy effect, weakness debuff (like from proteins deficiency) and stops regeneration blood level.