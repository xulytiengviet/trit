###  20 cách biểu diễn/encoding ternary cơ bản (đã liệt kê trước đó)

1. **Heptavintimal (cơ số 27) – bộ ký tự chuẩn**\
   Mỗi chữ số biểu diễn 3 trit (trybble). Bộ ký tự: `0–9, A, B, C, D, E, F, G, H, K, M, N, P, R, T, V, X, Z` (loại I và O). Đây là dạng shorthand ternary phổ biến nhất, tương tự hex với binary.
2. **Septemvigesimal (cơ số 27) dùng A–Q**\
   Biến thể cũ hơn: các chữ số 10–26 được ký hiệu bằng A–Q. Mỗi chữ số vẫn đại diện cho 3 trit.
3. **Base-27 với dấu gạch dưới&#x20;**`_`**&#x20;cho số 0**\
   Dùng `_` thay cho 0, còn 1–26 dùng A–Z. Thường gặp trong các bộ thư viện mã hóa base-27.
4. **Base-27 với khoảng trắng cho số 0**\
   Ánh xạ 0 thành khoảng trắng, 1–26 thành A–Z. Đôi khi được dùng trong các câu đố hoặc mã hóa văn bản từ ternary triplet.
5. **Base-27 với số 0 "ẩn" (elided)**\
   Số 0 được lược bỏ hoặc thay bằng `_`, thường thấy trong các định dạng floating-point như TAPI27. Ví dụ: `..._____A` thay vì `...00000A`.
6. **Balanced base-27 dùng&#x20;**`i`**&#x20;cho −1**\
   Trong balanced ternary base-27, trit âm (−1) được viết là `i`. Ví dụ: `Z` = `iii`, `ZA` = `iii001`... Mỗi chữ số vẫn là 3 trit.
7. **Balanced ternary với&#x20;**`T, 0, 1`\
   `T` đại diện cho −1, `0` và `1` giữ nguyên. Đây là quy ước phổ biến nhất khi viết balanced ternary bằng văn bản.
8. **Balanced ternary với&#x20;**`-, 0, +`\
   Dùng dấu trừ `-` cho −1, `0` cho 0, dấu cộng `+` cho +1. Cách này trực quan và hay dùng trong tài liệu giải thích thuật toán.
9. **Balanced ternary với ký hiệu Θ (theta)**\
   Một số tài liệu dùng chữ Hy Lạp theta (Θ) để biểu diễn −1, vì hình dạng giống dấu trừ trong vòng tròn.
10. **3's complement ternary**\
    Dùng các giá trị 0, 1, 2 cho từng trit, với cơ chế bù ba (3's complement) để biểu diễn số âm, tương tự 2's complement trong nhị phân.
11. **Unsigned ternary (0, 1, 2)**\
    Hệ tam phân cơ bản nhất: mỗi trit nhận một trong ba giá trị 0, 1, 2. Đây là nền tảng của mọi cách biểu diễn khác.
12. **Nonary (cơ số 9)**\
    Mỗi chữ số nonary (0–8) đại diện cho **2 trit**. Đây là dạng shorthand "nhẹ" hơn base-27, tương tự octal với binary.
13. **Tryte (IOTA)**\
    Một *tryte* gồm **3 trit** (27 giá trị) trong một số ngữ cảnh, hoặc **6 trit** trong các ngữ cảnh khác (IOTA dùng tryte 6 trit cho một số mục đích). IOTA dùng tryte làm đơn vị dữ liệu cơ bản trong giao thức của mình.
14. **Trybble**\
    Thuật ngữ chỉ nhóm **3 trit** (3³ = 27 giá trị). Đây là đơn vị mà các chữ số base-27 đại diện.
15. **Setun 18-trit word**\
    Máy tính ternary Setun (1958) dùng từ dài **18 trit** (balanced ternary). Đây là một "word format" cụ thể, không chỉ là cách viết ký tự, nhưng là một chuẩn biểu diễn dữ liệu ternary có ảnh hưởng lịch sử.
16. **TAPI27 floating-point**\
    Định dạng số thực dấu phẩy động dùng **balanced base-27**, trong đó mỗi "word" là một chuỗi trit base-27. Thường dùng trong các thư viện toán ternary.
17. **4B3T (4 binary, 3 ternary)**\
    Mã đường truyền biến **4 bit nhị phân** thành **3 ký hiệu ternary** (ba mức điện áp). Được dùng trong một số hệ thống truyền thông如 ISDN PRI.
