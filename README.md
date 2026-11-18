# Heaven's Mandate: Tactics

A browser lane battler. Build hands of cards to 21, form Synergies, and send your army across the bridge.

**Build 8.9**: live online battles, members-only Synergies, a soldier cap, and more (see Changes below).

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
- Sound effects: only CC0 (public domain) sounds are included: `stage.mp3` (7:00, 9:00, 12:00, 15:00), `minute.mp3` (each minute mark) and `hero_awaken.mp3` (you draw a Celestial 21) and `hero_enter.mp3` (a Celestial hero steps onto the bridge). Older Pixabay sound effects are kept out of this repo because their license doesn't allow sharing the files on their own.
- Music was made with Suno.

## Changes since 7.0

- **Synergies:** Pair, Two Pair, Three and Four of a Kind boost only the slots that make them. All Synergy bonuses are doubled, including Monolith Vanguard (Flush).
- **Income:** 10 gold a second, minus 1 for every 2 soldiers on the bridge (never below 1).
- **SEND recharge:** 15s, then 10s from 7:00, always ready from 9:00.
- **Card cost:** 10g, 15g from 12:00, 20g from 15:00.
- **Soldier cap:** 18 soldiers on the bridge, 20 from 9:00, 25 from 12:00. SEND shows BRIDGE FULL if your wave won't fit.
- **Tank:** 50 armor and Stand Firm (5% less damage for each extra enemy hitting it, up to 20%).
- **Healing:** Monolith Supports heal 6% every 3s (Five Tiger and Heaven's Mandate no longer heal).
- **Lancer:** 190 HP and 10 damage. **Vanguard:** 9 damage. Cao Cao's charge stuns and knocks back the 3 closest enemies.
- **Hero entrance:** a golden ink lightning bolt and shockwave ring (`fx/`) strike when a Celestial hero steps onto the bridge. The hero then lights up with the Celestial glow.
- **Barracks:** the card stack is now called the Barracks.
- **Match Time** on the Battle Report and in Match History.
- **Interface:** units stack by rank (Celestial on top). The top-right counter shows enemy | your soldiers. Profile fixes and Settings → Text Size.
- **How to Play:** unit cards show only the base stats; tap "Skills & Details" to open the rest.
- **Avatars:** 23 chibi avatars (`av/`). The Foot Soldier is open from the start, and the rest unlock by playing (hover a locked face for a hint; Synergy faces unlock only in online battles vs another player). Yours shows next to your base in battle, and your opponent sees it online. The computer is the Robot.
- **Expert computer (8.0):** counts cards, reads your waves and answers them, with less predictable timing.
- **8.1 balance:** Final Siege at 12:00 and Last Siege at 15:00. Five Tiger and Heaven's Mandate no longer heal, and Heaven's Mandate gets +30% Move Speed, ATK and ATK Speed. Armor Shred is replaced by armor: Dragon & Tiger +30%, Flowing Serpent +24%, Nine Dragons +24%, Emperor's +30%.
- **8.4:** each soldier you send shoves nearby enemies back once when it appears at your base. An "Avatar unlocked!" pop-up shows new avatars.
- **8.8 Base Strike:** once both of a side's barricades are broken, its base strikes back when hit: every enemy within 150px is stunned for 1s and takes 10 damage (5s cooldown).
- **8.9 art:** chibi fortresses at both ends of the bridge (they show damage at 66% and 33% HP). Base Strike flashes a red seal on the gate and sends out a gold ink ring.
- **Pause** against the computer (Options), and a **Computer** tab on your Profile with Easy / Normal / Hard / Expert records.
- **Locked content:** secret Synergies and late-match timeline entries unlock only by playing.
- Online players must be on the same build to find each other.
