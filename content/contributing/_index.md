---
title: "Contributing"
weight: 30
description: "How to contribute to HoneyBear Folio."
---

# Contributing to HoneyBear Folio

Thank you for your interest in contributing to HoneyBear Folio! We welcome bug reports, feature suggestions, documentation improvements, and code contributions.

## Ways to Contribute

1.  **Report Bugs**: Open an issue describing the bug. Include steps to reproduce, expected vs. actual behavior, your OS, and screenshots if relevant.
2.  **Suggest Enhancements**: Propose new features or UX improvements. Describe the user goal and any constraints.
3.  **Improve Documentation**: Help us improve the README, user guides, or this documentation site.
4.  **Submit Pull Requests**: Fix bugs, refactor code, or add new features.
5.  **Financial Contribution**: Support the project by buying me a coffee: [https://buymeacoffee.com/bernatbc](https://buymeacoffee.com/bernatbc)

## Development Setup

### Prerequisites

- **[Bun](https://bun.sh/) 1.3.6 or newer**
- A stable **[Rust](https://rustup.rs)** toolchain
- **Tauri system libraries** for your OS. See [Tauri Prerequisites](https://tauri.app/start/prerequisites/).

### Linux dependencies

Ubuntu or Debian:

```bash
sudo apt-get update
sudo apt-get install -y libwebkit2gtk-4.1-dev libappindicator3-dev librsvg2-dev patchelf build-essential curl wget file libssl-dev
```

Fedora:

```bash
sudo dnf install webkit2gtk4.1-devel libappindicator-gtk3-devel librsvg2-devel openssl-devel curl wget file patchelf gcc pkg-config
```

### 1. Clone & Install

Clone the repository and install frontend dependencies:

```bash
git clone https://github.com/HoneyBearFolio/HoneyBear-Folio.git
cd HoneyBear-Folio/app
bun install
```

### 2. Run in Development Mode

Run the app with hot-reloading:

```bash
bun run tauri dev
```

### 3. Build for Production

Build a production bundle (creates an AppImage/Deb/RPM on Linux):

```bash
bun run tauri build
```

The output will be in `src-tauri/target/release/bundle/`.

## Testing and checks

Run these from `app/` before submitting a PR:

| Command | Purpose |
| --- | --- |
| `bun test` | Run the Vitest suite |
| `bun run coverage` | Run tests and fail under 80% line coverage |
| `bun run lint` | ESLint, with zero warnings allowed |
| `bun run typecheck` | TypeScript check (`tsc --noEmit`) |
| `bun run version:sync` | Copy the version from `package.json` into the Tauri config and `Cargo.toml` |

Rust checks, from `app/src-tauri`:

```bash
cargo test
cargo fmt
cargo clippy
```

## Project layout

- `app/` — React, Vite, and the Tauri shell
- `app/src/features/` — screens for the dashboard, accounts, investments, assets, liabilities, FIRE, rules, scheduled transactions, the assistant, and settings
- `app/src/components/` — shared UI
- `app/src/api/tauri-client.ts` — typed calls into Rust
- `app/src/stores/` — client-side UI state
- `app/src-tauri/src/core/` — commands, SQLite, market data, import and export, and PDF reports

For error-handling conventions and the pull request checklist, see `CONTRIBUTING.md` in the application repository.
