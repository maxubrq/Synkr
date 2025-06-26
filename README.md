# Synkr

**Local‑first, zero‑trust file sync that feels as effortless as AirDrop and scales like S3.**

> Your files, your keys, your rules — from your laptop to the cloud, without the middleman reading a single byte.

---

## Table of Contents

1. Why Synkr?
2. Headline Features
3. How Synkr Is Different
4. Who Is It For?
5. Quick Try
6. Roadmap
7. Community & Contributing
8. License

---

## 1  Why Synkr?

Digital work is scattered across devices, clouds, and time zones. You either give up privacy (hello, SaaS) or fight with clunky self‑hosted stacks. **Synkr** offers a third path: local‑first software that *treats the server as a convenience, not a source of truth*, so your data is always in your hands.

---

## 2  Headline Features

* **End‑to‑end encryption by default** – only you hold the keys; servers see ciphertext and BLAKE3 hashes.
* **Delta & deduped sync** – uploads only changed blocks, saving bandwidth on spotty connections.
* **Instant previews** – peek at photos, PDFs, and docs while the rest streams in the background.
* **Smart collections** – virtual folders powered by local embeddings (e.g. `type:pdf tag:invoice 2024`).
* **Time‑shift slider** – scrub a folder’s history like a video timeline.
* **Presence glow** – see teammates viewing a file in real time, no chat pings needed.

---

## 3  How Synkr Is Different

|                       | Dropbox | Nextcloud       | Syncthing   | **Synkr**         |
| --------------------- | ------- | --------------- | ----------- | ----------------- |
| Zero‑trust encryption | ✖︎      | ⚠️ opt‑in       | ✅           | **✅**             |
| Local‑first core      | ✖︎      | ⚠️ offline mode | **✅**       | **✅**             |
| P2P + Cloud hybrid    | ✖︎      | ⚠️ federation   | ⚠️ no cloud | **✅**             |
| AI‑powered search     | ✖︎      | plugins         | ✖︎          | **✅**             |
| Lightweight stack     | SaaS    | LAMP/Redis      | Go binaries | **Rust + Svelte** |

---

## 4  Who Is It For?

* **Indie creators** wanting Dropbox simplicity without subscription creep.
* **Remote teams** who need HIPAA/GDPR compliance and self‑hosting.
* **Open‑source lovers** who prefer auditable code over black‑box binaries.
* **Privacy absolutists** who won’t settle for “encrypted at rest.”

---

## 5  Quick Try

```bash
# Clone & boot the stack (alpha demo)
git clone https://github.com/your‑handle/synkr.git && cd synkr
docker compose up -d            # start Postgres + MinIO
cargo run -p synkr-cli init     # create your first vault
pnpm --filter web dev           # launch the web UI
open http://localhost:5173
```

Uploads are limited to **2 GB per file** in this early alpha.

---

## 6  Roadmap

| Milestone                      | ETA     | Notes                         |
| ------------------------------ | ------- | ----------------------------- |
| Alpha 0.1 – basic sync & share | Q3 2025 | CLI + Web UI                  |
| Beta 0.5 – mobile apps         | Q1 2026 | iOS & Android (Capacitor)     |
| 1.0 – plug‑in marketplace      | Q3 2026 | backup, e‑sign, media gallery |

---

## 7  Community & Contributing

* **Chat** – `#synkr` on Matrix (`matrix.to/#/#synkr:matrix.org`)
* **Issues** – GitHub *Issues* for bugs; *Discussions* for ideas.
* **PRs welcome** – whether it’s docs, design tweaks, or code.

See **`CONTRIBUTING.md`** for the style guide and DCO sign‑off.

---

## 8  License

Synkr is **Apache 2.0** — permissive, business‑friendly, and GPL‑compatible.
