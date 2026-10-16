# Panzer Corps · 坦克军团

An indie **hex-and-counter turn-based wargame for Android**, built with **Godot 4**.
This repository is the game's **release & auto-update channel**: it hosts the APK
releases and the `update.json` manifest the game checks on every launch.

## Download

Get the latest APK from the **[Releases](../../releases/latest)** page and install
it on your device — no store account required.

- Platform: Android (arm64-v8a), landscape.
- Just tap the downloaded APK; updates install over the previous version and
  **keep your profile, friends and settings**.

## Auto-update

On launch the game fetches `update.json` from this repository and shows an in-game
banner when a newer version is available:

```json
{
  "version": "1.3.0",
  "url": "https://github.com/tanfound-code/panzercorps/releases/download/v1.3.0/Panzercorps-1.3.0.apk",
  "urls": ["...official link + mirrors, tried in order..."],
  "notes": "What's new in this release",
  "mandatory": false,
  "min_version": ""
}
```

If the default sources are unreachable on your network, the update source can be
changed in-game: **Menu → Network → Update Source**.

## The game

Four campaigns:

| Campaign | Setting | Description |
|---|---|---|
| Alam el Halfa / El Alamein | North Africa, 1942 | Rommel's last offensive: take the two British strongpoints or the coastal road — in 4 turns |
| Operation Dynamo (Dunkirk) | France, 1940 | Scoring campaign: the BEF evacuates through five ports — seal them |
| Kharkov | Eastern Front, 1943 | Eight-turn scoring battle: retake cities, destroy Soviet units |
| Winter of Stalingrad | Eastern Front, 1942–43 | Hold the city against the relief offensive |

### Combat

Two classic tabletop systems, one per campaign:

- **CRT** — dice resolved on a Combat Results Table: odds-based attacks, terrain
  doubles defenders in towns and mountains, results from AE to EX.
- **A/D** — separate attacker/defender dice system used in the Stalingrad campaign.

Both feature **Zones of Control**, stacking, retreats, disruption, and a readable
battle log for every roll.

### Modes

- **Single player** vs AI — three difficulty levels (Easy / Normal / Hard).
- **Hot-seat** — two players share one device.
- **Multiplayer** — LAN / WAN rooms. The host creates a room and shares a short
  room code; the guest pastes it in and joins. Works over Wi-Fi (LAN discovery),
  IPv6 direct codes, or UPnP port mapping.

### Built for touch

Drag to pan, pinch to zoom, tap to select. Capturing an objective and choosing
retreat directions are done by tapping the map. Room codes are one-tap
copy/paste; the whole UI is sized for phones.

### Local-first profile & friends

No sign-up: a local profile (nickname, avatar, friend ID) is created on first
launch. Friend lists and online status ride along with the multiplayer
connection — no third-party server involved.

## Tech notes

- Engine: **Godot 4.7** (GL Compatibility renderer, GDScript).
- Package: `com.steelfront.panzercorps` (Android, arm64-v8a).
- Releases are built and published from a single script; the only file served to
  clients at runtime is `update.json`.

## Disclaimer

This is an independent, non-commercial project made for fun and for learning.
It is **not affiliated with, endorsed by, or connected to** any commercial
wargame, publisher, or trademark. Place names and map details are reconstructed
from publicly available historical references for educational purposes.

---

*Bug reports and suggestions are welcome — open an Issue.*
