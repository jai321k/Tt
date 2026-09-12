DUO TROUBLE — GODOT WEB EXPORT

Place your Godot Web export files directly in this folder:

  games/duo-trouble/web/index.html
  games/duo-trouble/web/index.js
  games/duo-trouble/web/index.wasm
  games/duo-trouble/web/index.pck
  ...and any other files Godot generates.

The "PLAY DUO TROUBLE" button on games/duo-trouble.html checks for
this exact path:

  /games/duo-trouble/web/index.html

As soon as index.html exists here, the button will load it into an
embedded iframe automatically — no code changes needed.

Notes for hosting the Godot export:
- Export with "Godot Engine" template settings for Web (HTML5).
- Make sure your server sends the correct MIME types for .wasm
  (application/wasm) — most static hosts do this by default.
- If you enable threads in your Godot export, your host must send
  the two cross-origin isolation headers Godot's docs specify
  (COOP / COEP), or the build will fail to start.
