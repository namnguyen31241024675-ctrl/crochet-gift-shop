# Project Instructions for AI

## 1. Project context
Đây là đồ án website thương mại điện tử của sinh viên (UEH, môn Phát triển ứng dụng TMĐT): website bán móc len handmade cho một cửa hàng, có chức năng tạo giỏ quà theo ngân sách và đặt làm theo mẫu.

## 2. Scope
- Chỉ triển khai các chức năng đã được nhóm thống nhất trong `REQUIREMENTS.md`.
- Các mục ở "Ngoài phạm vi" (AI sinh mẫu, 3D, tự báo giá từ ảnh, sàn nhiều người bán…) **không** được tự ý thêm.
- Chức năng ưu tiên LS/XM chỉ làm khi nhóm yêu cầu.

## 3. Coding principles
- Giữ mã nguồn dễ đọc, dễ bảo trì.
- Không thay đổi kiến trúc lớn khi chưa được nhóm đồng ý.
- Không tự ý xóa chức năng đang hoạt động.
- Ưu tiên thay đổi nhỏ, có thể kiểm tra.
- Tính tiền (giỏ quà, giỏ hàng, voucher, phí vận chuyển) phải xử lý ở phía server, không tin dữ liệu giá do trình duyệt gửi lên.

## 4. Workflow
Trước khi sửa mã nguồn:
1. Đọc các tài liệu liên quan.
2. Phân tích hiện trạng.
3. Đề xuất phương án.
4. Chờ nhóm xác nhận.

Sau khi sửa mã nguồn:
1. Giải thích các thay đổi.
2. Nêu file đã sửa.
3. Hướng dẫn chạy và kiểm thử.
4. Báo cáo các giới hạn còn tồn tại.
5. Không khẳng định chức năng đã chạy nếu chưa có kết quả kiểm tra.

## 5. Security
- Không đưa mật khẩu, API key hoặc token vào mã nguồn.
- Không tự ý vô hiệu hóa kiểm tra bảo mật.
- Không sử dụng dữ liệu cá nhân thật khi chưa được phép.
- Chỉ dùng dữ liệu mẫu và ghi rõ cách tạo.

## 6. Communication
Nếu yêu cầu chưa rõ, hãy hỏi lại trước khi triển khai.

## 7. Git
- Không tự ý commit, push, merge hoặc xóa dữ liệu nếu chưa được yêu cầu.
- Mỗi chức năng làm trên nhánh riêng (`feature/...`, `fix/...`, `docs/...`).

## 8. Công nghệ
TODO – cập nhật sau khi nhóm chốt công nghệ.
