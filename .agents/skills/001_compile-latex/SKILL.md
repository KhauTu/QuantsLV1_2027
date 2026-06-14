---
name: compile-latex
description: Biên dịch dự án LaTeX hiện tại sang PDF và tự động chẩn đoán lỗi nếu việc biên dịch thất bại.
---

# Hướng dẫn Biên dịch LaTeX & Chẩn đoán Lỗi

Skill này giúp Agent tự động biên dịch file `.tex` chính sang PDF bằng cách phân tách rõ ràng các file trung gian và file thành phẩm cuối cùng.

## 1. Cách chạy biên dịch

Khi người dùng yêu cầu biên dịch (compile) hoặc cập nhật tài liệu PDF:
1. Đảm bảo file chính `QuantsLV1_2027.tex` là mục tiêu biên dịch.
2. Chạy lệnh PowerShell sử dụng các tham số tách thư mục:
   ```powershell
   latexmk -pdf -synctex=1 -interaction=nonstopmode -auxdir=004_intermediate -outdir=005_product QuantsLV1_2027.tex
   ```
   *Lưu ý: Nếu hệ thống không có `latexmk` mà sử dụng `pdflatex` trực tiếp:*
   ```powershell
   pdflatex -interaction=nonstopmode -aux-directory=004_intermediate -output-directory=005_product QuantsLV1_2027.tex
   ```

## 2. Kiểm tra kết quả
- **Thành công:** Thông báo cho người dùng file PDF thành phẩm tại [005_product/QuantsLV1_2027.pdf](file:///d:/LaTeX/QuantsLV1_2027/005_product/QuantsLV1_2027.pdf) đã được cập nhật thành công.
- **Thất bại:** 
  1. Đọc nội dung file log tại [004_intermediate/QuantsLV1_2027.log](file:///d:/LaTeX/QuantsLV1_2027/004_intermediate/QuantsLV1_2027.log) (đặc biệt là các dòng chứa chữ `! ` hoặc chỉ ra số dòng lỗi).
  2. Xác định file `.tex` nào trong `001_Module/` gây ra lỗi.
  3. Giải thích nguyên nhân lỗi và đề xuất bản sửa cụ thể cho người dùng.

## 3. Dọn dẹp file rác
Để dọn dẹp các tệp tin trung gian, hãy gọi kỹ năng `clean-latex-cache` để xóa toàn bộ thư mục `004_intermediate`.
