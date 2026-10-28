<div align="center">

<img src="snap/gui/zedis.png" alt="Zedis logo" width="128" />

# Zedis

**A native Redis and Valkey desktop client.**

[![zedis](https://snapcraft.io/zedis/badge.svg)](https://snapcraft.io/zedis)
[![Base: core26](https://img.shields.io/badge/Base-core26-2C8C3C?logo=canonical&logoColor=white)](https://snapcraft.io/core26)
![Confinement: strict](https://img.shields.io/badge/Confinement-strict-2C8C3C)
[![Maintainer: sidaliteir](https://img.shields.io/badge/Maintainer-sidaliteir-2C8C3C?logo=snapcraft&logoColor=white)](https://snapcraft.io/publisher/sidaliteir)
![Architectures: amd64 and arm64](https://img.shields.io/badge/Architectures-amd64%20%7C%20arm64-2C8C3C?logo=linux&logoColor=white)

[Getting Started](#getting-started) · [Configure](#configure) · [Limitations](#limitations) · [Build](#build) · [Support](#support) · [License](#license)

Unofficial snap packaging for [Zedis](https://github.com/vicanso/zedis), a desktop application for browsing, editing and monitoring Redis and Valkey databases.

</div>

---

## Getting Started

<a href="https://snapcraft.io/zedis"><img alt="Get it from the Snap Store" src="https://snapcraft.io/en/dark/install.svg" width="180"></a>

```bash
sudo snap install zedis
zedis
```

Launch from the terminal or your application menu and add a database connection.

## Configure

Manage connections, TLS certificates, SSH tunnels and preferences in the app. There are no `snap set` options.

| Optional access | Command |
| --- | --- |
| SSH keys in `~/.ssh` | `sudo snap connect zedis:ssh-keys` |
| Imports, exports and certificates on removable storage | `sudo snap connect zedis:removable-media` |

Settings, encrypted credentials and trusted SSH hosts are stored in `~/snap/zedis/current/.config/zedis/`. Select a key using its full host path when it is outside the snap's home.

## Limitations

- A working GPU and desktop session are required.
- Host SSH agents and automatic discovery of host SSH configuration are unavailable; use a key file or password in the connection settings.
- Custom shell actions can only use commands and files available inside the snap.
- Use TCP for Redis and Valkey; host Unix sockets outside accessible directories are restricted.
- Application updates are managed by snapd. The separate web edition and database servers are not included.

## Build

```bash
git clone https://github.com/sidalit/zedis-snap.git
cd zedis-snap
sudo snap install snapcraft --classic
snapcraft pack
```

## Support

- **Installation or snap issues:** [open a packaging issue](https://github.com/sidalit/zedis-snap/issues).
- **Application bugs:** [report them upstream](https://github.com/vicanso/zedis/issues).

## License

Snap packaging: [MIT](https://github.com/sidalit/zedis-snap/blob/main/LICENSE).
