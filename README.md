# Recurved Leveling
Oblivion Leveling Mod

## Problem Statement
One of, if not the strongest ways to build a character in Oblivion is to choose skills you don't plan on using as Major Skills, and the skills 
you do want to use as your minor skills. This results in players focusing on leveling Minor Skills over Major Skills, limiting 
the rate at which you level up. Who wants to play an RPG where you try not to gain levels? Not me.

## Goals
This is yet another mod made in an attempt to improve upon the unintuitive process that is Oblivion leveling. When I started
I had one main goal in mind, the elimination of the minor skill metagame, as I found it tedious and unfun. As I worked on the mod, a few other
goals started to take shape.

1. The Major Skills you pick should be the Skills you use. Major Skills should be what define your character.
2. Minor Skills should still be useful to your character, but leveling only minor skills as your core skills should be heavily discouraged.
3. Leveling should be something to look forward to, not something to avoid.
4. Leveling should be a more organic process and not require excessive micro management to maximize attribute increases.

## Major Skills
Several changes have been made to further incentivize the selection, use and leveling of Major Skills.

- Leveling a Major Skill has a larger impact on attribute increases than a Minor Skill.
- Attributes have a secondary attribute associated to them. When a Major Skill increases in level, the secondary Attribute also has its progress increased. Example:
  ```
  Blade is increased by 1
  Progress towards Blade's primary attribute Strength is increased by 2
  Progress towards Strength's secondary attribute Speed is increased by 1
  ```
- Overlevel protection has been added to help prevent overleveling a Major Skill to the determent of other attributes.
- The amount of Major Skill increases requred for leveling up starts higher than vanilla at lower levels, to lower than vanilla at higher levels.
- Leftover skill points that are normally discarded during level ups are now carried forward to the new level.
- Total Major Skill increases prior to leveling up are limited to the maximum for the current level plus the maximum for the next level minus one. In other words, once your character has enough skill
increases to level, they can only continue to increase major skills up right until another level would be gained before sleeping and leveling up.

The largest change to Major Skills is the new overage protection system for attribute progress. When a Major Skill's Attribute reaches it's maximum progress for a level, all 
Major Skills that share that same attribute have their experience demands greatly increased. This remains in place until maximum progress for 3 attributes has been reached, 
or the character levels. In addition, a system of secondary attributes has been implemented to both further encourage the leveling of Major Skills and ease the management
of progress towards attribute increases.

### Attribute Overage Protection Example
Scenario*
```
Major Skills: Blunt, Blade, Heavy Armor, Block, Athletics, Acrobatics, Restoration
Attribute Progress /Skill: 2
Required Increases /lvl: 15
- 5 Levels gained in Blunt. +10 Strength Progress (2 per skill progress * 5 Major Skill increases = 10 Attribte Progress)
- Blunt and Blade experience requirements increase drastically for future levels.
- 3 Levels gained in Heavy Armor. +6 Endurance Progress
- 2 Levels gained in in Block. +4 Endurance Progress (10 total)
- Heavy Armor and Block experience requirements increase drastically for future levels.
- Restoration increases 5 levels. +10 Wisdom Progress
- 3 Attributes now have maximum progress. Experience penalities are removed for all major skills.
```
\* Increases to secondary attribute progress were left out to simplify the math, but they are included in the mod's calculation.

## Level Curves
Level tiers have been introduced in an attempt to creeate a more satisfying leveling curve. The base game allows for adjusting several level settings, but 
they apply to every level. If for instance, you want to increase the amount of skills needed to level early on when skills increase quickly,
but lower that amount progressively through the mid to later levels, there's not really a way to do that without exiting the game and enabling / disabling mods that adjust those 
settings. 

This mod adds 4 tiers to Oblivion for early, early-mid, mid and late-end levels. Early levels require more skill increases to level, but grant fewer attribute
points on level up. As skill increases slow down, mid levels reduce skill increases required to level while increasing Attribute gains per level. The later tier
builds upon this, further decreasing required skills and increasing attribute gains.

The reason for reducing attribute gains at lower level was for a couple reasons. The first, was to incentivise the player to level up to the 20's where attribute
gains increase. The second was to deter Minor Skill abuse as minor skill levels are softcapped by a combination of their attribute and character level.

### Level Curve Tiers
The below are the "out of the box" settings for the mod, but are fully configurable.
#### Tier 1: Levels 1 - 10
```
- Attributes have a maximum increase of 4 per level.
- 15 Major Skill increases are required per level.
- Leveling a Major Skill increases its Attribute skill points by 1, for a total of 2 (1 Mod Bonus + 1 Vanilla Base).
- Leveling a Major Skill increases its Secondary Attribute skill points by 1.
```
#### Tier 2: Levels 11 - 20
```
- Attributes have a maximum increase of 4 per level.
- 12 Major Skill increases are required per level.
- Leveling a Major Skill increases its Attribute skill points by 2 (for a total of 3).
- Leveling a Major Skill increases its Secondary Attribute skill points by 1.
```
#### Tier 3: Levels 21 - 40
```
- Attributes have a maximum increase of 5 per level.
- 10 Major Skill increases are required per level.
- Leveling a Major Skill increases its Attribute skill points by 2 (for a total of 3).
- Leveling a Major Skill increases its Secondary Attribute skill points by 1.
```
#### Tier 4: Levels 41 - 50
```
- Attributes have a maximum increase of 8 per level.
- 8 Major Skill increases are required per level.
- Leveling a Major Skill increases its Attribute skill points by 3 (for a total of 4).
- Leveling a Major Skill increases its Secondary Attribute skill points by 2.
```


## Minor Skills
Minor skills get roughed up a little by this mod, but still come through in ok shape. The main "nerf" is the introduction of soft caps to prevent leveling Minor Skills far
higher than Major Skills. Minor Skills can still be leveled to 100, but not at level 1.

### Soft Caps
Minor Skills have been soft capped to half thier governing attribute plus the character level.
#### Soft Cap Formula
`Soft Cap Level = Attribute / 2 + CharacterLevel`

Example:
```
Minor Skill: Acrobatics
Governing Attribute: Speed
Attribute Value: 40
Character Level: 10

40 / 2 + 10 = 30 Soft Cap
```
In the above example, Acrobatics can be increased to a skill level of 30 with the same effort as Vanilla.  However, once at that threshold the amount of experience required
is increased by a factor of 5 (configurable).