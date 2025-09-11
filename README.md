# MC Mod Updater

**MC Mod Updater** helps you scan your Minecraft `mods/` folder, detect each mod and its loader, and download the latest compatible builds from Modrinth for a selected Minecraft version.

> Not affiliated with Mojang or Modrinth. Uses the public Modrinth API.

---

## Download

- **Windows installer (.exe)**: [Grab the latest release here](https://github.com/YOURNAME/mc-mod-updater-home/releases)  
- Portable zip (no install): same page.

> If you don’t see a release yet, I’m still packaging this build. Check back soon or open an issue.

---

## How it works (short)

1. Choose your existing `mods/` folder.
2. Pick a target Minecraft version (e.g., `1.21.3`).
3. The app looks up each mod on Modrinth and downloads the matching file into your chosen destination.
4. It never rehosts files — downloads come directly from Modrinth’s CDN.

---

## Features

- Detects Fabric / Quilt / Forge / NeoForge mods
- Pulls mod versions via Modrinth’s official API
- Slug resolver with metadata/link hints (handles cases like `ferritecore → ferrite-core`)
- Friendly errors (e.g., “No compatible 1.21.3 build”)
- Optional destination folder (keep your originals safe)

---

## System requirements

- Windows 10/11
- Internet access
- No separate Java install needed (bundled runtime)

---

## Usage

1. Launch the app.
2. Click **Select Mods Folder** and point to your `.minecraft/mods`.
3. Pick a version from the dropdown (e.g., `1.21.3`).
4. Click **Update**.
5. Watch the console/status list for:
   - **Downloaded** – saved to your chosen destination folder
   - **No compatible version** – try a nearby minor version, e.g., `1.21.2`

---

## Privacy

- **Default:** No telemetry is sent.
- If you opt in later, we may collect basic anonymous events (app start, number of mods scanned, downloads succeeded/failed) to improve reliability.
- No personal data, no PII. You can turn analytics off at any time in Settings.

---

## Support

- Open an issue: https://github.com/YOURNAME/mc-mod-updater-home/issues  
- Email: **support@YOURMAIL.COM**

---

## Known limitations

- Some projects may not have builds for the exact version you choose.
- Loader mismatches (e.g., trying Fabric for a Forge-only mod) won’t download.
- Discontinued mods (renamed/archived) may need manual replacement.

---

## Compliance & API etiquette

- Uses a unique **User-Agent**: `MC-Mod-Updater/VERSION (this page; support email)`
- Respects rate limits with throttle + backoff
- Downloads via official Modrinth file URLs only (no scraping, no rehosting)
- Honors project licenses; we don’t bundle third-party jars

---

## Changelog

### 0.1.0
- First prototype release: scanning, resolution, downloading, basic UI.

