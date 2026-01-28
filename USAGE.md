USAGE — HoneyBear‑Folio documentation module

1) Update `go.mod`'s module path to the repository import path (e.g. `github.com/your-username/honeybear-folio-docs`).

2) From the consuming Hugo site add an import and mount in `config.toml` or `config.yaml` (see `README.md`).

3) Run:

```bash
hugo mod get
hugo server -D
```

Notes:
- This repo intentionally contains only `markdown` under `content/` so it can be safely mounted into other sites.
- Tell me your repo URL and I will update `go.mod` + `README` examples for you.