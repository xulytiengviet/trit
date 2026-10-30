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

