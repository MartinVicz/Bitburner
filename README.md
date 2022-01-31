# Bitburner
Set of JS scripts to play bitburner

# Scope of the project
1. Crawler script that lists all accessible servers, provides access to previously unacessible servers and searches for coding contracts.
2. Script that solves coding contracts without further user input necessary.
3. Hacking script that uses the commands hack, grow and weaken while taking under consideration the stock market exchange script via ports and the current state of the game (early, mid, late).
4. Script that uses the TIX API to automatically trade stocks and provides information for the hacking script via ports.
5. Script that purchases and upgrades servers.
6. Script that automatically provides the necessary requisites for selected factions (crime, corporation, hacking) by making use of the Singularity API, joins them and buys suitable augmentations.
7. Script that tracks progress and automatically installs augmentations as soon as progess plateaus.
8. Script that uses the corporation API (not unlocked yet)
9. Script that uses the sleeve API (not unlocked yet)


https://github.com/danielyxie/bitburner/blob/dev/markdown/bitburner.md

Considerations:
2. Coding Contracts
https://github.com/danielyxie/bitburner/blob/dev/doc/source/basicgameplay/codingcontracts.rst
Solution:
https://github.com/danielyxie/bitburner/blob/dev/src/data/codingcontracttypes.ts
3. Hacking script
 const growTimeMultiplier = 3.2; // Relative to hacking time. 16/5 = 3.2
 const weakenTimeMultiplier = 4; // Relative to hacking time
 Hint: Hacking creates Intelligence Exp
 IntelligenceTerminalHackBaseExpGain: 200, // Hacking exp divided by this to determine int exp gain
4. TIX API
https://github.com/danielyxie/bitburner/blob/dev/doc/source/basicgameplay/stockmarket.rst
6. Singularity API
https://github.com/danielyxie/bitburner/blob/8b69fd7faa5e29cd7d72f4bb8aad6e6c3f6cbf24/markdown/bitburner.singularity.md
Hint: Using the Singularity API creates Intelligence Exp
IntelligenceSingFnBaseExpGain: 1.5
purchaseAugmentation: *10
installAugmentation: *10
joinFaction: *5
travel: /50000
