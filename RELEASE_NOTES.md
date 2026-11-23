# RELEASE_NOTES – DA Auto Detailing v7

## Phiên bản

- **Tên/Mã:** v7
- **Ngày cập nhật:** 24/11/2026
- **Nhánh:** `main`
- **Commit mã hiện tại:** `fca6de33c15396457e13845b6cca0a64a1cf76cb`
- **Repository:** https://github.com/ducanhdzct/da-auto-detailing
- **GitHub Pages:** https://ducanhdzct.github.io/da-auto-detailing/

## Bản mã được nộp

Đường dẫn xác nhận commit:

- https://github.com/ducanhdzct/da-auto-detailing/commit/fca6de33c15396457e13845b6cca0a64a1cf76cb

Tài liệu bàn giao v7 gồm `README.md`, `AI_LOG.md` và `RELEASE_NOTES.md`. Sau khi tài liệu được commit, hash của commit tài liệu cũng sẽ là mốc bàn giao bổ sung mà người kiểm tra có thể theo dõi trên GitHub.

## Thay đổi chính

- Hoàn thiện `README.md` để mô tả đúng sản phẩm, tác giả, repo, Pages, cấu trúc thư mục, cách chạy local và quy trình kiểm tra.
- Tạo `AI_LOG.md` ghi dữ kiện ban đầu, nhận định, gợi ý AI, quyết định và cách thử lại.
- Tạo `RELEASE_NOTES.md` cho bản bàn giao v7.
- Ghi rõ giới hạn của biểu mẫu tĩnh và nguồn xuất bản của trang.
- Dẫn link hồ sơ, repository, Pages, commit và hồ sơ minh chứng trong tài liệu.

## Lỗi đã sửa

- Sửa tình trạng README không đủ thông tin để người khác mở, chạy và kiểm tra sản phẩm.
- Sửa tình trạng thiếu tài liệu ghi quá trình/quyết định sử dụng AI.
- Sửa tình trạng thiếu ghi chú phạm vi của bản nộp v7.
- Tài liệu không tự suy đoán rằng sản phẩm đã có backend, gửi email hoặc lưu dữ liệu.

## Commit liên quan

- `212b53b` – commit khởi tạo repository.
- `fca6de33c15396457e13845b6cca0a64a1cf76cb` – commit gần nhất trước tài liệu v7.
- Commit tài liệu v7: chưa tạo nếu bàn giao được lưu trong working tree; hãy ghi hash sau khi commit.

## Hạn chế còn lại

- Biểu mẫu chỉ mô phỏng: dữ liệu được truyền qua `GET`, không gửi email và không lưu cơ sở dữ liệu.
- `ket-qua.html` không đọc hoặc hiển thị lại dữ liệu đã nhập; nó chỉ hiển thị thông báo kết quả tĩnh.
- Không có backend, xác thực, bảo mật dữ liệu hoặc logic quản lý lịch.
- Địa chỉ, hotline, tên dịch vụ và bảng giá chưa có bằng chứng xác nhận nguồn kinh doanh thực tế trong repo.
- Nguồn gốc và giấy phép của từng ảnh trong `assets/images/` chưa được ghi lại.
- Release chưa kèm ảnh chụp màn hình minh chứng desktop/mobile nếu chưa tự tạo và lưu vào repo.

## Cách tiếp tục kiểm tra/bàn giao

1. Dùng GitHub Pages hoặc chạy `python -m http.server 5500`.
2. Kiểm tra trang chủ, điều hướng neo, ba thẻ dịch vụ, bảng giá và responsive.
3. Kiểm tra ràng buộc biểu mẫu, rồi gửi dữ liệu hợp lệ và xác nhận URL chuyển sang `ket-qua.html`.
4. Kiểm tra README, AI_LOG và release notes mở đúng các đường dẫn tương đối.
5. Tạo commit mới cho tài liệu v7, cập nhật hash commit tài liệu vào phần này nếu cần bằng chứng nộp chính xác.
6. Kiểm tra GitHub Pages sau khi push để xác nhận trang công khai khớp với commit đã nộp.
