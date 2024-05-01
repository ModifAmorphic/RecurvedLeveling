# Recurved Leveling

An Oblivion Leveling Overhaul Mod

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
4. Leveling should be a more organic process and not require excessive micro-management to maximize attribute increases.

## Tutorial

Quick note in regards to the tutorial. This mod specifically avoids running until the tutorial has been completed to avoid having to deal with changes to class and birthsigns. So if you don't see any difference after installing the mod
with a new character, that's why. This is not to discourage anyone from starting a new character. Quite the opposite. Starting a new character with this mod is highly recommended.

## Major Skills

Several changes have been made to further incentivize the selection, use and leveling of Major Skills.

- Leveling a Major Skill has a larger impact on attribute increases than a Minor Skill.
- Attributes have a secondary attribute associated with them. When a Major Skill increases in level, the secondary Attribute also has its progress increased. Example:

  ```
  Blade is increased by 1
  Progress towards Blade's primary attribute Strength is increased by 2
  Progress towards Strength's secondary attribute Speed is increased by 1
  ```

- Overlevel protection has been added to help prevent overleveling a Major Skill to the detriment of other attributes.
  - Major Skills that have advanced enough to achieve the maximum attribute gain possible for the level have their experience demands increased until 2 other attributes can also be maxed.
  - Progress of all Major Skills will be stopped completely if a character is about to level up but has not maximized bonuses for at least 3 attributes.
- The amount of Major Skill increases required for leveling up starts higher than vanilla at lower levels and reduces to lower than vanilla at higher levels.
- Leftover skill points that are normally discarded during level-ups are now carried forward to the new level. *Secondary Bonus Attribute points do not carry forward.
- Total Major Skill increases before leveling up are limited to the maximum for the current level plus the maximum for the next level minus one. In other words, once your character has enough skill
increases to level, they can only continue to increase major skills up right until another level is gained before sleeping and leveling up.

The largest change to Major Skills is the new overage protection system for attribute progress. The system starts checking for major skill overages after enough progress has been made in a level where at least one attribute bonus should be maxed. When a Major Skill's Attribute reaches its maximum progress for a level, all
Major Skills that share that same attribute have their experience demands increased. The experience demands increase exponentially for any major skill increase from that point. This penalty remains in place until maximum progress for 3 attributes has been reached,
or the character levels. As an additional failsafe, a character that has not achieved maximum bonuses for at least 3 attributes by the end of a level will have all Major Skill progress
stopped. This gives the player a chance to gain additional progress through minor skills and not miss out on any potential attribute increases. This restriction is lifted once a maximum bonus has been reached for 3 attributes, allowing leveling to continue.

### Attribute Overage Protection Examples

#### Scenario 1 - Slowed Progress for Maxed Attribute Bonuses

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


#### Scenario 2 - Progress Stopped

```
Major Skills: Blunt, Blade, Heavy Armor, Block, Athletics, Acrobatics, Restoration
Major Skill Increases: +3 Blade (Strength), +2 Blunt (Strength), +4 Heavy Armor (Endurance), +2 Athletics, +3 Restoration (Wisdom)
Minor Skill Increases: +5 Armorer (Endurance)
Attribute Progress /Skill: 2
Required Increases /lvl: 15

- +3 Blade and +2 Blunt result in 10 progress increases total, enough to receive the maximum strength bonus on level up.
- +4 Heavy Armor and +5 Armorer result in 13 Endurance progress, enough to receive the maximum endurance bonus.
- +2 Restoration and no increases from minor skills results in 2 attribute progress, short of the 10 required for the full speed bonus.
- +3 Restoration and no increases from minor skills results in 6 attribute progress, short of the 10 required.
- Major Skill increases total 14 / 15 required for level up. All Major Skills are locked and can no longer increase in level.
- Character then levels Destruction four times.
- 4 Destruction + 6 Restoration = 10 Wisdom Bonus. 3 Attributes are now at maximum and Major Skill leveling is unlocked again.

```

## Minor Skills

Minor skills get roughed up a little by this mod, but still come through in ok shape. The main "nerf" is the introduction of soft caps to prevent leveling Minor Skills far
higher than Major Skills. Minor Skills can still be leveled to 100, but not at level 1.

### Soft Caps

Minor Skills have been soft-capped to half their governing attribute plus the character level. Skill specialization and racial bonuses do not count towards the soft cap,
allowing a character to exceed the soft-cap level before encountering experience penalties.

#### Soft Cap Formula

`Soft Cap Level = Attribute / 2 + CharacterLevel`

Example:

```
Race:           Argonian (+10 Athletics)
Minor Skill:    Athletics 
Specialization: Combat (+5 Athletics)
Attribute:      Speed
Speed Value:    50
Char Level:     1

50 / 2 + 1 = 26 Soft Cap (Base)
10 (racial bonus) + 5 (specialization) + 26 (Base) = 41 Modified Soft Cap
```

In the above example, Athletics can be increased to a skill level of 41 with the same effort as Vanilla.  However, once that threshold is hit the amount of experience increases by drastically for 
future skill levels (5x by default).

## Level Curves

Level tiers have been introduced in an attempt to create a more satisfying leveling curve. The base game allows for adjusting several level settings, but
they apply to every level. If for instance, you want to increase the amount of skills needed to level early on when skills increase quickly,
but lower that amount progressively through the mid to later levels, there's no way to do that without exiting the game and enabling / disabling mods that adjust those
settings.

This mod adds 4 tiers to Oblivion for early, early-mid, mid and late-end levels. Early levels require more skill increases to level, but grant fewer attribute
points on level up. As skill increases slow down, mid-levels reduce skill increases required to level while increasing Attribute gains per level. The later tier
builds upon this, further decreasing required skills and increasing attribute gains.

The reason for reducing attribute gains at lower levels was for a couple of reasons. The first was to incentivize the player to level up to the 20's where attribute
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

## Load Order / Compatibility

This mod does everything with scripts.