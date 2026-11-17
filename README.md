# Heaven's Mandate: Tactics

A browser lane battler. Build hands of cards to 21, form Synergies, and send your army across the bridge.

**Build 7.0** — adds live online battles.

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
- Sound effects and music are from Pixabay.
