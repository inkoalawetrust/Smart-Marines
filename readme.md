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
- They also have a rifle that they sometimes dorp, which you can pick up and use yourself.

## Improvements I want to make on them

- I noticed that there's a lot of marine taunt sprites, maybe I could make them taunt after killing something or seeing something die, such as making enemy marines have a chance to taunt after killing the player, or taunting after a large hostile monster like a Cyberdemon dies in their sight.
- Add the StayOnLift and AvoidHazards flags to the marines once the next GZDoom update that adds MBF21 support releases.
- Make them able to crouch across sectors with short ceilings, along with being able to crouch fire. I may not be able to do this though.
  - And of course if I can do it, then this should be toggleable as well.
- MAYBE I can give them some kind of cover system, that allows them to run to predetermined points in the map while fighting or running to reload.
  - I would need to somehow implement an actual pathfinding system of some kind, or use code for such a thing made by someone else. Since these marines still ultimately use (Z)Doom's brain dead AI, meaning they basically just randomly move around. Hence for example, why they just randomly run around to get out of their targets' sight and reload, instead of actually mapping a path to a location where their target cannot see them, and run to it.
  - As it stands currently, if I added a cover system with no pathfinding, it would suck because the marines wouldn't be able to actually go AROUND their cover and hide behind it, only go to its' general direction and then randomly move around, until MAYBE bypassing their own cover to go behind it.
- Improve the rifle they drop, due to being too busy playing Whack-a-Bug with the marines, I haven't be able to improve the rifles they drop to overall look, function, and feel better.
  - A more specific improvement I want to make on the rifle, is use overlays and all that good stuff to be able to zoom into the rifles' digital sights, with cool animated overlays and shit.
  - I wasn't able to mess with overlays because LZDoom, which I had to use on my old OptiPlex 760, doesn't fully support them yet. Which was an issue since I wouldn't be able to playtest the marines and rifle if I begun using and learning how to use overlays. Forcing me to have to playtest on the other PC I only had occasional access to. Not that it mattered at the end since my old PC ended up being too slow to even develop mods in a timely manner anymore.

# Note about the marines

Making just this basic version of them was an absolute nightmare, I begun work on them about 5 months ago or so, before I had my new PC, in that time I had to refactor them thrice because they got insanely buggy for some reason or another. And then, I lost access to the computer I used to develop my mods and make video showcases of them, and since my SFF OptiPlex 760 was too shit to be used for much of anything - I spent THREE MONTHS not being able to work on these marines or any major mod, until I finally got a new PC two weeks ago, and was able to continue working on my projects, starting with finishing these marines.

But as it turns out that would not be the end of it, after beginning to work on the marines on my new PC, I had to refactor them a fourth time due to the code being infested with bugs again, and then after working on the fourth iteration for 4-5 days, IT ALSO BROKE FROM TOO MANY BUGS.

Now, on my fifth iteration, I was finally fucking able to get AT LEAST the basic version to work without the AI going FUBAR **AGAIN**. I haven't even been able to work on many more of my projects, which I've amased a huge backlog of on my 3 month forced hiatus. And despite all that, because of how hard it was to even get the basic marine to work, I haven't been able to add the more advanced behaviour on them such as crouching and swimming. Or further work on the rifle they sometimes drop when killed.

It's pretty easy to tell how much of a huge pain the development of these marines has been, if you just look on the broken code folder, and how angry several of my comments are on the current, and some of the previous, iterations of the marines.
