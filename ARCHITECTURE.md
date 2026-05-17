# criomos-horizon-config Architecture

`criomos-horizon-config` is the pan-horizon configuration source for
the LiGoldragon CriomOS horizon.

The repository intentionally contains one small NOTA record:

- `horizon.nota` -> `horizon-rs::HorizonProposal`

The boundary is narrow:

- Cluster repositories author cluster facts.
- This repository authors horizon-wide identity and temporary network
  facts.
- `horizon-rs` derives projected views from both.
- CriomOS owns runtime defaults and implementation catalogs.

The IPv4 LAN record is an explicit transitional value. Keep it as exact
CIDR, gateway, and DHCP-pool data; replace it with the IPv6-first
network design when that lands.
