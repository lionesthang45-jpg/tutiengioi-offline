# Tu Tiên Giới Offline — RC4 thử nghiệm

Bộ đầy đủ **JxLTLauncher + Client + GameServer WSL2 + Liones AI + website MEL**. Không dùng VMware. GameServer và dữ liệu chạy trên máy của mỗi người chơi; không cần kết nối tới máy của người phát hành.

**Đây là bản thử nghiệm RC4, chưa phải Final.** Chưa nghiệm thu đầy đủ trên Windows sạch chưa có WSL2; còn kiểm tra trong game và rà soát bổ sung xử lý xóa item. Chỉ dùng dữ liệu thử, sao lưu trước khi cập nhật. Không chuyển nhân vật quan trọng vào để chơi lâu dài ở giai đoạn này.

## Tải bộ cài

Mở **[trang tải RC4](https://github.com/lionesthang45-jpg/tutiengioi-offline/releases/tag/v1.4.0-rc4-20261016)**, tìm mục **Assets** và tải:

1. `CaiDat-TuTienGioi-RC4.exe`.
2. Đủ **8 file** `CaiDat-TuTienGioi-RC4-1.bin` đến `CaiDat-TuTienGioi-RC4-8.bin`.
3. `BAT_DAU_O_DAY.txt`, hướng dẫn và checklist kiểm thử.

Tổng bộ cài khoảng **14,6 GB**. Giữ file `.exe` và tất cả `.bin` **cùng một thư mục**, không đổi tên, không mở/giải nén từng `.bin`. Chạy `.exe` sau khi tải xong tất cả. **Không chọn “Source code (zip)” hoặc “Source code (tar.gz)”** — đó không phải bộ cài game. Không trộn file của các bản phát hành khác nhau.

`SHA256SUMS.txt` kèm release chứa checksum để kiểm tra file tải về. Bộ cài này chưa có chứng thư ký số thương mại; chỉ dùng nguồn phát hành tin cậy, không tắt antivirus để bỏ qua cảnh báo.

## Cài và chơi — không cần gõ lệnh

1. Chạy `CaiDat-TuTienGioi-RC4.exe`, bấm **Tiếp tục → Cài đặt → Hoàn tất**.
2. Mở **JxLTLauncher** trên Desktop. Nếu máy chưa có WSL2, bấm **CHUẨN BỊ WSL2…**, chờ hoàn tất, lưu công việc và khởi động lại Windows. Cần Windows 10 x64 build 19041 trở lên hoặc Windows 11 x64, có ảo hóa phần cứng được bật. Nếu Windows báo thiếu thành phần hoặc BIOS chưa bật ảo hóa, gửi ảnh lỗi để được hỗ trợ, không tự xóa WSL đang có.
3. Bấm **CÀI ĐẦY ĐỦ OFFLINE**, chọn nơi lưu game còn ít nhất **40 GiB trống sau khi đã cài Launcher**. Chờ thông báo hoàn tất.
4. Bấm **CHƠI NGAY**. Chờ Server, Liones AI và website sẵn sàng; Client sẽ tự mở. Lần đầu có thể mất vài phút.
5. Có thể dùng **tài khoản mẫu `gm`, mật khẩu `1`** để thử nhanh. Hoặc bấm **MỞ WEBSITE** để tạo tài khoản riêng tại `http://127.0.0.1`, rồi đăng nhập bằng tài khoản đó. Tên nhân vật tự đặt; **không bắt buộc dùng tài khoản gm**.

Gói có sẵn dữ liệu game/model AI và MSI kernel Microsoft. Bước bật thành phần Windows phụ thuộc component store của Windows; máy thiếu thành phần có thể cần bộ cài Windows/WSL offline tương ứng. Không hứa cài offline thành công trên mọi máy chưa được kiểm thử.

### Những lần chơi sau

**Mở Launcher → CHƠI NGAY.**

Khi nghỉ: **thoát Client → DỪNG AN TOÀN → chờ đã dừng → mới tắt máy**. Đóng riêng Launcher không tự dừng Server. Website `127.0.0.1` chỉ mở trên chính máy đang chạy bộ game; không mở cổng quản trị/SQL ra Internet.

### Máy đã có WSL hoặc Server khác

Mở mục **Máy đã có Server/WSL khác?** trong Launcher. Nên **giữ dữ liệu và dừng bản cũ an toàn** trước khi bật bản mới. Chỉ một môi trường WSL được chạy khi khởi động bộ này. Nếu chọn xóa distro, đó là xóa toàn bộ dữ liệu trong đĩa của distro đó: phải xác nhận đúng tên và giữ bản sao lưu bên ngoài. Không xóa WSL để thử sửa lỗi kết nối. Môi trường không do Launcher quản lý cần dừng bằng công cụ riêng của nó sau khi lưu công việc.

## Cần người chơi kiểm thử gì?

Làm theo `KIEM_THU_TRONG_GAME.txt`, đặc biệt:

- Cài trên máy chưa có WSL2 và máy đã có WSL/Server khác.
- Tạo tài khoản/nhân vật, thoát và đăng nhập lại, dừng/bật Server và kiểm tra dữ liệu.
- F3 Hiệu Ứng/Tu Vi, chat SimCity, PM Tạ Hạo dùng Space trong tên.
- Nền map/minimap, ba map train cao cấp, hiệu thuốc, thú cưỡi và Linh Căn.
- Tống Kim: mở trận, bot di chuyển, quân hàm; liên trảm khi hạ nhiều mục tiêu.
- Liones AI và website MEL.

Nếu lỗi, mở **[Issues](https://github.com/lionesthang45-jpg/tutiengioi-offline/issues/new)** và gửi: phiên bản RC4, Windows đang dùng, bước tái hiện, ảnh lỗi, phần trạng thái Launcher. Không đăng mật khẩu, token, file đĩa WSL, SQL hoặc dữ liệu cá nhân công khai.

## Phạm vi phát hành

Kho này chỉ chứa hướng dẫn và bộ cài thử nghiệm, không phải kho mã nguồn. Database phát hành không chứa nhân vật người chơi QA; các tài khoản SimAI là dữ liệu hệ thống. Gỡ Launcher không tự xóa đĩa WSL/nhân vật đã cài riêng. Chưa chứng nhận Final hoặc cam kết không có lỗi.
