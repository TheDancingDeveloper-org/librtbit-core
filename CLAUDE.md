# librtbit-core

Core types and utilities for the rtbit BitTorrent client.

**Version:** 0.1.0 | **Edition:** Rust 2024 | **License:** MIT

## This Is a Shared Library

### Consumed By

| App | Via | Tag |
|-----|-----|-----|
| rustTorrent | git | v0.1.0 |
| Arz | git | v0.1.0 |
| NGMS | git | v0.1.0 |
| librtbit-peer-protocol (lib) | git | v0.1.0 |
| librtbit-dht (lib) | git | v0.1.0 |
| librtbit-tracker-comms (lib) | git | v0.1.0 |
| librtbit-lsd (lib) | git | v0.1.0 |
| librtbit-upnp-serve (lib) | git | v0.1.0 |

### Depends On

- **librtbit-buffers** (git, v0.1.0) — for ByteBuf/ByteBufOwned types
- **librtbit-bencode** (git, v0.1.0) — for bencode serialization
- **librtbit-clone-to-owned** (git, v0.1.0) — for CloneToOwned trait
- **librtbit-sha1-wrapper** (git, v0.1.0, optional) — for SHA1/SHA256 hashing

## Features

- `sha1-crypto-hash` (default) — uses crypto-hash (OpenSSL-backed)
- `sha1-ring` — uses aws-lc-rs

## BEP Implementations

- BEP 19 — WebSeed URL list parsing
- BEP 46 — Mutable torrent magnet link parsing (Ed25519 public key + salt)
- BEP 47 — Comment field parsing
- BEP 52 — BitTorrent v2 info hash, meta_version, hybrid torrent detection

## Key Types

- `Id20` — 20-byte info hash (v1)
- `Id32` — 32-byte info hash (v2)
- `TorrentMetaV1Info` / `TorrentMetaV1Owned` — torrent metainfo types
- `MagnetLink` — magnet URI parser
- `PeerId` — peer identification
