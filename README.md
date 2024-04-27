# Recurved Leveling
Oblivion Leveling Mod

## Statement
This is yet another mod made in an attempt to improve upon the unintuitive process that is Oblivion leveling. When I started,
I had a few goals in mind. I wanted to cut down (or eliminate entirely) the minor skill metagaming. One of, 
if not the strongest ways to build your character is to choose skills you don't plan on using as Major Skills, and the skills 
you do want to use as your minor skills. This results in players focusing on leveling Minor Skills over Major Skills, limiting 
the rate at which you level up. Who wants to play an RPG where you try not to gain levels? Completely backwards.

1. Major Skills should be what define your character.
2. Minor Skills should still be useful, but metagaming should be heavily discourged. 
3. Leveling should be something to look forward to, not something to avoid.

## Major Skills
Several changes have been made to further incentivize the selection and leveling of Major skills.

- Increasing a Major Skill counts double towards attribute increases on level up.
- Attributes have a secondary attribute associated to them. On leveling up a Major Skill, the Skill's Attribute's seconday Attribute also progess increased. Example:
  ```
  Blade is increased by 1
  Progress towards Blade's primary attribute Strength is increased by 2
  Progress towards Strength's secondary attribute Speed is increased by 1
  ```
- Major Skills gain additional benefits from their primary attribute.

## Level Curves
Level tiers have been introduced in an attempt to smooth out the leveling experience. The base game allows for adjusting several level settings, but 
they apply to every level. If for instance, you want to increase the amount of skills needed to level early on when skills increase quickly,
but slow them down in mid to later levels, there's not really a way to do that without exiting the game and enabling / disabling mods that adjust those 
settings. This mod adds 4 tiers to Oblivion for early, early-mid, mid and late-end levels. Early levels require more skill increases to level, but grant fewer attribute
points on level up. As skill increases slow down, mid levels reduce skill increases required to level while increasing Attribute increases. The later tier
builds upon this, further decreasing required skills and increasing attribute gains.

The reason for reducing attribute gains at lower level was for a couple reasons. The first, was to incentivise the player to level up to the 20's where attribute
gains increase. The second was to deter Minor Skill abuse as minor skill levels are softcapped by a combination of their attribute and character level.


Strength -> Agility -> Intelligence -> Personality -> Willpower -> Endurance -> Speed -> Strength

Strength -> Speed -> Endurance -> Willpower -> Personality -> Intelligence -> Agility -> Strength

## Minor Skills

### Soft Caps
#### Soft Cap Formula
`Soft Cap Level = Attribute / 2 + CharacterLevel`