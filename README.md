# 🍿 Jellyfin + Jellyseer Stack

This project provides a simple Docker-based setup for running **Jellyfin** (a media server) along with **Jellyseerr** (a request management and discovery frontend for Jellyfin).

Docker Compose contains following components:

- **[Jellyfin](https://jellyfin.org/)** — free and open source media server for streaming your media
- **[Jellyseerr](https://github.com/fallenbagel/jellyseerr)** — unofficial web UI for Jellyfin’s Live TV and DVR

---

## 📦 Services

### `jellyfin`

- A free software media system that puts you in control of managing and streaming your media.
- Web UI: [http://localhost:8096](http://localhost:8096)

### `jellyseerr`

- A companion for Jellyfin that lets users request movies and shows via an intuitive interface.
- Web UI: [http://localhost:5055](http://localhost:5055)

---

## 🗂 Volumes

| Container   | Path                   | Description                 |
| ----------- | ---------------------- | --------------------------- |
| jellyfin    | `./jellyfin`           | Config and metadata storage |
| jellyseerr  | `./jellyseerr`         | Jellyseerr app config       |
| Shared data | `/data` (host-mounted) | Media library for Jellyfin  |

---

## ✅ Requirements

- Docker + Docker Compose
- `.env` file with required variables:

```bash
PUID=1000
PGID=1000
TZ=Europe/Kyiv
```

---

## 🚀 Usage

```bash
docker compose up -d
```

or:

```bash
./start.sh
```

---

## 📄 License

MIT License
