# Zoom Demo Video

A single-file, browser-based tool for adding CapCut-style Ken Burns zoom effects to a video, then exporting the result — no install, no upload, no server.

**▶ [Try it now — no download needed](https://nixthinh-bit.github.io/zoom-demo-video/)**

[🇻🇳 Tiếng Việt](README.vi.md)

## Demo

https://github.com/user-attachments/assets/cbaa0d2c-6cca-428b-8ed2-0e9e0cc66167

*Recorded with the tool itself, zooming into a chat reply for emphasis. The content on screen (chat messages, a "7-11 Holiday Campaign" doc) is placeholder/example material used for demos and practice — it is not real data and is not related to any real company.*

## Why this exists

You want a quick zoom-in / zoom-out effect on parts of a video — a specific point, a specific time range, a specific speed — without opening a full video editor. This is a single HTML file that does exactly that and nothing else. Open it in a browser and it works.

## Features

- **Zoom segments** — mark a start and end point on the timeline; outside any segment the video always stays unzoomed.
- **Aim box** — select a zoom segment and a dashed box on the frame shows exactly what the zoom will land on at full ratio. Drag inside it to move the target, drag a corner to change the ratio. Near the frame edges the box stops at the boundary while the crosshair keeps moving, the same limit playback applies.
- **Highlighter** — turn on the tool and drag on the frame to draw a box that stays bright while the rest of the frame dims. Each highlight is its own timed item on a second timeline lane, with a Dim opacity slider and a short fade in and out. The dim layer is part of the recording.
- **Independent zoom-in / zoom-out speed** — control how fast it zooms in and how fast it eases back out, separately from the zoom ratio.
- **Keyboard shortcuts** — Space play/pause, `A` add zoom, `H` highlighter, `R` save video, `[` `]` adjust the ratio, arrows step the playhead, `?` opens a shortcut sheet. Full list under **? Keys** in the top bar.
- **Playhead follows your edit** — selecting a zoom segment or highlight pauses the video and parks the playhead on it; dragging its start or end handle then scrubs the preview to that exact edge, so you can line the effect up to the frame instead of watching playback run past it.
- **Smooth motion** — zoom is interpolated at display refresh rate with an easing curve that has zero velocity *and* zero acceleration at both ends of each ramp, so there's no stutter or "kick" at the edges.
- **Responsive canvas** — the preview sizes itself to the video's own aspect ratio, not a fixed pixel size.
- **One-click Save video** — rewinds to the start, plays, captures the canvas at the video's native resolution, stops automatically at the end, and saves the file (MP4 H.264/AAC where supported, WebM otherwise). It also measures the actual capture rate and warns you if the tab was backgrounded and the take stuttered.
- **English / Vietnamese toggle** — top-right corner, defaults to English, remembered between visits.
- **100% local** — the video is read via `URL.createObjectURL`; nothing is ever uploaded anywhere.

## Usage

1. Open [`index.html`](index.html) in a browser, or use the **[live version](https://nixthinh-bit.github.io/zoom-demo-video/)** — no download needed.
2. Drag & drop a video onto the frame, or click **Choose video…**.
3. Click **+ Add zoom segment at playhead** to create a zoom segment where the playhead currently is.
4. Drag the segment's edges on the timeline to set exactly when the zoom starts and ends. Drag its middle to move the whole thing.
5. Drag on the video frame to aim the zoom. The dashed aim box previews the framing; drag a corner to change the ratio.
6. Adjust **Zoom ratio**, **Zoom-in speed**, and **Zoom-out speed** with the sliders, or press `[` / `]` for the ratio.
7. Optional: click **Highlighter** (or press `H`), drag on the frame to draw a highlight box, then set its timing on the lower timeline lane and its **Dim opacity**.
8. Repeat to add as many zoom segments and highlights as you want, anywhere on the timeline.
9. Press **⤓ Save video**. It rewinds to the start, plays through automatically, and saves the finished clip once it reaches the end — nothing else to click.

That's it — no export settings, no render queue.

## Browser notes

- Works best in Chrome or Edge (full MP4/H.264+AAC recording support).
- Keep the tab **in the foreground** while recording — browsers suspend canvas drawing in background tabs, and the tool will warn you after the fact if the capture rate dropped too low.

## License

MIT — see [LICENSE](LICENSE).
