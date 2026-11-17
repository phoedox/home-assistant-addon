# Phoedox add-on for Home Assistant

[Phoedox](https://phoedox.com) is documentation with a knowledge graph for your
home: rooms, devices, network, manuals and an emergency folder. This
repository makes it a Home Assistant add-on.

## Install

1. In Home Assistant open **Settings → Add-ons → Add-on store**.
2. Open the menu (⋮) → **Repositories** and add
   `https://github.com/phoedox/home-assistant-addon`.
3. Install **Phoedox**, start it and open the web interface.

Details on the options (sign-in with Home Assistant, the public address) are
in [`phoedox/DOCS.md`](phoedox/DOCS.md).

## How this repository is kept up to date

The add-on files come from `deploy/homeassistant` in
[phoedox/phoedox](https://github.com/phoedox/phoedox). A daily workflow
(`.github/workflows/update.yml`) looks for a new Phoedox release, copies the
add-on files of that release, sets the add-on version to the release version
and pins the image (`ghcr.io/phoedox/phoedox:<version>`). Until the first
release it builds from the `main` image.

The add-on's data lives in `/data` and is part of Home Assistant backups.

## License

AGPL-3.0, like Phoedox.
