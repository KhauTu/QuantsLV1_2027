# Bộ Nhớ Ngữ Cảnh Dự Án (Project Memory)

Thư mục này đóng vai trò là nơi lưu trữ các kiến thức tĩnh, quy chuẩn biên soạn và từ vựng chuyên ngành được thống nhất trong suốt dự án. AI Agent sẽ tự động tham chiếu các tài liệu này trước khi tiến hành viết hoặc sửa đổi các tệp nguồn LaTeX.

## Danh mục Tài liệu Bộ nhớ

- **`001_user_profile.md`**: Lưu trữ thông tin cá nhân, phong cách và thói quen tương tác mong muốn của người dùng.
- **`002_project_overview.md`**: Định hình mục tiêu dài hạn, lộ trình và các cột mốc quan trọng của dự án.
- **`003_latex_styling.md`**: Quy định về cách hiển thị chữ, cấu trúc mã LaTeX, môi trường toán học, định dạng bảng biểu và cách phân biệt phần nội dung Curriculum gốc với nội dung chú thích/giảng giải của giảng viên.
- **`004_cfa_quant_terms.md`**: Tổng hợp danh sách thuật ngữ và công thức Định lượng CFA Level 1 (2027) bằng tiếng Việt và tiếng Anh, kèm ký hiệu toán học tiêu chuẩn để đảm bảo sự thống nhất trong biên dịch và trình bày.

## Nguyên tắc Cập nhật Memory

- Khi có bất kỳ thay đổi nào về quy chuẩn trình bày hoặc phát hiện một lỗi dịch thuật/ký hiệu có tính hệ thống, người dùng hoặc Agent nên cập nhật trực tiếp vào các file tương ứng trong thư mục này.
- Khi Agent giải quyết một lỗi lặp đi lặp lại hoặc học được một chỉ dẫn cụ thể từ người dùng, Agent cần ghi nhận nó vào `latex_styling.md` để tránh lặp lại sai lầm trong các phiên làm việc sau.
