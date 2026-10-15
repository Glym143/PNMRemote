<h1 align="center">PNMRemote</h1>

<p align="center">
  <strong>Your computers. One workspace.</strong><br>
  Remote desktop, terminal sessions and files — from your phone, tablet or another computer.
</p>

<p align="center">
  <a href="https://github.com/Glym143/PNMRemote/releases/latest"><img alt="Latest release" src="https://img.shields.io/github/v/release/Glym143/PNMRemote?style=flat-square&amp;label=latest&amp;color=8ab4f8"></a>
  <img alt="macOS 14 or later" src="https://img.shields.io/badge/macOS-14%2B-283142?style=flat-square">
  <img alt="Android 8 or later" src="https://img.shields.io/badge/Android-8%2B-283142?style=flat-square">
  <img alt="Ubuntu 24.04 x86_64" src="https://img.shields.io/badge/Linux-Ubuntu%2024.04%20x86__64-283142?style=flat-square">
  <img alt="Proprietary software" src="https://img.shields.io/badge/software-proprietary-283142?style=flat-square">
</p>

<p align="center">
  <a href="https://github.com/Glym143/PNMRemote/releases/latest"><strong>Download PNMRemote</strong></a>
  &nbsp; · &nbsp;
  <a href="#get-connected">Get connected</a>
  &nbsp; · &nbsp;
  <a href="https://github.com/Glym143/PNMRemote/releases">Release notes</a>
  &nbsp; · &nbsp;
  <a href="https://github.com/Glym143/PNMRemote/issues">Report an issue</a>
</p>

---

## Keep your work within reach

Use the computer you already work on, wherever you open PNMRemote. Connect on your local network or use a connection code over the internet, then choose the tools you need.

| Remote desktop | Terminal workspace | File transfer |
| :--- | :--- | :--- |
| View and control a shared screen with keyboard, pointer and session quality controls. | Keep several shells open, switch between sessions and reconnect to running work. | Send files between paired devices with file receiving under your control. |
| Adjust the remote desktop to your device where the host supports it. | Arrange multiple terminal panes on larger screens, including tablets and foldables. | Enable receiving when needed and turn it off from the sharing controls. |

### Built around your devices

- **Local and internet connections.** Find nearby devices or add a computer using its PNMRemote connection code.
- **Multiple sessions.** Work with several terminal sessions without opening a separate app for each one.
- **Device pairing.** Approve a new device or invite it with a connection code; manage paired devices in the app.
- **Sharing controls.** Choose what your computer shares and use **Stop all access** to end access.
- **In-app updates.** Check for a new release, review it and choose when to install.

Available tools depend on the connected device and the services it is sharing. Terminal sessions stay available while the host and their shells remain running.

## Download

