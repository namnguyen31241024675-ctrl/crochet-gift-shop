# Project Plan

## 1. Thành viên và vai trò
| Thành viên | Vai trò | Trách nhiệm chính |
|---|---|---|
| Nguyễn Quang Đức | Trưởng nhóm / BA | Tiến độ, yêu cầu, GitHub Issues, điều phối |
| Trần Quốc Bảo | UI/UX | Khảo sát giao diện, thiết kế, chuẩn bị tài nguyên |
| Đỗ Trọng Khanh | Frontend | Trang chủ, danh mục, chi tiết sản phẩm, giỏ hàng |
| Đặng Đình Quyến | Frontend | Giao diện tạo giỏ quà, đặt làm, trang quản trị |
| Nguyễn Thanh Nam | Backend / Database | Thiết kế CSDL, API sản phẩm, tài khoản, phân quyền |
| Nguyễn Anh Tuấn | Backend | Đơn hàng, thanh toán sandbox, vận chuyển, voucher |
| Nguyễn Đình Châu | QA / Integration | Kế hoạch kiểm thử, tích hợp, tài liệu |

Nguyên tắc: mỗi nhiệm vụ có một người chịu trách nhiệm chính; mỗi thành viên có sản phẩm cụ thể; không giao toàn bộ lập trình cho một người hoặc cho AI; cuối kỳ ai cũng phải giải thích được phần mình làm.

## 2. Các giai đoạn
| GĐ | Nội dung | Kết quả chính | Thời hạn |
|---|---|---|---|
| 1 | Khảo sát và xác định yêu cầu | Repo, REQUIREMENTS, phân tích website, quy trình nghiệp vụ | TODO |
| 2 | Thiết kế giao diện | Wireframe/mockup các trang chính | TODO |
| 3 | Xây dựng frontend | Trang chủ, danh mục, chi tiết, giỏ hàng, giỏ quà | TODO |
| 4 | Backend và CSDL | API, thiết kế CSDL, nghiệp vụ, phân quyền | TODO |
| 5 | Tích hợp và kiểm thử | Thanh toán sandbox, vận chuyển, voucher, test case | TODO |
| 6 | Triển khai và hoàn thiện | Website chạy thực tế, báo cáo, slide | TODO |

## 3. Công việc (giai đoạn 1)
| Mã | Công việc | Người phụ trách | Kết quả cần đạt | Thời hạn | Trạng thái |
|---|---|---|---|---|---|
| T01 | Tạo repo, cấu trúc thư mục, mời thành viên | Nguyễn Thanh Nam | Repo Public, đủ file khởi tạo | TODO | Hoàn thành |
| T02a | Khảo sát website A (LyLycraft) | Trần Quốc Bảo | Phần A trong competitor-analysis.md | TODO | Chưa bắt đầu |
| T02b | Khảo sát website B (Tiệm Chúng Mình) | Đỗ Trọng Khanh | Phần B trong competitor-analysis.md | TODO | Chưa bắt đầu |
| T02c | Khảo sát website C (chọn thêm) | Đặng Đình Quyến | Phần C trong competitor-analysis.md | TODO | Chưa bắt đầu |
| T02d | Tổng hợp bảng so sánh, "học được gì" | Nguyễn Quang Đức | competitor-analysis.md hoàn chỉnh | TODO | Chưa bắt đầu |
| T03 | Chạy quy trình AI 2 vòng, họp thảo luận | Nguyễn Quang Đức | Bảng tổng hợp trong AI_USAGE_LOG.md | TODO | Chưa bắt đầu |
| T04 | Chốt REQUIREMENTS | Nguyễn Quang Đức | REQUIREMENTS.md v1.0 | TODO | Chưa bắt đầu |
| T05a | Vai trò người dùng | Nguyễn Anh Tuấn | docs/user-roles.md | TODO | Chưa bắt đầu |
| T05b | Quy trình nghiệp vụ | Nguyễn Thanh Nam | docs/business-workflow.md | TODO | Chưa bắt đầu |
| T06 | Chọn công nghệ và kiến trúc dự kiến | Nguyễn Thanh Nam | Mục công nghệ trong README, AGENTS | TODO | Chưa bắt đầu |
| T07 | Rà soát repo trước khi nộp | Nguyễn Đình Châu | Checklist nộp bài đạt | TODO | Chưa bắt đầu |

## 4. Rủi ro
| Rủi ro | Mức | Phương án xử lý |
|---|---|---|
| Phạm vi quá rộng (giỏ quà + đặt làm + báo giá + đặt cọc) | Cao | Chốt MVP: FR13, FR14; FR15 và đặt cọc nhiều bước để "làm sau" |
| Thành viên chưa quen công nghệ đã chọn | Trung bình | Chọn công nghệ cả nhóm tối thiểu nắm được; chia việc theo module |
| Xung đột mã nguồn khi gộp | Trung bình | Mỗi chức năng một nhánh, merge qua Pull Request, có người review |
| Tích hợp thanh toán sandbox lỗi/khó | Trung bình | Thử tích hợp sớm (giai đoạn 4), có phương án dự phòng được GV chấp thuận |
| Thành viên không hiểu phần code AI sinh ra | Cao | Quy tắc 3 câu hỏi; review chéo; ghi AI_USAGE_LOG |
| Lộ khóa bí mật/dữ liệu thật lên repo Public | Cao | .gitignore, dùng biến môi trường, chỉ dùng dữ liệu mẫu |
| Link repo/website không truy cập được lúc chấm | Trung bình | Kiểm tra bằng cửa sổ ẩn danh trước hạn nộp |
