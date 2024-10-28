# IWD:EE compatibility fixer

If you've played IWDEE with mod kits, you may have noticed many kits aren't actually compatible with IWDEE, even if they say they are. Kits will generally work, but they'll be missing IWDEE abilities, or in the case of druids or paladins, have completely wrong abilities.

I decided to do something about it (a long time ago, but only getting it done now). More details below.

--

Additional info (Kit mods):
-

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

--

Notes:
- Safe to install at end of order (i.e. if you notice something wrong after making a big install).
- Install after all kit mods (kits with correct abilities are skipped by installer).
- Uses 2DA_MISSING_COLS function by K4thos (https://github.com/K4thos/IE-code-repository)
