# criomos-horizon-config Architecture

`criomos-horizon-config` is the pan-horizon configuration source for
the LiGoldragon CriomOS horizon.

The repository intentionally contains one small NOTA record:

- `horizon.nota` -> `horizon-rs::HorizonProposal`

The boundary is narrow:

- Cluster repositories author cluster facts.
- This repository authors horizon-wide identity and allocation facts.
- `horizon-rs` derives projected views from both.
- CriomOS owns runtime defaults and implementation catalogs.

The LAN allocation shape is versioned by `LanPool.hashNamespace`.
Changing it can renumber clusters and must be treated as a migration.
