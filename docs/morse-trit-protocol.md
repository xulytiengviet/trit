# TRITLAB — Morse–Trit Protocol v1

Đây là **quy ước thử nghiệm** chứ không phải tiêu chuẩn Morse quốc tế cho trit.

- Alphabet Base27: `␠ABCDEFGHIJKLMNOPQRSTUVWXYZ` (space=0, A=1, Z=26).
- Chữ số `n` viết dưới dạng ba chữ số cơ số 3 `a,b,c`. Đổi thành trit `(a−1,b−1,c−1)`, với mỗi trit thuộc `{-1,0,+1}`. Giá trị cân bằng `9t₁+3t₂+t₃=n−13`.
- Ký hiệu: `T=-1`, `0=0`, `1=+1`.
- Nhóm Morse–trit **định nghĩa tại TRITLAB**: `T → ..`, `0 → .-`, `1 → -.`. Mã có độ dài cố định **hai phần tử Morse/trit**.
- Chấm = 1 đơn vị, gạch = 3 đơn vị; nghỉ 1 đơn vị giữa hai phần tử; nghỉ 3 đơn vị giữa các trit; nghỉ 7 đơn vị giữa các chữ cái Base27.
- Chế độ `CVNSS→MORSE ITU` phát trực tiếp chuỗi CVNSS ASCII theo mã Morse quốc tế, không đi qua mã trit.
- Web Audio oscillator ẩn sau thao tác nhấn phát; WAV 16kHz/mono/PCM, có fade đầu/cuối xung chống tiếng click.
- Ký tự ngoài A–Z và khoảng trắng **không được bao hàm** trong lớp Base27, có cảnh báo; truyền tối đa 64 ký tự/lượt.
- 27 trạng thái Base27 ↔ 27 bộ ba trit có tính song ánh. **Không suy ra** Quốc ngữ ↔ CVNSS là song ánh do sự nhập nhằng của bộ rút gọn.
- Tham khảo [balanced-ternary Rust](https://github.com/Trehinos/balanced-ternary#1) và [ITU-R M.1677](https://www.itu.int/rec/R-REC-M.1677/en).
