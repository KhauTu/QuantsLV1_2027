# Quy Trình Đóng Gói & Xuất Bản PDF (003_release_pdf)

Quy trình này hướng dẫn các bước kiểm tra cuối cùng, cập nhật thông tin phiên bản, biên dịch hoàn chỉnh và dọn dẹp hệ thống trước khi phát hành tài liệu PDF học tập cho học viên Trustville.

---

## Các Bước Thực Hiện

### Bước 1: Kiểm tra Hiển thị Trực quan (Visual Quality Check)
Trước khi xuất bản tệp PDF cuối cùng, Agent cần hỗ trợ Giảng viên rà soát các yếu tố hiển thị trực quan:
- **Tràn lề (Overfull \hbox):** Kiểm tra log tại `004_intermediate/QuantsLV1_2027.log` để phát hiện các dòng chữ hoặc công thức toán quá dài bị tràn ra ngoài lề trang giấy. Nếu phát hiện, hãy đề xuất ngắt dòng công thức bằng môi trường `split` hoặc `aligned`.
- **Ngắt trang xấu (Bad Page Breaks):** Kiểm tra xem có tiêu đề phần nào bị nằm đơn độc ở cuối trang (orphan heading) hoặc các bảng biểu bị cắt đôi một cách không hợp lý hay không. Sử dụng lệnh `\newpage` hoặc `\clearpage` để ngắt trang thủ công nếu cần.
- **Vị trí hình ảnh:** Đảm bảo các ảnh đồ thị từ thư mục `002_figs/` không bị trôi tự do quá xa khỏi đoạn văn bản mô tả tương ứng. Sử dụng tùy chọn vị trí hình ảnh phù hợp (như `[H]` hoặc `[htbp]`).

### Bước 2: Cập nhật Metadata & Phiên bản (Version Control)
1. Kiểm tra ngày tháng và tên tác giả trong file chính `QuantsLV1_2027.tex`.
2. Định dạng ngày tháng phát hành chính xác trong lệnh `\date{Hanoi, [Tháng] [Năm]}`.
3. Nếu cần, ghi chú phiên bản tài liệu (ví dụ: Phiên bản 1.0 - Cập nhật Chương trình 2027) ở phần Lời giới thiệu.

### Bước 3: Biên dịch Xuất bản (Final Compilation)
Chạy biên dịch ít nhất 2 lần liên tiếp (hoặc dùng `latexmk` tự động kiểm tra) để đảm bảo Bảng mục lục (Table of Contents), Danh mục Bảng (List of Tables) và Danh mục Hình ảnh (List of Figures) được cập nhật liên kết chính xác tuyệt đối:
```powershell
latexmk -pdf -synctex=1 -interaction=nonstopmode -auxdir=004_intermediate -outdir=005_product QuantsLV1_2027.tex
```
*Lưu ý:* Kiểm tra tệp log tại `004_intermediate/QuantsLV1_2027.log` để đảm bảo không còn cảnh báo `Reference '...' on page ... undefined`.

### Bước 4: Dọn dẹp tệp tin rác (Clean Build Cache)
1. Xin xác nhận của Giảng viên về việc dọn dẹp các tệp auxiliary.
2. Thực hiện gọi kỹ năng **`clean-latex-cache`** để xóa sạch thư mục `004_intermediate/`.
3. Đảm bảo thư mục làm việc chỉ còn giữ lại tệp tin nguồn `.tex`, thư mục `001_Module/`, thư mục `002_figs/`, thư mục `.agents/` và tệp PDF thành phẩm tại thư mục `005_product/`.

### Bước 5: Đóng gói và Lưu trữ (Archiving)
1. Đảm bảo tệp thành phẩm tại [005_product/QuantsLV1_2027.pdf](file:///d:/LaTeX/QuantsLV1_2027/005_product/QuantsLV1_2027.pdf) đã được ghi đè/cập nhật thành công.
2. Nếu Giảng viên yêu cầu lưu trữ các phiên bản cũ, tiến hành sao chép và đổi tên tệp sao lưu theo định dạng:
   ```text
   Trustville_CFA_L1_Quant_2027_v[X.Y]_[Ngày_Tháng_Năm].pdf
   ```
