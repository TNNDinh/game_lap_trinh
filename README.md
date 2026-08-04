# Robot Lab — Học lập trình cơ bản bằng game

Khoá học lập trình nhập môn bằng tiếng Việt, gồm 7 chương và mỗi chương là một game
chứ không phải bài đọc. Toàn bộ nằm trong **một file `index.html` duy nhất**: không
build, không dependency, không script bên ngoài.

## Nội dung

| # | Chương | Game |
|---|--------|------|
| 01 | Kiểu dữ liệu | Phân loại 12 giá trị vào `int / float / str / bool / list`, có bẫy như `'7'`, `"True"`, `2.0` |
| 02 | Biến & phép gán | Đoán trước kết quả, rồi máy chạy từng dòng và vẽ ô nhớ để đối chiếu |
| 03 | Toán tử | 14 biểu thức: `// % ** == != and or not`, mỗi câu kèm giải thích |
| 04 | Chuỗi lệnh | Robot: đi thẳng, rẽ hướng, nhặt vật phẩm (3 màn) |
| 05 | Vòng lặp | `Lặp lại N lần`, thân nhiều lệnh, vòng lặp lồng nhau (3 màn) |
| 06 | Điều kiện | `Nếu…thì`, `Trong khi`, và lỗi vòng lặp vô hạn (2 màn) |
| 07 | Hàm & tổng hợp | Định nghĩa `leo_bac()` rồi gọi lại, màn cuối gộp mọi khái niệm (2 màn) |

## Đặc điểm

- **Cầu nối sang code thật** — khối lệnh được dịch trực tiếp sang Python ngay bên dưới
  (`for i in range(11):`, `if co_pha_le():`), giúp người học nối block với chữ.
- **Lỗi giải thích bằng tiếng Việt** — "Robot đâm vào tường", "Vòng lặp Trong khi chạy
  mãi không dừng", kèm hướng sửa.
- **Chấm sao theo độ gọn** — mỗi màn có số lệnh tối ưu; dùng thừa vẫn qua nhưng ít sao,
  để tạo thói quen rút gọn chương trình.
- Tiến độ lưu bằng `localStorage`, chương sau mở khoá dần.
- Giao diện hỗ trợ cả nền sáng và nền tối, có bàn phím và `prefers-reduced-motion`.

## Chạy tại máy

Mở thẳng `index.html` bằng trình duyệt. Không cần server.

Hoặc phục vụ qua HTTP tuỳ ý:

```bash
npx serve .
```

## Triển khai

Trang tĩnh thuần. Trên Vercel chọn framework preset **Other**, để trống lệnh build và
thư mục output — `index.html` ở gốc repo sẽ được phục vụ trực tiếp.