18. **PST (Pair Selected Ternary)**\
    Mã hóa các cặp bit nhị phân thành các cặp ký hiệu ternary, thường gặp trong truyền dẫn viễn thông.
19. **TerSCII (Ternary ASCII)**\
    Bộ ký tự dành cho máy tính ternary, dùng heptavintimal (base-27) để mã hóa ký tự, tương tự ASCII/Unicode trong thế giới nhị phân.
20. **Quy ước của ngôn ngữ lập trình Jo**\
    Ngôn ngữ Jo dùng dấu gạch dưới `_` để phân tách chữ số cho dễ đọc (ví dụ `1_000_000`), đồng thời tránh dùng chữ `O` trong biểu diễn số để không nhầm với số `0`. Đây là quy ước ở mức cú pháp ngôn ngữ, nhưng phản ánh cách cộng đồng ternary xử lý vấn đề nhập nhằng ký tự.

---

### ✨ 50 cách biểu diễn/encoding ternary bổ sung

#### 📐 Biến thể ký hiệu số (balanced & unsigned)

21. **Ký hiệu&#x20;**`1`**&#x20;lật ngược (overturned 1)**\
    Trong các tài liệu về máy tính Setun, −1 được biểu diễn bằng ký tự `1` bị lật ngược (giống chữ "1" quay ngược). Đây là quy ước lịch sử có một không hai.
22. **Ký hiệu&#x20;**`Y, W, X`\
    Một số bằng sáng chế dùng `Y` cho +1, `W` cho −1 và `X` cho 0 trong biểu diễn ternary không cân bằng.
23. **Ký hiệu&#x20;**`I, θ, +I`\
    Trong tài liệu học thuật về balanced ternary, các giá trị lần lượt là −1 (`I` hoặc `-I`), 0 (`θ`), +1 (`+I`).
24. **Balanced nonary (cơ số 9 cân bằng)**\
    Mỗi chữ số nonary đại diện cho 2 trit, nhưng các giá trị số được cân bằng quanh 0 (ví dụ −4 đến +4). Được dùng để rút gọn balanced ternary.
25. **Symmetric nonary**\
    Một biến thể của nonary trong đó các chữ số được chọn đối xứng qua 0, thường dùng trong các bảng mã hóa ternary.
26. **Balanced base-27 (BB27)**\
    Hệ cơ số 27 cân bằng, trong đó mỗi chữ số có giá trị từ −13 đến +13. Được dùng trong các giao thức mạng thử nghiệm (YIP) và máy tính "Yinrih" hư cấu.
27. **Biased ternary (số lệch)**\
    Thay vì dùng dấu, một hằng số lệch (bias) được cộng vào để dịch chuyển miền giá trị. Thường dùng trong biểu diễn số nguyên không dấu trong máy tính ternary.
28. **Two's complement ternary (bù hai ternary)**\
    Một biến thể của bù ba, nhưng dùng cơ chế tương tự bù hai trong nhị phân để biểu diễn số âm. Được nhắc đến như một khả năng trong lý thuyết số ternary.

#### 📦 Đơn vị dữ liệu và word size

29. **6-trit tryte (Setun-70)**\
    Máy tính Setun-70 dùng "syllable" (âm tiết) 6 trit thay cho byte, được gọi là tryte 6 trit.
30. **9-trit tryte**\
    Một định nghĩa khác của tryte là **9 trit**, tương ứng với 3 trybble, đủ để mã hóa 19.683 giá trị. Được đề xuất trong các kiến trúc ternary hiện đại.
31. **12-trit word**\
    Một số kiến trúc ternary dùng word 12 trit cho độ chính xác mở rộng (extended precision).
32. **18-trit word (Setun)**\
    Word tiêu chuẩn của máy tính Setun là 18 trit, với lệnh và bộ nhớ được tổ chức theo 9 trit.
33. **24-trit word (Ternac, 5500FP)**\
    Máy tính Ternac dùng word 24 trit cho số nguyên và 42 trit cho phần định trị số thực. Bộ xử lý 5500FP hiện đại cũng chọn word 24 trit.
34. **27-trit word**\
    Được đề xuất trong "Ternary Manifesto" như một đơn vị từ tự nhiên cho máy tính ternary, tương ứng với 3 tryte 9 trit hoặc 9 trybble.
