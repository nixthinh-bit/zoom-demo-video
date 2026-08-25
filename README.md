# Zoom Demo Video

A single-file, browser-based tool for adding CapCut-style Ken Burns zoom effects to a video, then exporting the result — no install, no upload, no server.

**▶ [Try it now — no download needed](https://nixthinh-bit.github.io/zoom-demo-video/)**

[🇻🇳 Tiếng Việt](README.vi.md)

## Demo

https://github.com/nixthinh-bit/zoom-demo-video/raw/main/assets/demo-recording.mp4

*If the video doesn't play inline above, [watch/download it directly](assets/demo-recording.mp4).*

*Recorded with the tool itself, zooming into a chat reply for emphasis. The content on screen (chat messages, a "7-11 Holiday Campaign" doc) is placeholder/example material used for demos and practice — it is not real data and is not related to any real company.*

## Why this exists

You want a quick zoom-in / zoom-out effect on parts of a video — a specific point, a specific time range, a specific speed — without opening a full video editor. This is a single HTML file that does exactly that and nothing else. Open it in a browser and it works.

## Features

- **Zoom segments** — mark a start and end point on the timeline; outside any segment the video always stays unzoomed.
- **Click to set the zoom point** — click or drag directly on the frame to choose what to zoom into; a magnifying-glass cursor shows you're in focus-picking mode.
- **Independent zoom-in / zoom-out speed** — control how fast it zooms in and how fast it eases back out, separately from the zoom ratio.
- **Edit while playing** — dragging a segment's edges or picking a new focus point never pauses or rewinds playback.
- **Smooth motion** — zoom is interpolated at display refresh rate with an easing curve that has zero velocity *and* zero acceleration at both ends of each ramp, so there's no stutter or "kick" at the edges.
- **Responsive canvas** — the preview sizes itself to the video's own aspect ratio, not a fixed pixel size.
- **One-click Record** — rewinds to the start, plays, captures the canvas at the video's native resolution, stops automatically at the end, and saves the file (MP4 H.264/AAC where supported, WebM otherwise). It also measures the actual capture rate and warns you if the tab was backgrounded and the take stuttered.
- **English / Vietnamese toggle** — top-right corner, defaults to English.
- **100% local** — the video is read via `URL.createObjectURL`; nothing is ever uploaded anywhere.

## Usage

1. Open [`index.html`](index.html) in a browser, or use the **[live version](https://nixthinh-bit.github.io/zoom-demo-video/)** — no download needed.
2. Drag & drop a video onto the frame, or click **Choose video…**.
3. Click **+ Add zoom segment at playhead** to create a zoom segment where the playhead currently is.
4. Drag the segment's edges on the timeline to set exactly when the zoom starts and ends. Drag its middle to move the whole thing.
5. Click on the video frame to set the point it zooms into.
6. Adjust **Zoom ratio**, **Zoom-in speed**, and **Zoom-out speed** with the sliders.
7. Repeat steps 3–6 to add as many zoom segments as you want, anywhere on the timeline.
8. Press **● Record**. It rewinds to the start, plays through automatically, and saves the finished clip once it reaches the end — nothing else to click.

That's it — no export settings, no render queue.

## Browser notes

- Works best in Chrome or Edge (full MP4/H.264+AAC recording support).
- Keep the tab **in the foreground** while recording — browsers suspend canvas drawing in background tabs, and the tool will warn you after the fact if the capture rate dropped too low.

## License

MIT — see [LICENSE](LICENSE).
