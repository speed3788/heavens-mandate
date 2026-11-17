# Heaven's Mandate: Tactics

A browser lane battler. Build hands of cards to 21, form Synergies, and send your army across the bridge.

**Build 7.2**: live online battles, members-only Synergies, hold income, and more (see Changes below).

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
- **Hold income:** while SEND is charged and you hold, income rises +1/s every second, up to 10/s total before 9:00 and 20/s from 9:00. It resets when you send.
- **7:00 Assault:** SEND recharges in 10 seconds.
- **Top right counter:** shows enemy | your soldiers on the bridge.
- **Profile:** fixes, plus Settings → Text Size (Small / Medium / Large).
- **Locked content:** secret Synergies and late-match timeline entries now unlock only by playing.
- Online players must be on the same build to find each other.
