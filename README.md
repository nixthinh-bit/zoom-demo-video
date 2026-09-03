# Zoom Demo Video

A single-file, browser-based tool for adding zoom-in / zoom-out effects to a video, then exporting the result — no install, no upload, no server.

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
2. Drag & drop a video onto the frame, or click **Choose video…**. The file is read locally; nothing is uploaded.
3. Move the playhead by clicking or dragging on the timeline, or with `←` / `→`.

### Add a zoom

4. Click **+ Add zoom segment at playhead** (or press `A`). A yellow segment appears on the top timeline lane and is selected; the video pauses and jumps onto it.
5. Drag the segment's **left / right edges** to set when the zoom starts and ends — the playhead sticks to the edge you drag, so you can line it up to the exact frame. Drag the **middle** to move the whole segment.
6. **Drag on the video frame** to aim the zoom. The dashed **aim box** shows exactly what will be in frame at full zoom; drag inside it to move the target, or drag a **corner** to change the ratio. Toggle **Aim view** (`V`) to preview the settled zoom while you aim.
7. Fine-tune with the **Zoom ratio**, **Zoom-in speed**, and **Zoom-out speed** sliders (or `[` / `]` for the ratio). Outside every segment the video always stays unzoomed.
8. Click a segment on the timeline to re-select it; **Delete** removes the selected one.

### Add a highlight (optional)

9. Click **Highlighter** (or press `H`), then **drag on the frame** to draw a box. It stays bright while the rest of the frame dims.
10. Set its timing by dragging it on the **lower timeline lane**, and its darkness with the **Dim opacity** slider. The dim layer is included in the exported video.

### Save

11. Press **⤓ Save video** (or `R`). It rewinds to the start, plays through once at the video's native resolution, and saves the file automatically at the end. Press again to stop early. Use **⤓ Download again** to grab the file a second time.

That's it — no export settings, no render queue.

## Keyboard shortcuts

Also shown in-app under **? Keys** in the top bar. Ignored while a slider is focused (except `Esc` and `?`).

| Key | Action |
|---|---|
| `Space` | Play / pause |
| `A` | Add a zoom segment at the playhead |
| `H` | Toggle the Highlighter tool |
| `R` | Save the video (rewind, play, save), or stop early |
| `V` | Toggle Aim view (preview the settled zoom while editing) |
| `[` `]` | Selected zoom ratio by 0.1, or highlight dim opacity by 5% |
| `←` `→` | Step the playhead one frame |
| `Shift` + `←` `→` | Step the playhead one second |
| `Alt` + arrows | Nudge the zoom focus point (if your browser allows it) |
| `Delete` / `Backspace` | Delete the selected segment or highlight |
| `Esc` | Cancel a draw, exit the tool, deselect, or close the shortcut sheet |
| `?` | Show / hide the shortcut sheet |

## Browser notes

- Works best in Chrome or Edge (full MP4/H.264+AAC recording support).
- Keep the tab **in the foreground** while recording — browsers suspend canvas drawing in background tabs, and the tool will warn you after the fact if the capture rate dropped too low.

## License

MIT — see [LICENSE](LICENSE).
