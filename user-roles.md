# Vai trò người dùng

> Bản nháp – nhóm rà soát và chốt.

## 1. Bảng vai trò
| Vai trò | Nhiệm vụ chính | Quyền hạn dự kiến |
|---|---|---|
| Khách chưa đăng nhập | Xem sản phẩm, tìm kiếm, lọc, thử tạo giỏ quà | Chỉ xem thông tin công khai; thêm vào giỏ tạm thời (nếu nhóm cho phép) |
| Khách hàng | Mua hàng, tạo giỏ quà, đặt làm, theo dõi đơn, đánh giá | Quản lý thông tin, địa chỉ, đơn và yêu cầu **của chính mình** |
| Nhân viên (được phân quyền) | Xử lý đơn mua, kiểm tra yêu cầu đặt làm, cập nhật trạng thái | Chỉ các thao tác được cấp (không quản lý người dùng, không xem doanh thu tổng nếu không cấp) |
| Chủ cửa hàng / Quản trị viên | Quản lý sản phẩm, danh mục, bộ quà, khuyến mãi, người dùng, xem thống kê | Toàn bộ chức năng quản trị |

## 2. Ma trận quyền (dự kiến)
| Chức năng | Chưa đăng nhập | Khách hàng | Nhân viên | Quản trị |
|---|:-:|:-:|:-:|:-:|
| Xem, tìm kiếm, lọc sản phẩm | ✔ | ✔ | ✔ | ✔ |
| Tạo giỏ quà theo ngân sách | ✔ | ✔ | – | – |
| Đăng ký / đăng nhập | ✔ | – | – | – |
| Giỏ hàng, đặt hàng, thanh toán | – | ✔ | – | – |
| Gửi yêu cầu đặt làm | – | ✔ | – | – |
| Xem đơn của mình | – | ✔ | – | – |
| Đánh giá sản phẩm | – | ✔ | – | – |
| Xử lý đơn mua / đơn đặt làm | – | – | ✔ | ✔ |
| Quản lý sản phẩm, bộ quà, khuyến mãi | – | – | TODO | ✔ |
| Quản lý người dùng | – | – | – | ✔ |
| Xem dashboard thống kê | – | – | TODO | ✔ |

TODO: nhóm quyết định có tách "Nhân viên" và "Quản trị" thành 2 vai trò không, hay gộp để giảm khối lượng.
