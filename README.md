# Heaven's Mandate: Tactics

A browser lane battler. Build hands of cards to 21, form Synergies, and send your army across the bridge.

**Build 12.8**: Zhuge Liang advises you during battle, avatars shout their Synergy in an ink speech bubble, the battle turns sideways by itself on an upright phone, the loading screen shows the battlefield, a tutorial arrow, Graphics in the in-game ⚙ menu, bigger menu text, seven battlefields with their own songs, live online battles, and more (see Changes below).

## Play

Open the GitHub Pages link for this repo (Settings → Pages). It's mouse or touch only.

- **Training Grounds**: play against the computer (Easy / Normal / Hard / Expert).
- **Skirmish**: find a random opponent. Joins an open public room, or pairs you with another player who is searching (random battlefield, the battle starts by itself).
- **War Council**: host a room (private with a 4-letter code, or public), or join one by code.

## How online works

Players connect straight to each other through the browser (WebRTC via [PeerJS](https://peerjs.com)). The free PeerJS lobby server is only used to find each other.
The host's browser runs the battle; the other player's taps are sent to the host and their screen is mirrored so each player sees their own army on the left, marching right.

Local testing: add `?net=local` to the URL and open two tabs of the same browser.

## Notes

- Guest profiles and match history are saved in your browser (playtest only).
- Sound effects: only CC0 (public domain) sounds are included: `stage.mp3` (7:00, 9:00, 12:00, 15:00), `minute.mp3` (each minute mark) and `hero_awaken.mp3` (you draw a Celestial 21) and `hero_enter.mp3` (a Celestial hero steps onto the bridge). Older Pixabay sound effects are kept out of this repo because their license doesn't allow sharing the files on their own.
- Music: original soundtrack by patokeem, composed with Suno. Each battlefield has its own song (`snd/music_battle.mp3`, `snd/music_b1.mp3` to `music_b6.mp3`).

## Changes since 7.0

- **Synergies:** Pair, Two Pair, Three and Four of a Kind boost only the slots that make them. All Synergy bonuses are doubled, including Monolith Vanguard (Flush).
- **Income:** 10 gold a second with an empty bridge, sliding evenly down to 0 when your soldiers fill the bridge to the cap.
- **SEND recharge:** 15s, then 10s from 7:00, always ready from 9:00.
- **Card cost:** 10g, 15g from 12:00, 20g from 15:00.
- **Soldier cap:** 19 soldiers on the bridge, 20 from 7:00, 24 from 9:00, 25 from 12:00, and no limit from 15:00 (income still reaches 0 at 25 soldiers).
- **Tank:** 50 armor and Stand Firm (5% less damage for each extra enemy hitting it, up to 20%).
- **Healing:** Monolith Supports heal 6% every 3s (Five Tiger and Heaven's Mandate no longer heal).
- **Lancer:** 190 HP and 10 damage. **Vanguard:** 9 damage. Cao Cao's charge stuns and knocks back the 3 closest enemies.
- **Hero entrance:** a golden ink lightning bolt and shockwave ring (`fx/`) strike when a Celestial hero steps onto the bridge. The hero then lights up with the Celestial glow.
- **Barracks:** the card stack is now called the Barracks.
- **Match Time** on the Battle Report and in Match History.
- **Interface:** units stack by rank (Celestial on top). The soldier counts sit beside the clock: yours on the left, the enemy's on the right. Profile fixes and Settings → Text Size.
- **How to Play:** unit cards show only the base stats; tap "Skills & Details" to open the rest.
- **Avatars:** 23 chibi avatars (`av/`). The Foot Soldier is open from the start, and the rest unlock by playing (hover a locked face for a hint; Synergy faces unlock only in online battles vs another player). Yours shows next to your base in battle, and your opponent sees it online. The computer is the Robot.
- **Expert computer (8.0):** a fourth, toughest level. Win 10 matches on Hard to unlock it.
- **8.1 balance:** Final Siege at 12:00 and Last Siege at 15:00. Five Tiger and Heaven's Mandate no longer heal, and Heaven's Mandate gets +30% Move Speed, ATK and ATK Speed. Armor Shred is replaced by armor: Dragon & Tiger +30%, Flowing Serpent +24%, Nine Dragons +24%, Emperor's +30%.
- **8.4:** each soldier you send shoves nearby enemies back once when it appears at your base. An "Avatar unlocked!" pop-up shows new avatars.
- **Base Strike (9.4):** the first enemy hit on a side's inner barricade switches it on. Then every 5s, hits on that barricade stun every enemy nearby for 1s. Once the barricade is broken, hits on the base stun them and take 5% of their max HP (armor soaks it first).
- **8.9 art:** chibi fortresses at both ends of the bridge (they show damage at 66% and 33% HP). Base Strike flashes a red seal on the gate and sends out a gold ink ring.
- **9.0 art:** each staging slot shows its suit's general (in gray). At 21 it shows the hero, in full color at Celestial. Huanglong's 500 hit now lands on the fortress.
- **9.1–9.2:** a plain "21" on Apex/Celestial slots. Soldier cap 19 before 9:00, and income reaches 0 at a full bridge.
- **9.5–9.6:** new How a Match Works pictures. Foot Soldier groups are now 5: 3 Foot Soldiers (3 dmg/hit) and 2 new Spear Soldiers (Lancer reach, 5 dmg/hit).
- **9.7:** from 9:00, soldiers move 50% faster on their own half of the bridge (was 25%).
- **9.9:** a secret avatar (a black silhouette until you unlock it), and a Code box in Settings → About.
- **10.0:** fix: the face-up Barracks card from a match that reached 12:00 no longer stays on screen in your next match.
- **10.1:** the High-Hand bonus is gone. Fortified soldiers now gain +2% (was +1%) HP, damage, armor and ATK speed for each number above 17.
- **10.2:** Easy, Normal, Hard and Expert now play very differently. Avatars show next to names in the room lobby, the VS screen, the Battle Report and Match History. The secret avatar takes longer to unlock.
- **10.3 art:** new chibi menu art (`menu/`): a bridge banner with a brush-ink 天命 title on Play, pictures behind the Play cards, and scenery banners on Profile, Rank, Synergies and How to Play. A Ranked card is on the Play page (coming soon).
- **10.4:** the opponent's color is now a muted red (was blue), the Play banner has the red fortress on the left and green on the right, your name and HP sit higher on the battle screen, and online your own soldiers' HP bars show your color.
- **10.5:** the enemy's name and HP sit at the same height as yours.
- **10.6:** a new look. The menus are now pale rice paper with ink-wash paintings (the chibi art is gone from the menus), the title screen shows the brush 天命, and the battle has a painted valley with a stone bridge. Synergies appear on brushstrokes colored by level (black, indigo, red, gold), Monolith Vanguard gets its own stroke, and Send is a sword that shows how many slots you have ready. Smoother play when the bridge is crowded.
- **10.7:** a march-order bar under the bridge shows each of your waves' Synergy front to back and drops it when that wave is beaten (the enemy's shows above their slots). Victory and Defeat appear on brush banners, in game and on the Battle Report. The gear moved to the bottom right, the How a Match Works pictures show the new look, and several menu banners and cards were tidied.
- **10.8:** while you build a hand, the Synergy under SEND shows its name, then the poker hand and the wave's DPS, then each bonus in its own colored box (same colors as the Synergies page). The emoji are gone: buttons use plain words, and the gear and locks are ink drawings. The gear is back in the top right.
- **10.9:** Heaven's Mandate, Nine Dragons Convergence and Emperor's Sovereign Army now list every bonus in their boxes, and any Synergy stacked with Monolith Vanguard shows Monolith's +20% HP/ATK. Only the labels changed: the game already gave these bonuses.
- **11.0:** the soldier counts moved beside the clock (enemy left, yours right), and game pop-ups now show at the top right next to the gear so they don't cover the enemy. Your march-order bar sits evenly between the bridge and your slots. The Battle Report wave columns line up (Synergy left, hand centered, DPS right). The Play card titles sit on the bottom of the picture, with no hard line under the art.
- **11.1:** fixed a wave showing up twice in the march-order bar (its first soldier was counted with the wave before), and free soldiers no longer show there. The Unlock pop-up now uses the rice-paper look.
- **11.2:** you now start on the left and march right (the enemy is on the right); the Play banner is flipped to match. New How to Play and Synergies cards sit under War Council. Victory / Defeat banners show just one word (SURRENDER when you give up), in the same font as BATTLE START.
- **11.3:** a Tutorial (Training Grounds, above Easy, or the Tactics page): Zhuge Liang walks you through one battle step by step, with set cards, no timer, one weak enemy wave and a Full House finish. Finishing it unlocks the Foot Soldier avatar; until then everyone starts with a blank 天命 avatar. New players are offered the Tutorial once. How to Play is now called Tactics, and the Play page's War Council card art fills the card.
- **11.4:** bigger menu text; Text Size now starts on Large and adds Extra Large. On phones the top tabs fold into a ☰ menu. The Golden Dragon avatar now needs 88 top-tier Synergy waves (was 10) and swaps places with the Robot. Fixed the march-order bar showing "No Synergy" once a wave's Synergy soldiers fell.
- **11.5:** Monolith Vanguard is now a Level 3 Synergy (red brush and red march-bar tag). The game can play a sound for each Synergy level when a Synergy first appears under SEND (those sound files aren't in this public version). Battle music is a touch quieter.
- **11.6:** on narrow screens the Settings sliders and Text Size buttons stack under their labels. Some battle sounds were rebalanced.
- **11.7:** seven battlefields, each with its own painting and song: Misty Valley, Red Cliffs, Bamboo Valley, Snowy Pass, Plum Blossom Spring, Autumn Gorge and Thunderstorm Peaks. Each computer level has its own (Easy Bamboo Valley, Normal Red Cliffs, Hard Autumn Gorge, Expert Snowy Pass; the Tutorial uses Misty Valley). Online, the host picks one (or Random) at the bottom of the room page. Settings → About credits the music to patokeem. On phones, the Synergies page rules sit under each name and the avatar picker scrolls and opens above the top bar. Waves with no Synergy no longer get a tag on the march-order bar, and the computer's wave numbers no longer skip. The loading screen shows only the quote, plus a reminder to turn your screen sideways when a phone or tablet is held upright.
- **11.8:** new battlefield songs: Misty Valley keeps the original battle theme; Red Cliffs, Bamboo Valley, Snowy Pass, Plum Blossom Spring, Autumn Gorge and Thunderstorm Peaks each get a new pairing.
- **11.9:** if two players tap Skirmish and nobody is hosting, they are put in a game together on a random battlefield, with no Start button needed. Each searcher quietly waits in a hidden queue slot while checking for others. If the opponent leaves before the battle, you go back to searching. Both players need 11.9.
- **12.0–12.2:** the Tactics page is now 5 picture buttons (Tutorial starts the tutorial; How a Match Works; Cards; Units, Heroes and Rank; Tactician's Tips). New **Graphics** setting in Settings (Full / Balanced / Performance / Auto; phones and tablets start on Balanced) for less lag with a crowded bridge, and the Show DPS Numbers switch now works. **Monolith Vanguard** now scales with the Synergy it's combined with: +10% HP/Armor/ATK alone, +20% with a Pair or Three of a Kind, +25% with Two Pair or Four of a Kind, +30% with a Full House, +35% with Five of a Kind or Heaven's Mandate (its suit bonus grows the same way), and that other Synergy now boosts the whole wave. **Nine Dragons Convergence** is now ×1.25 and **Emperor's Sovereign Army** ×1.5.
- **12.3:** Graphics now starts on **Auto** on every device, and there's a new lowest option, **No Animations** (soldiers slide along without animating; no effects, glows, shadows or damage numbers). Auto never drops below Performance by itself. The **Synergies** tab moved under **Tactics** as its own button; the Tactics order is now Tutorial, How a Match Works, Units, Heroes and Rank, Cards, Synergies, Tactician's Tips.
- **12.4:** the Pause pop-up says "Resume" (no emoji). The Robot avatar now needs 10 Expert wins in a row (a loss or surrender starts the count over; anyone who already has it keeps it). Removed three lines from the Unlock pop-up, the Voice Lines row in Settings, and the small note under the host room's Battlefield picker.
- **12.5:** ♦ slots are now orange and ♠ slots blue (yours and the enemy's). The stone bridge runs edge to edge and the old ink towers are gone. "REINFORCE THE RANKS" under SEND is bigger. In the Tutorial, a bouncing gold arrow points at what to tap (or hovers over your marching soldiers), the Next button glows gold when it's time to tap it, and glow boxes only show when you need to tap. The in-game ⚙ pop-up adds Graphics and Show DPS Numbers (tap outside it to go back to the battle). On a phone or tablet held upright, the battle turns sideways by itself (menus stay upright); on Android it also goes fullscreen and locks to landscape. The loading screen fills with the battlefield painting, with the info on a cream box and the battlefield's name at the bottom. Menu, Tactics, Profile, Settings and pop-up text is never smaller than 15px.
- **12.6:** when a wave with a Synergy marches out, that side's avatar shouts the Synergy's name in a small ink-brush speech bubble over their name (yours and the enemy's, also online; long names and Flush combos use two lines). It replaces the Synergy pop-up in the top right. The enemy's march-order bar under the timer is now half see-through so it doesn't pull your eye.
- **12.7:** Profile → Computer has an **All** button (picked first) that adds up every game vs the computer; the stat boxes, Career Stats and Match History now all follow the level you pick. The Tutorial button in the Training Grounds pop-up is gold. On phones and tablets, Settings → Text Size and Graphics are lists with one choice per row (✓ marks yours).
- **12.8:** Zhuge Liang now gives every battle message ("BUST!", "APEX RANK!", reminders) in an ink speech bubble beside the timer; it stays about 2 seconds and fades. VICTORY / DEFEAT keep their banner. New Settings switch **Zhuge Liang's Counsel** turns these messages on or off. Settings → Text Size and Graphics are now drop-down menus on every screen.
- **Pause** against the computer (Options), and a **Computer** tab on your Profile with Easy / Normal / Hard / Expert records.
- **Locked content:** secret Synergies and late-match timeline entries unlock only by playing.
- Online players must be on the same build to find each other.
