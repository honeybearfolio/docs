---
title: "Installation"
weight: 10
description: "How to install HoneyBear Folio."
---

## Linux

We offer several package formats to suit your distribution.

### Option 1: Flatpak (Recommended)
The Flatpak build is sandboxed and includes its dependencies.

1.  Download `honeybear-folio.flatpak` (x64) or `honeybear-folio-aarch64-unknown-linux-gnu.flatpak` from the [Releases page](https://github.com/HoneyBearFolio/HoneyBear-Folio/releases).
2.  Install it:
    ```bash
    flatpak install --user ./honeybear-folio.flatpak
    ```

### Option 2: AppImage (Portable)
The AppImage needs no installer. Download `honeybear-folio_*_amd64.AppImage` or `honeybear-folio_*_aarch64.AppImage`, then:

```bash
chmod +x honeybear-folio_*_amd64.AppImage
./honeybear-folio_*_amd64.AppImage
```

### Option 3: DEB / RPM
For Debian/Ubuntu or Fedora/RHEL based systems.

*   **Debian/Ubuntu**: `sudo dpkg -i honeybear-folio_*_amd64.deb` (or `*_arm64.deb`)
*   **Fedora**: `sudo dnf install ./honeybear-folio-*-1.x86_64.rpm` (or `aarch64.rpm`)

---

## Windows

1.  Download `honeybear-folio_*_x64-setup.exe` or `honeybear-folio_*_arm64-setup.exe` from the [Releases page](https://github.com/HoneyBearFolio/HoneyBear-Folio/releases).
2.  Run the installer.

**Microsoft Defender SmartScreen Warning:**
Because HoneyBear Folio is an open-source project and may not be code-signed with a costly certificate yet, you might see a "Windows protected your PC" popup.
1.  Click **More Info**.
2.  Click **Run anyway**.

---

## macOS

1.  Download `honeybear-folio_*_aarch64.dmg` (Apple silicon) or `honeybear-folio_*_x64.dmg` (Intel).
2.  Open it and drag HoneyBear Folio into your **Applications** folder.

**"Unidentified Developer" Warning:**
On the first launch, macOS may block the app because it wasn't downloaded from the App Store.
1.  Go to **System Settings** > **Privacy & Security**.
2.  Scroll down to the Security section.
3.  You should see a message about HoneyBear Folio being blocked. Click **Open Anyway**.

---

## Updates

The running app can check the releases page for a newer version.

---

## Building from Source

Compiling the app yourself needs [Bun](https://bun.sh) 1.3.6 or newer, a stable [Rust](https://rustup.rs) toolchain, and Tauri’s system libraries. See [Contributing](../../contributing/) for the day-to-day development commands.

Ubuntu or Debian:

```bash
sudo apt-get update
sudo apt-get install -y libwebkit2gtk-4.1-dev libappindicator3-dev librsvg2-dev patchelf build-essential curl wget file libssl-dev
```

Fedora:

```bash
sudo dnf install webkit2gtk4.1-devel libappindicator-gtk3-devel librsvg2-devel openssl-devel curl wget file patchelf gcc pkg-config
```

Clone and build:

```bash
git clone https://github.com/HoneyBearFolio/HoneyBear-Folio.git
cd HoneyBear-Folio/app

# Install JS dependencies
bun install

# Build installers for the current platform
bun run tauri build
```

Installers for the current platform are written to `src-tauri/target/release/bundle/`.
