# TRITLAB.EXE — Ternary vs Binary KPI

Bảng điều khiển **100 KPI về điện toán tam phân (ternary/trit) và nhị phân (binary/bit)** bằng tiếng Việt, giao diện **Neon Audit DOS — nền đen MS-DOS, chữ neon đa sắc kiểu thám mã/kiểm toán**.

## Trải nghiệm
- Nền đen giữ nguyên phong cách MS-DOS cổ điển; chỉ chữ, nhãn và trạng thái thay đổi màu neon (cyan, xanh lá, hồng, tím, vàng, đỏ), không sử dụng nền màu rực.
- 100 KPI, 11 lĩnh vực; tìm kiếm có hỗ trợ không dấu, lọc nhóm, sắp xếp và phân trang.
- Biểu đồ SVG tự dựng và bảng dữ liệu; xem giải thích, đường dẫn nguồn theo từng KPI.
- Dòng lệnh mô phỏng DOS: `HELP`, `FIND`, `CAT`, `VIEW`, `SORT`, `EXPORT`, `RESET`, `CRT`, `INVERT`, `TOP`, `CLS`.
- Tải CSV UTF-8, chuyển nền trắng/đen bằng F2, bố cục đáp ứng thiết bị di động.
- Một tệp HTML độc lập, không cần Chart.js, CDN hay bước build, có thể mở offline.

## Chạy cục bộ
Mở `index.html` trực tiếp bằng trình duyệt; hoặc chạy web server tĩnh bất kỳ ở thư mục repository.

## GitHub Pages
Nếu Pages chưa bật, vào **Settings → Pages → Build and deployment → Deploy from a branch**, chọn **main** và **/(root)** rồi Save. URL dự kiến khi Pages được bật: https://xulytiengviet.github.io/trit/

## Lưu ý học thuật
Bộ KPI, mô tả và nguồn dẫn được **giữ lại từ tệp HTML gốc do người dùng cung cấp**. Các trích dẫn và tuyên bố định lượng chưa được xác minh độc lập. Giá trị `adv` trong dữ liệu gốc chứa cả tỷ lệ %, chỉ số quy đổi từ số lần tăng tốc và các trường hợp bất lợi; **không được coi là một thước đo thống nhất**. Không dùng trung bình và bảng xếp hạng `adv` để kết luận ưu thế tuyệt đối của phần cứng tam phân.

## Giấy phép
Chưa có giấy phép mã nguồn được công bố trong repository. Liên hệ chủ sở hữu để xin phép tái sử dụng ngoài phạm vi được luật cho phép.


## Tab BIỂU DIỄN — 70 cách biểu diễn / encoding ternary

