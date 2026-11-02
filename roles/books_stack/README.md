# books_stack

[Calibre-Web Automated](https://github.com/crocodilestick/Calibre-Web-Automated): your ebook
library in the browser and synced to a Kobo. Books in `books-ingest` are imported into it.

- **Runs:** with `homelab_books: true` (the default). Tag: `books`.
- **Settings:** `defaults/main.yml`: the image version.
- **Note:** plain http on the LAN address, so a Kobo can sync (it can't run Tailscale). The
  login, Kobo sync and users are set by `app_config`.
