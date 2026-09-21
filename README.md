# LiTime ESP32 Gateway Landing Page

Static landing page for the open-source [LiTime ESP32 Gateway](https://github.com/TristanEDU/litime-esp32-gateway) project.

Target domain:

```text
litime-gateway.tjt-media.online
```

The page is plain HTML and CSS. It can be hosted by GitHub Pages, Cloudflare Pages, Vercel, Netlify, or any static file host.

## Files

- `index.html` - landing page
- `styles.css` - responsive page styling
- `local-gateway-wifi-setup.jpeg` - local setup screenshot copied from the project docs
- `remote-dashboard-preview.jpeg` - remote dashboard screenshot copied from the project docs
- `outreach/community-posts.md` - source-backed community list and tailored post drafts
- `CNAME` - GitHub Pages custom domain target

## Local Preview

```sh
python3 -m http.server 8080
```

Open:

```text
http://127.0.0.1:8080
```

## Deploy Notes

For GitHub Pages:

1. Push this repo to GitHub.
2. Enable Pages from the repository settings.
3. Set the source to the `main` branch root.
4. Add DNS for `litime-gateway.tjt-media.online` to point at GitHub Pages.

For Cloudflare Pages:

1. Connect this repo.
2. Use no build command.
3. Use `/` as the output directory.
4. Add `litime-gateway.tjt-media.online` as the custom domain.
