# AI_LOG – DA Auto Detailing

## 1. Hoàn thiện tài liệu bàn giao

**Hiện tượng và dữ kiện ban đầu**
- Repository có trang `index.html`, trang kết quả `ket-qua.html`, CSS và 4 ảnh tĩnh.
- `README.md` ban đầu chỉ có tên và một mô tả ngắn.
- Chưa có `AI_LOG.md` và `RELEASE_NOTES.md`.
- Tác giả là Lê Đức Anh, MSV 2071020017.
- Repository: `ducanhdzct/da-auto-detailing`; nhánh chính `main`; commit gần nhất đang kiểm tra: `fca6de33c15396457e13845b6cca0a64a1cf76cb`.

**Nhận định trước AI**
- Dữ liệu trong tài liệu phải khớp với chức năng thật của HTML/CSS: không mô tả biểu mẫu là hệ thống gửi email hay lưu cơ sở dữ liệu.
- README cần nêu rõ GitHub Pages, cách chạy local, cấu trúc, nguồn xuất bản và các bước kiểm tra có thể làm ngay.
- AI_LOG phải ghi các quyết định và kết quả đã thực sự kiểm tra, không chép toàn bộ cuộc trò chuyện.

**Công cụ/prompt hoặc phản hồi mẫu**
- Công cụ: Copilot SDK trong VS Code.
- Prompt của sinh viên: yêu cầu tạo/sửa `README.md`, `AI_LOG.md`, `RELEASE_NOTES.md` theo yêu cầu bàn giao.
- Phản hồi mẫu: đề xuất cấu trúc tài liệu; liệt kê rõ tên sản phẩm, tác giả, link repo/Pages, chức năng, giới hạn và commit.

**Gợi ý**
- Bổ sung cách chạy bằng Python HTTP server.
- Phân biệt trang kết quả mô phỏng với biểu mẫu thật.
- Ghi nguồn ảnh là tài sản cần xác minh lại thay vì tự nhận là nguồn có giấy phép.
- Ghi hạn chế backend và dữ liệu kinh doanh chưa xác thực.

**Quyết định có lý do**
- Sinh viên đồng ý tạo tài liệu bằng tiếng Việt để phù hợp sản phẩm và yêu cầu bài tập.
- Sinh viên yêu cầu nội dung chỉ mô tả điều đã kiểm chứng qua mã: biểu mẫu dùng `method="get"`, chuyển sang trang kết quả, không có backend.
- Sinh viên không ghi các ảnh, địa chỉ, hotline hoặc bảng giá là nguồn chính thức nếu repo không cung cấp bằng chứng tương ứng.
- Các link GitHub dùng tên repo và tài khoản thực hiện trong cấu hình repository; đường dẫn commit dùng commit hiện tại của repo.

**Phần sửa**
- Thay README ngắn bằng README mô tả sản phẩm, cấu trúc, chạy local, kiểm thử, nguồn xuất bản và liên kết minh chứng.
- Thêm AI_LOG ghi rõ quá trình ra quyết định và công cụ AI.
- Thêm RELEASE_NOTES mô tả bản v7, thay đổi, lỗi đã sửa, commit và hạn chế.

**Cách thử lại và kết quả**
- Kiểm tra các tệp mục tiêu bằng công cụ đọc tệp sau khi sửa.
- Kiểm tra repository bằng `git status` và `git log`.
- Thử Python HTTP server; lệnh không khởi động vì môi trường hiện tại không tìm thấy runtime Python.
- Dùng máy chủ tĩnh tạm bằng `System.Net.HttpListener` của PowerShell trên cổng `5500`; kiểm tra các URL bằng `Invoke-WebRequest`.
- Kết quả: `index.html`, `ket-qua.html` và `css/style.css` đều trả HTTP `200`.
- Kiểm tra mã nguồn xác nhận form có `action="ket-qua.html"` và `method="get"`; trang kết quả có nội dung xác nhận và ghi rõ đây là form tĩnh mô phỏng.
- Chưa thực hiện kiểm tra chuột/trình duyệt trên giao diện desktop/mobile và chưa kiểm tra ràng buộc form bằng thao tác trình duyệt trong phiên làm việc này.

## Khai báo sử dụng AI

Đã sử dụng AI để hỗ trợ đọc cấu trúc repo, đối chiếu mã nguồn và soạn thảo tài liệu. Quyết định nội dung cuối cùng dựa trên dữ kiện có trong repository và được sinh viên yêu cầu giữ giới hạn đúng thực tế.
