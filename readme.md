![](https://i.imgur.com/BgUlzkp.png)

# Smart Marines

A marine NPC actor that is quite a bit smarter than the vanilla brain dead monsters.

## What they can do

- Attack stuff by:
  - Bashing it with their rifle. But they normally avoid it if they can help it. (Melee)
	- Can also use berserk packs, if one is somehow in their inventory, which triple their melee damage, and make them more likely to engage in melee.
  - Shoot at it, with a random chance of changing position while doing so. (Ranged)
  - Throw a grenade at it, more likely to throw it at crowds of enemies. (Area of effect)
- They avoid firing their rifles, grenades, or turrets if their line of fire to the target is blocked by obstacles or allies.
- Run away from the grenades they throw, if those grenades are about to explode.
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
- Can have a randomized personality, that gives the marine a random armor color, different attention spans and chances to throw a grenade etc. Adding a custom value to a user variable prevents it from being randomied.
- They also have a rifle that they sometimes drop, which you can pick up and use yourself.
  - The rifle fires at full auto, and needs reloading after firing 20 rounds, just like when the marines use them. You can reload before the magazine fully runs out too.
  - It also features animated digital sights complete with an animation for looking in and out of them, using the sights increased you accuracy as well.
  - The rifle can be entirely disabled from dropping from dead marines, by enabling User_NoRifleDrop on the marine.

More information, such as info on what all the user variables available on the marines are, and what they do. Can be found inside Document.txt


## Scrapped features

- Swimming, the code and behavior for it is janky (Or rather, it was always more janky than the rest of my shit code from the very beginning.). Their water movement is just moving in a straight line, and on top of all that. I still have not been able to get any swimming sprites for the marine, so it still used the normal player moving animation as a placeholder. So the swimming behavior will be scraped entirely.
- Taunting, I have had to rewrite this NPC 6 goddamn times, so I won't even bother readding this. Plus it looked kinda stupid anyway.

# Note about the marines (January 25, 2021)

While I was working on gz_bigcity 2 weeks ago, a map originally made, so I could showcase the marines on after I make a showcase video for them. I decided to place one of them down for fun, and it only threw a grenade at me once, then refused to attack. Which indicated that they broke once again. So now I have to waste a month total recoding them for the sixth time, so that they will inevitably completely break once again. And the cycle can start again.

# Note about the marines (August 21, 2021) (Old)

Making just this basic version of them was an absolute nightmare, I begun work on them about 5 months ago or so, before I had my new PC, in that time I had to refactor them thrice because they got insanely buggy for some reason or another. And then, I lost access to the computer I used to develop my mods and make video showcases of them, and since my SFF OptiPlex 760 was too shit to be used for much of anything - I spent THREE MONTHS not being able to work on these marines or any major mod, until I finally got a new PC two weeks ago, and was able to continue working on my projects, starting with finishing these marines.

But as it turns out that would not be the end of it, after beginning to work on the marines on my new PC, I had to refactor them a fourth time due to the code being infested with bugs again, and then after working on the fourth iteration for 4-5 days, IT ALSO BROKE FROM TOO MANY BUGS.

Now, on my fifth iteration, I was finally fucking able to get AT LEAST the basic version to work without the AI going FUBAR **AGAIN**. I haven't even been able to work on many more of my projects, which I've amassed a huge backlog of on my 3 month forced hiatus. And despite all that, because of how hard it was to even get the basic marine to work, I haven't been able to add the more advanced behaviour on them such as crouching and swimming. Or further work on the rifle they sometimes drop when killed.

It's pretty easy to tell how much of a huge pain the development of these marines has been, if you just look on the broken code folder, and how angry several of my comments are on the current, and some of the previous, iterations of the marines.
