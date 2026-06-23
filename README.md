# cs2-assets

Counter-Strike 2 art pulled from the game files - radar map images, kill feed icons, and a couple of UI bits. Handy for web radars, stat sites, overlays, or anywhere you need CS2 visuals without extracting them yourself.

Everything sits in the repo root. No build step, no folders to dig through.

## What's in here

### Map radar images

Top-down radar PNGs for active maps. Filenames follow the in-game pattern (`de_dust2_radar_psd.png`, etc.). Multi-level maps include a lower-floor variant.

- **Defusal (de_*)** - ancient (day, night, legacy v1), anubis, dust2, inferno, mirage, nuke, overpass, train, vertigo
- **Arms Race (ar_*)** - baggage, shoots (day and night)
- **Hostage (cs_*)** - italy, office

### Kill feed icons

SVG icons for special kill types and events:

- headshot, noscope, penetrate (wallbang)
- blind kill, smoke kill, smoke grenade impact
- in-air kill, revenge, domination
- suicide

### Other

- `icon-defuser_png.png` - defuse kit icon
- `radialgradient_png.png` - radial gradient overlay used in CS2 UI

## Stats

- Map radar images: 20
- Kill feed icons: 10
- Other PNGs: 2
- 32 asset files total

## Usage

**Web radar** - load the map PNG that matches the current map name. Pair with player coordinates from your data source and draw dots on a `<canvas>` or absolutely positioned divs. Multi-floor maps need the `_lower_` variant when players are on the lower level.

**Kill feed / stats UI** - reference the SVGs directly or inline them. They scale cleanly at any size.

**Direct links** - point at raw GitHub URLs:

```
https://raw.githubusercontent.com/huntiezz/cs2-assets/main/de_mirage_radar_psd.png
https://raw.githubusercontent.com/huntiezz/cs2-assets/main/icon_headshot.svg
```

**Map name lookup** - strip the `_radar_psd` suffix from the filename to get the map id (`de_mirage_radar_psd.png` -> `de_mirage`).

## Notes

- Images are PNG despite the `_psd` in the filename - that's just how Valve names them internally.
- Night variants exist for maps that ship them (ancient, shoots).
- Assets reflect whatever is in the current game build. New maps won't appear here until they're added manually.
