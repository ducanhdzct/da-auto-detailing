# Nhật ký sử dụng AI

**Sinh viên:** Lê Đức Anh (MSV: 2071020017), lớp CNTT 20-04<br>
**Học phần:** FIT4014

## Tóm tắt

| Ngày | Dùng AI làm gì | Em sửa lại gì |
|---|---|---|
| 24/11/2026 | Hỗ trợ rà soát bố cục CSS responsive và đề xuất kiểm tra các kích thước màn hình cùng vùng bảng giá cuộn ngang. | Đối chiếu với CSS hiện có; chỉ ghi nhận các kiểm tra đã thực sự chạy, không coi đề xuất là kết quả kiểm thử. |
| 24/11/2026 | Hỗ trợ chuẩn hóa README, CHANGELOG, nhật ký AI và bảng minh chứng cho bản v3. | Sửa theo mã nguồn và lịch sử commit; loại các khẳng định chưa xác minh, ghi rõ phần chưa chụp/chưa kiểm tra. |

## Lượt 1 – Rà soát Responsive Mobile-first

**Hiện tượng và dữ kiện ban đầu:** CSS hiện có thiết lập lưới dịch vụ một cột mặc định, breakpoint `640px` và `960px`, cùng `.table-wrapper { overflow-x: auto; }` và bảng có `min-width: 32rem`. Các quy tắc này đã có trong mã nguồn trước lượt chuẩn hóa v3.

**Nhận định trước khi hỏi AI:** Cấu trúc mã cho thấy thiết kế hướng mobile-first và bảng có thể cuộn ngang độc lập. Cần xác nhận bằng trình duyệt rằng tại viewport hẹp trang không bị tràn ngang và bảng vẫn đọc được.

**Công cụ/prompt hoặc phản hồi mẫu:** Dùng trợ lý AI để rà soát CSS responsive; nội dung yêu cầu là kiểm tra cách xác nhận bố cục ở kích thước desktop/mobile và hành vi bảng giá trong `.table-wrapper`.

**Gợi ý:** Thử các chiều rộng `375px` và `320px`, xác nhận số cột dịch vụ và đo tràn ngang trang so với khung bảng.

**Quyết định có lý do:** Không sửa CSS chỉ dựa trên gợi ý vì mã hiện có đã chứa các breakpoint và wrapper cần thiết; kiểm tra trên trình duyệt ở `375×812` và `320×812` trước khi kết luận.

**Phần sửa:** Không có thay đổi CSS được quy cho lượt này. Bản v3 chỉ chuẩn hóa tài liệu và sửa liên kết repository sai trong phần liên hệ trang chủ.

**Cách thử lại và kết quả:** Trình duyệt báo viewport `375×812` và `320×812`; lưới có một cột. Ở hai kích thước, `scrollWidth` của trang không vượt `clientWidth`; bảng rộng `512px` bên trong wrapper hẹp hơn (`326px` tại 375px, `271px` tại 320px). Ảnh viewport 375px được lưu trong [bảng minh chứng](./evidence-index.md). Chưa kiểm thử trên iPhone vật lý.

## Lượt 2 – Chuẩn hóa hồ sơ bàn giao v3

**Hiện tượng và dữ kiện ban đầu:** Tài liệu trước đó nằm ở thư mục gốc với tên `AI_LOG.md` và `RELEASE_NOTES.md`; README chứa đường dẫn local của môi trường làm việc. Repository có các trang tĩnh và ảnh, biểu mẫu chuyển dữ liệu bằng `GET`, không có xử lý backend.

**Nhận định trước khi hỏi AI:** Hồ sơ cần tổ chức lại theo `docs/`, đổi ghi chú phát hành thành changelog, và phải phân biệt rõ kiểm tra HTTP/mã nguồn với kiểm thử giao diện có ảnh chụp.

**Công cụ/prompt hoặc phản hồi mẫu:** Sinh viên yêu cầu trợ lý AI đọc repository, chuẩn hóa tài liệu cho A3/Lab 8, chạy kiểm tra thực tế và chụp ảnh nếu công cụ hỗ trợ.

**Gợi ý:** Viết README tiếng Việt với cách mở và tính năng; lập CHANGELOG có lịch sử phiên bản; tạo bảng evidence; ghi nguồn tài nguyên, giới hạn form và trạng thái ảnh chụp một cách kiểm chứng được.

**Quyết định có lý do:** Chấp nhận cấu trúc tài liệu mới. Không ghi nhận ảnh chụp hoặc thao tác trình duyệt nếu chưa thực hiện; kết quả HTTP chỉ chứng minh các URL phản hồi, không thay thế kiểm tra tương tác hay responsive.

**Phần sửa:** Tạo `CHANGELOG.md`, `docs/AI_LOG.md`, `docs/evidence-index.md`; cập nhật README; loại các tệp tài liệu cũ theo tên khỏi thư mục gốc; sửa liên kết repository trong trang chính.

**Cách thử lại và kết quả:** Kiểm tra Pages trả HTTP 200 cho trang, CSS và bốn ảnh; dùng trình duyệt local để bấm bốn mục menu và gửi biểu mẫu sai/hợp lệ. Email `ducanh@` bị chặn, khớp `:user-invalid` và có viền đỏ; ảnh lỗi chỉ lấy phần biểu mẫu, không gồm hộp thông báo trình duyệt. Dữ liệu hợp lệ chuyển đến `ket-qua.html` cùng tham số GET. Bốn ảnh kiểm thử được lưu trong `docs/evidence/` và liệt kê tại [evidence-index.md](./evidence-index.md). Chưa kiểm tra cửa sổ ẩn danh hoặc iPhone vật lý.
