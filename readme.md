# Smart Marines

A marine NPC actor that is quite a bit smarter than the vanilla brain dead monsters.

## What they can do (So far)

- Attack stuff by:
  - Bashing it with their rifle. (Melee)
  - Shoot at it in bursts of 5 rounds. (Ranged)
  - Throw a grenade at it, more likely to throw it at crowds of enemies. (Area of effect) 
- Run away from their own grenades.
- Reload their rifles for every 20 rounds they fire in total.
  - They first try a few times to run away from their target until out of sight, to not reload while vulnerable.
- Chase around their target for some time before losing track of it, if they can't hear or see it for too long.
- When not set to friendly, they attack friendly NPCs on sight, unlike normal enemy NPCs/monsters, that don't attack friendly NPCs unless provoked by them first.
- Can swim across swimmable 3D sectors to reach their target.
- Can be frightened if their target is big and/or strong enough.
- Can have a chance to taunt and wave their rifle after killing a powerful NPC, player, or a lot of weaker enemies*.
- Can be colored with a variety of colors:
  - Red
  - Gray
  - White
  - Black
  - Blue
  - Yellow
  - Orange
  - Pink
  - Random (Randomly pick a color.)
- Can have a randomized personality, that gives the marine a random armor color, different attention spans and chances to throw a grenade etc.
- Most of the marines' behaviour can be configured on a per actor basis using user variables.
- They also have a rifle that they sometimes drop, which you can pick up and use yourself.
  - The rifle fires bursts of 5 rounds, and needs reloading after firing 20 rounds, just like when the marines use them. You can reload before the magazine fully runs out too.
  - It also features animated digital sights complete with an animation for looking in and out of them, using the sights increased you accuracy as well.

*Such as Imps and Pinkies, anything that is really weak (5 or less HP), won't even count as a kill for the marine, so they won't be dancing afer killing 40 flies.

## Improvements I want to make on them

- Add the StayOnLift and AvoidHazards flags to the marines once the next GZDoom update that adds MBF21 support releases.
- Make them able to crouch across sectors with short ceilings, along with being able to crouch fire. I may not be able to do this though.
  - And of course if I can do it, then this should be toggleable as well.
- MAYBE I can give them some kind of cover system, that allows them to run to predetermined points in the map while fighting or running to reload.
  - I would need to somehow implement an actual pathfinding system of some kind, or use code for such a thing made by someone else. Since these marines still ultimately use (Z)Doom's brain dead AI, meaning they basically just randomly move around. Hence for example, why they just randomly run around to get out of their targets' sight and reload, instead of actually mapping a path to a location where their target cannot see them, and run to it.
  - As it stands currently, if I added a cover system with no pathfinding, it would suck because the marines wouldn't be able to actually go AROUND their cover and hide behind it, only go to its' general direction and then randomly move around, until MAYBE bypassing their own cover to go behind it.

# Note about the marines (August 21 2021)

Making just this basic version of them was an absolute nightmare, I begun work on them about 5 months ago or so, before I had my new PC, in that time I had to refactor them thrice because they got insanely buggy for some reason or another. And then, I lost access to the computer I used to develop my mods and make video showcases of them, and since my SFF OptiPlex 760 was too shit to be used for much of anything - I spent THREE MONTHS not being able to work on these marines or any major mod, until I finally got a new PC two weeks ago, and was able to continue working on my projects, starting with finishing these marines.

But as it turns out that would not be the end of it, after beginning to work on the marines on my new PC, I had to refactor them a fourth time due to the code being infested with bugs again, and then after working on the fourth iteration for 4-5 days, IT ALSO BROKE FROM TOO MANY BUGS.

Now, on my fifth iteration, I was finally fucking able to get AT LEAST the basic version to work without the AI going FUBAR **AGAIN**. I haven't even been able to work on many more of my projects, which I've amased a huge backlog of on my 3 month forced hiatus. And despite all that, because of how hard it was to even get the basic marine to work, I haven't been able to add the more advanced behaviour on them such as crouching and swimming. Or further work on the rifle they sometimes drop when killed.

It's pretty easy to tell how much of a huge pain the development of these marines has been, if you just look on the broken code folder, and how angry several of my comments are on the current, and some of the previous, iterations of the marines.