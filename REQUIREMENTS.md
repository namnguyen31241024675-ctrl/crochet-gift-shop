# Requirements

> **Bản nháp v0.1.** Đây là đề xuất khởi đầu, nhóm phải họp rà soát, sửa hoặc loại bỏ trước khi chốt (xem quy trình AI trong AI_USAGE_LOG.md).
> Cột "Ưu tiên": **BB** = bắt buộc • **NC** = nên có • **LS** = làm sau nếu kịp • **XM** = cần nhóm xác minh thêm.

## 1. Mục tiêu dự án
- **Mục tiêu kinh doanh:** giúp một cửa hàng móc len bán sản phẩm làm sẵn, bộ quà và đơn đặt làm trên một hệ thống, quản lý được đơn hàng và yêu cầu.
- **Giá trị cho khách:** chọn quà trong giới hạn chi tiêu mà không phải tự tính; thống nhất rõ nội dung, giá, thời gian đặt làm; biết đơn đang ở bước nào.

## 2. Phạm vi
### Trong phạm vi (phiên bản đầu)
- Danh mục, tìm kiếm, lọc, chi tiết sản phẩm.
- Tài khoản, giỏ hàng, đặt hàng, thanh toán sandbox, phí vận chuyển, mã giảm giá.
- Tạo giỏ quà theo ngân sách từ các bộ quà cửa hàng cấu hình sẵn.
- Đặt làm theo mẫu của cửa hàng với tùy chọn đã có giá niêm yết.
- Theo dõi đơn, đánh giá sản phẩm.
- Quản trị: sản phẩm, danh mục, bộ quà, đơn, yêu cầu đặt làm, khuyến mãi, người dùng; dashboard thống kê.
- Giao diện dùng được trên máy tính và điện thoại.

### Ngoài phạm vi
- AI tự sinh mẫu sản phẩm; mô phỏng 3D hộp quà/sản phẩm.
- Tự động báo giá từ ảnh.
- Nhận mọi thiết kế tự do.
- Bán nguyên liệu DIY.
- Sàn nhiều người bán; đơn doanh nghiệp số lượng lớn.
- Thông báo tự động nâng cao (email/SMS hàng loạt) – chỉ xem xét sau khi luồng chính ổn định.

## 3. Người dùng
Xem [docs/user-roles.md](docs/user-roles.md).

## 4. Yêu cầu chức năng

