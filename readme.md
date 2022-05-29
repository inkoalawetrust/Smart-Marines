![](https://i.imgur.com/HKnzbLI.png)

# Smart Marines

Smart marines are NPCs for Doom that are far more intelligent than vanilla monsters

## What they can do (There is a lot)

- Attack stuff by:
  - Bashing it with their rifle. But they normally avoid it if they can help it. (Melee)
	- Can also use berserk packs, if one is somehow in their inventory, which triple their melee damage, and make them more likely to engage in melee.
  - Shoot at it, with a random chance of changing position while doing so. (Ranged)
  - Throw a grenade at it, more likely to throw it at crowds of enemies. (Area of effect)
- They avoid firing their rifles, grenades, or turrets if their line of fire to the target is blocked by obstacles or allies.
- Run away from the grenades they throw, if those grenades are about to explode.
- Intelligently dodge enemy or extremely harmful projectiles heading their way. More information can be found inside Document.txt
- Dynamically take cover behind sufficiently tall level geometry or shootable actors when attacking enemies. More information can be found inside Document.txt
- They have multiple death animations that can play randomly.
- Reload their rifles for every 20 rounds they fire in total.
  - They first try a few times to run away from their target until out of sight, to not reload while vulnerable.
- Chase around their target for some time before losing track of it, if they can't hear or see it for too long.
- When not set to friendly, they attack friendly NPCs on sight, unlike normal enemy NPCs/monsters, that don't attack friendly NPCs unless provoked by them first.
- Alert other marines that are on their side of their current target, if the other marines have no target they are dealing with already. They can also hear the alerts of enemy marines.
- Retreat and keep a distance away from very powerful or large enemies like Cyberdemons. Or enemy players and marines on turrets.
- Marines friendly to the player can be ordered to stand still or wander around by pressing use on them. This only works if they aren't currently fighting.
- They work with ZDoom's built-in patrol system, so you can have them walk around set paths. To do stuff like guard areas.*
- Has placeable machine gun turrets that both players and the marines can use, you can press the use key on a friendly marine to get him off of one.
- Includes a separate marine that permanently stays on the turret until killed, who can also be colored like below. Pressing use on them will get them off, if they are friendly, and User_DisobeyCommands is off.
- Can be colored with a variety of colors:
  - Red
  - Gray
  - White
  - Black
  - Blue
  - Yellow
  - Orange
  - Pink
  - Dark Green
  - Random (Randomly pick a color.)
  - Default (Use the default shade of green. Similar to just leaving User_Color empty.)
- Most of the marines' behaviour can be configured on a per actor basis using user variables.
- Can have a randomized personality, that gives the marine a random armor color, different attention spans and chances to throw a grenade etc. Adding a custom value to a user variable prevents it from being randomized.
- They also have a rifle that they sometimes drop, which you can pick up and use yourself.
  - The rifle fires at full auto, and needs reloading after firing 20 rounds, just like when the marines use them. You can reload before the magazine fully runs out too.
  - It also features animated digital sights complete with an animation for looking in and out of them, using the sights increases your accuracy as well.
  - The rifle can be entirely disabled from dropping from dead marines, by enabling User_NoRifleDrop on the marine.

More information, such as info on what all the user variables available on the marines are, and what they do. Can be found inside Document.txt


## Scrapped features

- Swimming, the code and behavior for it was janky, barebones, and prone to breaking. And TG5 was never able to make the swimming sprites for the marine, so it was scrapped.
- Taunting, I have had to rewrite this NPC 6 goddamn times, so I won't even bother readding this. Plus it looked kinda stupid anyway.
