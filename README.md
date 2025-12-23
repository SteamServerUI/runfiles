# Runfiles for SteamServerUI

## 🛠️ The Runfile: Heart of SteamServerUI

A **runfile** is a JSON configuration file that tells **SteamServerUI (SSUI)** exactly how to launch and configure a dedicated game server. It defines:

- The game's metadata (name, images, etc.)
- Steam AppID
- Executable paths for Windows and Linux
- All command-line arguments with defaults, descriptions, and UI hints
- Optional backup directory and exposed config files

It specifies the game’s Steam App ID, executables, and command-line arguments, which SteamServerUI uses to launch and manage the server.

SteamServerUI reads this, builds the command-line args, and serves them up in the UI for easy tweaking. Want to run Valheim instead? Select Valheim from the UI's runfile libary, and you’re off to the races. SSUI handles the rest, no PhD in command-line wizardry required, writing a bash scrupt to run the game server will be a thing of the past.

With a gallery of well-written runfiles, users can select a game from SSUIs runfile gallery, tweak settings in a friendly UI, and launch the server — no manual command-line editing required.

## Runfiles Documentation
- [Home](https://github.com/SteamServerUI/runfiles/wiki)
- [Getting started](https://github.com/SteamServerUI/runfiles/wiki/Getting-started)
- [Best Practices](https://github.com/SteamServerUI/runfiles/wiki/Best-practises)

### Core Structure
- [Core Fields Reference](https://github.com/SteamServerUI/runfiles/wiki/Core-Structure)
- [Arguments Reference](https://github.com/SteamServerUI/runfiles/wiki/Arguments)
- [Special Arg Fields](https://github.com/SteamServerUI/runfiles/wiki/Special-arg-fields)

### Advanced Topics
- [Exposed Config Files](https://github.com/SteamServerUI/runfiles/wiki/Exposed-files)

### Complete Runfiles
- [Full Example](https://github.com/SteamServerUI/runfiles/wiki/Full-Runfile-Example)

### The Runfile gallery
- [Contributing to the runfile gallery](https://github.com/SteamServerUI/runfiles/blob/main/CONTRIBUTING.md)
