# Heaven's Mandate: Tactics

A browser lane battler. Build hands of cards to 21, form Synergies, and send your army across the bridge.

**Build 9.7**: live online battles, members-only Synergies, a soldier cap, and more (see Changes below).

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
- **Income:** 10 gold a second with an empty bridge, sliding evenly down to 0 when your soldiers fill the bridge to the cap.
- **SEND recharge:** 15s, then 10s from 7:00, always ready from 9:00.
- **Card cost:** 10g, 15g from 12:00, 20g from 15:00.
- **Soldier cap:** 19 soldiers on the bridge, 20 from 7:00, 25 from 9:00, 30 from 12:00, and no limit from 15:00 (income still reaches 0 at 30 soldiers).
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
- **Base Strike (9.4):** the first enemy hit on a side's inner barricade switches it on. Then every 5s, hits on that barricade stun every enemy nearby for 1s. Once the barricade is broken, hits on the base stun them and take 5% of their max HP (armor soaks it first).
- **8.9 art:** chibi fortresses at both ends of the bridge (they show damage at 66% and 33% HP). Base Strike flashes a red seal on the gate and sends out a gold ink ring.
- **9.0 art:** each staging slot shows its suit's general (in gray). At 21 it shows the hero, in full color at Celestial. Huanglong's 500 hit now lands on the fortress.
- **9.1–9.2:** a plain "21" on Apex/Celestial slots. Soldier cap 19 before 9:00, and income reaches 0 at a full bridge.
- **9.5–9.6:** new How a Match Works pictures. Foot Soldier groups are now 5: 3 Foot Soldiers (3 dmg/hit) and 2 new Spear Soldiers (Lancer reach, 5 dmg/hit).
- **9.7:** from 9:00, soldiers move 50% faster on their own half of the bridge (was 25%).
- **Pause** against the computer (Options), and a **Computer** tab on your Profile with Easy / Normal / Hard / Expert records.
- **Locked content:** secret Synergies and late-match timeline entries unlock only by playing.
- Online players must be on the same build to find each other.