Truy cập [BIỂU DIỄN](https://xulytiengviet.github.io/trit/#representations) để xem 70 bản ghi chia thành **8 nhóm**: ký hiệu/cơ số, balanced ternary, đơn vị & kiến trúc, mã ký tự, đường truyền, dấu phẩy động, chuyển đổi/đóng gói và mã sửa lỗi.

- Tìm kiếm theo tên, mô tả, tài liệu; lọc nhóm và mức đối chiếu nguồn.
- Mỗi mục có giải thích, nguồn liên kết, trạng thái **TRỰC TIẾP / LIÊN QUAN / CẦN KIỂM CHỨNG**, và cảnh báo kỹ thuật khi cần.
- 35 mục có tài liệu đối chiếu trực tiếp cho thuật ngữ/chủ đề chính; 22 mục được đánh dấu cần rà soát kỹ thuật. Con số không mang nghĩa đã xác thực mọi tuyên bố.
- Lưu danh sách đã chú thích trong `data/representations.json` và nguyên bản tài liệu người dùng ở `docs/70-bieu-dien-nguon.md`.

**Lưu ý khoa học:** 70 mục không tương đương 70 tiêu chuẩn độc lập. Có các biến thể tên gọi hoặc dữ liệu trùng lặp; một số tuyên bố có giới hạn toán học: 2 bit có 4 trạng thái không thể ánh xạ mất-mát-bằng-không thành 1 trit có 3 trạng thái; 5 trit chỉ mã hóa được 243 giá trị; tryte có độ rộng khác nhau theo kiến trúc. Nguồn loại LIÊN QUAN chỉ là tài liệu nền, không phải bằng chứng trực tiếp cho biến thể.



## Tab MORSE / TRIT / AUDIO

[Mở phòng thí nghiệm tín hiệu](https://xulytiengviet.github.io/trit/morse.html) — giao diện Neon Audit DOS tự chạy (converter CVNSS4.0 được nhúng offline).

Pipeline trực quan: **Quốc ngữ → CVNSS4.0 v5.0.0-audit-safe → Base27 → 3 balanced trits → Morse → Audio**.

- Dùng nguyên thuật toán CVNSS4.0 audit-safe do người dùng cung cấp, có `selfTest()` 23 phép kiểm tra.
- Hai chế độ: **TRIT→MORSE** (mã thí nghiệm 2 phần tử/trit, có ranh giới) và **CVNSS→MORSE ITU** (Morse quốc tế cho A–Z).
- Phát / tạm dừng / dừng; chỉnh tốc độ WPM, tần số âm; waveform, từng ký tự/trit tô sáng theo thời gian.
- Xuất âm thanh WAV (PCM mono) và sao chép chuỗi Morse; hoàn toàn client-side.
- Bộ ký tự thử nghiệm: khoảng trắng + A–Z; một ký tự → một số Base27 → 3 trit cân bằng. Ký tự khác được báo rõ là bị bỏ khỏi kênh truyền; giới hạn 64 ký tự/lượt.
- **Lưu ý khoa học:** TRIT→MORSE là ánh xạ có khung riêng của TRITLAB, *không phải* Morse ITU tiêu chuẩn cho trit. Bộ ba trit bảo toàn chuỗi CVNSS trong phạm vi alphabet nói trên, nhưng CVNSS không luôn bảo toàn khả năng giải mã Quốc ngữ duy nhất.

Tham khảo số học balanced ternary: https://github.com/Trehinos/balanced-ternary#1; quy tắc Morse quốc tế: https://www.itu.int/rec/R-REC-M.1677/en.


## Chuyên mục CVNSS4.0 — Base27 × 3 Trit

[Mở phòng thí nghiệm CVNSS4.0](https://xulytiengviet.github.io/trit/cvnss.html) — tab [04] trong điều hướng chung.

- Tận dụng `cvnss-converter.js` tách từ bộ chuyển đổi `v5.0.0-audit-safe` đã có trong `morse.html`, không tự sáng tác lại quy tắc CVNSS4.0.
- Hai chế độ đầu vào: Quốc ngữ hoặc CVNSS4.0; xuất CVN, CVNSS, chỉ số Base27 và bộ 3 trit cân bằng theo bảng `␠ABCDEFGHIJKLMNOPQRSTUVWXYZ`.
- Mã ngược `T/0/1 → 0..26 → CVNSS`, kiểm thử vét cạn 27/27 và self-test của converter; thao tác trong trình duyệt, hỗ trợ tải JSON.
- Bảy hướng nghiên cứu: mã hóa trạng thái, phân cấp 3 × 9, số học balanced ternary, kiểm chứng hình thức, ternary LLM, lưu trữ/IoT và qutrit.
- Phân biệt rõ: `3 trit = log₂27 ≈ 4,755 bit thông tin`; `1 trit = log₂3 ≈ 1,585 bit`. Việc có đủ 27 mã **không tạo khả năng phát hiện lỗi**, không tự chứng minh nén dữ liệu hay giảm tiêu thụ năng lượng.
- Bộ mã Base27 ↔ trit bảo toàn tuyệt đối chuỗi CVNSS nằm trong bảng 27 ký hiệu, nhưng **không bảo đảm** giải mã Quốc ngữ duy nhất trong các trường hợp nhập nhằng.

Trang `cvnss.html` cần được phân phối cùng tệp `cvnss-converter.js` khi mở offline. Nguồn mở tham khảo: [Trehinos/balanced-ternary](https://github.com/Trehinos/balanced-ternary), [microsoft/BitNet](https://github.com/microsoft/BitNet).

