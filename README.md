# DA Auto Detailing

Website tĩnh giới thiệu dịch vụ chăm sóc và bảo vệ sơn xe công nghệ cao DA Auto Detailing.

- **Sản phẩm:** DA Auto Detailing – website giới thiệu dịch vụ và đặt lịch mô phỏng
- **Tác giả:** Lê Đức Anh
- **Mã sinh viên:** 2071020017
- **Lớp/môn:** FIT4014

## Liên kết sản phẩm

- **Repository:** https://github.com/ducanhdzct/da-auto-detailing
- **GitHub Pages:** https://ducanhdzct.github.io/da-auto-detailing/
- **Trang chính:** https://ducanhdzct.github.io/da-auto-detailing/index.html
- **Trang kết quả:** https://ducanhdzct.github.io/da-auto-detailing/ket-qua.html
- **Hồ sơ GitHub tác giả:** https://github.com/ducanhdzct

## Mô tả ngắn

Trang chủ là một website HTML5/CSS3 dùng để giới thiệu ba dịch vụ: rửa xe chi tiết 12 bước, phủ gốm Ceramic 9H và dán phim PPF TPU. Trang có điều hướng neo đến phần giới thiệu, dịch vụ, bảng giá và đặt lịch; có bảng giá theo phân khúc xe và biểu mẫu đặt lịch tĩnh. Sau khi dữ liệu hợp lệ, biểu mẫu gửi bằng phương thức `GET` sang `ket-qua.html`. Website **chưa** gửi email, gọi API hoặc lưu dữ liệu vào cơ sở dữ liệu.

## Cấu trúc thư mục

```text
da-auto-detailing/
├── index.html           # Trang chính và biểu mẫu đặt lịch
├── ket-qua.html         # Trang kết quả mô phỏng sau khi biểu mẫu hợp lệ
├── css/
│   └── style.css        # Kiểu dáng, responsive và trạng thái focus
├── assets/
│   └── images/          # Ảnh hero và ảnh đại diện các dịch vụ
├── README.md            # Hướng dẫn kiểm tra và nguồn bàn giao
├── AI_LOG.md            # Ghi nhận quyết định có sử dụng AI
└── RELEASE_NOTES.md     # Ghi chú bản v7 bàn giao
```

## Chạy local

Không cần cài đặt framework hay package.

### Cách 1: mở trực tiếp

Mở [index.html](./index.html) bằng trình duyệt. Liên kết nội bộ, CSS và ảnh dùng đường dẫn tương đối nên trang chính có thể xem trực tiếp.

### Cách 2: chạy máy chủ tĩnh

```powershell
cd D:\A3_LeDucAnh\da-auto-detailing
python -m http.server 5500
```

Sau đó truy cập:

- http://localhost:5500/
- http://localhost:5500/index.html
- http://localhost:5500/ket-qua.html

Ngừng máy chủ bằng tổ hợp `Ctrl+C`.

## Nguồn xuất bản

- Mã nguồn do tác giả biên tập và lưu tại GitHub repository nêu trên.
- Website được xuất bản bằng GitHub Pages từ nhánh `main` của repository.
- Nội dung dịch vụ, bảng giá, địa chỉ, giờ làm việc và hotline là dữ liệu hiển thị trong sản phẩm học tập; cần được xác nhận lại trước khi dùng cho hoạt động kinh doanh thực tế.
- Các bức ảnh nằm trong `assets/images/` là tài sản tĩnh của sản phẩm. Repo hiện không ghi kèm thông tin giấy phép, phạm vi sử dụng hay nguồn gốc từng ảnh; không nên tái sử dụng bên ngoài bài tập nếu chưa xác minh quyền sử dụng.

## Cách kiểm tra

1. Mở trang chủ hoặc GitHub Pages.
2. Kiểm tra thanh điều hướng: `Giới thiệu`, `Dịch vụ`, `Bảng giá`, `Đặt lịch` phải cuộn đến đúng phần tương ứng.
3. Kiểm tra ba thẻ dịch vụ, bảng giá và toàn bộ ảnh hiển thị; thử ở cửa sổ desktop và mobile.
4. Tại phần `Đặt Lịch Chăm Sóc Xe`, gửi biểu mẫu bỏ trống để xác nhận ràng buộc HTML5 không cho submit.
5. Nhập họ tên ít nhất 2 ký tự, email đúng dạng và nội dung ít nhất 10 ký tự.
6. Nhấn `Gửi yêu cầu đặt lịch`; trình duyệt phải chuyển sang `ket-qua.html` và tham số `fullname`, `email`, `service_note` xuất hiện trên thanh địa chỉ.
7. Kiểm tra nút `Quay lại trang chủ` hoặc `Đặt lịch lại` đều dẫn về trang chủ.
8. Thử Tab để kiểm tra vùng focus màu xanh rõ ràng trên liên kết, ô nhập và nút.

**Giới hạn kiểm tra:** trang kết quả chỉ mô phỏng việc nhận biểu mẫu; không kiểm tra được gửi email hoặc lưu dữ liệu phía máy chủ.

## Hồ sơ và minh chứng

- [Hồ sơ tác giả](https://github.com/ducanhdzct)
- [Mã nguồn repository](https://github.com/ducanhdzct/da-auto-detailing)
- [Bản nộp v7](./RELEASE_NOTES.md)
- [Quyết định khi sử dụng AI](./AI_LOG.md)
- [Commit mới nhất hiện tại](https://github.com/ducanhdzct/da-auto-detailing/commit/fca6de33c15396457e13845b6cca0a64a1cf76cb)