35. **42-trit mantissa + 6-trit exponent (Ternac)**\
    Định dạng dấu phẩy động cụ thể của máy Ternac: phần định trị 42 trit, phần mũ 6 trit.

#### 🔤 Mã hóa ký tự (character encoding)

36. **TerSCII TTF-3 (3-trit trybble)**\
    Một trong hai encoding chính thức của TerSCII: mỗi ký tự được biểu diễn bằng các trybble (3 trit).
37. **TerSCII TTF-9 (9-trit tryte)**\
    Encoding còn lại của TerSCII: mỗi ký tự được biểu diễn bằng các tryte (9 trit).
38. **Terscii 4-trit (n/z/p)**\
    Một bộ ký tự ternary độc lập dùng **4 trit** cho mỗi ký tự, với các trit được ký hiệu là `n` (negative), `z` (zero), `p` (positive). Thiết kế đối xứng qua phép phủ định.
39. **Terscii 4-trit (0/1/2)**\
    Biến thể của Terscii dùng trực tiếp các giá trị 0, 1, 2 thay vì n/z/p.
40. **5-trit trên ký tự (TerSCII mở rộng)**\
    Được đề xuất để biểu diễn ASCII/Unicode trên máy ternary: 5 trit cho 243 giá trị, gần đủ cho UTF-8 nhưng chưa hoàn chỉnh.
41. **6-trit trên ký tự (TerSCII mở rộng)**\
    Đề xuất dùng 6 trit cho 729 giá trị, đủ để bao phủ nhiều ký tự Unicode hơn, dù hơi dư thừa.

#### 🚀 Mã hóa đường truyền (line coding)

42. **AMI (Alternate Mark Inversion) – 1B1T**\
    Mã đường truyền ternary cổ điển: mỗi bit nhị phân được ánh xạ thành một ký hiệu ternary (+ , 0, −), với các dấu "mark" luân phiên đảo cực để cân bằng DC.
43. **3B2T (3 binary, 2 ternary)**\
    Mã đường truyền biến **3 bit nhị phân** thành **2 ký hiệu ternary**, thường được so sánh với 4B3T trong các hệ thống ISDN.
44. **2B1T (2 binary, 1 ternary)**\
    Một sơ đồ mã hóa trong đó **2 bit nhị phân** được biểu diễn bằng **1 ký hiệu ternary** (với ba mức điện áp). Được nhắc đến trong các bằng sáng chế về truyền dữ liệu.
45. **MMS43 (Modified Monitoring State 43)**\
    Bảng mã hóa cụ thể được dùng trong 4B3T để ánh xạ 4 bit sang 3 ký hiệu ternary, có tính đến trạng thái DC offset lũy kế.
46. **HDB3 (High Density Bipolar 3) – ternary variant**\
    Một biến thể của AMI dùng các ký hiệu ternary để thay thế chuỗi 0 dài, thường được so sánh với 4B3T trong truyền thông.
47. **CMI (Coded Mark Inversion) – ternary levels**\
    Mã đường truyền dùng ba mức ternary (+, 0, −) với quy tắc đảo dấu, được xem là một trong những mã ternary thực tế trong viễn thông.
48. **Barker code ternary (11-symbol sync)**\
    Chuỗi đồng bộ 11 ký hiệu ternary (`+ + + - + - + - + - + -`) được dùng trong các hệ thống 4B3T để đồng bộ khung truyền.

#### 🧮 Định dạng số thực (floating-point)

49. **GoldenFloat (GF) – họ định dạng φ-tối ưu**\
    Một họ bảy định dạng dấu phẩy động hẹp cho máy tính ternary, được tham số hóa bởi tỷ lệ vàng φ ≈ 1.618. Ví dụ: GF4, GF8, GF16, GF32....
50. **Ternary6 (T6) – định dạng thử nghiệm tối giản**\
    Một định dạng floating-point ternary tối giản được đề xuất trong các dự án phần cứng ternary (Ternary27), dùng ít trit hơn để kiểm thử.
51. **Ternary27 (T27) – định dạng 27-trit**\
    Một định dạng số thực 27 trit được thiết kế cho kiến trúc ternary 27-trit, thường được mô tả trong các dự án DIY và tài liệu phần cứng mở.
52. **TAPI27 (Ternary Arbitrary Precision Integer 27)**\
    Định dạng số nguyên chính xác tùy ý dùng các word 27 trit, với word đầu tiên mã hóa kích thước. Được dùng trong thư viện Perl `Math::Logic::Ternary::TAPI27`.

