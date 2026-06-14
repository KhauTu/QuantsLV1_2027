# Quy Chuẩn Định Dạng LaTeX

Tài liệu này lưu trữ các quy chuẩn định dạng LaTeX được áp dụng cho dự án biên soạn tài liệu **CFA Level 1 Quant (2027)**. AI Agent phải tuân thủ nghiêm ngặt các quy tắc này để đảm bảo tính nhất quán của sản phẩm đầu ra.

---

## 1. Lời Giải Thích & Annotation của Giảng Viên

Để phân biệt rõ ràng giữa nội dung Curriculum chính gốc và phần diễn giải/chú thích thêm bằng tiếng Việt của giảng viên:
- **Quy tắc:** Sử dụng chữ in nghiêng màu xanh dương.
- **Tương tác:** Lồng ghép các câu hỏi gợi mở suy nghĩ cho học viên trong phần diễn giải.
- **Cú pháp LaTeX:**
  ```latex
  \textcolor{blue}{\textit{Nội dung diễn giải tiếng Việt kèm câu hỏi gợi mở?}}
  ```
- *Lưu ý:* Tránh lạm dụng định dạng này cho các đoạn văn Curriculum chính thức.

---

## 2. Công Thức Toán Học (Math Environments)

- **Công thức độc lập quan trọng (cần đánh số):**
  Sử dụng môi trường `\begin{equation}` hoặc `\begin{alignedat}`.
  ```latex
  \begin{equation}
  PV = \frac{FV}{(1 + r)^n}
  \end{equation}
  ```
- **Công thức không cần đánh số:**
  Sử dụng `\begin{align*}` hoặc dấu ngoặc vuông toán học `\[ ... \]`.
  ```latex
  \[ R = \ln(1 + R_{\text{period}}) \]
  ```
- **Ký hiệu & Hàm toán học tiêu chuẩn:**
  Luôn sử dụng lệnh toán học chuẩn và định dạng văn bản đúng cách cho các biến chữ:
  - Sử dụng `\ln`, `\log`, `\exp` thay vì viết chữ thường.
  - Các cụm từ viết bằng chữ trong công thức toán học phải nằm trong lệnh `\text{...}` (ví dụ: `\text{Total Return}`, `\text{NPV}`).
  - Ví dụ đúng: `\text{Total Return} = \text{Price Apprec.} + \text{Income}`.

---

## 3. Trình Bày Bảng Biểu (Tables)

Bảng biểu trong tài liệu cần thiết kế tối giản, chuyên nghiệp và có kích thước rõ ràng:
- **Quy chuẩn gói lệnh:** Kết hợp package `booktabs` với môi trường `tabular` định kích thước cột cố định.
- **Đường kẻ bảng:** Sử dụng `\toprule` (đường kẻ trên cùng), `\midrule` (đường kẻ giữa tiêu đề và nội dung), và `\bottomrule` (đường kẻ dưới cùng). Hạn chế tối đa các đường kẻ dọc trong bảng để tạo cảm giác thoáng đãng và hiện đại.
- **Cú pháp ví dụ:**
  ```latex
  \begin{table}[h]
  \centering
  \caption{Ví dụ về bảng số liệu}
  \label{tab:example}
  \begin{tabular}{p{0.3\linewidth} | p{0.6\linewidth}}
  \toprule
  \textbf{Chỉ số} & \textbf{Mô tả chi tiết} \\
  \midrule
  NPV & Giá trị hiện tại thuần của dự án dòng tiền \\
  IRR & Tỷ suất hoàn vốn nội bộ \\
  \bottomrule
  \end{tabular}
  \end{table}
  ```

---

## 4. Định Dạng Thương Hiệu Trustville (Colors & Page Style)

Tài liệu được cấu hình màu sắc và chân trang đồng bộ với bộ nhận diện thương hiệu của Trustville.

### A. Định nghĩa màu sắc (Brand Colors)
Định nghĩa trong preamble của file `QuantsLV1_2027.tex`:
```latex
\usepackage{xcolor}
\definecolor{trustvilleblue}{HTML}{1D70B8}  % Xanh lam chủ đạo
\definecolor{trustvillegreen}{HTML}{0F8A5F} % Xanh lá bổ trợ
```
- Sử dụng màu `trustvilleblue` hoặc `trustvillegreen` cho các đề mục chính (Section/Subsection) bằng cách cấu hình qua package `titlesec` (nếu có) hoặc bọc tiêu đề thủ công:
  ```latex
  \section{\textcolor{trustvilleblue}{Tên đề mục chính}}
  ```

### B. Logo Chân Trang (Footer Logo)
Sử dụng package `fancyhdr` để đưa logo Trustville vào góc chân trang của tất cả các trang nội dung:
```latex
\usepackage{fancyhdr}
\pagestyle{fancy}
\fancyhf{} % Xóa các thiết lập mặc định
\fancyfoot[R]{\includegraphics[height=15pt]{figs/logo Trustville + text.png}} % Logo bên phải chân trang
\fancyfoot[C]{\thepage} % Số trang ở giữa
\renewcommand{\headrulewidth}{0pt} % Xóa đường kẻ ngang ở đầu trang
\renewcommand{\footrulewidth}{0.4pt} % Kẻ đường ngang mảnh ở chân trang
```

---

## 5. Định Dạng Hộp Mẹo Thi Cử (Exam Tips Box)

Sử dụng package `tcolorbox` để tạo khối hộp nổi bật cho các mẹo thi cử (**Exam Tips**):
```latex
\newtcolorbox{examtip}[1][]{
    colback=trustvilleblue!5!white, % Nền xanh lam nhạt 5%
    colframe=trustvilleblue,        % Viền xanh lam chủ đạo
    fonttitle=\bfseries,
    title=Exam Tip,
    boxrule=1pt,
    arc=3pt,
    #1
}
```
**Cách sử dụng trong file Module:**
```latex
\begin{examtip}
Khi tính toán Holding Period Return (HPR), hãy luôn nhớ cộng thêm cả dòng tiền nhận được từ cổ tức hoặc tiền lãi trong kỳ!
\end{examtip}
```

---

## 6. Bảo Toàn Cấu Trúc File & Biên Dịch
- **File chính:** `QuantsLV1_2027.tex` (quản lý preamble và `\input{...}`). Không được thay đổi phần preamble nếu không được yêu cầu cụ thể.
- **Thư mục hình ảnh:** Tất cả tệp hình ảnh phải nằm trong `figs/`. Sử dụng đường dẫn tương đối khi nhúng: `figs/ten_anh.png`.
