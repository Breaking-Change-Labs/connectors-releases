# Breaking Change Labs connectors releases

This repository publishes the releases of the connectors by Breaking Change Labs. A connector links a customer's own systems to one of our products:

- **WordPress plugin** and **OpenCart extension** let OverlAI read a site's public content and products.
- **Archive** connects a firm's local document folders to Modus.

The source code is developed in a private repository. Its release workflows publish each build here, so that sites and servers can download it without credentials.

## What is here

- **Releases.** Each release is tagged `<component>-v<version>`, for example `wordpress-v1.2.0`, and carries that component's packages. Every package has a `.sha256` file with its checksum.
- **Update feeds.** `<component>/update.json` describes the newest release of each component. An installed connector reads its feed to learn about a newer release: WordPress offers it in the dashboard, OpenCart shows it on the extension's settings page, and Archive installs it by itself.

## Components

| Component | Product | Tag | Packages | Licence |
| --- | --- | --- | --- | --- |
| WordPress plugin | OverlAI | `wordpress-v*` | `overlai-connector-<version>.zip` | GNU GPL, version 2 or later |
| OpenCart extension | OverlAI | `opencart-v*` | `overlai_connector.ocmod.zip` (OpenCart 4), `overlai-connector-<version>-oc3.ocmod.zip` (OpenCart 3) | GNU GPL, version 3 or later |
| Archive | Modus | `archive-v*` | MSI, `.pkg`, `.deb`, and `.rpm` per operating system and architecture | Proprietary, all rights reserved |

Each plugin package carries the full text of its licence in `LICENSE`.

## Installing

Download the package for your platform from the newest release of its component, and install it through the platform's own installer: Plugins, Add New, Upload Plugin in WordPress, Extensions, Installer in OpenCart, or the system's package installer for Archive. After that, each connector updates from this repository.

Do not open issues or pull requests here. Contact Breaking Change Labs for support.
