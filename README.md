# Rà soát User Story và sắp xếp Product Backlog (ứng dụng đặt món FoodNow)

## Bước 1. Tìm lỗi

Dưới đây là kết quả rà soát các mục trong Product Backlog theo tiêu chí INVEST:

| Mã | Kết quả và lý do |
|----|------------------|
| US1 | Đạt: vai trò rõ, một việc, có lợi ích, thử được bằng cách chọn loại món rồi xem kết quả. |
| US2 | Sai: **M** (Measurable - Có thể đo lường được), **T** (Testable - Có thể kiểm thử được). Các từ "đẹp" và "dễ dùng" là chủ quan, khó đo lường và kiểm thử xem khi nào thì đạt yêu cầu. |
| US3 | Sai: **V** (Valuable - Có giá trị). Mặc dù việc kỹ thuật vẫn có thể có trong Product Backlog (dưới dạng Enabler Story hoặc là phần của User Story), nhưng "Là một lập trình viên" và mong muốn "dùng React để làm lại giao diện đặt món" là một giải pháp kỹ thuật cụ thể, không trực tiếp mang lại giá trị có thể nhận thấy ngay cho người dùng cuối (khách hàng hoặc admin). Nó tập trung vào *cách làm* chứ không phải *giá trị mang lại*. Một Product Backlog Item nên tập trung vào nhu cầu của người dùng nghiệp vụ. |
| US4 | Sai: **S** (Small - Nhỏ), **T** (Testable - Có thể kiểm thử được). Story này quá lớn, bao gồm nhiều chức năng riêng biệt như xem báo cáo theo nhiều tiêu chí khác nhau, xuất Excel và tự động gửi email. Điều này khiến việc ước lượng và kiểm thử trở nên khó khăn. |

## Bước 2. Sửa lỗi

**a) Viết lại US2 với một tiêu chí "dễ dùng" đo được:**

**US2 (Sửa):** Là một khách hàng, tôi muốn giao diện đặt món cho phép hoàn tất đơn hàng trong tối đa 5 bước, để có trải nghiệm đặt món nhanh chóng và thuận tiện.

_Hoặc:_ Là một khách hàng, tôi muốn giao diện đặt món có độ hài lòng người dùng (System Usability Scale - SUS) đạt ít nhất 80 điểm, để cảm thấy hài lòng khi đặt món.

**b) Tách US4 thành 2 story nhỏ, rồi đặt vào cây 3 cấp:**

*   **Epic:** Quản lý và theo dõi hiệu suất kinh doanh
    *   **Feature:** Báo cáo doanh thu
        *   **User Story 1 (tách từ US4):** Là một admin, tôi muốn xem báo cáo doanh thu theo ngày, tuần, tháng và theo từng nhà hàng, để đánh giá hiệu quả kinh doanh.
        *   **User Story 2 (tách từ US4):** Là một admin, tôi muốn xuất báo cáo doanh thu ra file Excel và tự động gửi email cho ban giám đốc định kỳ, để đảm bảo ban giám đốc nắm bắt thông tin kịp thời.

## Bước 3. Xếp lại backlog

**a) Xếp thứ tự ưu tiên cho US1, US2 đã sửa và 2 story tách từ US4:**

Tôi sẽ sắp xếp thứ tự ưu tiên dựa trên giá trị mang lại cho người dùng cuối (khách hàng) và tầm quan trọng của tính năng cốt lõi.

1.  **US1:** Là một khách hàng, tôi muốn lọc nhà hàng theo loại món, để nhanh tìm được món muốn ăn.
    *   _Lý do:_ Đây là tính năng cốt lõi, giúp khách hàng dễ dàng tìm kiếm sản phẩm mong muốn, tăng trải nghiệm người dùng ngay từ đầu. Mang lại giá trị trực tiếp và thiết yếu cho khách hàng.
2.  **US2 (Sửa):** Là một khách hàng, tôi muốn giao diện đặt món cho phép hoàn tất đơn hàng trong tối đa 5 bước, để có trải nghiệm đặt món nhanh chóng và thuận tiện.
    *   _Lý do:_ Cải thiện trải nghiệm đặt hàng, giảm thiểu rào cản và tăng tỷ lệ chuyển đổi cho khách hàng. Sau khi tìm được món, việc đặt món dễ dàng là yếu tố quan trọng.
3.  **User Story 1 (tách từ US4):** Là một admin, tôi muốn xem báo cáo doanh thu theo ngày, tuần, tháng và theo từng nhà hàng, để đánh giá hiệu quả kinh doanh.
    *   _Lý do:_ Mang lại giá trị cho người dùng admin, giúp theo dõi và quản lý hoạt động kinh doanh. Mặc dù không trực tiếp phục vụ khách hàng, nhưng việc nắm bắt số liệu kinh doanh là rất quan trọng cho hoạt động của công ty. Đây là nền tảng để có thể xuất báo cáo hay gửi email tự động.
4.  **User Story 2 (tách từ US4):** Là một admin, tôi muốn xuất báo cáo doanh thu ra file Excel và tự động gửi email cho ban giám đốc định kỳ, để đảm bảo ban giám đốc nắm bắt thông tin kịp thời.
    *   _Lý do:_ Tự động hóa việc phân phối báo cáo, giúp ban giám đốc có thông tin nhanh chóng. Tuy nhiên, việc xem báo cáo trực tiếp (User Story 1) có thể được ưu tiên hơn một chút để đảm bảo dữ liệu hiển thị đúng trước khi tự động hóa phân phối.

**b) Theo DEEP, story đứng đầu cần chi tiết đến mức nào? Buổi Refinement còn phải làm gì với nó trước khi đưa vào Sprint?**

Theo nguyên tắc DEEP của Product Backlog, story đứng đầu (top item) cần phải được **Detailed Appropriately** (Chi tiết một cách thích hợp). Điều này có nghĩa là story đó phải đủ chi tiết, rõ ràng và dễ hiểu đến mức nhóm phát triển có thể bắt đầu làm việc ngay trong Sprint tiếp theo mà không cần thêm thông tin mơ hồ. Nó cần đạt đến trạng thái 