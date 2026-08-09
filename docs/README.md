# ONE STAR

ONE STAR is a browser-based multiplayer VR puzzle game built around a
ten-minute emergency scenario aboard a sealed observatory. Players must
solve station-specific puzzles and activate the reserve star before the
constellation collapses.

## Game Photos

<!-- Add screenshots here -->

## Features

- Desktop gameplay with interactive first-person controls.
- Mobile VR mode using a connected phone as a stereoscopic display.
- Automatic phone pairing through a QR code.
- Peer-to-peer communication using PeerJS and WebRTC.
- Synchronized game state between the laptop and connected phone.
- Synchronized game start so the laptop and phone enter the scenario together.
- Role-based specialist stations for multiplayer gameplay.
- Solo mode with access to all specialist roles.
- Interactive puzzle interfaces for the Engineer, Scientist, Explorer,
  and Navigator stations.
- Ten-minute countdown and emergency cinematic sequence.
- Browser-based deployment with no installation required.

## Run the shipped application

Open the deployed game URL in a supported desktop browser.

For production deployment, the application can be hosted as a static site
using Render.

The application is contained in a single `index.html` file and does not
require a backend application server for the game itself.

### Phone VR

To connect a phone:

1. Open the game on the laptop.
2. Select **CONNECT PHONE**.
3. The laptop automatically creates a phone session.
4. A QR code appears on the laptop.
5. Scan the QR code using the phone.
6. The phone automatically opens the game with the room information embedded
   in the URL.
7. PeerJS establishes the WebRTC connection.
8. The laptop displays **PHONE CONNECTED → VR READY**.
9. Starting the game synchronizes the laptop and phone.

The phone does not require manual room-code entry.

### First Launch

For production use, the game should be served over HTTPS.

This is important because browser VR, device-orientation, and related APIs
can be restricted when the page is opened directly from a local `file://`
URL.

## Build from source

Requirements:

- Modern Chromium-based desktop browser
- Modern mobile browser for phone VR
- Internet connection
- HTTPS deployment for production VR functionality

Clone the repository:

```bash
git clone https://github.com/your-username/one-star.git
cd one-star
```
