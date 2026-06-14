# Quy Trình Xuất Bản Module (001_publish_module)

Quy trình này định nghĩa các bước Agent cần thực hiện khi viết mới, cập nhật hoặc đánh giá một Module kiến thức LaTeX trong dự án CFA Level 1 Quant.

---

## Các bước thực hiện

### Bước 1: Soạn thảo & Cập nhật Nội dung
1. Thực hiện các chỉnh sửa nội dung trong tệp `001_Module/[subfolder]/00x_Module_x.tex` tương ứng (hoặc tạo mới nếu là Module mới).
2. Đảm bảo file chính `QuantsLV1_2027.tex` có lệnh `\input{001_Module/[subfolder]/00x_Module_x.tex}` được khai báo đúng vị trí.

### Bước 2: Kiểm tra Định dạng & Quy chuẩn Trình bày (Linting)
Trước khi biên dịch, Agent đối chiếu nội dung với quy chuẩn lưu trong bộ nhớ `001_memory/003_latex_styling.md`:
1. **Annotations:** Sử dụng `\textcolor{blue}{\textit{...}}` cho chú thích giảng viên, đặt câu hỏi gợi mở để kích thích tư duy.
2. **Công thức toán học:** Công thức quan trọng dùng `equation` hoặc `alignedat`, ký hiệu đúng chuẩn (ví dụ: `\text{NPV}`).
3. **Bảng biểu:** Sử dụng gói lệnh `booktabs` (không dòng kẻ dọc), cột cố định `p{width}`.

### Bước 3: Biên dịch thử nghiệm (Compile & Verify)
1. Gọi kỹ năng **`compile-latex`** bằng lệnh:
   ```powershell
   latexmk -pdf -synctex=1 -interaction=nonstopmode -auxdir=004_intermediate -outdir=005_product QuantsLV1_2027.tex
   ```
2. Kiểm tra log biên dịch:
   - Nếu biên dịch **Thành công**: Tiến hành bước tiếp theo.
   - Nếu biên dịch **Thất bại**: Đọc tệp log tại `004_intermediate/QuantsLV1_2027.log`, xác định dòng bị lỗi và thực hiện sửa lỗi trước khi biên dịch lại.

### Bước 4: Xem trước & Xác minh
1. Thông báo cho người dùng biết việc cập nhật đã hoàn tất và tệp PDF thành phẩm tại [005_product/QuantsLV1_2027.pdf](file:///d:/LaTeX/QuantsLV1_2027/005_product/QuantsLV1_2027.pdf) đã được cập nhật thành công.
2. Cung cấp thông tin chi tiết về các trang vừa cập nhật để người dùng dễ kiểm tra.

### Bước 5: Dọn dẹp Cache Biên dịch
1. Hỏi ý kiến người dùng về việc dọn dẹp các tệp tin trung gian.
2. Khi được đồng ý, gọi kỹ năng **`clean-latex-cache`** để xóa sạch thư mục `004_intermediate/`.
