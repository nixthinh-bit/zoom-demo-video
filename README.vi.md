# Zoom Demo Video

Công cụ thêm hiệu ứng zoom in / zoom out cho video, chạy gọn trong một file HTML — không cần cài đặt, không upload, không cần server.

**▶ [Dùng thử ngay — không cần tải về](https://nixthinh-bit.github.io/zoom-demo-video/)**

[🇬🇧 English](README.md)

## Demo

https://github.com/user-attachments/assets/cbaa0d2c-6cca-428b-8ed2-0e9e0cc66167

*Quay bằng chính công cụ này, zoom vào một tin nhắn trả lời để nhấn mạnh. Nội dung xuất hiện trong video (tin nhắn chat, tài liệu "7-11 Holiday Campaign") là dữ liệu ví dụ/demo dùng để luyện tập, không phải dữ liệu thật và không liên quan đến bất kỳ công ty nào.*

## Vì sao có tool này

Đôi khi bạn chỉ cần zoom vào một điểm cụ thể, trong một khoảng thời gian cụ thể, với tốc độ cụ thể — mà không muốn mở hẳn một phần mềm dựng phim. Đây là một file HTML duy nhất làm đúng việc đó. Mở lên là dùng được ngay.

## Tính năng

- **Đoạn zoom (zoom segment)** — đánh dấu điểm bắt đầu và kết thúc trên timeline; ngoài các đoạn đã đặt, video luôn giữ nguyên không zoom.
- **Khung ngắm** — chọn một đoạn zoom, trên khung hình hiện một khung nét đứt cho thấy đúng phần sẽ lọt vào frame khi zoom hết cỡ. Kéo bên trong để dời tâm, kéo góc để đổi tỷ lệ. Gần mép frame, khung dừng ở biên trong khi dấu ngắm vẫn chạy tiếp, đúng như giới hạn lúc phát video.
- **Làm sáng vùng (highlighter)** — bật công cụ rồi kéo trên khung hình để vẽ một vùng giữ nguyên độ sáng còn phần còn lại bị tối đi. Mỗi vùng sáng là một mục có thời gian riêng ở làn thứ hai của timeline, kèm thanh Độ tối nền và fade vào/ra ngắn. Lớp tối nằm trong bản quay.
- **Tốc độ zoom vào / zoom ra độc lập** — chỉnh riêng tốc độ zoom vào và tốc độ zoom trở lại, tách biệt với tỷ lệ zoom.
- **Phím tắt** — Space phát/dừng, `A` thêm đoạn zoom, `H` làm sáng vùng, `R` lưu video, `[` `]` chỉnh tỷ lệ, phím mũi tên dời playhead, `?` mở bảng phím tắt. Danh sách đầy đủ ở nút **? Phím tắt** trên thanh trên cùng.
- **Playhead bám theo thao tác chỉnh** — chọn một đoạn zoom hay vùng sáng thì video tạm dừng và playhead nhảy vào mục đó; kéo hai đầu đoạn thì preview tua theo đúng cạnh đang kéo, để bạn canh hiệu ứng khớp tới từng khung hình thay vì video cứ chạy tiếp qua mất.
- **Chuyển động mượt** — zoom được nội suy theo nhịp làm mới màn hình với đường cong easing triệt tiêu cả vận tốc lẫn gia tốc ở hai đầu mỗi đoạn chuyển, nên không bị khựng hay giật ở điểm nối.
- **Canvas responsive** — khung preview tự co giãn theo đúng tỷ lệ khung hình của video, không cố định kích thước.
- **Bấm Lưu video là xong** — tự tua về đầu, tự phát, ghi thẳng từ canvas ở đúng độ phân giải gốc video, tự dừng khi hết video, tự lưu file (MP4 H.264/AAC nếu trình duyệt hỗ trợ, WebM nếu không). Tool còn đo tốc độ ghi thực tế và cảnh báo nếu tab bị chạy nền khiến bản ghi bị khựng.
- **Chuyển ngôn ngữ Anh/Việt** — nút ở góc trên phải, mặc định tiếng Anh, ghi nhớ cho lần sau.
- **Chạy hoàn toàn cục bộ** — video được đọc qua `URL.createObjectURL`, không bao giờ upload lên đâu cả.

## Cách dùng

1. Mở [`index.html`](index.html) bằng trình duyệt, hoặc dùng **[bản online](https://nixthinh-bit.github.io/zoom-demo-video/)** — không cần tải về.
2. Kéo-thả video vào khung hình, hoặc bấm **Choose video…**. File đọc trực tiếp trên máy, không upload đi đâu.
3. Dời playhead bằng cách click hoặc kéo trên timeline, hoặc dùng `←` / `→`.

### Thêm một đoạn zoom

4. Bấm **+ Add zoom segment at playhead** (hoặc phím `A`). Một đoạn màu vàng hiện ở làn trên của timeline và được chọn; video tạm dừng và nhảy vào đoạn đó.
5. Kéo **hai đầu** đoạn để đặt thời điểm zoom bắt đầu và kết thúc — playhead bám theo đúng cạnh bạn kéo, canh được tới từng khung hình. Kéo **phần giữa** để dời cả đoạn.
6. **Kéo trên khung hình** để ngắm điểm zoom. **Khung ngắm** nét đứt cho thấy đúng phần sẽ lọt frame khi zoom hết cỡ; kéo bên trong để dời tâm, kéo **góc** để đổi tỷ lệ. Bật **Aim view** (`V`) để xem trước mức zoom đã đặt trong lúc căn.
7. Tinh chỉnh bằng 3 thanh **Zoom ratio**, **Zoom-in speed**, **Zoom-out speed** (hoặc `[` / `]` cho tỷ lệ). Ngoài mọi đoạn, video luôn giữ nguyên không zoom.
8. Click một đoạn trên timeline để chọn lại; **Delete** xoá đoạn đang chọn.

### Thêm vùng làm sáng (tuỳ chọn)

9. Bấm **Highlighter** (hoặc phím `H`), rồi **kéo trên khung hình** để vẽ một vùng. Vùng đó giữ nguyên độ sáng, phần còn lại bị tối đi.
10. Đặt thời gian bằng cách kéo nó trên **làn dưới của timeline**, chỉnh độ tối bằng thanh **Dim opacity**. Lớp tối này nằm trong video xuất ra.

### Lưu

11. Bấm **⤓ Lưu video** (hoặc `R`). App tự tua về đầu, phát hết một lượt ở độ phân giải gốc, và tự lưu file khi kết thúc. Bấm lần nữa để dừng sớm. Dùng **⤓ Tải lại file** nếu cần lấy file thêm lần nữa.

Vậy là xong — không cần chỉnh export, không cần chờ render.

## Phím tắt

Cũng có trong app ở nút **? Phím tắt** trên thanh trên cùng. Bỏ qua khi con trỏ đang ở trong thanh trượt (trừ `Esc` và `?`).

| Phím | Tác dụng |
|---|---|
| `Space` | Phát / tạm dừng |
| `A` | Thêm đoạn zoom tại playhead |
| `H` | Bật / tắt công cụ Làm sáng vùng |
| `R` | Lưu video (tua về đầu, phát, lưu), hoặc dừng sớm |
| `V` | Bật / tắt Aim view (xem trước mức zoom khi đang chỉnh) |
| `[` `]` | Tỷ lệ zoom ±0.1, hoặc độ tối nền vùng sáng ±5% |
| `←` `→` | Dời playhead một khung hình |
| `Shift` + `←` `→` | Dời playhead một giây |
| `Alt` + phím mũi tên | Nhích điểm zoom (nếu trình duyệt cho phép) |
| `Delete` / `Backspace` | Xoá đoạn zoom hoặc vùng sáng đang chọn |
| `Esc` | Huỷ nét đang vẽ, thoát công cụ, bỏ chọn, hoặc đóng bảng phím tắt |
| `?` | Hiện / ẩn bảng phím tắt |

## Lưu ý về trình duyệt

- Dùng Chrome hoặc Edge cho kết quả tốt nhất (hỗ trợ đầy đủ ghi MP4 H.264+AAC).
- Giữ tab ở **phía trước** trong lúc quay — trình duyệt sẽ ngưng vẽ canvas khi tab chạy nền, và tool sẽ cảnh báo sau đó nếu tốc độ ghi bị tụt quá thấp.

## Giấy phép

MIT — xem [LICENSE](LICENSE).
