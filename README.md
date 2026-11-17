# Heaven's Mandate: Tactics

A browser lane battler. Build hands of cards to 21, form Synergies, and send your army across the bridge.

**Build 7.3**: live online battles, members-only Synergies, a soldier cap, and more (see Changes below).

## Play

Open the GitHub Pages link for this repo (Settings → Pages). It's mouse or touch only.

- **Training Grounds**: play against the computer (Easy / Normal / Hard / Expert).
- **Skirmish**: join a random public room.
- **War Council**: host a room (private with a 4-letter code, or public), or join one by code.

## How online works

Players connect straight to each other through the browser (WebRTC via [PeerJS](https://peerjs.com)). The free PeerJS lobby server is only used to find each other.
The host's browser runs the battle; the other player's taps are sent to the host and their screen is mirrored so their own army is on the right.

Local testing: add `?net=local` to the URL and open two tabs of the same browser.

## Notes

- Guest profiles and match history are saved in your browser (playtest only).
- Sound effects are turned off in this build. The sound effect files (from Pixabay) are kept out of this repo because their license doesn't allow sharing the files on their own.
- Music was made with Suno.

## Changes since 7.0

- **Synergies:** Pair, Two Pair, Three and Four of a Kind boost only the slots that make them. All Synergy bonuses are doubled, including Monolith Vanguard (Flush).
- **Income:** 10 gold a second, minus 1 for every 2 soldiers on the bridge (never below 1).
- **SEND recharge:** 20s, then 10s from 7:00, always ready from 9:00.
- **Soldier cap:** 20 soldiers on the bridge, 35 from 9:00, 40 from 15:00. SEND shows BRIDGE FULL if your wave won't fit.
- **Lancer:** 190 HP and 10 damage. Cao Cao's charge stuns and knocks back the 3 closest enemies.
- **Barracks:** the card stack is now called the Barracks.
- **Interface:** units stack by rank (Celestial on top). The top-right counter shows enemy | your soldiers. Profile fixes and Settings → Text Size.
- **Locked content:** secret Synergies and late-match timeline entries unlock only by playing.
- Online players must be on the same build to find each other.
