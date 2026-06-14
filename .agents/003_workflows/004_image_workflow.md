# Quy Trình Trích Xuất & Chèn Hình Ảnh (Image Acquisition & LaTeX Insertion Workflow)

Quy trình này hướng dẫn Giảng viên cách trích xuất hình ảnh (Exhibits/Tables/Charts) từ tài liệu gốc **CFA Curriculum 2027** và cách chèn chúng vào mã nguồn LaTeX một cách chuẩn hóa, sắc nét, không lỗi biên dịch.

---

## 1. Tìm kiếm và Chụp ảnh từ PDF gốc (Screen Capture Guide)

Tất cả các hình ảnh minh họa, bảng biểu và biểu đồ trong chương trình CFA 2027 đều được thống nhất gọi là **Exhibit** (không sử dụng nhãn "Figure" hay "Table" riêng lẻ).

### 💡 Quy trình thực hiện chụp ảnh:
1. **Mở PDF gốc:** Mở tệp `2027_CFA_L1V1_Quant.pdf` trong phần mềm đọc PDF của bạn (ví dụ: Adobe Acrobat, Foxit Reader, Chrome, v.v.).
2. **Định vị Exhibit:** Tìm đến trang tương ứng được liệt kê trong [Bản Đồ Tham Chiếu Công Thức & Hình Ảnh Minh Họa](file:///d:/LaTeX/QuantsLV1_2027/.agents/001_memory/006_math_image_mapping.md).
3. **Phóng to (Zoom):** Phóng to tài liệu lên **150% - 200%** trước khi chụp. Việc này đảm bảo độ phân giải của ảnh chụp màn hình đủ cao, khi in hoặc hiển thị trên PDF thành phẩm không bị mờ hay vỡ hạt.
4. **Cắt ảnh (Crop):** 
   - Sử dụng công cụ Snipping Tool (Windows: `Win + Shift + S`) hoặc phần mềm chụp màn hình tương đương.
   - Cắt sát viền biểu đồ/bảng biểu. **Không** chụp kèm thanh cuộn PDF, số trang của PDF reader, hay các dòng chữ văn bản xung quanh trừ khi chúng là một phần của bảng.
5. **Định dạng file:** Lưu file dưới định dạng **PNG** (để giữ nguyên chất lượng ảnh chụp không bị nén mất chi tiết).

---

## 2. Quy tắc Lưu trữ & Đặt tên (Naming & Directory Structure)

Để tránh lộn xộn và dễ quản lý, tất cả các hình ảnh minh họa phải tuân theo cấu trúc thư mục sau:

- **Thư mục lưu trữ:** `002_figs/00x_Module_x/`
  - *Ví dụ cho Module 1:* `002_figs/001_Module_1/`
- **Quy tắc đặt tên file:** 
  - `exhibit_[number].png` (viết thường, dùng dấu gạch dưới, không dấu, không khoảng trắng).
  - *Ví dụ:* `002_figs/001_Module_1/exhibit_1.png`
  - Nếu một Exhibit có nhiều phần nhỏ (ví dụ Panel A, Panel B) mà được tách làm các file ảnh khác nhau: `exhibit_18_a.png`, `exhibit_18_b.png`.

---

## 3. Quy chuẩn viết mã nguồn LaTeX (LaTeX Insertion Syntax)

Khi chèn hình ảnh vào tài liệu LaTeX, luôn sử dụng môi trường `figure` tiêu chuẩn kết hợp với các thiết lập căn lề và co dãn tỷ lệ linh hoạt.

### 📝 Mã LaTeX Mẫu:
```latex
\begin{figure}[H]
    \centering
    \includegraphics[width=0.85\linewidth]{002_figs/001_Module_1/exhibit_1.png}
    \caption{Ørsted A/S Equity Performance 1 January 2016--29 December 2023 (in DKK)}
    \label{fig:mod1_exhibit_1}
\end{figure}
% Reference: CFA Curriculum 2027, Volume 1, Module 1, Page 18
```

### ⚠️ Các điểm lưu ý quan trọng:
1. **Môi trường `[H]`:** Sử dụng gói `float` (đã khai báo trong preamble) và đặt tham số `[H]` để ép hình ảnh hiển thị đúng tại vị trí viết code, tránh bị nhảy trang tự động làm gián đoạn mạch đọc của học viên.
2. **Tỷ lệ hiển thị (`width=...`):**
   - Đối với biểu đồ ngang, rộng: sử dụng `width=0.85\linewidth` hoặc `width=0.9\linewidth`.
   - Đối với biểu đồ dọc, hẹp: sử dụng `width=0.6\linewidth` hoặc `width=0.7\linewidth`.
   - Không được fix kích thước cứng bằng cm hay inch để đảm bảo tính responsive khi xuất bản các khổ giấy khác nhau.
3. **Đánh nhãn (`\label`):** Đặt nhãn theo cấu pháp `fig:mod[X]_exhibit_[Y]` để dễ dàng tham chiếu chéo trong văn bản bằng lệnh `\ref{fig:...}` (ví dụ: *Như thể hiện ở Exhibit \ref{fig:mod1_exhibit_1}...*).
4. **Chú thích nguồn gốc (`% Reference`):** Bắt buộc chèn dòng chú thích ghi chú trang gốc trong Curriculum ngay bên dưới môi trường hình ảnh để phục vụ việc rà soát học thuật sau này.

---

## 4. Quy trình Cập nhật Tài liệu Tham chiếu

Mỗi khi bổ sung hoặc thay đổi một hình ảnh minh họa trong mã nguồn TeX:
1. Giảng viên chụp ảnh và lưu vào thư mục `002_figs/` tương ứng.
2. Cập nhật dòng tham chiếu trong file LaTeX nguồn.
3. Bổ sung/cập nhật thông tin tệp tin vào bảng quản lý tại tệp tin bộ nhớ [006_math_image_mapping.md](file:///d:/LaTeX/QuantsLV1_2027/.agents/001_memory/006_math_image_mapping.md).
