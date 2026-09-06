# Hookline — Windows playtest builds

Public download host for **Hookline**, a 2D grapple-hook team shooter (5v5, mid-match body swapping,
deterministic simulation with rollback netcode). Built with Godot 4.7.2. **Source code is private.**

## Download

Grab the newest archive from the [Releases page](../../releases/latest). Both players must use the same build.

## Get started

1. Extract the whole archive to a folder. Do not run the game from inside the archive viewer.
2. Open `Hookline.exe`. Keep `Hookline.pck` beside it. No Godot install is needed.
3. Practice mode works alone. If the normal launch reports a graphics-driver error, try `Play-Compatibility.cmd`.
4. Full host/join, port-forwarding and controls instructions are in `READ-ME-FIRST.txt` inside the archive.

## Controls

| Key | Action |
|---|---|
| WASD / Space | Move / jump (S drops through one-way platforms) |
| Mouse | Aim |
| Left mouse / E / R / Q | Primary / secondary / ultimate / held item |
| Hold right mouse | Grapple (release to drop); W/S reel, A/D pump the swing |
| 1-5, Tab | Select a teammate body, take/request/accept it |
| F11 or Alt+Enter | Toggle fullscreen |
| C | Free camera |

## Notes

- Multiplayer is ENet over UDP port 7777. The host forwards that port; the joining player does not.
- The build is unsigned. It changes no router or firewall settings.
- This is an early test build; the independent quality review is still open.

## Feedback

Open an issue with the build name, map and classes, who hosted, what you pressed, what happened and what you
expected. For crashes include `godot.log` from `%APPDATA%\Godot\app_userdata\Hookline\logs\`.
