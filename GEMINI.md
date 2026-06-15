# Workspace Guidelines: CFA Level 1 Quant LaTeX Project

Chào mừng bạn đến với hướng dẫn hoạt động của Antigravity AI Agent trong dự án biên soạn tài liệu **Quantitative Methods CFA Level 1 (2027)**. File này định nghĩa các quy tắc cốt lõi giúp AI hiểu ngữ cảnh và cộng tác với bạn hiệu quả nhất.

---

## 1. Cấu trúc Thư mục & Quy tắc Tên file
- **Tài liệu chính:** `QuantsLV1_2027.tex` (chứa khai báo preamble, mục lục, danh sách hình/bảng và các lệnh `\input{Module/...}`).
- **Các Module kiến thức:** Nằm trong thư mục `Module/` với định dạng tên `Module_X.tex` (ví dụ: `Module_1.tex`).
- **Hình ảnh / Đồ thị:** Tất cả ảnh minh họa phải lưu trữ trong thư mục `figs/`. Khi nhúng ảnh, sử dụng đường dẫn tương đối (ví dụ: `figs/logo.png`).

---

## 2. Quy chuẩn Định dạng LaTeX & Nội dung
- **Lời giải thích/Annotation của Giảng viên:** Sử dụng chữ in nghiêng màu xanh dương để phân biệt với nội dung Curriculum chính gốc:
  ```latex
  \textcolor{blue}{\textit{Nội dung diễn giải tiếng Việt...}}
  ```
- **Công thức toán học:**
  - Công thức độc lập quan trọng cần đánh số: Sử dụng môi trường `\begin{equation}` hoặc `\begin{alignedat}`.
  - Công thức không cần đánh số: Sử dụng `\begin{align*}` hoặc `\[ ... \]`.
  - Luôn viết hoa các hàm toán học tiêu chuẩn và ký hiệu (ví dụ: `\ln`, `\log`, `\text{Total Return}`).
- **Bảng biểu (Tables):** Sử dụng các package `booktabs` (`\toprule`, `\midrule`, `\bottomrule`) kết hợp với `tabular` có định kích thước cột cố định (ví dụ: `p{0.06\linewidth} | p{0.88\linewidth}`).
- **Ví dụ (Examples) & Nghiên cứu Tình huống (Case Studies):**
  - Nội dung cần được biên soạn lại (wording) ngắn gọn, súc tích hơn so với văn bản gốc.
  - Phải được đóng khung riêng biệt (sử dụng môi trường `tcolorbox` hoặc tương đương có thuộc tính `breakable`) để phân biệt trực quan với phần kiến thức cốt lõi.
- **Khoảng cách và Khoảng trống (Spacing & Whitespace):**
  - Tránh lạm dụng các lệnh tạo khoảng cách dọc trống như `\vspace{...}` hoặc `\\[...]` không cần thiết.
  - Giữ khoảng cách giữa các đoạn văn và công thức ở mức vừa phải, chỉ sử dụng một dòng trống duy nhất để tách biệt đoạn văn.
  - **Quản lý khoảng trắng lớn (Page stretching)**:
    - Sử dụng `\raggedbottom` trong preamble để ngăn LaTeX co giãn khoảng cách giữa các đoạn văn/công thức/box khi trang chưa đầy.
    - Hạn chế lạm dụng thuộc tính cưỡng bức vị trí `[H]` đối với hình ảnh/bảng biểu lớn. Nên ưu tiên các tùy chọn linh hoạt như `[!htbp]` hoặc `[tb]` để LaTeX tự động tối ưu hóa vị trí mà không gây đứt gãy trang đột ngột tạo khoảng trắng lớn.
    - Không lồng ghép các hộp `tcolorbox` không thể bẻ trang (ví dụ như `examtip` không để `breakable`) sâu bên trong các hộp `tcolorbox` cha khác, vì điều này tạo ra một khối không thể chia tách rất lớn, dễ gây ra lỗi tràn trang hoặc kéo giãn khoảng cách.

---

## 3. Quy trình Biên dịch & Kiểm tra (Compilation)
- Khi thực hiện thay đổi trên các file `.tex`, bạn có thể yêu cầu Agent chạy biên dịch thử để kiểm tra lỗi cú pháp bằng cách chạy lệnh:
  ```powershell
  latexmk -pdf -synctex=1 -interaction=nonstopmode QuantsLV1_2027.tex
  ```
  hoặc
  ```powershell
  pdflatex -interaction=nonstopmode QuantsLV1_2027.tex
  ```
- **Xử lý lỗi:** Nếu quá trình compile gặp lỗi (kiểm tra qua file `.log`), Agent phải tự động phân tích dòng bị lỗi, đề xuất giải pháp sửa cú pháp trước khi chạy lại compile.

---

## 4. Chỉ thị Đặc quyền dành cho AI Agent
- **Bảo toàn Cấu trúc:** Tuyệt đối không thay đổi phần preamble ở `QuantsLV1_2027.tex` trừ khi được yêu cầu thêm package cụ thể.
- **Không ghi đè tự động:** Trước khi chạy các lệnh dọn dẹp thư mục biên dịch (như `git clean` hay xóa các file aux/log/out), phải xin ý kiến của người dùng.
- **Xem trước tài liệu:** Hỗ trợ người dùng kiểm tra cách hiển thị PDF sau khi compile.
