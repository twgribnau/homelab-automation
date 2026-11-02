# tailscale

Keeps Tailscale up to date and routes the server's LAN address over it (a subnet route of just
that one address, a /32), so `http://<LAN address>:<port>` works away from home too. Tailscale
itself is installed and logged in by `./setup.sh`.

- **Runs:** with `homelab_tailscale: true` (the default). Tag: `tailscale`.
- **Settings:** none of its own; the address is `homelab_lan_ip` in
  `inventory/group_vars/homelab/main.yml`.
- **Note:** approve the route once in the Tailscale admin console (main README, Away from home).
