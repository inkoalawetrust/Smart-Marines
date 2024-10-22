![](https://i.imgur.com/HKnzbLI.png)

>WARNING: THIS MOD REQUIRES THE [KAI LIBRARY](https://github.com/inkoalawetrust/KAI) TO WORK AT ALL. PREFERRABLY THE LATEST RELEASES, AT LEAST UNTIL THE MARINES ARE FINISHED.


# Smart Marines

Smart Marines are a drop in mod resource for mapsets and mods, that adds a very smart marine NPC (And more in the future) to Doom. Unlike vanilla Doom monsters, they move and behave very differently, running away from danger, dodging, taking cover, climbing, crouching, and much more.

### Features (There's a lot)
- Attacks
  - They know to generally avoid using certain attacks if they would be blocked by actors (e.g allies), projectile blocking lines, etc.
  - Can attack by firing their rifle (Duh), they can use different firemodes based on the actual chance of hitting their target:
    - Single Shots: Most accurate, has an effective range of around 300-500 meters. Mostly used when the chance of the rifle hitting is very low.
    - Burst Fire: Fires a 3 round burst. Decent accuracy, has an effective range of about 250 meters. Used when a lot of full auto shots will miss. This is likely to be the average fire mode on large maps.
    - Full Auto: Fires the whole magazine as fast as possible. Likely to be the average fire mode at close range. Marines fire in this mode if 12 or more of the shots would land, or if 6 or more would land if they are VERY low on health and desperate. They are also more likely to fire in this mode at dangerous enemies.
    - Marines reload every 30 shots they fire, and can also reload after a fight to not have to do it mid-battle.
    - In addition, they can sometimes decide to kneel or lie down to fire, which gives them an additional accuracy boost.
    - Marines can experience recoil when firing in full auto, which is reduced when kneeling, and entirely removed when lying down.
  - Have multiple melee attacks, which can also be buffed if the marine has a Berserk/strength powerup in their inventory. Marines normally avoid melee, but are more likely to commit to it if they have a Berserk pack.
    - Can smack enemies with the butt of their rifle. And push them away with Berserk too.
    - Can kick enemies, including sending them flying with Berserk. If within 8 meters of the target, they might sometimes run up to the enemy to kick them.
    - Can drop kick enemies around, sending them even further with Berserk. Is incrementally more likely to use this attack if the following conditions are met: The monster would fall off a ledge taller than its' own height (And therefore be likely to get stuck down there). And extra likely if the enemy would take fall damage from the fall. - But will avoid it if he's likely to fall off too, if the enemy can fly anyway, or if it's immune to the "Falling" damage type.
  - Can throw several types of grenades when in range (768 map units), being more likely to do so at crowds and/or dangerous enemies:
     - Smoke: Mostly throws them for concealment when retreating. But also sometimes throws them in crowds. In addition to of course reducing player visibility, they can actually affect monster aiming too for enemies that try firing through it, [using GZDoom flags I added myself](https://zdoom.org/wiki/Actor_flags#SHADOWBLOCK).
     - HE-FRAG: An explosive grenade with a frag sleeve, produces a normal explosion, but also spawns dozens of shrapnel hitscans that can harm enemies at a longer range. Marines are especially likely to throw these at NPCs immune or highly resilient to splash damage, so that the shrapnel will harm them instead, such as Cyberdemons.
     - High explosive: Doesn't produce shrapnel, but makes an even stronger and larger explosion. Marines can alternate between this and HE-FRAG. But will also especially be likely to use them for dangerous enemies that have no special explosion immunity or littke total resilience. Like [enemy tanks](https://github.com/inkoalawetrust/Military-Vehicles-Pack/wiki/Main-Battle-Tank) for example.
     - Flashbang: TBD
     - Marines are also likely to throw grenades if the enemy at hand is really resistant or immune at their rifles.
- The mod comes with a machine gun turret that can be used by both players, marines, and KAI humanoid NPCs in general. The turret mostly functions like it did originally (Except far more stable and reliably). But marines on turrets will also avoid all dogpiling on the same turret, will not go to it if its' too dangerous (Turret is in a hazard zone or dangerous projectiles are going towards it), and will also get off the turret if it gets too dangerous. The turret also offers a little bit of protection by reducing damage that hits the front of the turret by 20% for whoever is in it. 
- Can retreat away from danger, such as when an enemy gets too close, when a hazard is near, or when they need to reload. In addition to running away, they will also run behind corners if possible, like deliberately running behind a wall to reload. And will also try to run around obstacles.
	- Marines running away to reload account for both how dangerous their target is (i.e they will run pretty far from a Cyberdemon to reload, but not a Hell Knight). But they will also reduce how much they'll retreat based on how many allies and especially allies they share a group with are around them. This accounts both for the quantity of allies and also how individually power every ally is.
- Can detect and run away from [nearby hazards](https://github.com/inkoalawetrust/KAI/wiki/Hazard-system), or just walk around them if they are minor enough. Keep in mind these hazards have to be explicitly defined though.
	- Can run away from their own grenades. And from the attacks of [MVP vehicles](https://github.com/inkoalawetrust/Military-Vehicles-Pack/wiki/), alongside other threats like flaming wrecks, the front of moving tanks, etc.
	- Can detect and run away from KAI hazard zones in general, so they can also know to avoid hazards emitted from other KAI NPCs, map placed hazard zones, and so on.
	- They try to avoid getting too close to enemies, even more so if they're particularly dangerous.
- Marines friendly to you can be ordered to sit around when idle, wander off on their own, or follow the player. By pressing use on them. This will also cause them to begin following you instead of whatever other marine or NPC was their group leader. If you order a group leader, the order you gave the leader will propagate to all KAI NPCs following them.
- Friendly marines can walk up to, and give stimpacks to other friendly NPCs and players. With a customizable 40 second cooldown.
- Marines that have the night vision powerup in their inventory get +SEEINVISIBLE. Allowing them to perfectly aim through smoke screens and other shadow blockers, and aim at shadow/invisible actors normally.
- CAN CLIMB OVER LEDGES, CROUCH UNDER TIGHT SPACES, AND JUMP ACROSS GAPS SHORTER THAN 288 MAP UNITS. This is totally dynamic and should work on any arbitrary maps, and works with normal sectors, blocking actors, and 3D floors. However it might get them stuck sometimes, particularly in tight spaces with a bunch of stuff.
- Can dodge incoming projectiles by jumping out of the way, depending on how much space they have, like to avoid jumping off a cliff or into a wall. Unlike on the original marines, this should work a lot more reliably. They can also "dodge" homing projectiles by running away from them (And occasionally ducking under them if they get too close to try throwing them off), including running behind a corner if possible.
- Can alert other allied marines and KAI NPCs of any new target they've seen, as long as the other friend isn't busy with an existing target.
- Marines have several features when they're present in groups:
	- Marines in groups will take the order of their group leader (i.e if the leader is wandering around, all members are too).
	- They alert other NPC squadmates (Be they other marines, or other KAI NPCs in general, as long as they're not a KAI_Creature) of their target, unlike their alert of non-squad members, which has a set range, this particular alert has no range limit.
	- Marines in groups retreat even less even if their squadmates are even further away than their non-squadmate allies.
- Can take cover behind blocking actors and level geometry, or over ledges if the enemy is below (e.g rooftops). This works both incidentally (If they just happen to be near cover), but also. They will now actively run towards cover that is in front of them when fighting.
- They eventually stop chasing their target if it goes out of sight for more than ~30 seconds. To prevent them from constantly chasing something like a monster that teleported away.
- Marines have a chance to taunt powerful enemies after they shoot or (Especially) beat them to death, such as Cyberdemons and players. Including a low chance of teabagging the corpse.
- Marines have multiple death animations that can randomly play, including one for getting killed while crouched. They also play back correctly when the marine is resurrected.
- Can drop their rifle when killed, which can then be picked up by the player. It needs to reload, can zoom with the zoom key, and like the marines, you can also get a stacking accuracy buff by firing it while crouched.
- Most of their behavior is configurable through user variables. Which can also be used to give them custom colors and different armor.
- Includes a restriction zone that can be used to stop marines from performing certain actions like climbing. e.g to prevent marines from parkouring inside interiors and potentially getting stuck.
- Easter eggs.


### Spawn aliases
Marines have several alternate class names that can be used alongside the _summon_ and _summonfriend_ console commands, to spawn marines with specific attributes.

- SM_Marine_Berserk: Spawns a marine that already has a berserk pack.
- SM_Marine_Unarmored: Spawns a marine with night vision goggles, that allow him to see and shoot at shadow and shadow block actors without any aim penalty or chance of not detecting the enemy.
- SM_Marine_Unarmored: Spawns a marine that's not wearing any armor and just has 100 health. Kinda like the original marines.
- SM_Marine_BlueArmor: Spawns a marine that's wearing blue armor instead of green armor.
- SM_GigaMarine: Spawns a marine that wears blue armor, is actually colored blue, has a berserk pack, night vision, and has 200 health. [And is THREAT_DANGEROUS instead of THREAT_ABOVENORMAL](https://github.com/inkoalawetrust/KAI/wiki/Threat-assessment).

### CVARs
- SM_Disable_DoShadowBlock: [Works like the same CVAR on my MVP resource/mod.](https://github.com/inkoalawetrust/Military-Vehicles-Pack/wiki#global-mod-changes)
- SM_DumbHitCheck: If on, the marines will only determine the chance of their shots hitting a target using math and trigonometry, instead of actually firing hypothetical hitscan shots. Should be cheaper than the more accurate hitscan approach. And therefore possibly useful if a bunch of marines are lagging the game for some reason.

### User variables
- User_NoWeaponDrop: The marine never drops their rifle when killed.
- User_Color: Changes the marines' colors, typing "random" picks one randomly, supported colors are Red, Gray, White, Black, Blue, Yellow, Orange, Dark Green, Dark Reed, and Default (Can be passed as a color to reset the marines' translation).
- User_Armor: The armor item the marines are equipped with, the default is Green Armor. Can be any armor class, as long as it doesn't not work with monsters for some reason.
- User_IgnoreOrders: The marine will ignore orders from the player when they press use on it, or the MVP's radio item.
- More to be added as I finish coding the NPC.

### Marine restriction zone
(Write info here)

### Todo
This a list of all the major features that the marines are still missing as of 23/1/2024.

### New features (In order of difficulty)
* Make some kind of official addon that allows using the marines more like a gameplay mod, without them having to be integrated into any mods or maps. Like to replace certain items with beacons that teleport marines in.
* Add the ability for marines (Or rather KAI NPCs in general) to swim in swimmable 3D floors.
* Make additional marine types, like snipers and spotters, marines wielding ATGMs, juggernauts with chainguns and 200 health + Blue Armor, and combat engineers that can performn actions like placing landmines, destroying enemy landmines, digging foxholes, and repairing friendly KAI vehicles.
* Make new emplacements that players and marines can use, like foxholes, mortars, and tripod mounted ATGMs.