**[Open the latest release →](https://github.com/Glym143/PNMRemote/releases/latest)**

| Platform | Requirements | Package | Installation |
| :--- | :--- | :--- | :--- |
| **macOS** | Apple Silicon · macOS 14 or later | [1.0.217 · `.dmg`](https://github.com/Glym143/PNMRemote/releases/download/v1.0.217/pnmremote-1.0.217-macos-arm64-PNMRemote.dmg) | Open the image and drag PNMRemote to Applications. |
| **Android** | Android 8 or later · ARM64 or x86_64 | [1.0.216 · `.apk`](https://github.com/Glym143/PNMRemote/releases/download/v1.0.217/pnmremote-1.0.216-android-universal-PNMRemote.apk) | Open the APK and confirm installation. Install over your existing app to retain its data. |
| **Linux** | Ubuntu 24.04 · x86_64 · desktop runtime libraries | [1.0.218 · `.tar.gz`](https://github.com/Glym143/PNMRemote/releases/download/v1.0.218/PNMRemote-1.0.218-linux-x86_64.tar.gz) | Extract the complete archive into a folder you own, then run `pnmremote`. See below. |

Platform releases can advance independently. The current builds are **macOS 1.0.217**, **Android 1.0.216** and **Linux 1.0.218**. In-app updates select the build for your platform.

The current Mac download uses an Apple Development signature and is not notarized. See the release notes for distribution details.

iPhone and iPad installation is distributed separately; this repository does not publish IPA files. A Windows package is not included in the current public release.

### macOS installation

Requires **Apple Silicon and macOS 14 or later**.

1. Download the [**macOS 1.0.217 `.dmg`**](https://github.com/Glym143/PNMRemote/releases/download/v1.0.217/pnmremote-1.0.217-macos-arm64-PNMRemote.dmg).
2. Open the DMG and drag **PNMRemote** into **Applications**. When updating manually, quit the running app first and replace the existing copy.
3. Launch **PNMRemote** from Applications or Spotlight, then eject the DMG.

#### First launch

The current build has an **Apple Development signature** and is **not notarized**. macOS may block the first launch.

After trying to open PNMRemote, go to **System Settings → Privacy & Security**, find the message about PNMRemote, choose **Open Anyway**, and confirm **Open**. See [Apple's first-launch instructions](https://support.apple.com/en-us/102445).

If it is still blocked by download quarantine, and you obtained this build from this repository and trust it, run the following in **Terminal** after copying the app to Applications:

```bash
xattr -dr com.apple.quarantine "/Applications/PNMRemote.app"
```

Then open PNMRemote again. This command removes the quarantine attribute only from this app; it does not disable Gatekeeper for your Mac.

#### Enable sharing

In **PNMRemote → Settings → Access → System permissions**, open the corresponding macOS settings and allow:

- **Screen & System Audio Recording** to share this Mac's screen and audio.
- **Accessibility** to control this Mac's keyboard and pointer remotely.

Allow **Local Network** if macOS asks, so devices on the same network can connect. Quit and reopen PNMRemote after granting screen-recording access, then start sharing in **This Mac**. These host permissions are for sharing this Mac; they are not needed merely to view another computer.

### Linux installation

Download [**`PNMRemote-1.0.218-linux-x86_64.tar.gz`**](https://github.com/Glym143/PNMRemote/releases/download/v1.0.218/PNMRemote-1.0.218-linux-x86_64.tar.gz) for your first installation. From the folder containing the download, extract and run it as your normal user:

```bash
install -d -m 700 "$HOME/.local/opt/pnmremote"
tar -xzf PNMRemote-1.0.218-linux-x86_64.tar.gz \
    --strip-components=1 -C "$HOME/.local/opt/pnmremote"
"$HOME/.local/opt/pnmremote/pnmremote"
```

Keep the `assets` folder beside the executable. The archive also includes `pnmremote-cli`, a Linux guide, an input setup helper and third-party license notices. The separate Linux executable in the release is the in-app update download; use the full archive to install the application and its supporting files.

This package uses Ubuntu's desktop libraries; it does not bundle a complete Linux runtime. Use Ubuntu 24.04 x86_64 and install the runtime packages listed in the release notes. Compatibility with other distributions has not been established.

To share the Linux screen, a running desktop session with PipeWire, a matching `xdg-desktop-portal` backend and a working H.264 hardware encoder through VA-API or NVENC are required. Screen hosting has no software encoder fallback; viewing another computer can use CPU decoding. Remote keyboard and pointer control additionally require `/dev/uinput` access; the archive includes a setup helper. Terminal and file sharing can be used without screen capture.

## Get connected

1. **Open PNMRemote on both devices.** On the computer you want to access, enable the services you need in its sharing section.
2. **Find or add your computer.** Select it under **Devices** on the same network, or use **Add Device** with a connection code created on that computer.
3. **Authorize access.** Approve a new connection on the computer when prompted. Keep invitation codes private.
4. **Choose your workspace.** Open **Desktop**, **Terminal** or **Files**, depending on what the computer shares.

For access over the internet, enable internet connections on the sharing computer before creating its connection code.

### Share an Android screen

Screen sharing requires **Android 10 or later**. The Android viewer app supports Android 8 or later.

On the Android phone, open **Settings → Share this phone → Start screen sharing** and approve Android’s capture prompt. Enable internet sharing before starting if you want to create a connection code. Add that code on the viewing device.

To let a trusted device control the phone, enable **Allow remote control**, then enable the **PNMRemote** accessibility service in Android settings. Share the **entire screen** when Android asks. Connected viewers can send taps, swipes, scrolling and supported keyboard input. Turn off **Allow remote control** to keep sharing in view-only mode.

Screen sharing must be started manually on the phone. Connecting from another device does not display a capture-consent request on Android. Android can hide protected screens and sensitive content; locking the phone stops screen sharing on supported Android versions. Start sharing again after unlocking when needed. You can stop sharing from the phone at any time.

## Stay up to date

On **macOS**, open **Settings → General → Updates**, or choose **Check for Updates…** from the PNMRemote application menu. On **Android and Linux**, open **Settings → Updates → Check for Updates**.

Automatic checks normally run once per day when enabled. Downloads are verified before installation, and you decide when to install. An update check does not restart your session.

On Linux, open **Settings → Updates → Check for Updates**, then choose **Download Update → Install & Restart**. Installation closes active remote sessions and retains the previous executable as a backup. In-app installation requires the application and its directory to be owned and writable only by your user. For an installation in a system-owned directory, update manually; use the package manager for package-managed installations. The portable updater replaces the GUI executable; download the full archive when you need to refresh the CLI or supporting assets as well.

Versions use **major.minor.build**: for example, `1.0.199` is build 199, followed by `1.0.200`. Older releases remain in the [release archive](https://github.com/Glym143/PNMRemote/releases).

## Help improve PNMRemote

[Open an issue](https://github.com/Glym143/PNMRemote/issues/new) with your app version, the devices involved and the steps that reproduce the problem. A screenshot can help explain a layout or display issue.

Issues are public. Remove connection codes, access keys and personal information before posting screenshots or logs.

---

**PNMRemote is proprietary software.** This repository contains the public product page, compiled application downloads and signed update feeds. The application source code is not published here. GitHub's automatic “Source code” archives contain only this README. Third-party license notices are included with the application.
