# HoneyBear‑Folio Documentation

This repository is a Hugo content module that contains only `markdown` documentation under `content/` for the HoneyBear‑Folio desktop app.

## Quick usage (replace the module path with your repo path):

TOML (in the consuming site's `config.toml`):

```toml
module = {
  imports = [
    { path = "example.com/your-username/honeybear-folio-docs" }
  ],
  mounts = [
    { source = "content", target = "content/honeybear-folio" }
  ]
}
```

Preview locally from a Hugo site that imports this module:

```bash
hugo mod get
hugo server -D
```