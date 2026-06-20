# Lite

A lightweight Destiny 2 network tool for packet interception and connection management. Built with WinDivert and WPF on .NET 8.

## Features

- **Port-level control** — Block or throttle traffic on individual game ports (3074, 30K, 27K, 7500)
- **DL/UL separation** — Independent download and upload blocking per port
- **Slow mode** — Throttle packets with configurable delay instead of full blocking
- **Buffering** — Queue blocked packets and release them when you untoggle
- **Reconnect** — Kill active game connections via TCP RST injection
- **Auto-resync** — Automatically reconnect when blocking is disabled
- **Auto disable** — Unblock ports when the game exits
- **Hotkeys** — Global keybinds for every feature, assignable per port
- **In-game overlay** — Transparent click-through overlay showing active port status
- **Auto-updater** — Checks for new releases on startup with SHA256 verification
- **Single-file exe** — No installation, no dependencies, one portable executable

## Ports

| Port | Protocol | Range | Use |
|------|----------|-------|-----|
| 3074 | UDP | 3074 | Primary game traffic |
| 30K | TCP | 30000-30009 | Matchmaking / session |
| 27K | UDP | 27015-27200 | Voice / auxiliary |
| 7500 | TCP | 7500-7509 | Telemetry / services |

## Usage

1. **Run as administrator** — WinDivert requires elevated privileges
2. Ports appear in the main window with live DL/UL rates
3. Toggle the checkboxes to block traffic, or click a port row to open settings
4. Assign hotkeys, enable slow mode, buffering, or auto-resync per port
5. Use the reconnect button (or hotkey) to force-kill game connections

## Building

```
dotnet build -c Release -r win-x64 --self-contained
```

For an obfuscated release build:

```
.\build-protected.ps1
```

Output: `bin\publish\Lite.exe`

## Requirements

- Windows 10/11 (x64)
- Administrator privileges
- .NET 8 runtime (bundled in single-file build)

## License

This project is provided as-is for personal use.
