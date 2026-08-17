# Robot Lab — Học lập trình cơ bản bằng game

Khoá học lập trình nhập môn bằng tiếng Việt, gồm 9 chương và mỗi chương là một game
chứ không phải bài đọc. Bảy chương đầu chơi bằng khối lệnh, hai chương cuối **gõ code
thật** bằng Python, JavaScript hoặc C++.

Toàn bộ nằm trong **một file `index.html` duy nhất**: không build, không dependency,
không script bên ngoài — kể cả bộ thông dịch 3 ngôn ngữ cũng tự viết.

## Nội dung

| # | Chương | Game |
|---|--------|------|
| 01 | Kiểu dữ liệu | Phân loại 20 giá trị vào `int / float / str / bool / list`, có bẫy như `'7'`, `"True"`, `2.0`, `"[1, 2]"` |
| 02 | Biến & phép gán | 9 bài: đoán trước kết quả, rồi máy chạy từng dòng và vẽ ô nhớ để đối chiếu |
| 03 | Toán tử | 24 biểu thức: `// % ** == != and or not`, mỗi câu kèm giải thích |
| 04 | Chuỗi lệnh | Robot: đi thẳng, rẽ hướng, nhặt vật phẩm (3 màn) |
| 05 | Vòng lặp | `Lặp lại N lần`, thân nhiều lệnh, vòng lặp lồng nhau (3 màn) |
| 06 | Điều kiện | `Nếu…thì`, `Trong khi`, và lỗi vòng lặp vô hạn (2 màn) |
| 07 | Hàm & tổng hợp | Định nghĩa `leo_bac()` rồi gọi lại, màn cuối gộp mọi khái niệm (2 màn) |
| 08 | Gõ code điều khiển robot | Bỏ khối lệnh, viết code thật trong IDE — 9 màn kiểm tra lại chương 4–7 |
| 09 | Tự viết chương trình | 18 bài toán, chấm khớp từng dòng in ra — kiểm tra lại chương 1–3 |

### 18 bài toán ở chương 9

Xếp từ dễ tới khó: in một dòng chữ · biến & toán tử · chẵn lẻ · tính tổng 1..10 ·
bảng cửu chương · **FizzBuzz** · đổi chỗ hai biến · chu vi &amp; diện tích · đếm ngược ·
số lớn nhất trong ba số · giai thừa · tổng các chữ số · đảo ngược số · **dãy Fibonacci** ·
tam giác sao · xếp loại điểm · bỏ qua bằng `continue` · **tìm số nguyên tố**.

## Ba ngôn ngữ, một cách nghĩ

Hai chương cuối cho chọn **Python**, **JavaScript** hoặc **C++**. Cùng một bài giải
được bằng cả ba: cú pháp khác nhau, logic y hệt. Bộ thông dịch tự viết hỗ trợ biến,
toán tử, `if/elif/else`, `while`, `for` (cả `range()` lẫn `for(;;)`), `break`,
`continue`, hàm có tham số và giá trị trả về, `print` / `console.log` /
`cout << … << endl`.

Ngữ nghĩa được giữ đúng theo từng ngôn ngữ thay vì gộp làm một — đó chính là bài học:

- `7 / 2` cho `3.5` ở Python, `3.5` ở JavaScript, nhưng `3` ở C++ (hai số nguyên chia nhau).
- `"diem: " + 10` chạy được ở JavaScript, còn Python và C++ báo lỗi — đúng như thật.
- Python in `True`, JavaScript in `true`, C++ in `1`.

## Đặc điểm

- **IDE thật sự** — đánh số dòng, tô màu cú pháp, tự thụt lề sau `:` và `{`, tự đóng
  ngoặc, gợi ý lệnh khi gõ, `Ctrl + Enter` để chạy, console báo lỗi kèm số dòng, và
  dòng gây lỗi được tô đỏ ngay trong trình soạn thảo.
- **Chạy từng bước có hình** — robot di chuyển theo đúng dòng code đang chạy, dòng đó
  sáng lên trong IDE.
- **Cầu nối sang code thật** — ở chương khối lệnh, chương trình được dịch trực tiếp sang
  Python ngay bên dưới (`for i in range(11):`), giúp người học nối block với chữ.
- **Lỗi giải thích bằng tiếng Việt** — "Thiếu dấu hai chấm ':' ở cuối dòng", "Python
  không cộng được chuỗi với số. Đổi số thành chuỗi trước: str(10)", "Vòng lặp while chạy
  mãi không dừng" — kèm hướng sửa, không phải stack trace.
- **Chấm sao theo độ gọn** — mỗi màn khối lệnh có số lệnh tối ưu; dùng thừa vẫn qua
  nhưng ít sao, để tạo thói quen rút gọn chương trình.
- Tiến độ và **bản nháp code** lưu bằng `localStorage`, chương sau mở khoá dần.
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
