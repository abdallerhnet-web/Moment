# MOMENT

Turn your world into a game. A mobile-first, first-person night driving game that rebuilds the streets around you in 3D.

## How it works
1. **Capture** a photo. It sets the colours and mood of the night. It does not generate geometry.
2. **Locate** with GPS or typed `lat, lng`. Real roads and buildings come from OpenStreetMap (Overpass API).
3. **Reconstruct** roads, buildings, lamps and traffic in Three.js.
4. **Drive** with touch steering, GAS and BRAKE (or arrow keys / WASD). Hit 5 checkpoints for XP.

If location or map data is unavailable, a generated city seeded by the photo is used and the HUD says so.

## Run
Single static file, no build step. Serve `index.html` over HTTPS (GitHub Pages, Vercel, any static host). Camera and GPS need HTTPS.

## Limits
- One photo cannot reconstruct a neighbourhood. Streets come from map data; building heights are guessed unless tagged in OSM.
- No true road reflections yet; wet-road look is faked with light pools.
- Not yet profiled on low-end phones.

## Roadmap
- Snap spawn and checkpoints to named places / POIs
- Real height data and road surface types
- Proper cockpit model, reflections, engine and ambient audio
- Saved worlds and shareable missions
