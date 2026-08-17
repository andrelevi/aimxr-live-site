# aimxr-web-assets

Sprite and image assets for AimXR web-facing surfaces (in-client store, dashboard, WebClient).

## Layout

- `consumables/` — consumable-item cards (XP booster, karma pack, etc.)
- `equipment/weapons/` — weapon + grenade + magazine skin cards
- `player/backgrounds/` — profile background videos (`.webm`)
- `player/badges/` — achievement/role badges
- `player/frames/` — avatar frames
- `warbonds/banners/` — warbond premium-track banners
- `maps/` — map preview thumbnails

## Conventions

- Lowercase `snake_case` filenames, type-prefixed (`badge_*`, `frame_*`, `map_*`, `skin_wpn_*`, `bg_video_*`).
- Where present, raster assets ship as `.png` + `.webp` pairs. Prefer `.webp` in web consumers; keep `.png` for Unity or legacy fallback.

## Source assets (not committed here)

Some items in this repo are **compressed derivatives** of uncompressed sources that live in other repos. When regenerating, pull from source rather than re-encoding the lossy copy:

| Asset | Source |
|---|---|
| `maps/map_<slug>_thumb.webp` | `AimXR_Android_Dev/Assets/AimXR/Textures/MapPreviewImages/<MapName>__map-preview-image.png` (full-size lossless PNG, 1920×1080 or 2048×1024). Thumbs are scaled to 400w preserving aspect, then encoded webp q85. |
