# Archetype Not Created Equal (ATNCE) - Latest Version 2.1

A Balanced Procedural Stat Mod for WOTC and LWotC

Unlike traditional NCE mods that can create "God-Soldiers or Soldiers where Stat combinations dont mean much," ATNCE uses a Static Probability Pool and a Biological Limit (3-Stat Cap). Soldiers are unique, diverse, and tactically distinct without breaking the early-game balance of Long War.

Key Features:

- Tiered Rarity: HP, Aim, and Mobility are weighted (D to A).
- No Power Creep: High-tier stats are limited to 3 per soldier.
- Archetypes: A 5% chance to find "Hero" recruits with guaranteed specialties.
- LWotC Optimized: Pre-configured for 13-17 Mobility and 55-75 Aim.

NOTE: If you are not playing LWOTC, update the XComATNCE.ini configuration and adjust the TierRanges. The only ones that need some change is the low and high ranges for HP and Mobility

# Why did I create this mod?

So when I was playing with LWNCE and Point Based NCE (PBNCE), both utilise a point based system, based on randomisation of how those points are allocated (to my understanding)

They both work by the way, however, I found they negelected relationships between stats and you could get very very poor combinations. Both attempted to resolve this through Point swapping and/or Chance to allocate i.e. they promoted certain stats via a chance. I also found it very confusing to configure their systems to work how I like, and in some cases it was impossible. I wanted to have a chance to relate stat 1 to stat 2 for example

What I did was look at their intentions and determined you can achieve the same behaviour using statistics and distributions, with a scaling system. They also have min and max values, with a baseline. In a way, the stats are already being manipulated into a range, which is very important to this mod as I used those ranges to determine the default distribution/weightings of values at certain tiers.

A-High, B-Above Average, C-Average, D-Below Avaerage => Each Tiers has a range of values that can be selected and a distribution is used to decded the chance of rolling one of the tiers.

The first thing I did was repliacte LWNCE and PBNCE outcomes using my algorithms. This worked as expected and was more intuitive to configure. All you need to set is Low, Good, and HIgh ranges and I will dynamically generate tier ranges. You can also easily make the game harder or easier with a few config changes.

The second part, Archetypes. This is where I differ again from LWNCE and PBNCE. Along with removing the points/swapping points algorithms, I introduced Archetypes to relate 2 skills together. This has a very low chance to roll (5%), but when it does, the Algorithm will treat Primary and Secondary stats as related and promote their values i.e. not random. Primary will have a chance to roll Tiers B to A, while Secondaries will get a chance to roll tiers C to A.

All other cases (Archetype is not triggered), at least 1 Primary stat must be a B or A, where B is heavily favoured (to roll an A you need to pray alot). A single primary stat is randonly selected for this initial step. Then we leave it up to fate (or your stat ranges and distribution that have been configured) to decide the rest of the stats :-)

To balance the Mod and ensure a NCE feel, each soldier has a LIMIT on the HIgh-Tiers that can roll (A or B). This again is the same idea as LWNCE or PBNCE, but in their cases, was achieved using a COST system, I am just being more open about it and applying a hard limit (default is 3)

At the end of this, you get NCE like normal (for 95% of soldiers), however, you will also see some times a soldier that has good HP with good mobility. Think of this like a Hybrif approach between NCE and HIdden Potential :-)

# Installation

1. Install via Steam or Download one of the Release zips from the github repo and extract into ..\Steam\steamapps\common\XCOM 2\XCom2-WarOfTheChosen\XComGame\Mods\
1.a - STEAM is easier
2. Ensure the mod is enabled in the XCOM 2 mod launcher.
3. Enable in SecondWave options [ATNCE] -> Enable
4. Start a new campaign for changes to take effect.
5. **CRITICAL** - You must disable Long Wars NCE Algorithms - and restart XCOM2 WOTC/LWOTC

..\Steam\steamapps\workshop\content\268500\2683996590\Config\XComLW_Toolbox.ini

[LW_Toolbox_Integrated.X2DownloadableContentInfo_LWToolbox]
bRandomizedInitialStatsEnabledAtStart=false

# Dependencies

- X2WOTCCommunityHighlander v1.30.4
- Better Second Wave Mod Support
- XCOM2 WOTC
- Must use the XCOM Alternative Mod Launcher (AML)


## License

Anyone can reuse this code. MIT Free Licence :-)



