IWDEE compatibility fixer

If you've played IWDEE with mod kits, you may have noticed many kits aren't actually compatible with IWDEE, even if they say they are. Kits will generally work, but they'll be missing IWDEE abilities, or in the case of druids or paladins, have completely wrong abilities.

I decided to do something about it (a long time ago, but only getting it done now). There's also a component for Tome & Blood's Innate Metamagic (options 1 and 2). More details below.

Components:
1. Kit mods
2. Innate Metamagic (Tome & Blood)

----------------------------------------------------------------------------------------------------
----------------------------------------------------------------------------------------------------

Additional info (Kit mods):

Paladins:
- Gains IWD Detect/Protection From Evil (and removes BG2 versions if detected)
- Cure Disease is given if a kit gains Lay On Hands
- Gains disease immunity
- Gains fear immunity at level 3
- Blackguard is skipped
- Smite Evil is skipped (too many different kits with custom smite abilities)

Rangers:
- Gains Tracking at level 1

Thief:
- Gains Evasion at level 7

Druid
- Gains Timeless Body at level 15
- Gains poison immunity at level 9
- Removes BG2 abilities (resists, poison immunity, shapeshifts)
- Gains IWD shapeshifts (only if BG2 shapeshifts were detected)

----------------------------------------------------------------------------------------------------
----------------------------------------------------------------------------------------------------

Known Issue:

If the Artisan's Kitpack (v3.0) Paladin Overhaul is detected, no changes will be made to Detect Evil or Protection From Evil. The reason is the BG2 Detect Evil and the IWD Protection from Evil use the same filename (SPCL212.spl). Artisan's Kitpack changes the IWD file into Detect Evil and uses the BG2 filename for Protection From Evil (SPCL213.spl).

Haven't decided the best way to handle it, so I just left it alone for now. Note that other mod kits that expect SPCL212.spl to still be Protection From Evil will instead gain Detect Evil. My own paladin kits from The Workshop Kitpack are compatible, as long as they're installed after Artisan's Kitpack.

----------------------------------------------------------------------------------------------------
----------------------------------------------------------------------------------------------------

Innate Metamagic (Tome & Blood)

Note: According to subtledoctor, the level discrepancies from the Innate Metamagic component are intended. I prefer the abilities to be gained at the same time as the spell level, so I'm keeping the change.

- The following issues are in IWDEE:
	- Chain Contingency is unobtainable in pre-v0.9.42 versions of TnB (changed to an HLA, but game has no HLAs)
	- Bards don't get Spell Sequencer/Trigger, even though they get level 7 and 8 spells
	- Some abilities are gained at a different level than the spell level.

- This component does the following for IWDEE:
	- Mages and Sorcerers gain Chain Contingency at level 18 (no conflicts with the v0.9.42 update).
	- Bards gain Spell Sequencer at level 21 and Spell Trigger at level 29.
	- All abilities are gained at the same level that the spell level is gained (unmodded spell progression)

- Can also be installed for the BGEE games. Will only adjust the level discrepancies.

----------------------------------------------------------------------------------------------------
----------------------------------------------------------------------------------------------------

Notes:
- Uses 2DA_MISSING_COLS by K4thos (https://github.com/K4thos/IE-code-repository)

v0.7
- Paladin: Fear immunity will be correctly gained at level 3 (was at level 1)
- Fixed an issue that could cause abilities to not be added to kit table correctly.

v0.4
- Fixed WeiDU error when installed after TnB Revised Specialists.
- Will now check multiclass files (QD_MCD) for BG Druid abilities.

