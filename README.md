# 给阿嬷的情书 · Online Player

A lightweight, dependency-free web player that streams the full movie **《给阿嬷的情书》** (A Love Letter to Grandma, 1:58:03) directly in the browser — no download required by viewers.

**▶ Watch online: https://quant202602.github.io/love-letter-player/**

## How it works

| Piece | Role |
|---|---|
| `index.html` | Player page (pure HTML/CSS, no frameworks) served by GitHub Pages |
| `poster.jpg` | Poster frame extracted from the film |
| [Release asset `movie_720p.mp4`](https://github.com/quant202602/love-letter-player/releases/latest/download/movie_720p.mp4) | The 720p H.264/AAC encode (~1.8 GB), streamed with HTTP Range requests from GitHub's release CDN |

The video lives as a GitHub **Release asset** (2 GiB per-file limit) instead of inside the repository (100 MiB per-file limit), so the repo itself stays tiny while the stream is served by GitHub's CDN. The page uses `preload="metadata"` and `+faststart`, so playback starts quickly and seeking works without downloading the whole file.

## Encode details

- Source: YouTube 1080p (VP9/Opus)
- Output: 1280×720 H.264 High + AAC 128k, VBR ~2 Mbps, `+faststart`
- Encoded with NVENC (GTX 1080) in ~5 minutes

## Notes

- All rights to the film belong to its rightful owner(s). This page is for authorized distribution only.
