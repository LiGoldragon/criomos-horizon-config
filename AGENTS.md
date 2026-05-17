# Agent Bootstrap - criomos-horizon-config

This repository contains pan-horizon authored configuration consumed by
`horizon-rs` alongside per-cluster `datom.nota` files.

## Required Reading

1. `/home/li/primary/ESSENCE.md`
2. `/home/li/primary/repos/lore/AGENTS.md`
3. `/home/li/primary/protocols/orchestration.md`
4. `/home/li/primary/skills/system-specialist.md`
5. This repo's `ARCHITECTURE.md`

## Scope

This repo owns facts that are true for the whole LiGoldragon CriomOS
horizon, not for one cluster:

- internal DNS suffix;
- public DNS suffix;
- temporary exact IPv4 LAN, until the IPv6-first network design lands.

Per-cluster node data, users, trust, key material, provider selections,
and secrets stay in cluster repositories such as `goldragon`.

## Rules

- NOTA is the authored data format.
- Do not put cluster-specific data here.
- Do not put CriomOS runtime defaults or catalogs here.
- Use `jj` for all version-control operations.
