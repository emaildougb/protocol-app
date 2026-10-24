# NCEMS Quick Protocols

Clark County EMS protocol quick reference for NCEMS crews (the Quick Protocols button on the Hub). One file, no backend, works offline once loaded. All protocol content is the `P` array at the top of the script in `index.html`. See HANDOFF.md for how it's built.

**Version 1.2**

## Links

- Live: [https://emaildougb.github.io/protocol-app/](https://emaildougb.github.io/protocol-app/)
- Upload: [https://github.com/emaildougb/protocol-app/upload/main](https://github.com/emaildougb/protocol-app/upload/main)
- Repo: [https://github.com/emaildougb/protocol-app](https://github.com/emaildougb/protocol-app)

## Files (upload ALL of these)

- `index.html`: the whole app
- `protocol-app.html`: redirect stub to index.html so old bookmarks still work
- `HANDOFF.md`: how the app is built
- `README.md`: this file

## Changelog

### v1.2 (10/24/2026)
- New top bar, the same as CG Staff: white bar, house button on the left goes to NCEMS Clinical, NCEMS logo, "NCEMS" in black and the app name in green, North Country EMS in gray, and the i button on the right for details. iPhone status bar set to default so the clock shows on the white bar
- Protocol count moved into the top bar; search and categories sit right under it. The i shows a short about box
- Browser tab icon and home screen icon added (apple-touch-icon.png, icon-512.png from Clinical), plus logo.png
- Changed index.html, README.md and added the icon files

### v1.1
- Haptics: a light tick when you tap a button, link, tab or card, the same way the EP Checker does it. iPhone needs iOS 18 or newer with System Haptics on (Settings, Sounds & Haptics). Android phones vibrate. Nothing else changed
- First README for this repo. The app had no version number before, so the 8/7/2026 build counts as 1.0

### v1.0
- 21 protocols in six categories with Signs/Sx, Meds, Actions and Red Flags tabs, live search and category filters (8/7/2026)
