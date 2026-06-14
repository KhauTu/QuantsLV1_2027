# Cấu hình Thư mục Tự động hóa Dự án (.agents)

Thư mục này chứa các thiết lập, quy chuẩn, kỹ năng (skills), và quy trình (workflows) giúp AI Agent hoạt động hiệu quả, thống nhất và giảm thiểu sai sót khi làm việc trên dự án biên soạn tài liệu LaTeX **Quantitative Methods CFA Level 1 (2027)**.

## Cấu trúc Thư mục

- **`memory/`**: Bộ nhớ ngữ cảnh của dự án. Chứa các quy chuẩn phong cách trình bày (styling) và từ điển thuật ngữ chuyên ngành (vocabulary/formulas) để Agent sử dụng thuật ngữ nhất quán.
- **`skills/`**: Kỹ năng chuyên biệt dưới dạng công cụ hoặc kịch bản lệnh để Agent có thể gọi trực tiếp nhằm xử lý các công việc mang tính kỹ thuật (ví dụ: biên dịch LaTeX, dọn cache).
- **`workflows/`**: Quy trình phối hợp nhiều bước chuẩn hóa, giúp Agent hướng dẫn hoặc tự thực hiện tuần tự việc biên soạn, đánh giá và xuất bản tài liệu.

## Nguyên tắc Vận hành

1. **Tuân thủ quy tắc an toàn dữ liệu:** Không xóa hay sửa đổi các tệp cấu trúc gốc mà không có sự đồng ý của người dùng.
2. **Luôn tham chiếu Memory:** Trước khi tạo hoặc sửa đổi tài liệu toán học hay bảng biểu, Agent cần đọc tệp cấu hình trong thư mục `memory/` để giữ định dạng đồng nhất.
3. **Cập nhật định kỳ:** Khi có quy chuẩn mới hoặc công thức đặc thù, người dùng và Agent có thể bổ sung vào `memory/` hoặc tạo mới `skills/` để nâng cao năng lực hỗ trợ.
