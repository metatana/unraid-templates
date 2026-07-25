# MetaTana — Unraid Templates

Unraid Community Applications template for **[MetaTana](https://metatana.com)**, an AI-powered media
manager. Drop a folder and it identifies, enriches, and organizes your library.

| | |
| --- | --- |
| Template | [`templates/metatana.xml`](templates/metatana.xml) |
| Image | `ghcr.io/metatana/metatana-app:stable` |
| Architectures | `linux/amd64`, `linux/arm64` |
| Web UI | port `3000` |

## Install

Search for **MetaTana** in **Apps** (Community Applications) on your Unraid server.

Full walkthrough: **<https://metatana.com/install/unraid>**

### Settings at a glance

| Setting | Value |
| --- | --- |
| App Data | `/app/data` → `/mnt/user/appdata/metatana` (Read/Write) |
| Media | `/media` → your share, e.g. `/mnt/user/Media` |
| Web UI Port | `3000` |
| PUID / PGID | `99` / `100` |

Map **App Data** to `/app/data` so your library, settings, and thumbnails survive a container update.
Use **Read/Write** on media so MetaTana can rename files and write artwork, or **Read Only** to scan
without changing anything. Unraid share paths are case-sensitive.

MetaTana publishes `stable` and versioned tags — there is no `latest` tag. Leave the Docker **User**
override and **Extra Parameters** blank.

## Support

Questions and problems: **<https://github.com/metatana/support/discussions>**

Or email **support@watari.dev**.

## Notes

MetaTana is metadata-only and downloader-agnostic. It works alongside any media library and any player,
including Plex, Jellyfin, Kodi, and Emby.

This repository contains only the Unraid template. MetaTana itself is closed source.
