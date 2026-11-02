# tailscale

Keeps Tailscale up to date and publishes every web UI with `tailscale serve` at
`https://<server>.<tailnet>.ts.net:<port>`. Tailscale itself is installed and logged in by
`./setup.sh`.

- **Runs:** with `homelab_tailscale: true` (the default). Tag: `tailscale`.
- **Settings:** the apps and their ports are in `inventory/group_vars/homelab/main.yml`
  (`homelab_web_apps`, `homelab_ports`, `homelab_tailscale_ports`). Apps that are off are left out.
- **Optional:** `tailscale_lan_route: true` also routes the server's LAN address (only that
  /32) over Tailscale, so one Jellyfin address works at home and away (main README, One
  Jellyfin address).
- **Note:** it only adds; an HTTPS address you no longer want:
  `sudo tailscale serve --https=<port> off`.
