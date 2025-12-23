# The Runfile Gallery in SteamServerUI

## What is the Runfile Gallery?

The Runfile Gallery is a built-in feature of SteamServerUI that lets users browse and download community-created runfiles directly from within the application.

- **Hosted on GitHub Pages:** https://steamserverui.github.io/runfiles/
- **Central manifest:** `manifest.ssui` (JSON array of available runfiles)
- **Individual runfiles:** `run<GameName>.ssui` files

When you open the gallery in SSUI:

1. It fetches the latest manifest
2. Filters entries based on your SSUI version and OS
3. Shows compatible runfiles with pretty backgrounds, logos, and details
4. One-click download → places the runfile in your local runfiles folder and selects it

> [!NOTE]
> The gallery automatically adds the current OS to each entry and filters recommended settings/plugins accordingly.

## Gallery Features

- **Version compatibility:** Each entry has `min_version` — skipped if your SSUI is too old
- **OS support:** `supported_os` can be `"all"`, `"linux"`, `"windows"`, or `"untested, all"`
- **Recommended settings:** Optional hints for SSUI settings (e.g., enable BepInEx or SSCM)
- **Recommended plugins:** Suggest useful SSUI plugins for that game - for Example, we have a custom Backup manager for Stationeers based on the implementation in [StationeersServerUI](https://github.com/SteamServerUI/StationeersServerUI)

## Manifest Fields (for Contributors)

```json
{
  "name": "Stationeers",                  // Display name (can have spaces)
  "filename": "runStationeers.ssui",     // Exact filename on server
  "version": "3.0",                      // Your runfile version
  "background_url": "https://...",       // Header/banner image
  "logo_url": "https://...",             // Square icon/logo
  "supported_os": "all",                 // "all", "linux", "windows", or "untested, all"
  "min_version": "7.0.0",                // Minimum required SSUI version (x.y.z)
  "recommended_settings": [ ... ],       // Optional SSUI setting hints. See Stationeers runfile for full reference.
  "recommended_plugins": [ ... ]         // Optional plugin suggestions. See Stationeers runfile for full reference.
}
```

### recommended_settings example

```json
{
  "name": "IsBepInExEnabled",
  "boolValue": true,
  "supported_os": "all"
}
```

**Supported types: `intValue`, `boolValue`, `stringValue`**

### recommended_plugins example

```json
{
  "name": "StationeersBackupManager",
  "supported_os": "linux"
}
```

## Contributing to the Gallery

The gallery is community-driven! To get **your** runfile added:

1. Create a high-quality runfile following the documentation
3. Submit a request via:
   - Pull request to the gallery repository (preferred)
   - Or open a ticket on the SteamServerUI Discord server.
We do NOT accept externally hosted runfiles in the Gallery for security reasons.

> [!TIP]
> Include good background/logo URLs (Steam store assets work great) and test thoroughly.

We review submissions for quality, compatibility, functionality and security before adding them to the gallery. Providing proof of functionality (screenshots, videos) is appreciated and encouraged.

**Thank you for contributing — you make server hosting easier for everyone!**
