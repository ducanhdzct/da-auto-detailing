# DA Auto Detailing

**Tác giả:** Lê Đức Anh (MSV: 2071020017)<br>
**Lớp:** CNTT 20-04<br>
**Học phần:** FIT4014

## Sản phẩm này là gì?

DA Auto Detailing là website tĩnh HTML5/CSS3 giới thiệu dịch vụ chăm sóc và hiệu chỉnh sơn ô tô, phủ Ceramic 9H và dán phim bảo vệ sơn PPF TPU. Sản phẩm có bảng giá tham khảo và biểu mẫu đặt lịch mô phỏng.

## Demo

- **GitHub Pages:** https://ducanhdzct.github.io/da-auto-detailing/
- **Repository:** https://github.com/ducanhdzct/da-auto-detailing

## Tính năng chính

1. Điều hướng cuộn mượt đến bốn phân mục: Giới thiệu, Dịch vụ, Bảng giá và Đặt lịch.
2. Lưới ba gói dịch vụ tự điều chỉnh theo kích thước màn hình.
3. Bảng giá theo hai phân khúc xe; trên màn hình hẹp, có thể cuộn ngang bên trong khung bảng giá.
4. Biểu mẫu đặt lịch sử dụng ràng buộc HTML5, gửi dữ liệu bằng `GET` và chuyển đến `ket-qua.html` khi hợp lệ. Đây là luồng mô phỏng, không gửi email hoặc lưu dữ liệu.

## Cách mở và kiểm tra

1. Truy cập https://ducanhdzct.github.io/da-auto-detailing/ bằng trình duyệt. Có thể thay bằng cách mở `index.html` trực tiếp hoặc chạy Live Server tại cổng `5500`.
2. Nhấn lần lượt `Giới thiệu`, `Dịch vụ`, `Bảng giá` và `Đặt lịch` trên thanh menu để xem các phần tương ứng.
3. Tại mục `Đặt Lịch Chăm Sóc Xe`, nhập họ tên, email và nhu cầu dịch vụ; nhấn `Gửi yêu cầu đặt lịch` để kiểm tra chuyển trang xác nhận `ket-qua.html`.

Hướng dẫn chạy bằng máy chủ tĩnh Python (tùy chọn):

```powershell
python -m http.server 5500
```

Sau đó mở http://localhost:5500/ và dừng máy chủ bằng `Ctrl+C`.

## Cấu trúc thư mục

```text
da-auto-detailing/
├── index.html
├── ket-qua.html
├── css/
│   └── style.css
├── assets/
│   └── images/
│       ├── dan-ppf.jpg
│       ├── hero-detailing.jpg
│       ├── phu-ceramic.jpg
│       └── rua-xe-chi-tiet.jpg
├── docs/
│   ├── AI_LOG.md
│   ├── evidence-index.md
│   └── evidence/
├── CHANGELOG.md
└── README.md
```

## Nguồn xuất bản và tài nguyên

- Website được xuất bản từ nhánh `main` qua GitHub Pages.
- Các ảnh trong `assets/images/` được tải từ Unsplash và lưu trong repository. Repository hiện không lưu URL nguồn cụ thể hoặc thông tin giấy phép theo từng ảnh; cần đối chiếu lại trang nguồn và điều kiện sử dụng trước khi tái sử dụng.
- Tên studio, địa chỉ, hotline, dịch vụ và giá là dữ liệu giả lập phục vụ đồ án, không phải thông tin giao dịch thực tế.

## Đã kiểm tra

Kết quả và minh chứng kiểm thử được tổng hợp tại [docs/evidence-index.md](./docs/evidence-index.md). Changelog các phiên bản có tại [CHANGELOG.md](./CHANGELOG.md).

## Hạn chế và phần chưa kiểm tra

- Biểu mẫu chạy tĩnh bằng phương thức `GET`, chưa gửi email hoặc lưu dữ liệu vào cơ sở dữ liệu.
- Trang xác nhận là trang tĩnh; không xử lý hay lưu thông tin khách hàng.
- Chưa kiểm tra trên thiết bị iPhone vật lý thực tế.
- Ảnh chụp giao diện chỉ được liệt kê là minh chứng khi đã chụp và lưu thật trong `docs/evidence/`.

## Khai báo sử dụng AI

Nhật ký các lượt sử dụng AI, gợi ý, quyết định và phần sinh viên tự kiểm tra được ghi tại [docs/AI_LOG.md](./docs/AI_LOG.md).
