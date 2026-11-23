# Bảng minh chứng kiểm thử – DA Auto Detailing v3

Ngày đối chiếu: 24/11/2026. Tương tác giao diện được kiểm tra trên bản local; các ảnh PNG bên dưới được chụp trong trình duyệt từ đúng giao diện local. Trang công khai được kiểm tra riêng qua HTTP.

| Em thử gì | Kết quả | Ảnh/link |
|---|---|---|
| Mở trang công khai và kiểm tra tài nguyên | GitHub Pages trả HTTP 200; stylesheet và bốn ảnh JPEG cũng trả HTTP 200. Chưa dùng cửa sổ ẩn danh. | [Trang GitHub Pages](https://ducanhdzct.github.io/da-auto-detailing/); [ảnh desktop](./evidence/01-desktop-1440px.png). |
| Bấm lần lượt bốn mục menu `Giới thiệu`, `Dịch vụ`, `Bảng giá`, `Đặt lịch` | Đã bấm từng mục trong trình duyệt local; URL lần lượt đổi hash thành `#gioi-thieu`, `#dich-vu`, `#bang-gia`, `#dat-lich`. | [Ảnh desktop](./evidence/01-desktop-1440px.png). |
| Xem ở viewport `1440×900` | Đã đặt viewport trình duyệt `1440×900`; giao diện hiển thị thanh điều hướng, hero và ba thẻ dịch vụ. Ảnh lưu theo kích thước toàn trang nên chiều cao tệp PNG dài hơn viewport. | [evidence/01-desktop-1440px.png](./evidence/01-desktop-1440px.png). |
| Xem ở viewport `375×812` và `320×812` | Đã kiểm tra cả hai viewport. Lưới dịch vụ một cột. `scrollWidth` trang không vượt `clientWidth` (375px: 360/360; 320px: 305/305). Bảng rộng 512px trong wrapper hẹp hơn (326px và 271px); tại 375px, `scrollLeft` của wrapper dịch được tới 185.6px trong khi trang không tràn ngang. Chưa kiểm tra iPhone vật lý. | [evidence/02-mobile-375px.png](./evidence/02-mobile-375px.png) (ảnh toàn trang ở viewport 375×812); 320px đã đo nhưng không có ảnh riêng. |
| Gửi biểu mẫu với email sai (`ducanh@`) rồi nhấn nút gửi | Trình duyệt chặn gửi; trang vẫn ở biểu mẫu, `checkValidity()` trả false, email khớp `:user-invalid` và viền có màu đỏ `rgb(239, 68, 68)`. Ảnh chụp lấy riêng biểu mẫu; hộp thông báo trình duyệt được bỏ qua trong ảnh, không ảnh hưởng kết quả chặn gửi. | [evidence/03-form-validation-error.png](./evidence/03-form-validation-error.png). |
| Gửi biểu mẫu hợp lệ và xem trang kết quả | Đã gửi `Lê Đức Anh`, `ducanh@example.com`, `Tư vấn gói phủ Ceramic 9H cho xe Mazda 3`. Trang kết quả hiển thị tiêu đề xác nhận. URL local: `http://localhost:5500/ket-qua.html?fullname=L%C3%AA+%C4%90%E1%BB%A9c+Anh&email=ducanh%40example.com&service_note=T%C6%B0+v%E1%BA%A5n+g%C3%B3i+ph%E1%BB%A7+Ceramic+9H+cho+xe+Mazda+3`. Ảnh chụp trang không chứa thanh địa chỉ trình duyệt, nên URL được ghi riêng tại đây. | [evidence/04-form-submit-ket-qua.png](./evidence/04-form-submit-ket-qua.png). |

## Giới hạn minh chứng

- Đã kiểm tra HTTP các URL công khai bằng HEAD request, gồm trang chủ, stylesheet và bốn ảnh. Chưa kiểm tra trong cửa sổ ẩn danh.
- Tương tác menu, viewport và biểu mẫu được thử trên máy chủ local để kiểm tra đúng phiên bản đang bàn giao; thao tác đó không xác nhận trang GitHub Pages đã được cập nhật theo các thay đổi chưa đẩy.
- Ảnh chụp trang không bao gồm thanh địa chỉ trình duyệt; URL GET của ca hợp lệ được chép riêng ở hàng tương ứng.
- Chưa kiểm tra trên iPhone vật lý.
