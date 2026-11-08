# ffmpeg-binaries

A pinned copy of the ffmpeg build that the [`ffmpeg-static`](https://github.com/eugeneware/ffmpeg-static) npm package downloads, so our builds do not depend on that project's release downloads being up.

## What is here

| Folder | Files | Source |
|---|---|---|
| `b6.1.1/` | `ffmpeg-linux-x64.gz`, `linux-x64.README`, `linux-x64.LICENSE` | `https://github.com/eugeneware/ffmpeg-static/releases/download/b6.1.1/` (`ffmpeg-static` 5.3.0) |

The files are unchanged. Their SHA-256 sums are in `b6.1.1/SHA256SUMS`.

## How it is used

`ffmpeg-static` reads the download location from `FFMPEG_BINARIES_URL` and fetches `<url>/<release>/ffmpeg-<platform>-<arch>.gz`. Builds point it here:

```
FFMPEG_BINARIES_URL=https://raw.githubusercontent.com/Lechatchila-org/ffmpeg-binaries/main
```

The files are served as plain repository files, not as release assets, so they do not depend on GitHub's release downloads either.

## License

ffmpeg is licensed under the GNU GPL. The license and the build's notes are in `linux-x64.LICENSE` and `linux-x64.README`. The source code is at https://ffmpeg.org/download.html, and the build scripts are at https://github.com/eugeneware/ffmpeg-static.
