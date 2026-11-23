# Lịch sử thay đổi

## v3 (24/11/2026) - Bản bàn giao chính thức A3

- Chuẩn hóa tài liệu trong `docs/`: thêm `docs/AI_LOG.md` và `docs/evidence-index.md`, dành `docs/evidence/` cho ảnh kiểm thử thực tế.
- Thay `RELEASE_NOTES.md` bằng `CHANGELOG.md` và chuyển nhật ký AI từ thư mục gốc vào `docs/`.
- Bổ sung hướng dẫn mở, tính năng, giới hạn và kết quả kiểm thử vào README.
- Ghi rõ nguồn tài nguyên ảnh theo thông tin hiện có và nêu việc URL/giấy phép của từng ảnh chưa được lưu trong repository.
- Sửa liên kết repository trong phần liên hệ trang chính về repository đang bàn giao.
- Chụp và lưu bốn ảnh minh chứng giao diện trong `docs/evidence/`; kết quả và phạm vi kiểm tra được ghi trong `docs/evidence-index.md`.
- Kiểm tra giả lập trình duyệt ở `375×812`, `320×812` và `1440×900`; chưa kiểm tra trên iPhone vật lý.
- Các thay đổi v3 hiện có trong working tree; chưa tạo commit hoặc đẩy lên GitHub trong lượt này. GitHub Pages công khai chưa được xác nhận là đã cập nhật theo v3.
- Chưa xác minh URL và giấy phép riêng của từng ảnh Unsplash; chưa kiểm tra cửa sổ ẩn danh.
- Biểu mẫu vẫn là mô phỏng tĩnh dùng `GET`, không gửi email hoặc lưu dữ liệu. Ảnh trang kết quả không có thanh địa chỉ; URL kiểm thử được ghi riêng trong bảng minh chứng.
- Bàn giao tiếp theo: commit và đẩy thay đổi lên `main`, xác nhận lại GitHub Pages, rồi lưu hash commit v3 và bổ sung ảnh chụp có thanh địa chỉ nếu yêu cầu nộp bắt buộc.

## v2 (24/11/2026) - Bổ sung tài liệu lần đầu

- Bổ sung README và nhật ký AI cùng ghi chú phát hành đầu tiên.
- Sau đó phát hiện hồ sơ chưa theo đúng cấu trúc `docs/` và README chưa chuẩn hóa đầy đủ, nên tiếp tục hoàn thiện trong v3.
- Commit liên quan: `5c980b70065528891757e2e36175992f49cd4342`.

## v1 (24/11/2026) - Khởi tạo mã nguồn giao diện tĩnh

- Hoàn thiện `index.html`, `ket-qua.html` và `css/style.css`.
- Giao diện CSS mobile-first có breakpoint `640px` và `960px`, ba thẻ dịch vụ, bảng giá và biểu mẫu tĩnh.
- Thêm bốn ảnh cục bộ vào `assets/images/` và triển khai website lên GitHub Pages.
- Commit liên quan: `fca6de33c15396457e13845b6cca0a64a1cf76cb`.
