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

- **Bố cục bento** - video bên trái, ô Chuyển động và ô Đang chọn bên phải, thanh phát và timeline nằm ngang bên dưới, nên mọi thứ vừa một màn hình. Trên điện thoại các ô xếp chồng.
- **Thêm zoom ngay trên timeline** - click vào dải Zoom để thêm zoom tại đó, hoặc kéo quét trên dải để tạo đoạn dài đúng bằng khoảng kéo. Trước khi click đã thấy một khối `+` nét đứt báo chỗ khối sẽ nằm. Phím `A` thêm tại playhead.
- **Mỗi đoạn zoom chỉ có 2 thứ để chỉnh** - zoom sâu bao nhiêu (thanh trượt, nút bấm nhanh 1.5×, 2×, 2.5×, 3× và **Áp cho tất cả**) và nhìn vào đâu (kéo chấm trên video). Đoạn mới dùng lại tỷ lệ bạn chọn gần nhất.
- **Zoom vào, giữ, tự trở lại** - mỗi đoạn zoom vào ở điểm bắt đầu, giữ nguyên khung hình trong số giây bạn đặt, rồi tự trở lại màn hình thường. Zoom vào và zoom ra mất cố định nửa giây, nên thời gian giữ là thứ duy nhất bạn cần đặt. Đoạn mới giữ lâu bằng đoạn bạn đặt gần nhất.
- **Một cài đặt chuyển động cho cả video** - chọn một lần **Mượt**, **Nhanh**, **Nảy** hoặc **Cắt cứng**, mọi đoạn zoom chuyển động giống nhau. Cắt cứng bỏ hiệu ứng, nhảy thẳng vào và nhảy thẳng ra. Chọn xong app phát thử một đoạn; **▶ Xem thử** để phát lại. Lựa chọn được ghi nhớ.
- **Lia giữa hai chỗ** - đặt hai đoạn zoom sát nhau (cạnh tự hút vào nhau, hoặc tách một đoạn bằng `X`), khung hình sẽ trượt từ chỗ thứ nhất sang chỗ thứ hai mà không zoom ra ở giữa. Dấu ⇄ nhỏ đánh dấu mỗi chỗ lia.
- **Menu chuột phải** - trên một khối: tách tại playhead, mức zoom, áp tỷ lệ cho tất cả, sao chép, nhân bản, xoá. Trên chỗ trống của dải: thêm ở đây, dán vào đây. Trên dải Video: cắt tại playhead, bỏ cắt.
- **Hoàn tác và làm lại** - `Cmd` + `Z` và `Shift` + `Cmd` + `Z` (Windows dùng `Ctrl`) cho mọi thao tác, kể cả cắt video và kéo khối.
- **Timeline phóng được** - chụm hai ngón trên touchpad (hoặc `Ctrl` + cuộn) để phóng timeline quanh con trỏ, cuộn để lướt dọc, hoặc dùng `=` / `-` / `0`, thanh trượt và nút **Vừa khung**. Thước thời gian tự đổi vạch chia theo mức phóng, timeline tự cuộn theo playhead khi phát.
- **Khối zoom vẽ theo chuyển động** - mỗi khối zoom vẽ theo đường cong đã chọn: cạnh lên là zoom vào, mặt phẳng là giữ, cạnh xuống là zoom ra, kèm tỷ lệ ghi trên đó.
- **Nhập số chính xác và hút cạnh** - ô Đang chọn có **Zoom vào lúc** và **Giữ zoom** để gõ thẳng, kèm một dòng cho biết lúc nào trở lại màn hình thường. Kéo một cạnh sẽ hút vào các khối khác, điểm cắt và hai đầu video; giữ `Alt` để kéo tự do.
- **Vùng sáng** - click vào dải Vùng sáng (hoặc bấm `H`) để thêm một khung giữ nguyên độ sáng trong khi phần còn lại tối đi. Khi đang chọn vùng sáng, kéo khung hoặc tay cầm trên video, hoặc kéo ra ngoài khung để vẽ lại. Lớp tối nằm trong bản quay.
- **Cắt video ngay trên dải của nó** - dải Video hiện video của bạn thành một thanh; kéo một trong hai đầu màu xanh để cắt phần đầu hoặc phần cuối, hoặc bấm `I` / `O` tại playhead. Phát và Lưu video chỉ dùng đoạn bạn giữ lại. File gốc không bị đụng tới, nút ↺ cạnh tên dải trả lại toàn bộ.
- **Playhead bám theo thao tác chỉnh** - chọn một khối thì video tạm dừng và playhead nhảy vào khối đó; kéo một cạnh thì preview tua theo đúng cạnh đang kéo, để bạn canh hiệu ứng khớp tới từng khung hình.
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

