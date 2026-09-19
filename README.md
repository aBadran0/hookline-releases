# Hookline — playtest builds

Public download host for **Hookline**, a 2D grapple-hook team shooter (5v5, mid-match body swapping,
deterministic simulation with rollback netcode). Built with Godot 4.7.2 for **Windows and Linux** (x86_64). **Source code is private.**

## Download

Grab the archive for your OS from the [Releases page](../../releases/latest) — `Hookline-Windows-*.zip` or
`Hookline-Linux-*.zip`. Both players must be on the same release; a Windows player and a Linux player from the
same release can join the same match.

The 2026-09-19 (r8) beta is Windows only; the last Linux build is [r7](../../releases/tag/v2026.09.08-r7), which cannot
join r8 matches.

## Get started

1. Extract the whole archive to a folder. Do not run the game from inside the archive viewer.
2. Open `Hookline.exe` (Windows) or run `./Hookline.x86_64` (Linux). Keep `Hookline.pck` beside it. No Godot
   install is needed. On Linux, extract with `unzip` or your file manager so the executable bit survives;
   otherwise run `chmod +x Hookline.x86_64` first.
3. Practice mode works alone. If the normal launch reports a graphics-driver error, try `Play-Compatibility.cmd`
   on Windows or `./Play-Compatibility.sh` on Linux.
4. Full host/join, port-forwarding and controls instructions are in `READ-ME-FIRST.txt` inside the archive.

## Controls

| Key | Action |
|---|---|
| WASD / Space | Move / jump (S drops through one-way platforms) |
| Ctrl | Crouch (Space while crouched also drops) |
| Mouse | Aim |
| Left mouse / E / R / Q | Primary / secondary / ultimate / held item |
| Hold right mouse | Grapple (release to drop); W/S reel, A/D pump the swing |
| 1-9, 0, Tab | Unfold a teammate's icon in the bottom row, take/request/accept that body (free before the round starts) |
| Hold Caps Lock | Scoreboard |
| F11 or Alt+Enter | Toggle fullscreen |
| C | Free camera |
| Hover the PASSIVE cell | Read your class passive and idle-craft item |
| Escape | Settings (in a match: also LEAVE MATCH) |

These are the defaults. From r8 every binding can be changed in Settings > Controls. The same tab has
**Auto-reel while grappling** (off by default): the rope reels in on its own while you hold the grapple button; hold S to pause.

## Notes

- Multiplayer is ENet over UDP port 7777. The host forwards that port; the joining player does not. On Linux,
  allow inbound UDP 7777 if you run a local firewall (`sudo ufw allow 7777/udp`).
- Linux needs a glibc-based x86_64 distribution (Ubuntu 22.04 or newer and equivalents) with Vulkan or
  OpenGL 3.3 drivers.
- The builds are unsigned. They change no router or firewall settings.
- This is an early test build; the independent quality review is still open.

## Feedback

Open an issue with the build name, map and classes, who hosted, what you pressed, what happened and what you
expected. For crashes include `godot.log` from `%APPDATA%\Godot\app_userdata\Hookline\logs\` on Windows or
`~/.local/share/godot/app_userdata/Hookline/logs/` on Linux.
