# Quy Trình Rà Soát Học Thuật & Nội Dung (002_review_content)

Quy trình này hướng dẫn Agent cách rà soát chất lượng nội dung học thuật, tính chính xác của toán học, tính tương tác của lời giảng và tính đúng đắn của các bước bấm máy tính tài chính.

---

## Các Hạng Mục Cần Rà Soát

### 1. Kiểm tra Chứng minh Toán học (Math & Proofs)
- **Độ trực quan:** Kiểm tra xem các bước biến đổi toán học có quá tắt hay không. Nếu có bước chuyển đổi phức tạp, hãy chèn thêm một dòng giải thích bằng lời giản dị (mức độ toán phổ thông).
- **Ký hiệu chuẩn:** Đảm bảo tất cả các biến số, hàm số được định dạng đúng trong môi trường toán học (ví dụ: `x`, `y` phải nằm trong `$x$`, `$y$`; các hàm chuẩn phải dùng `\ln`, `\log`, `\exp`).
- **Đồng nhất công thức:** Đối chiếu công thức trong Module với bảng tra cứu `004_cfa_quant_terms.md` để đảm bảo không viết sai lệch ký hiệu.

### 2. Xác minh các Bước bấm Máy tính BA II Plus
Với mỗi ví dụ tính toán cần dùng máy tính tài chính Texas Instruments BA II Plus:
- **Tính toán độc lập:** Agent phải tự động tính toán lại kết quả dựa trên các dữ kiện đề bài để đảm bảo không bị sai lệch số liệu.
- **Chi tiết các phím bấm:** Đảm bảo hướng dẫn bấm máy được trình bày rõ ràng. Đối với các bài toán dòng tiền (NPV/IRR), luôn nhắc học viên xóa bộ nhớ đệm trước khi nhập:
  ```latex
  Bấm: [CF] -> [2nd] -> [CLR WRK] để xóa dữ liệu cũ.
  Sau đó nhập: [CF0] = ..., [C01] = ..., [F01] = ...
  ```
- **Bài toán TVM:** Ghi rõ từng tham số đầu vào: `N = ...`, `I/Y = ...`, `PV = ...`, `PMT = ...`, sau đó mới ghi phím cần bấm cuối cùng `CPT` -> `[FV]`.

### 3. Đánh giá tính Tương tác của Lời giảng (Interactive Annotations)
- **Kiểm tra câu hỏi gợi mở:** Đọc các đoạn chú thích của giảng viên (`\textcolor{blue}{\textit{...}}`). Đảm bảo lời văn không chỉ mang tính khẳng định lý thuyết mà lồng ghép các câu hỏi kích thích tư duy.
  * *Ví dụ chưa tốt:* "Lãi suất EAR luôn lớn hơn hoặc bằng lãi suất danh nghĩa."
  * *Ví dụ tốt:* "Chúng ta hãy suy nghĩ: Tại sao lãi suất thực tế nhận được (EAR) lại luôn lớn hơn hoặc bằng lãi suất danh nghĩa ghi trên hợp đồng? Có phải do tần suất ghép lãi trong năm quyết định điều này không?"

### 4. Kiểm tra cấu trúc Bảng biểu & Exam Tips
- **Bảng biểu:** Tuyệt đối không được chứa các đường kẻ dọc `|` trong phần `tabular`. Chỉ sử dụng `\toprule`, `\midrule`, `\bottomrule` để phân tách tiêu đề và nội dung.
- **Khung viền:** Đảm bảo các mẹo thi cử quan trọng được bọc chính xác trong môi trường `\begin{examtip} ... \end{examtip}`.

---

## Tiêu chí Đạt (Definition of Done)
Một Module được coi là vượt qua vòng rà soát nội dung khi:
1. Tất cả các công thức toán được hiển thị đúng định dạng và có giải thích nghĩa các biến số.
2. Kết quả tính toán bằng số trong ví dụ khớp hoàn toàn với các bước bấm máy tính BA II Plus được hướng dẫn.
3. Không có lỗi biên dịch LaTeX và không có đường kẻ dọc trong bảng biểu.
4. Lời giảng của giảng viên thể hiện đúng xưng xô "Chúng ta" và có câu hỏi gợi mở.
