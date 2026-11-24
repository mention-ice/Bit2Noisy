# Bit2Noisy

Send text and pictures through the air: one device plays the message through its speaker, and every phone in the room decodes it through its microphone. One web page, no app, no settings.

- `index.html`: the page. Its modem is the one of AudioComm's `acoustic_modem_v7.html`, line for line, so the two pages read each other's frames.
  It opens in a **simple view** (write, send, listen); the **Lab** switch in the header shows every modem setting and measurement. The choice is kept on the device. `?view=lab` or `?view=simple` forces one; a link that carries modem settings (`?mod=…`, `?code=…`) opens the lab, and receiver QR codes carry the current view, the named class room and an explicit `tele=off` opt-out.
- `check/index.html` tests the speaker and microphone. Both modem pages link to it beside **Start listening** and in the microphone error message.
- `chat/index.html`: Bit2Noisy Chat, a group chat through sound.
- Visits: both pages load the anonymous visit counter of the Bit2Noisy telemetry server (`v.js` with `data-site="bit2noisy"` or `"chat"`, since 2026-11-16): one beacon when a page opens and one with the seconds it was in view. No cookie and nothing stored on the device; the server keeps a visitor code that changes every day, never the IP address. Not counted with Do Not Track, Global Privacy Control or `?tele=off`, which on `index.html` also turns off the class telemetry (live counts, reports, recordings). Both pages say so in their small print. Figures: the server's /stats page.
- `favicon.ico`, `apple-touch-icon.png`: browser and home-screen icons.
- `logo/`: the lockup (icon + name), the wordmark and the icon as SVG, and the icon as a 512 px PNG.

Address: https://mention-ice.github.io/Bit2Noisy/ (GitHub Pages of the repository `mention-ice/Bit2Noisy`). The QR code button uses `PAGE_SITE` in `index.html`; change that line if the page is published elsewhere.

© 2026 Sheng Yang. All rights reserved.
