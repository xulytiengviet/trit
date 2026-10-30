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
