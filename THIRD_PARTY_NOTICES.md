# Third-Party Notices

- **@ffmpeg/ffmpeg 0.12.15** — MIT. The JavaScript wrapper is vendored in
  `public-site/vendor/ffmpeg/`. Source and license:
  <https://github.com/ffmpegwasm/ffmpeg.wasm>.
- **@ffmpeg/core 0.12.10** — GPL-2.0-or-later. The single-thread WebAssembly
  core is fetched from the version-pinned jsDelivr URL only after local
  processing consent. Its loader and WebAssembly binary are SHA-256 verified
  before execution. Source and license:
  <https://github.com/ffmpegwasm/ffmpeg.wasm>.
- **Vette1123/social-media-downloader** — MIT, Copyright 2025 Mohamed Gado.
  Small public-embed parsing patterns were adapted for the Cloudflare resolver;
  the project was not imported wholesale. Source and license:
  <https://github.com/Vette1123/social-media-downloader>.

The vendored FFmpeg browser wrapper has a local modification to reject pending
calls and terminate its Worker when a Worker error occurs.
