# Tin Tức Online — Tu Tiên Giới

Launcher đọc thông báo công khai từ file [news.json](news.json) của repository này. Không cần GitHub token trên máy người chơi.

## Dành cho người chơi

- Mở Launcher: tin được tải ở chế độ nền.
- Trang Tin Tức → Làm mới tin: kiểm tra ngay; tự kiểm tra mỗi 10 phút khi Launcher đang mở.
- Bấm Đọc chi tiết để xem toàn bài trong Launcher.
- Mất mạng: vẫn đọc được tin gần nhất đã lưu; chơi offline và điều khiển Server không phụ thuộc nguồn tin.
- Tin Tức Online chưa phải chức năng tự tải/cài bản vá.

## Dành cho Thắng — đăng hoặc sửa tin

1. Mở file `launcher/news/news.json` trên GitHub, chọn sửa file.
2. Thêm một mục vào đầu `items` hoặc sửa nội dung cần thay. Giữ `schema: 1`, cập nhật `updatedAt` theo thời gian ISO8601 có múi giờ, ví dụ `2026-10-29T16:00:00+07:00`.
3. Mỗi tin có `id` riêng chỉ gồm chữ không dấu, số, dấu gạch dưới hoặc gạch ngang; không trùng ID.
4. Điền `title`, `description`, `body`, `date` theo dạng `yyyy-MM-dd`, `category`; `demo` phải là `false`.
5. `body` là văn bản thuần; xuống dòng dùng `\n` trong JSON. Không dùng HTML/script/XAML.
6. Có thể bỏ `imageUrl`; nếu có ảnh, dùng URL HTTPS trên `raw.githubusercontent.com/lionesthang45-jpg/tutiengioi-offline/`. Ảnh tối đa 3 MiB. Khi đổi ảnh, nên dùng tên file mới để cache nhận đúng ảnh mới.
7. Có thể bỏ `url`; nếu có, chỉ dùng HTTPS dẫn về chính repository GitHub Tu Tiên Giới.
8. Commit thay đổi, mở Launcher → Tin Tức → Làm mới tin để kiểm tra. Bộ nhớ đệm phía GitHub có thể làm thay đổi chưa hiện ngay.

Giới hạn: tối đa 20 tin, JSON 128 KiB, tiêu đề 180 ký tự, mô tả 900, nội dung 12.000 ký tự/tin. Nếu JSON bị lỗi hoặc vượt giới hạn, Launcher giữ bản tin hợp lệ gần nhất. Đừng đăng dữ liệu nhân vật, gói HoTro, mật khẩu hoặc token vào nguồn tin công khai.

## Khôi phục

Nếu đăng nhầm, sửa lại file hoặc revert commit tin tức trên GitHub. Không cần sửa GameServer, Database hay cài lại game.