#### 🔄 Chuyển đổi và mã hóa nhị phân–ternary

53. **t5b1 (5 trits → 1 byte)**\
    Encoding trong giao thức IOTA: 5 trit được lưu trong 1 byte. Đây là cách "nén" ternary vào môi trường lưu trữ nhị phân.
54. **b1t6 (1 byte → 6 trits)**\
    Encoding ngược lại của IOTA: 1 byte được chuyển thành 6 trit (little-endian balanced ternary). Được dùng để nhúng dữ liệu nhị phân vào giao dịch ternary.
55. **BytePerTrit (mỗi trit một byte)**\
    Wire format đơn giản nhất: mỗi trit được lưu trong một byte (−1 → 0xFF, 0 → 0x00, +1 → 0x01).
56. **Packed nibble (2 trit/byte)**\
    Hai trit được đóng gói vào một nibble (4 bit) của byte, tăng mật độ lưu trữ gấp đôi so với BytePerTrit.
57. **T1B1 (1 trit → 1 byte)**\
    Encoding chuẩn trong thư viện `bee_ternary` (IOTA): mỗi trit được biểu diễn bằng một byte. Đây là dạng "canonical default" cho xử lý ternary trên nền nhị phân.
58. **T3B1 (3 trit → 1 byte)**\
    Ba trit được đóng gói vào một byte, thường được dùng trong các thư viện ternary hiện đại để tiết kiệm bộ nhớ.
59. **T5B1 (5 trit → 1 byte)**\
    Năm trit được đóng gói vào một byte, là encoding nén nhất trong một số thư viện ternary, tương ứng với t5b1 của IOTA.

#### 🏛️ Kiến trúc và chuẩn lịch sử

60. **Setun 9-trit command word**\
    Máy Setun dùng word lệnh 9 trit, tách biệt với word dữ liệu 18 trit.
61. **TRIA "byte" (6 trit)**\
    Một đề xuất trong bằng sáng chế về hệ thống máy tính hỗn hợp nhị phân–ternary: "TRIA" byte gồm 6 trit, tương đương khái niệm byte trong thế giới ternary.
62. **Ternac word (24 trit integer / 48 trit float)**\
    Máy Ternac dùng word 24 trit cho số nguyên và 48 trit cho số thực (42 trit định trị + 6 trit mũ).
63. **5500FP 24-trit word**\
    Bộ xử lý RISC ternary 5500FP hiện đại chọn word 24 trit làm độ rộng từ gốc, với các thanh ghi và bus dữ liệu 24 trit.
64. **81-tryte seed (IOTA)**\
    Seed trong giao thức IOTA là một chuỗi **81 tryte** (243 trit), được dùng để sinh khóa riêng. Đây là một định dạng dữ liệu ternary có cấu trúc cố định.
65. **Mnemonic ternary seed (BIP-39 mở rộng)**\
    Seed 81-tryte của IOTA có thể được biểu diễn dưới dạng câu ghi nhớ 36 từ (mỗi từ 11 bit), tương tự BIP-39 trong Bitcoin.

#### 📡 Mã hóa và xử lý tín hiệu ternary

66. **Ternary BCH code**\
    Mã sửa lỗi BCH (Bose–Chaudhuri–Hocquenghem) được mở rộng cho ký hiệu ternary, dùng đa thức sinh với các hệ số 0, 1, 2. Được dùng trong các hệ thống thông tin đa mức.
67. **Ternary Hamming code**\
    Mã Hamming ternary (single-error-correcting) được xây dựng từ mở rộng của mã Hamming nhị phân, dùng để sửa lỗi đơn trong hệ thống ternary.
68. **Ternary Berger code**\
    Mã kiểm tra lỗi Berger được thiết kế cho hệ thống ternary, dùng các trit 0 và 1 để mã hóa trọng số và giá trị, giúp phát hiện lỗi đơn hướng.
69. **Ternary parity code**\
    Mã chẵn lẻ ternary đơn giản: thêm một trit parity vào cuối từ để phát hiện lỗi, thường dùng trong chẩn đoán offline cho hệ thống ternary.
70. **Ternary cyclic code**\
    Mã vòng (cyclic) ternary được dùng để sửa lỗi chùm (burst error) trong truyền thông và lưu trữ ternary, dựa trên cấu trúc đại số của vành đa thức trên trường hữu hạn ternary.