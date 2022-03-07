![](https://i.imgur.com/phgBzq8.png)

# Smart Marines

A marine NPC actor that is quite a bit smarter than the vanilla brain dead monsters. If it ever stops bugging out every 2 seconds.

## Note: The marines are currently being rewritten again. Hopefully they won't totally break once again.

## What they will be able to (hopefully) do

- Attack stuff by:
  - Bashing it with their rifle. They normally avoid it if they can help it though. (Melee)
  - Shoot at it, with a random chance of changing position while doing so. (Ranged)
  - Throw a grenade at it, more likely to throw it at crowds of enemies. (Area of effect)
- Run away from their own grenades.
- Reload their rifles for every 20 rounds they fire in total.
  - They first try a few times to run away from their target until out of sight, to not reload while vulnerable.
- Chase around their target for some time before losing track of it, if they can't hear or see it for too long.
- When not set to friendly, they attack friendly NPCs on sight, unlike normal enemy NPCs/monsters, that don't attack friendly NPCs unless provoked by them first.
- Can be frightened if their target is big and/or strong enough.
- Alert other marines that are on their side of their current target, if the other marines have no target they are dealing with already.
- Retreat and keep a distance away from very powerful or large enemies like Cyberdemons.
- Marines friendly to the player can be ordered to stand still or wander around by pressing use on them. This only works if they aren't currently fighting.
- Can have a chance to taunt and wave their rifle after killing a powerful NPC, player, or a lot of weaker enemies*. (Unfinished)
- Has placeable machine gun turrets that both players and the marines can use, you can press the use key on a friendly marine to get him off of one. (Unfinished)
- Includes a separate marine that permanently stays on the turret until killed, who can also be colored like below. Pressing use on him doesn't get him off. (Unfinished)
- You can press the use key on friendly marines when they are in their initial Sawn state, to get them to move, or press use on them while they are standing still or looking for enemies. To get them go back to their Spawn state.
- Can be colored with a variety of colors:  (Unfinished)
  - Red
  - Gray
  - White
  - Black
  - Blue
  - Yellow
  - Orange
  - Pink
  - Random (Randomly pick a color.)
- Can have a randomized personality, that gives the marine a random armor color, different attention spans and chances to throw a grenade etc. Adding a custom value to a user variable prevents it from being randomied. (Unfinished)
- Most of the marines' behaviour can be configured on a per actor basis using user variables. (Unfinished)
- They also have a rifle that they sometimes drop, which you can pick up and use yourself.
  - The rifle fires at full auto, and needs reloading after firing 20 rounds, just like when the marines use them. You can reload before the magazine fully runs out too.
  - It also features animated digital sights complete with an animation for looking in and out of them, using the sights increased you accuracy as well.

*Such as Imps and Pinkies, anything that is really weak (5 or less HP), won't even count as a kill for the marine, so they won't be dancing after killing 40 flies.

## Potential future additions for the marines
Note: Considering how much of a pain coding these marines to completion has been, I'll probably only do the first one. And someone else will have to go through the pain of coding the rest. If I can even finish the above list of features that is.

- Add the StayOnLift and AvoidHazards flags to the marines.
- Make them able to crouch across sectors with short ceilings, along with being able to crouch fire. I will not be able to do this though.
- Give them some kind of cover system, that allows them to run to predetermined points in the map while fighting or running to reload.
  - I would need to somehow implement an actual pathfinding system of some kind, or use code for such a thing made by someone else. Since these marines still ultimately use (Z)Doom's brain dead AI, meaning they basically just randomly move around. Hence for example, why they just randomly run around to get out of their targets' sight and reload, instead of actually mapping a path to a location where their target cannot see them, and run to it.
  - As it stands currently, if I added a cover system with no pathfinding, it would suck because the marines wouldn't be able to actually go AROUND their cover and hide behind it, only go to its' general direction and then randomly move around, until MAYBE bypassing their own cover to go behind it.

## Scrapped features

- Swimming, the code and behavior for it is janky (Or rather, it was always more janky than the rest of my shit code from the very beginning.). Their water movement is just moving in a straight line, and on top of all that. I still have not been able to get any swimming sprites for the marine, so it still used the normal player moving animation as a placeholder. So the swimming behavior will be scraped entirely.

# Note about the marines (January 25, 2021)

While I was working on gz_bigcity 2 weeks ago, a map originally made, so I could showcase the marines on after I make a showcase video for them. I decided to place one of them down for fun, and it only threw a grenade at me once, then refused to attack. Which indicated that they broke once again. So now I have to waste a month total recoding them for the sixth time, so that they will inevitably completely break once again. And the cycle can start again.

# Note about the marines (August 21, 2021) (Old)

Making just this basic version of them was an absolute nightmare, I begun work on them about 5 months ago or so, before I had my new PC, in that time I had to refactor them thrice because they got insanely buggy for some reason or another. And then, I lost access to the computer I used to develop my mods and make video showcases of them, and since my SFF OptiPlex 760 was too shit to be used for much of anything - I spent THREE MONTHS not being able to work on these marines or any major mod, until I finally got a new PC two weeks ago, and was able to continue working on my projects, starting with finishing these marines.

But as it turns out that would not be the end of it, after beginning to work on the marines on my new PC, I had to refactor them a fourth time due to the code being infested with bugs again, and then after working on the fourth iteration for 4-5 days, IT ALSO BROKE FROM TOO MANY BUGS.

Now, on my fifth iteration, I was finally fucking able to get AT LEAST the basic version to work without the AI going FUBAR **AGAIN**. I haven't even been able to work on many more of my projects, which I've amassed a huge backlog of on my 3 month forced hiatus. And despite all that, because of how hard it was to even get the basic marine to work, I haven't been able to add the more advanced behaviour on them such as crouching and swimming. Or further work on the rifle they sometimes drop when killed.

It's pretty easy to tell how much of a huge pain the development of these marines has been, if you just look on the broken code folder, and how angry several of my comments are on the current, and some of the previous, iterations of the marines.
