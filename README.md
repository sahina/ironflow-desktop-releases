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
— macOS 12+, Windows 10+ (x64), or Linux x64.

## Platform support

> **macOS on Apple Silicon is the only supported platform.** Intel macOS, Windows, and Linux builds
> are published on every release and auto-update normally, but they are **experimental** — they are
> not regularly tested.
>
> This is a capacity limit, not a technical one: Ironflow is built by one developer, working on Apple
> Silicon. Every platform's build pipeline is green. If you hit a problem on one of them — or want to
> help look after one — [open an issue](https://github.com/sahina/ironflow-desktop-releases/issues).

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

> Every release ships macOS, Windows (x64), and Linux (x64) builds. macOS on Apple Silicon is the supported one; the rest are experimental.

## macOS

macOS 12 Monterey or later. **Apple Silicon is the supported platform.**

1. Download the `.dmg` from the latest release. When a release ships more than one Mac build, the
   architecture is in the filename — take the one containing `arm64`. (Not sure which Mac you have?
   Run `uname -m`: it prints `arm64` for Apple Silicon, `x86_64` for Intel.)
2. Open it and drag **Ironflow Desktop** into **Applications**.
3. Launch it from **Applications**. The build is signed and notarized (Developer ID), so it opens without a Gatekeeper prompt.

If macOS says *"this application is not supported on this Mac"*, you downloaded the wrong architecture — grab the other file.

Intel Macs can run the `x64` build where one is published, but it is untested and ships one known
limitation: the built-in agent's `xz` and `zstd` compression paths fail with an error. The rest of the
app, including the engine, works.

## Windows

**Experimental** — published and auto-updating, but not regularly tested.

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

**Experimental** — published and auto-updating, but not regularly tested.

x64, as an AppImage. Built against Ubuntu 18.04+, Debian 10+, and Fedora 32+.

```bash
chmod +x Ironflow-Desktop-*.AppImage
./Ironflow-Desktop-*.AppImage
```

If it fails with `dlopen(): error loading libfuse.so.2`, install FUSE 2 (`sudo apt install libfuse2`
on Ubuntu 22.04+) or run it once with `./Ironflow-Desktop-*.AppImage --appimage-extract-and-run`.

## Updates

The app auto-updates from this repository's releases. You can also grab any version manually from the [releases page](https://github.com/sahina/ironflow-desktop-releases/releases).
