# Ironflow Desktop — Releases

Downloads for the **Ironflow Desktop** app.

- Website: <https://ironflow.run>
- Docs: <https://docs.ironflow.run>
- Getting started: <https://docs.ironflow.run/tutorials/getting-started/>
- Cloud: <https://ironflow.run/cloud/>
- All releases: <https://github.com/sahina/ironflow-desktop-releases/releases>
- **Latest release: <https://github.com/sahina/ironflow-desktop-releases/releases/latest>**

Download the installer for your OS from the **latest release** page, then follow the steps below.

**Before you download:** check the [system requirements](https://docs.ironflow.run/tutorials/desktop/#system-requirements)
— macOS 12+ (Apple Silicon or Intel), Windows 10+ (x64), or Linux x64.

## Screenshots

Ironflow Desktop v0.5.

### Dashboard + Ironflow agent — live metrics with a coding agent alongside

Functions, runs, workers, component health, and the event feed at a glance. The **Ironflow agent** panel on the right is a coding agent grounded in your workspace, the Ironflow runtime, and the built-in Ironflow skills — it can build and verify against your running server without leaving the app.

![Ironflow Desktop dashboard showing the Overview page with metrics and the Ironflow agent panel](docs/images/dashboard.png)

### Add a workspace — point Ironflow at your project

Open an existing project folder or start from a template.

![Add a workspace screen with "Your project" and "Templates" tabs](docs/images/add-workspace.png)

### Built-in docs — the full documentation, in-app

Browse the Ironflow docs in a tab next to your workspace.

![Built-in docs tab showing the Getting Started guide](docs/images/built-in-docs.png)

> All three platforms ship on every release: macOS (Apple Silicon and Intel), Windows (x64), and Linux (x64).

## macOS

macOS 12 Monterey or later. Both Apple Silicon and Intel are supported — pick the matching download:

| Your Mac | Download |
| --- | --- |
| Apple Silicon (M1–M4) | `Ironflow-Desktop-<version>-arm64.dmg` |
| Intel | `Ironflow-Desktop-<version>-x64.dmg` |

Not sure? Run `uname -m` — it prints `arm64` for Apple Silicon, `x86_64` for Intel.

1. Download the `.dmg` for your chip (or the equivalent `-mac-arm64.zip` / `-mac-x64.zip`).
2. Open it and drag **Ironflow Desktop** into **Applications**.
3. Launch it from **Applications**. The build is signed and notarized (Developer ID), so it opens without a Gatekeeper prompt.

If macOS says *"this application is not supported on this Mac"*, you downloaded the wrong architecture — grab the other file.

## Windows

x64 only. Install with [Scoop](https://scoop.sh):

```powershell
scoop bucket add ironflow https://github.com/sahina/scoop-ironflow
scoop install ironflow/ironflow-desktop
scoop update ironflow-desktop   # future upgrades
```

Scoop is the recommended path: it strips the Mark-of-the-Web, so the SmartScreen "unknown publisher" warning never appears even though the build isn't Authenticode-signed yet.

On Windows, updates come from Scoop (`scoop update`), not the in-app auto-updater — they're separate channels.

A direct `Ironflow-Desktop-<version>-setup.exe` installer is also on the [release page](https://github.com/sahina/ironflow-desktop-releases/releases), but it currently triggers a SmartScreen warning because it's unsigned, so Scoop is preferred.

## Linux

x64, as an AppImage. Verified on Ubuntu 18.04+, Debian 10+, and Fedora 32+.

```bash
chmod +x Ironflow-Desktop-*.AppImage
./Ironflow-Desktop-*.AppImage

## Updates

The app auto-updates from this repository's releases. You can also grab any version manually from the [releases page](https://github.com/sahina/ironflow-desktop-releases/releases).