4. **Click vào dải Zoom** của timeline tại chỗ zoom nên bắt đầu (hoặc bấm `A` để thêm tại playhead). Muốn đặt luôn độ dài thì **kéo quét trên dải**. Khối mới được chọn và video dừng ngay trên đó.
5. Kéo **hai cạnh** khối để đổi lúc bắt đầu và kết thúc (playhead bám theo cạnh đang kéo), kéo **phần giữa** để dời, hoặc gõ số vào **Zoom vào lúc** và **Giữ zoom** ở ô Đang chọn. Khối nhỏ quá khó nắm thì phóng timeline lên (chụm hai ngón hoặc `Ctrl` + cuộn).
6. **Kéo chấm xanh trên video** để chọn chỗ cần nhìn. Khung nét đứt cho thấy đúng phần sẽ lọt vào frame khi zoom hết cỡ; kéo **góc** khung để đổi tỷ lệ. Bật **Xem khung zoom** (`V`) để xem trước mức zoom đã đặt trong lúc căn.
7. Đặt tỷ lệ bằng thanh trượt hoặc một trong các nút **1.5× / 2× / 2.5× / 3×** (hoặc `[` / `]`, hay chụm hai ngón trên khung hình). **Áp cho tất cả** đặt tỷ lệ này cho mọi đoạn zoom.
8. Ở ô **Chuyển động**, chọn cách mọi đoạn zoom vào và ra (Mượt, Nhanh, Nảy hoặc Cắt cứng). **▶ Xem thử** để xem.
9. Muốn lia từ chỗ này sang chỗ kia, đặt đoạn zoom thứ hai sát vào đoạn thứ nhất (hoặc chọn một đoạn rồi bấm `X` để tách tại playhead), rồi kéo chấm của đoạn thứ hai. Dấu ⇄ hiện ở chỗ lia.
10. Chuột phải vào khối để tách, đổi mức zoom, sao chép, nhân bản hoặc xoá. `Cmd` + `Z` hoàn tác bất kỳ bước nào.

### Thêm vùng làm sáng (tuỳ chọn)

11. Click vào **dải Vùng sáng** (hoặc bấm `H`). Một khung hiện trên video; kéo khung hoặc tay cầm vào đúng chỗ, hoặc kéo ra ngoài khung để vẽ lại.
12. Đặt thời gian bằng cách kéo khối trên dải Vùng sáng, chỉnh độ tối bằng thanh **Độ tối nền**. Lớp tối này nằm trong video xuất ra.

### Cắt video (tuỳ chọn)

13. Kéo **hai đầu màu xanh của dải Video** vào trong, hoặc bấm `I` / `O` để cắt tại playhead. Playhead bám theo đầu đang kéo nên bạn thấy đúng khung hình đầu hoặc cuối được giữ lại. **Phát** và **Lưu video** chỉ dùng phần đó; nút ↺ cạnh tên dải để bỏ cắt.

### Lưu

14. Bấm **⤓ Lưu video** (hoặc `R`). App tự tua về đầu đoạn đã cắt, phát hết một lượt ở độ phân giải gốc, và tự lưu file khi kết thúc. Bấm lần nữa để dừng sớm. Dùng **⤓ Tải lại file** nếu cần lấy file thêm lần nữa.

Vậy là xong — không cần chỉnh export, không cần chờ render.

## Phím tắt

Cũng có trong app ở nút **? Phím tắt** trên thanh trên cùng. Bỏ qua khi con trỏ đang ở trong thanh trượt (trừ `Esc` và `?`).

| Phím | Tác dụng |
|---|---|
| Click / kéo quét dải Zoom | Thêm zoom tại đó, dài đúng bằng khoảng kéo |
| Chuột phải vào khối | Tách, mức zoom, sao chép, nhân bản, xoá |
| `Space` | Phát / tạm dừng |
| `A` / `H` | Thêm zoom / vùng sáng tại playhead |
| `X` | Tách khối đang chọn (hoặc đoạn zoom dưới playhead) tại playhead |
| `Cmd` + `Z` / `Shift` + `Cmd` + `Z` | Hoàn tác / làm lại (Windows dùng `Ctrl`) |
| `Cmd` + `C` / `V` / `D` | Sao chép / dán tại playhead / nhân bản |
| `R` | Lưu video (tua về đầu, phát, lưu), hoặc dừng sớm |
| `I` `O` | Cắt: cho video bắt đầu / kết thúc tại playhead |
| `V` | Bật / tắt Xem khung zoom (xem trước mức zoom khi đang chỉnh) |
| `[` `]` | Tỷ lệ zoom ±0.1, hoặc độ tối nền vùng sáng ±5% |
| `←` `→` | Dời playhead một khung hình (`Shift`: một giây) |
| `=` `-` `0` | Phóng to / thu nhỏ timeline / xem toàn bộ video |
| Chụm hai ngón, `Ctrl` + cuộn | Trên timeline: phóng timeline. Trên video: đổi tỷ lệ đoạn zoom đang chọn |
| Giữ `Alt` khi kéo | Tắt hút cạnh |
| `Delete` / `Backspace` | Xoá khối đang chọn |
| `Esc` | Đóng menu, bỏ chọn, hoặc đóng bảng phím tắt |
| `?` | Hiện / ẩn bảng phím tắt |

## Lưu ý về trình duyệt

- Dùng Chrome hoặc Edge cho kết quả tốt nhất (hỗ trợ đầy đủ ghi MP4 H.264+AAC).
- Giữ tab ở **phía trước** trong lúc quay — trình duyệt sẽ ngưng vẽ canvas khi tab chạy nền, và tool sẽ cảnh báo sau đó nếu tốc độ ghi bị tụt quá thấp.

## Giấy phép

MIT — xem [LICENSE](LICENSE).
