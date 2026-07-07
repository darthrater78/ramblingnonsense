# Rambling Nonsense — Docker & Config References

Reference configs from my homelab blog at [ramblingnonsense.nscriven.net](https://ramblingnonsense.nscriven.net).

All bind mounts follow my standardized `/opt/docker/<service>` convention — see [this post](https://ramblingnonsense.nscriven.net/p/its-docker-ing-time-ac9) for the full setup process.

**Conventions used across all configs:**
- Timezone: `America/New_York` — change to match your locale
- Placeholder values are marked `YOUR_*` — fill these in before deploying

---

## Docker Compose

| File | Description |
|------|-------------|
| [dozzle-main.yml](docker-compose/dozzle-main.yml) | Dozzle container log viewer — main instance with remote agent support |
| [dozzle-agent.yml](docker-compose/dozzle-agent.yml) | Dozzle remote agent — deploy on each host you want to aggregate logs from |
| [uptime-kuma.yml](docker-compose/uptime-kuma.yml) | Uptime Kuma uptime and status monitoring |
| [wud.yml](docker-compose/wud.yml) | What's Up Docker — tracks container image updates, triggers Apprise notifications |
| [music-assistant.yml](docker-compose/music-assistant.yml) | Music Assistant Server (requires host networking and elevated capabilities) |
| [nginx-proxy-manager.yml](docker-compose/nginx-proxy-manager.yml) | Nginx Proxy Manager reverse proxy with Let's Encrypt |
| [trilium-notes.yml](docker-compose/trilium-notes.yml) | Trilium Notes self-hosted note-taking |
| [zigbee2mqtt.yml](docker-compose/zigbee2mqtt.yml) | Zigbee2MQTT — bridges Zigbee devices to MQTT |
| [zwave-js-ui.yml](docker-compose/zwave-js-ui.yml) | Z-Wave JS UI with web interface and websocket |
| [pulse.yml](docker-compose/pulse.yml) | Portainer Pulse monitoring stack with Docker agent for remote hosts |
| [termix.yml](docker-compose/termix.yml) | Termix web-based SSH/RDP/VNC client with guacd backend and SSL |
| [phpipam.yml](docker-compose/phpipam.yml) | phpIPAM IP address management with MariaDB and scheduled scanning |

## Config Snippets

| File | Description |
|------|-------------|
| [docker-bip-change.md](config-snippets/docker-bip-change.md) | Change Docker's bridge IP to avoid subnet conflicts with your network |
| [ha-notifications.md](config-snippets/ha-notifications.md) | Home Assistant / Node-RED notification payload examples |
| [wud-node-red.md](config-snippets/wud-node-red.md) | WUD container label templates and Node-RED JSON for update notifications |
