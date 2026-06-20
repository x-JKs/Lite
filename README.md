# Lite

Packet interception tool for Destiny 2. Single exe, no install, just run as admin and go.

## What it does

Intercepts game traffic at the port level. You can block, throttle, or buffer packets on each port independently. Comes with a reconnect feature that kills active TCP connections.

**Ports:**
- `3074` UDP — primary game traffic
- `30K` TCP — matchmaking
- `27K` UDP — voice/auxiliary
- `7500` TCP — telemetry

**Per-port settings:**
- DL / UL blocking with separate hotkeys
- Slow mode (delays packets instead of dropping them)
- Buffering (queues packets, releases when you untoggle)
- Auto-resync (reconnects when you stop blocking)
- Auto disable (unblocks when the game closes)

Also has an in-game overlay and auto-updates when a new version drops.

## How to use

1. Download `Lite.zip` from the [latest release](https://github.com/x-JKs/Lite/releases/latest)
2. Extract and run `Lite.exe` as administrator
3. Toggle DL/UL checkboxes to block traffic, click a port row to configure hotkeys and settings
4. Hit reconnect (or bind a hotkey) to kill game connections

## Requirements

- Windows 10/11 x64
- Run as administrator
