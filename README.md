# Crochet Gift Shop – Website bán móc len handmade

> Đồ án nhóm môn Phát triển ứng dụng TMĐT – UEH. **Nhóm 7 – lớp ST5**.
> Trạng thái: giai đoạn 1 (khảo sát và xác định yêu cầu). Chưa có mã nguồn website.

## 1. Giới thiệu
Website kinh doanh sản phẩm móc len handmade cho **một cửa hàng** (móc khóa, thú len, hoa len, phụ kiện nhỏ).
Ngoài bán hàng làm sẵn, website hỗ trợ hai nghiệp vụ chuyên biệt:

- **Tạo giỏ quà theo ngân sách**: khách nhập ngân sách, hệ thống gợi ý bộ quà, khách đổi món và xem tổng tiền được tính lại.
- **Đặt làm theo mẫu**: khách chọn mẫu và các tùy chọn có giá niêm yết (màu, kích thước, thêm tên), cửa hàng xác nhận khả năng nhận làm và thời gian hoàn thành.

**Vấn đề kinh doanh (giả thuyết ban đầu, cần đối chiếu khảo sát):** khách mua quà phải tự cộng tiền để vừa ngân sách; thông tin đặt làm bị trao đổi rời rạc; khách khó biết đơn đang ở bước nào.

## 2. Khách hàng mục tiêu
- Sinh viên và người đi làm trẻ tại Việt Nam, mua móc len cho bản thân hoặc làm quà (sinh nhật, tốt nghiệp, kỷ niệm).
- Phía vận hành: chủ cửa hàng và nhân viên được phân quyền.

## 3. Chức năng chính
Xem danh mục/tìm kiếm/lọc sản phẩm • Tài khoản • Giỏ hàng và đặt hàng • Thanh toán thử nghiệm • Phí vận chuyển • Mã giảm giá • Tạo giỏ quà theo ngân sách • Đặt làm theo mẫu • Theo dõi đơn • Đánh giá sản phẩm • Quản trị và thống kê.

Chi tiết xem [REQUIREMENTS.md](REQUIREMENTS.md).

## 4. Thành viên
| STT | Họ tên | Vai trò | Trách nhiệm chính | GitHub |
|---|---|---|---|---|
| 1 | Nguyễn Quang Đức | Trưởng nhóm / BA | Tiến độ, yêu cầu, GitHub Issues, điều phối | TODO |
| 2 | Trần Quốc Bảo | UI/UX | Khảo sát giao diện, thiết kế, chuẩn bị tài nguyên | TODO |
| 3 | Đỗ Trọng Khanh | Frontend | Trang chủ, danh mục, chi tiết sản phẩm, giỏ hàng | TODO |
| 4 | Đặng Đình Quyến | Frontend | Giao diện tạo giỏ quà, đặt làm, trang quản trị | TODO |
| 5 | Nguyễn Thanh Nam | Backend / Database | Thiết kế CSDL, API sản phẩm, tài khoản, phân quyền | TODO |
| 6 | Nguyễn Anh Tuấn | Backend | Đơn hàng, thanh toán sandbox, vận chuyển, voucher | TODO |
| 7 | Nguyễn Đình Châu | QA / Integration | Kế hoạch kiểm thử, tích hợp, tài liệu | TODO |


(Thêm hoặc bớt dòng theo số thành viên thực tế; vai trò có thể gộp.)

## 5. Công nghệ dự kiến
**TODO – nhóm họp thống nhất rồi điền.** Ví dụ cần chốt:
- Backend: TODO
- Frontend: TODO
- Cơ sở dữ liệu: TODO
- Thanh toán sandbox: TODO (VNPay / MoMo / PayPal / Stripe…)
- Triển khai (hosting): TODO

## 6. Kế hoạch thực hiện
6 giai đoạn: Khảo sát và yêu cầu → Thiết kế giao diện → Frontend → Backend và CSDL → Tích hợp và kiểm thử → Triển khai và hoàn thiện. Xem [PROJECT_PLAN.md](PROJECT_PLAN.md).

## 7. Liên kết
- Bảng yêu cầu: [REQUIREMENTS.md](REQUIREMENTS.md)
- Kế hoạch: [PROJECT_PLAN.md](PROJECT_PLAN.md)
- Quy tắc cho AI: [AGENTS.md](AGENTS.md)
- Nhật ký dùng AI: [AI_USAGE_LOG.md](AI_USAGE_LOG.md)
- Phân tích website: [docs/competitor-analysis.md](docs/competitor-analysis.md)
- Vai trò người dùng: [docs/user-roles.md](docs/user-roles.md)
- Quy trình nghiệp vụ: [docs/business-workflow.md](docs/business-workflow.md)
