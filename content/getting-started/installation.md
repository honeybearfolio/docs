---
title: "Installation"
weight: 10
---

## 🐧 Linux

We offer several package formats to suit your distribution.

### Option 1: Flatpak (Recommended)
The Flatpak version is sandboxed and includes all necessary dependencies.

1.  Download the `.flatpak` file from the [Releases page](https://github.com/HoneyBearFolio/HoneyBear-Folio/releases).
2.  Install via command line:
    ```bash
    flatpak install com.honeybearfolio.honeybearfolio.flatpak
    ```

### Option 2: AppImage (Portable)
The AppImage requires no installation—just download and run.

1.  Download `HoneyBear-Folio-x.x.x.AppImage`.
2.  Make it executable:
    ```bash
    chmod +x HoneyBear-Folio-*.AppImage
    ```
3.  Run it:
    ```bash
    ./HoneyBear-Folio-*.AppImage
    ```

### Option 3: DEB / RPM
For Debian/Ubuntu or Fedora/RHEL based systems.

*   **Debian/Ubuntu**: `sudo dpkg -i honeybear-folio_*.deb`
*   **Fedora**: `sudo dnf install ./honeybear-folio-*.rpm`

---

## 🪟 Windows

1.  Download the installer (`HoneyBear-Folio_x.x.x_x64-setup.exe` or `.msi`) from the [Releases page](https://github.com/HoneyBearFolio/HoneyBear-Folio/releases).
2.  Run the installer.

**Microsoft Defender SmartScreen Warning:**
Because HoneyBear Folio is an open-source project and may not be code-signed with a costly certificate yet, you might see a "Windows protected your PC" popup.
1.  Click **More Info**.
2.  Click **Run anyway**.

---

## 🍎 macOS

1.  Download the `.dmg` disk image.
2.  Open it and drag "HoneyBear Folio" into your **Applications** folder.

**"Unidentified Developer" Warning:**
On the first launch, macOS may block the app because it wasn't downloaded from the App Store.
1.  Go to **System Settings** > **Privacy & Security**.
2.  Scroll down to the Security section.
3.  You should see a message about HoneyBear Folio being blocked. Click **Open Anyway**.

---

## 🛠 Building from Source

If you prefer to compile the application yourself (e.g., for Arch Linux or development), you will need **Bun** and **Rust**.

1.  **Install Prerequisites**:
    *   [Rust](https://www.rust-lang.org/tools/install)
    *   [Bun](https://bun.sh/)
    *   System libraries (gtk, webkit2gtk). See [Contributing](../../contributing/) for the full list.
2.  **Clone and Build**:
    ```bash
    git clone https://github.com/HoneyBearFolio/HoneyBear-Folio.git
    cd HoneyBear-Folio/app
    
    # Install JS dependencies
    bun install
    
    # Build the binary (release mode)
    bun run tauri build
    ```
3.  The binary will be located in `src-tauri/target/release/bundle/`.
