# Sus Station

A multiplayer social-deduction game in the style of Among Us. It runs in the browser on phones and PCs.

## Put it online (GitHub Pages)
1. Upload everything in this folder to a GitHub repo, keeping the `css/` and `js/` folders.
2. Open the repo's **Settings → Pages**, choose **Deploy from branch** and pick `main` with `/ (root)`.
3. Open the HTTPS link. The microphone only works on HTTPS.
4. Tap **Create Room** and share the invite link. The host starts the game once enough players have joined.

## Test without internet
Open `index.html?local=1` in two tabs of the same browser. This uses an offline test mode. Voice chat is off in this mode.

## Files
| File | Contents |
|---|---|
| `js/maps.js` | The 5 maps (rooms, tasks, vents, sabotages) and the exact line-of-sight and visibility code |
| `js/render.js` | Floor art, lighting, ambient particles, and the soft-edged vision fog |
| `js/world3d.js` | 2.5D engine: walls with height and perspective, parallax backdrop, depth sorting |
| `js/postfx.js` | WebGL cinematic effects: bloom, colour grading, lens edge, film grain, alarm and impact flashes (toggle in Menu) |
| `js/cosmetics.js` | Colors, hats, visors, outfits, pets, and crewmate drawing |
| `js/host.js` | The game server, which runs in the host's browser: roles, kills, meetings, sabotage, bots |
| `js/net.js` | PeerJS peer-to-peer connections with auto-reconnect |
| `js/voice.js` | Proximity voice chat |
| `js/ui.js`, `js/tasks.js` | Interface screens and task mini-games |

## Optional: TURN server
Some strict mobile or office networks block direct peer-to-peer connections. If players can't connect, add a TURN server in `js/net.js`; the place to add it is marked with a comment in the `ICE` section.
