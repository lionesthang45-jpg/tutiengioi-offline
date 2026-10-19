# Tu Tiên Giới Offline — WSL2 Easy2 RC1

**Bộ cài WSL2 hiện hành, thay RC4 cho lượt tải và cài mới.** Có Client, GameServer Linux, website MEL, Liones AI và bước chuẩn bị WSL2 tích hợp. Không cần VMware.

Đây là RC đã qua kiểm thử tự động, chưa phải bản Final nghiệm thu gameplay trên mọi máy. Không phải bản vá chép đè và **không tự chuyển nhân vật từ bộ cũ**.

## Tải bộ cài đầy đủ

Mở **[trang tải WSL2 Easy2 RC1](https://github.com/lionesthang45-jpg/tutiengioi-offline/releases/tag/v1.7.0-wsl2-easy2-rc1-20261018)** → Assets. Tải đủ **9 file**, để cùng một thư mục:

- [CaiDat-TuTienGioi-WSL2-Easy2-RC1.exe](https://github.com/lionesthang45-jpg/tutiengioi-offline/releases/download/v1.7.0-wsl2-easy2-rc1-20261018/CaiDat-TuTienGioi-WSL2-Easy2-RC1.exe)
- [BIN 1](https://github.com/lionesthang45-jpg/tutiengioi-offline/releases/download/v1.7.0-wsl2-easy2-rc1-20261018/CaiDat-TuTienGioi-WSL2-Easy2-RC1-1.bin)
- [BIN 2](https://github.com/lionesthang45-jpg/tutiengioi-offline/releases/download/v1.7.0-wsl2-easy2-rc1-20261018/CaiDat-TuTienGioi-WSL2-Easy2-RC1-2.bin)
- [BIN 3](https://github.com/lionesthang45-jpg/tutiengioi-offline/releases/download/v1.7.0-wsl2-easy2-rc1-20261018/CaiDat-TuTienGioi-WSL2-Easy2-RC1-3.bin)
- [BIN 4](https://github.com/lionesthang45-jpg/tutiengioi-offline/releases/download/v1.7.0-wsl2-easy2-rc1-20261018/CaiDat-TuTienGioi-WSL2-Easy2-RC1-4.bin)
- [BIN 5](https://github.com/lionesthang45-jpg/tutiengioi-offline/releases/download/v1.7.0-wsl2-easy2-rc1-20261018/CaiDat-TuTienGioi-WSL2-Easy2-RC1-5.bin)
- [BIN 6](https://github.com/lionesthang45-jpg/tutiengioi-offline/releases/download/v1.7.0-wsl2-easy2-rc1-20261018/CaiDat-TuTienGioi-WSL2-Easy2-RC1-6.bin)
- [BIN 7](https://github.com/lionesthang45-jpg/tutiengioi-offline/releases/download/v1.7.0-wsl2-easy2-rc1-20261018/CaiDat-TuTienGioi-WSL2-Easy2-RC1-7.bin)
- [BIN 8](https://github.com/lionesthang45-jpg/tutiengioi-offline/releases/download/v1.7.0-wsl2-easy2-rc1-20261018/CaiDat-TuTienGioi-WSL2-Easy2-RC1-8.bin)

Tổng 15.847.490.585 byte, khoảng **15,85 GB / 14,76 GiB**. Không gửi riêng EXE, không đổi tên BIN, không trộn file RC4/VMware. Không dùng “Source code (zip/tar.gz)” làm bộ cài game.

[Hướng dẫn WSL2 chi tiết](https://github.com/lionesthang45-jpg/tutiengioi-offline/releases/download/v1.7.0-wsl2-easy2-rc1-20261018/HUONG_DAN_CAI_WSL2.md) · [Checksum tải xuống](https://github.com/lionesthang45-jpg/tutiengioi-offline/releases/download/v1.7.0-wsl2-easy2-rc1-20261018/DOWNLOAD_SHA256SUMS.txt) · [Kết quả và giới hạn kiểm thử](https://github.com/lionesthang45-jpg/tutiengioi-offline/releases/download/v1.7.0-wsl2-easy2-rc1-20261018/QA-KET_QUA.txt)

## Cài và chơi

1. Sao lưu GameServer/nhân vật cũ trước khi đồng ý chuẩn bị Windows/WSL. Giữ nguyên thư mục game cũ có dữ liệu.
2. Windows 10 x64 build 19041+ hoặc Windows 11 x64; không hỗ trợ Windows 32-bit/ARM64. Máy cần ảo hóa, khoảng 8 GiB RAM trở lên; nên 16 GiB nếu chơi song song server khác. Chọn thư mục local mới, còn khoảng 40 GiB trống sau khi tải setup.
3. Chạy EXE, chọn thư mục mới, đọc và đồng ý cảnh báo. Setup chuẩn bị WSL2 nếu thiếu, import distro riêng, khởi động và kiểm tra Server + AI + website thật.
4. Nếu có UAC/BIOS/restart, chủ máy cần hoàn tất yêu cầu đó. Sau restart, mở Launcher → **CHUẨN BỊ / TIẾP TỤC CÀI** nếu chưa tự tiếp tục; không cần chép/cài lại payload.
5. Chờ **SẴN SÀNG** → **CHƠI NGAY**. Tài khoản mẫu `gm / 1`. Khi nghỉ: thoát Client → **DỪNG AN TOÀN** → chờ hoàn tất. Đóng Launcher không tự dừng Server.

## Những điểm đã tích hợp

- Chọn cổng Windows trống và đồng bộ Client/website/AI/SFTP; dùng MỞ WEBSITE và thông tin kết nối trong Launcher, không cố định cổng 80.
- Distro/đĩa/mạng riêng để cài song song WSL của game khác. Phần chuẩn bị Windows, kernel WSL và reboot vẫn là tài nguyên chung; cần sao lưu trước.
- Xác minh và tiếp tục import, phục hồi hồ sơ thiếu/hỏng từ nhật ký khi đủ bằng chứng; không tự xóa đĩa có nhân vật. Chặn đường dẫn UNC/ADS/junction không phù hợp, đã thử đường dẫn có dấu/khoảng trắng/ngoặc.
- Liones AI kiểm tra heartbeat/native bridge; mặc định **Tự động + mô hình nhẹ Qwen3:1.7b**, chuyển CPU khi GPU không tương thích. Có cấu hình CPU/GPU và mô hình 8B tùy tài nguyên; không có cam kết GPU sẽ hoạt động trên mọi card.
- **WINSCP / SỬA FILE** hiển thị địa chỉ/cổng SFTP thực của bản cài, không cần mở GameServer/database/AI để truy cập file. WinSCP là ứng dụng tùy chọn, tải riêng từ trang chính thức.
- Xuất gói hỗ trợ ngay trong Launcher; người chơi không cần tự vào `/home` hay `/opt` lấy log.

## Giới hạn và lưu ý

Đã kiểm chính EXE cuối: cài mới, Server/AI/website tự chạy, 8497 hash bất biến, cổng bị chiếm, song song distro thử, phục hồi profile, SFTP thật và dừng an toàn. Việc song song được thử với WSL khác chứa dịch vụ test, không phải mọi GameServer của người dùng. Các ca chuẩn bị Windows thiếu tính năng/MSI/reboot có fixture/mock; chưa nghiệm thu trên mọi Windows 10 sạch.

Cần người chơi xác nhận đăng nhập/tạo/đăng nhập lại nhân vật, chat, F3/maps và nút GUI trên cấu hình của mình; mô hình 8B chưa lặp kiểm thử end-to-end trong RC này. Setup chưa có chữ ký số; MSI WSL Microsoft đi kèm có chữ ký Microsoft. Không thể tự vượt BIOS/UAC/GPO hay thiếu RAM/đĩa vật lý.

RC4 cũ vẫn giữ để dự phòng, không dùng cho cài mới; không xóa bản cũ có nhân vật khi chưa sao lưu/chuyển dữ liệu. [Bản VMware riêng ở kho này](https://github.com/lionesthang45-jpg/tutiengioi-offline-vmware).

Nếu lỗi, gửi gói HoTro cho người hỗ trợ tin cậy. Không đăng công khai VHD/database/profile/private key hoặc gói hỗ trợ có dữ liệu cá nhân. [Mở yêu cầu hỗ trợ](https://github.com/lionesthang45-jpg/tutiengioi-offline/issues/new).

Giấy phép thành phần đóng kèm và đính chính mẫu thông báo VMware cũ trong payload: xem `ThirdPartyLicenses.zip` và `THIRD_PARTY_WSL2.txt` trong Assets. Quyền nội dung game của bên thứ ba vẫn áp dụng.
