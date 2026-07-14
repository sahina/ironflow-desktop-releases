# Ironflow Desktop — Releases

Downloads for the **Ironflow Desktop** app.

- Website: https://ironflow.run
- Docs: https://docs.ironflow.run
- Getting started: https://docs.ironflow.run/tutorials/getting-started/
- Cloud: https://ironflow.run/cloud/
- All releases: https://github.com/sahina/ironflow-desktop-releases/releases
- **Latest release: https://github.com/sahina/ironflow-desktop-releases/releases/latest**

Download the installer for your OS from the **latest release** page, then follow the steps below.

> Availability by OS depends on which builds are attached to a given release. macOS (Apple Silicon) is available today; Windows and Linux builds appear on the release page as they ship.

## macOS

Apple Silicon (M1/M2/M3/M4).

1. Download `desktop-electron-<version>.dmg` (or `desktop-electron-<version>-arm64.zip`).
2. Open the `.dmg` (or extract the `.zip`) and drag **Ironflow Desktop** into **Applications**.
3. First launch: the app isn't notarized yet, so macOS Gatekeeper may block it. Right-click the app → **Open** → **Open**. If it still won't open, run:
   ```bash
   xattr -dr com.apple.quarantine "/Applications/Ironflow Desktop.app"
   ```

## Windows / Linux

Windows and Linux builds appear on the [release page](https://github.com/sahina/ironflow-desktop-releases/releases) as they ship. macOS (Apple Silicon) is the only build available today.

## Updates

The app auto-updates from this repository's releases. You can also grab any version manually from the [releases page](https://github.com/sahina/ironflow-desktop-releases/releases).
