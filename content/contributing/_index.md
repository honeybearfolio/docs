---
title: "Contributing"
weight: 30
---

# Contributing to HoneyBear Folio

Thank you for your interest in contributing to HoneyBear Folio! We welcome bug reports, feature suggestions, documentation improvements, and code contributions.

## Ways to Contribute

1.  **Report Bugs**: Open an issue describing the bug. Include steps to reproduce, expected vs. actual behavior, your OS, and screenshots if relevant.
2.  **Suggest Enhancements**: Propose new features or UX improvements. Describe the user goal and any constraints.
3.  **Improve Documentation**: Help us improve the README, user guides, or this documentation site.
4.  **Submit Pull Requests**: Fix bugs, refactor code, or add new features.

## Development Setup

### Prerequisites

- **[Bun](https://bun.sh/) v1.3.6+** (JavaScript runtime)
- **[Rust](https://www.rust-lang.org/) toolchain** (stable)
- **Tauri system dependencies** (WebView/build tools). See [Tauri Prerequisites](https://tauri.app/v1/guides/getting-started/prerequisites).

### Linux Dependencies (Ubuntu/Debian)

```bash
sudo apt-get update
sudo apt-get install -y libwebkit2gtk-4.1-dev libappindicator3-dev librsvg2-dev patchelf
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

## Testing

Please ensure tests pass before submitting a PR.

### Frontend Tests

We use Vitest for React components and logic.

```bash
bun run test
# OR to check coverage
bun run coverage
```

### Backend Tests

Rust unit and integration tests.

```bash
cd src-tauri
cargo test
```

## Code Quality

### Formatting & Linting

**Frontend**:
```bash
bun run format  # Prettier
bun run lint    # ESLint
```

**Backend**:
```bash
cd src-tauri
cargo fmt       # Rustfmt
cargo clippy    # Linter
```

## Project Structure

The project assumes a structure where the main application code resides in `app/`.

- **`app/src/`**: React application source.
  - **`components/`**: Reusable UI components.
  - **`features/`**: Feature-specific logic and views.
  - **`hooks/`**: Custom React hooks.
  - **`utils/`**: Helper functions.
- **`app/src-tauri/`**: Rust backend source.
  - **`src/`**: Rust source code (commands, database logic, market data).
  - **`migrations/`**: Database migrations (if applicable).