| Mã | Tên chức năng | Mô tả | Người dùng | Ưu tiên | Tiêu chí nghiệm thu |
|---|---|---|---|---|---|
| FR01 | Xem danh sách sản phẩm | Trang chủ và trang danh mục hiển thị sản phẩm (ảnh, tên, giá, giá giảm nếu có) | Khách | BB | Mở danh mục thấy đúng sản phẩm theo danh mục; sản phẩm hết hàng được đánh dấu |
| FR02 | Xem chi tiết sản phẩm | Hình ảnh, mô tả, chất liệu, kích thước, màu, giá, tồn kho, sản phẩm liên quan, đánh giá | Khách | BB | Trang chi tiết hiển thị đủ các trường trên; sản phẩm không tồn tại báo lỗi thân thiện |
| FR03 | Tìm kiếm, lọc, sắp xếp | Tìm theo từ khóa; lọc ≥ 5 thuộc tính (loại, màu, chất liệu, kích thước, khoảng giá); sắp xếp theo giá/mới nhất | Khách | BB | Kết hợp nhiều bộ lọc trả đúng kết quả; không có kết quả thì có thông báo |
| FR04 | Đăng ký / đăng nhập | Tạo tài khoản, đăng nhập, đăng xuất | Khách | BB | Email trùng bị từ chối; mật khẩu lưu dạng băm; sai mật khẩu báo lỗi |
| FR05 | Hồ sơ và địa chỉ | Sửa thông tin cá nhân, quản lý địa chỉ nhận hàng | Khách hàng | BB | Chỉ xem và sửa được dữ liệu của chính mình |
| FR06 | Giỏ hàng | Thêm/xóa/đổi số lượng, hiển thị tổng tiền | Khách hàng | BB | Số lượng vượt tồn kho bị chặn; tổng tiền cập nhật đúng |
| FR07 | Đặt hàng (checkout) | Nhập địa chỉ, chọn vận chuyển/thanh toán, xác nhận đơn | Khách hàng | BB | Đơn được lưu đúng sản phẩm, giá, phí, địa chỉ; tồn kho giảm tương ứng |
| FR08 | Thanh toán sandbox | Tích hợp ≥ 1 cổng thanh toán thử nghiệm; xử lý thành công, thất bại, hủy | Khách hàng | BB | Demo được 3 kết quả; trạng thái đơn cập nhật đúng; xác thực kết quả trả về |
| FR09 | Phí vận chuyển | Tính phí theo quy tắc nhóm định nghĩa (TODO: theo khu vực/cân nặng/đồng giá) | Khách hàng | BB | Phí hiển thị trước khi xác nhận và lưu đúng vào đơn |
| FR10 | Mã giảm giá | Kiểm tra: tồn tại, hiệu lực, điều kiện đơn, mức giảm, số lần dùng | Khách hàng, Admin | BB | Mã hết hạn/đủ lượt/không đủ điều kiện bị từ chối kèm lý do; tổng tiền tính lại đúng |
| FR11 | Lịch sử và trạng thái đơn | Xem danh sách đơn, chi tiết, trạng thái | Khách hàng | BB | Chỉ thấy đơn của mình (chặn truy cập đơn người khác bằng đổi ID) |
| FR12 | Đánh giá sản phẩm | Đánh giá sao và bình luận sau khi nhận hàng | Khách hàng | NC | Chỉ người đã mua và đã nhận hàng được đánh giá |
| FR13 | **Tạo giỏ quà theo ngân sách** | Nhập ngân sách → gợi ý bộ quà từ bộ cấu hình sẵn có tổng giá phù hợp → đổi món/đổi số lượng/bỏ món → tính lại tổng, hiển thị số tiền còn lại hoặc phần vượt → chuyển vào giỏ hàng | Khách | BB | Ngân sách X: mọi bộ gợi ý có tổng ≤ X; chỉ dùng sản phẩm còn hàng; vượt ngân sách thì hiện số tiền vượt; không có bộ phù hợp thì thông báo và cho đổi ngân sách; chuyển vào giỏ giữ đúng món và số lượng |
| FR14 | **Đặt làm theo mẫu** | Chọn mẫu cửa hàng hỗ trợ + tùy chọn có giá (màu, kích thước, tên) → xem tổng theo giá niêm yết → gửi yêu cầu; cửa hàng xác nhận khả năng và thời gian hoàn thành | Khách hàng, Nhân viên | BB | Tổng tiền đúng giá niêm yết; yêu cầu lưu đủ mẫu + tùy chọn; nhân viên xác nhận/từ chối được; khách thấy kết quả |
| FR15 | Yêu cầu riêng và báo giá | Khách gửi mô tả/ảnh tham khảo; cửa hàng báo giá và thời gian; khách xác nhận hoặc từ chối | Khách hàng, Nhân viên | XM → LS | (Chỉ làm nếu còn thời gian; không tự động định giá từ ảnh) |
| FR16 | Theo dõi đơn đặt làm | Trạng thái: chờ xác nhận → đã đặt cọc → đang làm → hoàn thành → giao nhận; xử lý hủy | Khách hàng, Nhân viên | NC | Chuyển trạng thái đúng thứ tự, ghi lại thời điểm; không nhảy cóc trạng thái |
| FR17 | Quản trị danh mục dữ liệu | CRUD sản phẩm, danh mục, bộ quà, tồn kho, khuyến mãi/voucher, người dùng | Admin | BB | Thêm/sửa/xóa có xác nhận; dữ liệu nhập được kiểm tra hợp lệ |
| FR18 | Quản lý đơn và yêu cầu đặt làm | Xem, lọc, cập nhật trạng thái đơn mua và đơn đặt làm | Admin, Nhân viên | BB | Nhân viên chỉ làm được thao tác được phân quyền |
| FR19 | Dashboard thống kê | Tổng doanh thu, số đơn, sản phẩm bán chạy, đơn chờ giao, số khách hàng | Admin | BB | Số liệu khớp với dữ liệu trong CSDL |
| FR20 | Danh sách yêu thích | Lưu sản phẩm yêu thích | Khách hàng | LS | Thêm/xóa được; chỉ xem của mình |

## 5. Yêu cầu phi chức năng
- **Responsive:** các trang chính dùng được ở ≥ 2 kích thước màn hình (máy tính, điện thoại).
- **Bảo mật:** phân quyền (xác thực + ủy quyền); kiểm tra dữ liệu đầu vào; chống XSS, SQL injection, CSRF, IDOR; mật khẩu băm; không đưa khóa bí mật vào mã nguồn.
- **Dữ liệu:** chỉ dùng dữ liệu mẫu; không dùng dữ liệu cá nhân thật.
- **Kiểm thử:** có test case cho chức năng chính, dữ liệu biên và trường hợp lỗi.
- **Mã nguồn:** tổ chức rõ ràng, có lịch sử commit hợp lý, mỗi thành viên có đóng góp kiểm chứng được.
- **Hiệu năng/khả dụng:** TODO (ví dụ: trang danh mục tải dưới X giây với dữ liệu mẫu).

## 6. Giới hạn và giả định
- Thời gian: theo lịch học phần (TODO điền số tuần/mốc).
- Nhân lực: TODO số thành viên và mức độ quen công nghệ.
- Công nghệ: TODO (sau khi nhóm chốt).
- Giả định: một cửa hàng, dữ liệu sản phẩm và bộ quà do nhóm tự tạo; phí vận chuyển/đóng gói theo quy tắc đơn giản nhóm đặt ra.
- Ngân sách giỏ quà tính theo **tổng giá sản phẩm**; phí vận chuyển và phát sinh hiển thị riêng trước khi xác nhận.

## 7. Câu hỏi còn mở (nhóm cần chốt)
1. Đặt cọc cho đơn đặt làm: thanh toán sandbox một phần hay chỉ ghi nhận thủ công?
2. Có làm FR15 (báo giá yêu cầu riêng) trong học kỳ này không?
3. Chọn 1 chức năng "Innovation" (điểm cộng) nào? (gợi ý trong đề: Recommendation, so sánh sản phẩm, thông báo trạng thái đơn…)
4. Phí vận chuyển tính theo quy tắc nào?
