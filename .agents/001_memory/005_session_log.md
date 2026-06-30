# Nhật Ký Phiên Làm Việc & Lịch Sử Dự Án (Session History Log)

Tài liệu này lưu trữ lịch sử chi tiết của từng phiên làm việc giữa Giảng viên và AI Agent, giúp quản lý tiến độ và định hình kế hoạch cải tiến liên tục cho dự án.

---

## 📅 Phiên làm việc 01: Thiết lập Hệ thống & Phân vùng Dự án
*Thời gian hoàn thành: 14/06/2026*

### 1. Báo cáo công việc đã hoàn thành (Completed Tasks)
- **Thiết lập cấu hình tự động hóa:**
  - Khởi tạo thư mục `.agents/` với 3 phần cốt lõi: `001_memory/` (chứa Profile giảng viên, tổng quan dự án, quy chuẩn LaTeX, từ điển Quant), `skills/` (chứa skill biên dịch và dọn dẹp cache), và `003_workflows/` (chứa 3 quy trình xuất bản, rà soát học thuật, phát hành PDF).
  - Tích hợp thành công bộ nhận diện thương hiệu Trustville vào file gốc `QuantsLV1_2027.tex` (định nghĩa màu xanh lam/lá, thêm logo chân trang bằng `fancyhdr`, thiết kế hộp tcolorbox `examtip`).
- **Phân tách và tối ưu hóa thư mục (Max 10 items rule):**
  - Di chuyển các file `.tex` hoạt động vào thư mục con có nhóm chủ đề thuộc `001_Module/` (mỗi thư mục chứa tối đa 3 file).
  - Phân loại hình ảnh đồ thị gốc vào các thư mục con theo Module tương ứng thuộc `002_figs/` để dọn dẹp thư mục hình ảnh.
  - Thiết lập phân vùng biên dịch: Dồn toàn bộ tệp rác trung gian vào `004_intermediate/` và tệp PDF sản phẩm hoàn chỉnh vào `005_product/`.
- **Đóng gói mã nguồn lên GitHub:**
  - Khởi tạo Git repository và viết tệp `.gitignore` chuẩn hóa để loại bỏ các tệp rác và tệp tham khảo nặng.
  - Chia nhỏ các thay đổi và thực hiện **5 commit local chuyên biệt**.
  - Thực hiện `git push` thành công lên kho lưu trữ GitHub của giảng viên tại: `https://github.com/KhauTu/QuantsLV1_2027.git`.

### 2. Danh sách Git Commits trong phiên
- `59200f5` ci: add agent workspace settings including memories, skills, and workflows
- `2933a87` feat: add LaTeX module source files organized in thematic subfolders
- `5bb5e22` asset: add figure assets grouped in module subfolders
- `fa369a6` feat: add main LaTeX entrypoint with Trustville brand style
- `49d7108` docs: initialize project guidelines and gitignore configurations

### 3. Đề xuất cải tiến & Kế hoạch phiên tiếp theo (Next Session Plan)
- **Đề xuất cải tiến (Improvement Ideas):**
  - *Cải tiến 1:* Xây dựng một lệnh macro hoặc phím tắt compile nhanh trong editor để Giảng viên có thể chạy biên dịch và xuất ra tệp PDF trong `005_product/` chỉ bằng 1 tổ hợp phím.
  - *Cải tiến 2:* Thêm các ví dụ thực tế liên quan đến thị trường chứng khoán Việt Nam (như lãi suất danh nghĩa và lãi suất thực tế khi gửi tiết kiệm tại các ngân hàng lớn) vào phần ghi chú giảng viên ở Module 1 để học viên dễ liên hệ.
- **Kế hoạch phiên tiếp theo:**
  - *Bước 1:* Hoàn thiện nội dung và cấu trúc chi tiết cho **Module 2** (Đã hoàn thành trong phiên 2).

---

## 📅 Phiên làm việc 02: Hoàn thiện & Tái cấu trúc Module 2
*Thời gian hoàn thành: 14/06/2026 (Phiên chiều)*

### 1. Báo cáo công việc đã hoàn thành (Completed Tasks)
- **Tái cấu trúc đề mục Module 2:**
  - Đổi tên chương thành `Types of Returns for Financial Assets, Instruments, and Indicators` bám sát sách giáo trình CFA 2027.
  - Tổ chức lại nội dung thành 3 học phần lớn: *Types of Returns*, *Long-Term Financial Asset Returns*, và *Risks and Returns*.
- **Tối ưu hóa thiết kế & trình bày:**
  - Bổ sung bảng Matrix Mapping trực quan (Bảng 2.1) phân loại Price Return và Capital Distribution Return của từng loại tài sản/chỉ báo.
  - Khắc phục các lỗi hiển thị Learning Outcomes bằng cách định dạng chính xác vị trí hiển thị bảng LOS.
  - Xử lý triệt để cảnh báo `overfull/underfull hbox` bằng cách sử dụng các hàng lồng cột (nested tabular) trong tiêu đề bảng biểu và thu nhỏ tỷ lệ cột.
- **Git Push:** Pushed commit `21a1b28` lên master.

### 2. Danh sách Git Commits trong phiên
- `21a1b28` Format and restructure CFA 2027 Module 2 LaTeX chapter, integrate return type matrix mapping

### 3. Đề xuất cải tiến & Kế hoạch phiên tiếp theo (Next Session Plan)
- **Đề xuất cải tiến:**
  - *Cải tiến 1:* Tạo ra các bảng biểu chuẩn hóa cho phần so sánh Money-Weighted và Time-Weighted Returns ở Module 3 để học viên dễ nắm bắt bản chất (Đã hoàn thành).
- **Kế hoạch phiên tiếp theo (Phiên làm việc 03):**
  - Đã chuyển giao và hoàn thành trong phiên 3.

---

## 📅 Phiên làm việc 03: Tối ưu hóa Khoảng trắng & Biên soạn Module 3
*Thời gian hoàn thành: 15/06/2026 (Phiên sáng)*

### 1. Báo cáo công việc đã hoàn thành (Completed Tasks)
- **Biên soạn Module 3:**
  - Soạn thảo nội dung hoàn chỉnh cho `003_Module_3.tex` về Benchmarking Returns (Money-Weighted Return, Time-Weighted Return, Index Weighting).
  - Tích hợp 2 biểu đồ minh họa `exhibit_7.png` và `exhibit_15.png`.
- **Khắc phục triệt để lỗi khoảng trắng kéo giãn (Page stretching):**
  - Cấu hình lệnh toàn cục `\raggedbottom` tại `QuantsLV1_2027.tex` để ngăn LaTeX tự động giãn khoảng cách dòng/đoạn văn bất hợp lý khi trang chưa đầy.
  - Thay thế thuộc tính định vị tuyệt đối `[H]` bằng `[!htbp]` linh hoạt cho các đối tượng float lớn (hình ảnh và bảng biểu) trong toàn bộ các Module 1, 2 và 3 để tránh việc đứt gãy trang tạo ra các khoảng trống lớn.
  - Biên dịch và xác thực thành công file PDF không còn lỗi co giãn khoảng trắng.

---

## 📅 Phiên làm việc 04: Biên soạn & Tích hợp Hình ảnh Module 4
*Thời gian hoàn thành: 15/06/2026 (Phiên chiều)*

### 1. Báo cáo công việc đã hoàn thành (Completed Tasks)
- **Soạn thảo và Hoàn thiện nội dung Module 4:**
  - Hoàn thành nội dung của `004_Module_4.tex` (The Time Value of Money in Finance) đáp ứng tất cả các Learning Outcomes (TVM trong Fixed Income & Equity, Suất sinh lời/Hệ số tăng trưởng ngầm định, Cộng dồn dòng tiền và Định giá Quyền chọn).
  - Áp dụng các quy chuẩn thiết kế: tcolorbox compact (`before/after skip=6pt, breakable`), lời giải thích in nghiêng xanh dương của giảng viên.
- **Tích hợp hình ảnh minh họa:**
  - Tạo thư mục hình ảnh `002_figs/004_Module_4` chứa 16 tệp hình ảnh placeholder từ logo Trustville.
  - Khai báo 16 hình ảnh tương ứng (`exhibit_1` đến `exhibit_22`) trong file `.tex` để tăng tính trực quan.
  - Định vị toàn bộ các khối `figure` ở lớp ngoài (outer par mode), tránh lồng ghép bên trong các hộp `tcolorbox` để ngăn ngừa lỗi biên dịch LaTeX.
- **Biên dịch & Kiểm tra PDF:**
  - Biên dịch thành công dự án bằng `latexmk` lên 57 trang, không phát sinh lỗi cú pháp hay lỗi nhóm box. PDF thành phẩm được lưu tại `005_product/QuantsLV1_2027.pdf`.

### 2. Đề xuất cải tiến & Kế hoạch phiên tiếp theo (Next Session Plan)
- **Kế hoạch phiên tiếp theo (Phiên làm việc 05):**
  - Thực hiện dọn dẹp và rà soát định dạng Module 5, 6, 7 (Đã hoàn thành).

---

## 📅 Phiên làm việc 05: Dọn dẹp Workspace & Chuẩn hóa Định dạng Module 5, 6, 7
*Thời gian hoàn thành: 24/06/2026*

### 1. Báo cáo công việc đã hoàn thành (Completed Tasks)
- **Dọn dẹp & Phân loại file hệ thống:**
  - Xóa bỏ các tệp rác trung gian sinh ra trong quá trình biên dịch ở thư mục gốc (.aux, .log, .pdf, .toc, v.v.).
  - Tạo thư mục [000_references/text_dumps/](file:///d:/LaTeX/QuantsLV1_2027/000_references/text_dumps) và di chuyển toàn bộ 15 tệp `.txt` tạm/nháp vào đây để trả lại sự ngăn nắp cho thư mục gốc.
- **Rà soát & Chuẩn hóa định dạng Modules 5, 6, 7:**
  - **Module 5:** Chuyển đổi Bảng 5.1 và 5.3 sang cột định kích thước cố định (`p{...}`).
  - **Module 6:** Kích hoạt (uncomment) các lời giảng viên in nghiêng màu xanh dương ở các dòng đầu và dòng 66; chuyển đổi các Bảng 6.2, 6.3, 6.8, 6.9, 6.10 sang cột định kích thước cố định.
  - **Module 7:** Chuyển đổi các Bảng 7.2, 7.5, 7.7, 7.8 sang cột định kích thước cố định.
- **Biên dịch & Xác thực:**
  - Chạy biên dịch thành công tài liệu thông qua `latexmk` lên 112 trang. PDF đầu ra tại [005_product/QuantsLV1_2027.pdf](file:///d:/LaTeX/QuantsLV1_2027/005_product/QuantsLV1_2027.pdf) được cập nhật chính xác và hiển thị đẹp mắt.

### 2. Đề xuất cải tiến & Kế hoạch phiên tiếp theo (Next Session Plan)
- **Kế hoạch phiên tiếp theo (Phiên làm việc 06):**
  - Triển khai viết nội dung chi tiết cho **Module 8: The Return and Risk of a Financial Portfolio** ([008_Module_8.tex](file:///d:/LaTeX/QuantsLV1_2027/001_Module/003_inference_and_portfolios/008_Module_8.tex)) bám sát các LOS (a, b, c).

---

## 📅 Phiên làm việc 06: Chuẩn hóa, Dịch Thuật & Cắt Ảnh Đồ Thị Module 8
*Thời gian hoàn thành: 25/06/2026*

### 1. Báo cáo công việc đã hoàn thành (Completed Tasks)
- **Chuẩn hóa đồ thị (Figure Cropping):**
  - Tự động hóa việc cắt lề và loại bỏ các phần chữ thừa xung quanh toàn bộ 15 đồ thị trong `002_figs/008_Module_8/` bằng script Pillow.
  - Thay thế các tệp ảnh gốc bằng các phiên bản đã cắt sát phần đồ thị để đảm bảo tính mỹ thuật.
- **Biên dịch dịch thuật và Bổ sung Hướng dẫn bấm máy tính:**
  - Dịch toàn bộ lời giải thích của các ví dụ (Example 1-13, 14, 15, 17), bộ câu hỏi ôn tập (Question Sets 1-3), và 10 bài tập thực hành (Practice Problems) sang tiếng Việt học thuật, giữ nguyên văn bản tiếng Anh của đề bài.
  - Bổ sung hướng dẫn bấm máy tính tài chính Texas Instruments BA II Plus chi tiết cho các phép toán phức tạp (như tính tỷ suất sinh lời trung bình hình học và độ lệch chuẩn).
- **Lược bỏ đường kẻ dọc trong bảng biểu:**
  - Loại bỏ hoàn toàn tất cả các đường kẻ dọc (`|`) trong toàn bộ các bảng biểu của Module 8 (Bảng LOS, Bảng 8.1, bảng dữ liệu ví dụ/bài tập) để tuân thủ thiết kế `booktabs` hiện đại và sạch sẽ.
- **Làm phong phú Ghi chú Giảng viên (Teacher Notes):**
  - Thêm mới và nâng cấp các ghi chú giảng viên màu xanh dương in nghiêng sử dụng đại từ chung "Chúng ta" kèm các câu hỏi gợi mở tư duy (ví dụ: so sánh bản chất rủi ro giữa CML và SML, ý nghĩa của Global MVP).
- **Biên dịch & Sửa lỗi cú pháp:**
  - Phát hiện và sửa lỗi thiếu ký tự đóng mở công thức toán học `$` trong lời giải bài tập 8.
  - Biên dịch thành công tài liệu lên 140 trang thông qua `latexmk` mà không gặp bất kỳ lỗi cú pháp nào. PDF thành phẩm đạt chất lượng xuất bản cao nhất.

### 2. Đề xuất cải tiến & Kế hoạch phiên tiếp theo (Next Session Plan)
- **Kế hoạch phiên tiếp theo:**
  - Tiến hành viết tiếp và biên dịch **Module 9** bám sát quy chuẩn LaTeX và rà soát ảnh đồ thị tương tự.

---

## 📅 Phiên làm việc 07: Tối ưu hóa Dung lượng trang qua việc Rút ngắn Ghi chú Giảng viên
*Thời gian hoàn thành: 25/06/2026 (Phiên chiều)*

### 1. Báo cáo công việc đã hoàn thành (Completed Tasks)
- **Rút gọn 56 Ghi chú Giảng viên:**
  - Viết lại toàn bộ 56 ghi chú của giảng viên (màu xanh dương in nghiêng) trên các file từ Module 1 đến Module 8 để tối giản từ ngữ, loại bỏ các từ đệm xã giao dư thừa nhưng vẫn giữ nguyên đại từ "Chúng ta" và các câu hỏi gợi mở cốt lõi.
  - Sửa lỗi cú pháp tại comment ID 46 (phần chứng minh phân phối Logistic trong `006_Module_6.tex`) bằng cách bọc chính xác các lệnh toán học `\text{Var}`, `\frac` và phương trình vào trong môi trường toán học inline `$ ... $`.
- **Tự động hóa thay thế:**
  - Triển khai thành công mã nguồn Python `replace_comments_by_order.py` để tự động hóa việc rà soát và thay thế chuẩn xác toàn bộ 56 ghi chú giảng viên theo thứ tự xuất hiện của các file.
- **Biên dịch & Xác thực PDF:**
  - Biên dịch dự án hoàn chỉnh sang PDF thông qua `latexmk` một cách trơn tru, không có bất kỳ cảnh báo/lỗi biên dịch nào.
  - Tải và lưu trữ PDF thành phẩm tại [005_product/QuantsLV1_2027.pdf](file:///d:/LaTeX/QuantsLV1_2027/005_product/QuantsLV1_2027.pdf).
  - **Kết quả giảm trang:** Tổng số trang của tài liệu đã được giảm thành công từ **140 trang xuống còn 138 trang** (giảm 2 trang) hoàn toàn sạch sẽ, không thay đổi bất kỳ tỷ lệ hình ảnh, cỡ chữ hay căn lề nào của định dạng tài liệu gốc.

### 2. Đề xuất cải tiến & Kế hoạch phiên tiếp theo (Next Session Plan)
- **Kế hoạch phiên tiếp theo:**
  - Tiếp tục phát triển và hoàn thiện **Module 9: Simple Linear Regression in Finance** ([009_Module_9.tex](file:///d:/LaTeX/QuantsLV1_2027/001_Module/003_inference_and_portfolios/009_Module_9.tex)). (Đã hoàn thành trong phiên 8)

---

## 📅 Phiên làm việc 08: Rút gọn & Tối ưu hóa Module 9
*Thời gian hoàn thành: 27/06/2026*

### 1. Báo cáo công việc đã hoàn thành (Completed Tasks)
- **Phục hồi & Đồng bộ Module 9:**
  - Trích xuất thành công các đoạn mã nguồn dựng trang từ tệp lịch sử để khôi phục cấu trúc ban đầu của [009_Module_9.tex](file:///d:/LaTeX/QuantsLV1_2027/001_Module/003_inference_and_portfolios/009_Module_9.tex) (1,719 dòng) bị mất do thao tác kiểm kho trước đó.
- **Rút gọn văn bản chương tối đa:**
  - Áp dụng thành công 25 khối thay thế để làm cô đọng các phần văn bản lý thuyết và ghi chú giảng viên dài dòng.
  - Dung lượng tệp nguồn `.tex` giảm từ **113KB xuống còn 75KB** (giảm khoảng **33%**).
  - Đảm bảo giữ nguyên các phần toán lý thuyết, bảng biểu, các bộ câu hỏi ôn tập (Question Sets 1-3) và lời giải chi tiết có hướng dẫn máy tính tài chính Texas Instruments BA II Plus.
- **Vá lỗi và Biên dịch dự án:**
  - Sửa lỗi cú pháp liên quan đến ký tự `\n` đặc biệt xuất hiện tại các dòng 58 và 702 trong tệp LaTeX.
  - Biên dịch toàn bộ tài liệu thành công đạt **170 trang** bằng `latexmk` mà không gặp bất kỳ lỗi cảnh báo hay lỗi cú pháp nào. Tệp PDF kết quả được lưu trữ tại [005_product/QuantsLV1_2027.pdf](file:///d:/LaTeX/QuantsLV1_2027/005_product/QuantsLV1_2027.pdf).
- **Dọn dẹp tệp rác hệ thống:**
  - Xóa bỏ toàn bộ các script tạm thời và các file txt hỗ trợ trong quá trình tối ưu để khôi phục trạng thái sạch sẽ cho thư mục làm việc.

### 2. Kế hoạch phiên tiếp theo (Next Session Plan)
- **Kế hoạch phiên tiếp theo:**
  - Bắt đầu triển khai và tối ưu hóa nội dung cho **Module 10: Applications of Simple Linear Regression in Finance** ([010_Module_10.tex](file:///d:/LaTeX/QuantsLV1_2027/001_Module/004_regression_and_data_science/010_Module_10.tex)). (Đã hoàn thành trong phiên 9)

---

## 📅 Phiên làm việc 09: Thiết kế & Biên soạn Module 10
*Thời gian hoàn thành: 29/06/2026*

### 1. Báo cáo công việc đã hoàn thành (Completed Tasks)
- **Đồng bộ và Commit thay đổi cũ:**
  - Commit toàn bộ các thay đổi chưa staged từ Phiên làm việc 08 liên quan đến Module 9 (`c955481`) để làm sạch kho mã nguồn làm việc.
- **Trích xuất và Xử lý hình ảnh đồ thị:**
  - Kết xuất (render) thành công các trang PDF chứa hình ảnh vector.
  - Sử dụng script Python `crop_all_images.py` để tự động cắt và lưu chính xác 5 đồ thị chất lượng cao dạng PNG vào thư mục `002_figs/010_Module_10/` (đặt tên: `10.1-Nonlinear.png`, `10.2-Interest vs Inflation.png`, `10.3-Residual Plots.png`, `10.4-Quarterly Rev vs Time.png`, `10.5-Residual Quarterly Rev vs Time.png`).
- **Soạn thảo và Hoàn thiện nội dung Module 10:**
  - Hoàn thành nội dung tệp `010_Module_10.tex` đáp ứng toàn bộ các mục tiêu học tập (LOS a, b, c, d).
  - Biên soạn lý thuyết chi tiết về ước lượng OLS, 5 giả định quan trọng của OLS, cách đọc bảng phân tích phương sai ANOVA (FIRN AG), khoảng dự báo (Prediction Interval), các dạng hàm phi tuyến Log-Lin, Lin-Log, Log-Log và ứng dụng CAPM thực tế (LVMH so với chỉ số CAC 40).
  - Tích hợp ghi chú giảng viên màu xanh dương in nghiêng và các tcolorbox bài tập/ví dụ có thuộc tính `breakable`.
- **Biên dịch & Xác thực PDF:**
  - Biên dịch thành công dự án lên **181 trang** bằng `latexmk` mà không gặp bất kỳ lỗi cú pháp nào. Tài liệu PDF kết quả lưu tại [005_product/QuantsLV1_2027.pdf](file:///d:/LaTeX/QuantsLV1_2027/005_product/QuantsLV1_2027.pdf).

### 2. Danh sách Git Commits trong phiên
- `c955481` feat(quants): sync and optimize Module 9, update session log for Session 8
- `2479676` feat(quants): implement Module 10 regression, extract figures, clean build

### 3. Đề xuất cải tiến & Kế hoạch phiên tiếp theo (Next Session Plan)
- **Kế hoạch phiên tiếp theo:**
  - Triển khai và tối ưu hóa nội dung cho **Module 11: Introduction to Financial Data Science** ([011_Module_11.tex](file:///d:/LaTeX/QuantsLV1_2027/001_Module/004_regression_and_data_science/011_Module_11.tex)). (Đã hoàn thành trong phiên 10)

---

## 📅 Phiên làm việc 10: Biên soạn & Hoàn thiện Module 11
*Thời gian hoàn thành: 29/06/2026*

### 1. Báo cáo công việc đã hoàn thành (Completed Tasks)
- **Chuẩn hóa định dạng Learning Outcomes:**
  - Định cấu hình lại các bảng Học tập ở cấp độ mục (`\section`) trong Module 9 và Module 10 để loại bỏ hoàn toàn tiêu đề "LEARNING OUTCOMES" và các đường kẻ ngang, đồng thời đồng bộ hóa dấu phân cách cột `|` như yêu cầu của Giảng viên.
- **Trích xuất và Xử lý hình ảnh đồ thị cho Module 11:**
  - Sử dụng script Python `crop_m11_images.py` để trích xuất 3 sơ đồ minh họa chất lượng cao trực tiếp từ PDF gốc vào [002_figs/011_Module_11/](file:///d:/LaTeX/QuantsLV1_2027/002_figs/011_Module_11/):
    - `11.1-Big Data Characteristics.png` (Đặc tính 3Vs của Big Data).
    - `11.2-Time vs Rolling.png` (Time-Based Split vs Rolling-Window Validation).
    - `11.3-Neural Network.png` (Mạng Nơ-ron Nhân tạo).
- **Soạn thảo và Hoàn thiện nội dung Module 11:**
  - Viết chi tiết toàn bộ nội dung tệp [011_Module_11.tex](file:///d:/LaTeX/QuantsLV1_2027/001_Module/004_regression_and_data_science/011_Module_11.tex) bám sát mục tiêu học tập (LOS a).
  - Phân tích chi tiết lý thuyết về Big Data, 4 Vs (Volume, Velocity, Variety, Veracity), nguồn Alternative Data (Individuals, Business Processes, Sensors/IoT), các thử thách của Big Data.
  - Giải thích Financial Data Science, các đặc tính riêng của dữ liệu tài chính (độ nhiễu, phi tĩnh, đuôi béo, phi tuyến - Copulas và Neural Networks, dữ liệu thưa thớt).
  - Phân tích cơ chế Machine Learning & AI, phân tách tập dữ liệu (huấn luyện, xác thực, kiểm thử) và kỹ thuật kiểm thử cho chuỗi thời gian (time-based, rolling-window).
  - Trình bày 4 phương thức học máy (Supervised, Unsupervised, Reinforcement, Deep Learning) dưới dạng bảng biểu `booktabs`.
  - Phân tích mạng nơ-ron (Forward pass, Backpropagation, Gradient descent, epochs), mạng GANs/VAEs, NLP & ứng dụng tài chính (sắc thái báo cáo, tuyên bố ngân hàng trung ương), LLMs (transformers, huấn luyện song miền, rủi ro ảo giác/sai số) và Generative AI.
  - Soạn thảo 8 câu hỏi trắc nghiệm tiếng Anh bám sát cấu trúc CFA kèm lời giải chi tiết tiếng Việt.
- **Biên dịch & Xác thực PDF:**
  - Biên dịch thành công dự án lên **189 trang** bằng `latexmk` mà không gặp bất kỳ lỗi cú pháp nào. Tệp PDF kết quả lưu tại [005_product/QuantsLV1_2027.pdf](file:///d:/LaTeX/QuantsLV1_2027/005_product/QuantsLV1_2027.pdf).
  - Tối ưu hóa chiều rộng các cột trong bảng `tab:ml_approaches` để tránh lỗi tràn lề trang (`Overfull \hbox`).

- **Quy hoạch học liệu (Phương án 1):**
  - Trích xuất toàn bộ các mục **Summary**, **Question Set**, và **Practice Problems & Solutions** từ Module 8, 9, 10, 11 ra khỏi các tệp gốc.
  - Sắp xếp và quy hoạch lại thành 3 chương phụ lục mới độc lập đặt ở cuối tài liệu:
    - [012_Summaries.tex](file:///d:/LaTeX/QuantsLV1_2027/001_Module/005_final_appendices/012_Summaries.tex) (Tóm tắt bài học).
    - [013_Question_Sets.tex](file:///d:/LaTeX/QuantsLV1_2027/001_Module/005_final_appendices/013_Question_Sets.tex) (Câu hỏi củng cố).
    - [014_Practice_Problems_and_Solutions.tex](file:///d:/LaTeX/QuantsLV1_2027/001_Module/005_final_appendices/014_Practice_Problems_and_Solutions.tex) (Bài tập ôn tập và Lời giải).
  - Cập nhật tệp [QuantsLV1_2027.tex](file:///d:/LaTeX/QuantsLV1_2027/QuantsLV1_2027.tex) để load các chương mới, tổng độ dài tài liệu PDF đạt **195 trang**.
  - Đã khắc phục triệt để cảnh báo trùng lặp nhãn (`multiply-defined labels`) bằng cách đổi tiền tố nhãn các câu hỏi trong phụ lục thành `app_` và cập nhật các liên kết dẫn hướng tương ứng.

### 2. Danh sách Git Commits trong phiên
- Bổ sung bảng Matrix Mapping trực quan (Bảng 2.1) phân loại Price Return và Capital Distribution Return của từng loại tài sản/chỉ báo.
  - Khắc phục các lỗi hiển thị Learning Outcomes bằng cách định dạng chính xác vị trí hiển thị bảng LOS.
  - Xử lý triệt để cảnh báo `overfull/underfull hbox` bằng cách sử dụng các hàng lồng cột (nested tabular) trong tiêu đề bảng biểu và thu nhỏ tỷ lệ cột.
- **Git Push:** Pushed commit `21a1b28` lên master.

### 2. Danh sách Git Commits trong phiên
- `21a1b28` Format and restructure CFA 2027 Module 2 LaTeX chapter, integrate return type matrix mapping

### 3. Đề xuất cải tiến & Kế hoạch phiên tiếp theo (Next Session Plan)
- **Đề xuất cải tiến:**
  - *Cải tiến 1:* Tạo ra các bảng biểu chuẩn hóa cho phần so sánh Money-Weighted và Time-Weighted Returns ở Module 3 để học viên dễ nắm bắt bản chất (Đã hoàn thành).
- **Kế hoạch phiên tiếp theo (Phiên làm việc 03):**
  - Đã chuyển giao và hoàn thành trong phiên 3.

---

## 📅 Phiên làm việc 03: Tối ưu hóa Khoảng trắng & Biên soạn Module 3
*Thời gian hoàn thành: 15/06/2026 (Phiên sáng)*

### 1. Báo cáo công việc đã hoàn thành (Completed Tasks)
- **Biên soạn Module 3:**
  - Soạn thảo nội dung hoàn chỉnh cho `003_Module_3.tex` về Benchmarking Returns (Money-Weighted Return, Time-Weighted Return, Index Weighting).
  - Tích hợp 2 biểu đồ minh họa `exhibit_7.png` và `exhibit_15.png`.
- **Khắc phục triệt để lỗi khoảng trắng kéo giãn (Page stretching):**
  - Cấu hình lệnh toàn cục `\raggedbottom` tại `QuantsLV1_2027.tex` để ngăn LaTeX tự động giãn khoảng cách dòng/đoạn văn bất hợp lý khi trang chưa đầy.
  - Thay thế thuộc tính định vị tuyệt đối `[H]` bằng `[!htbp]` linh hoạt cho các đối tượng float lớn (hình ảnh và bảng biểu) trong toàn bộ các Module 1, 2 và 3 để tránh việc đứt gãy trang tạo ra các khoảng trống lớn.
  - Biên dịch và xác thực thành công file PDF không còn lỗi co giãn khoảng trắng.

---

## 📅 Phiên làm việc 04: Biên soạn & Tích hợp Hình ảnh Module 4
*Thời gian hoàn thành: 15/06/2026 (Phiên chiều)*

### 1. Báo cáo công việc đã hoàn thành (Completed Tasks)
- **Soạn thảo và Hoàn thiện nội dung Module 4:**
  - Hoàn thành nội dung của `004_Module_4.tex` (The Time Value of Money in Finance) đáp ứng tất cả các Learning Outcomes (TVM trong Fixed Income & Equity, Suất sinh lời/Hệ số tăng trưởng ngầm định, Cộng dồn dòng tiền và Định giá Quyền chọn).
  - Áp dụng các quy chuẩn thiết kế: tcolorbox compact (`before/after skip=6pt, breakable`), lời giải thích in nghiêng xanh dương của giảng viên.
- **Tích hợp hình ảnh minh họa:**
  - Tạo thư mục hình ảnh `002_figs/004_Module_4` chứa 16 tệp hình ảnh placeholder từ logo Trustville.
  - Khai báo 16 hình ảnh tương ứng (`exhibit_1` đến `exhibit_22`) trong file `.tex` để tăng tính trực quan.
  - Định vị toàn bộ các khối `figure` ở lớp ngoài (outer par mode), tránh lồng ghép bên trong các hộp `tcolorbox` để ngăn ngừa lỗi biên dịch LaTeX.
- **Biên dịch & Kiểm tra PDF:**
  - Biên dịch thành công dự án bằng `latexmk` lên 57 trang, không phát sinh lỗi cú pháp hay lỗi nhóm box. PDF thành phẩm được lưu tại `005_product/QuantsLV1_2027.pdf`.

### 2. Đề xuất cải tiến & Kế hoạch phiên tiếp theo (Next Session Plan)
- **Kế hoạch phiên tiếp theo (Phiên làm việc 05):**
  - Thực hiện dọn dẹp và rà soát định dạng Module 5, 6, 7 (Đã hoàn thành).

---

## 📅 Phiên làm việc 05: Dọn dẹp Workspace & Chuẩn hóa Định dạng Module 5, 6, 7
*Thời gian hoàn thành: 24/06/2026*

### 1. Báo cáo công việc đã hoàn thành (Completed Tasks)
- **Dọn dẹp & Phân loại file hệ thống:**
  - Xóa bỏ các tệp rác trung gian sinh ra trong quá trình biên dịch ở thư mục gốc (.aux, .log, .pdf, .toc, v.v.).
  - Tạo thư mục [000_references/text_dumps/](file:///d:/LaTeX/QuantsLV1_2027/000_references/text_dumps) và di chuyển toàn bộ 15 tệp `.txt` tạm/nháp vào đây để trả lại sự ngăn nắp cho thư mục gốc.
- **Rà soát & Chuẩn hóa định dạng Modules 5, 6, 7:**
  - **Module 5:** Chuyển đổi Bảng 5.1 và 5.3 sang cột định kích thước cố định (`p{...}`).
  - **Module 6:** Kích hoạt (uncomment) các lời giảng viên in nghiêng màu xanh dương ở các dòng đầu và dòng 66; chuyển đổi các Bảng 6.2, 6.3, 6.8, 6.9, 6.10 sang cột định kích thước cố định.
  - **Module 7:** Chuyển đổi các Bảng 7.2, 7.5, 7.7, 7.8 sang cột định kích thước cố định.
- **Biên dịch & Xác thực:**
  - Chạy biên dịch thành công tài liệu thông qua `latexmk` lên 112 trang. PDF đầu ra tại [005_product/QuantsLV1_2027.pdf](file:///d:/LaTeX/QuantsLV1_2027/005_product/QuantsLV1_2027.pdf) được cập nhật chính xác và hiển thị đẹp mắt.

### 2. Đề xuất cải tiến & Kế hoạch phiên tiếp theo (Next Session Plan)
- **Kế hoạch phiên tiếp theo (Phiên làm việc 06):**
  - Triển khai viết nội dung chi tiết cho **Module 8: The Return and Risk of a Financial Portfolio** ([008_Module_8.tex](file:///d:/LaTeX/QuantsLV1_2027/001_Module/003_inference_and_portfolios/008_Module_8.tex)) bám sát các LOS (a, b, c).

---

## 📅 Phiên làm việc 06: Chuẩn hóa, Dịch Thuật & Cắt Ảnh Đồ Thị Module 8
*Thời gian hoàn thành: 25/06/2026*

### 1. Báo cáo công việc đã hoàn thành (Completed Tasks)
- **Chuẩn hóa đồ thị (Figure Cropping):**
  - Tự động hóa việc cắt lề và loại bỏ các phần chữ thừa xung quanh toàn bộ 15 đồ thị trong `002_figs/008_Module_8/` bằng script Pillow.
  - Thay thế các tệp ảnh gốc bằng các phiên bản đã cắt sát phần đồ thị để đảm bảo tính mỹ thuật.
- **Biên dịch dịch thuật và Bổ sung Hướng dẫn bấm máy tính:**
  - Dịch toàn bộ lời giải thích của các ví dụ (Example 1-13, 14, 15, 17), bộ câu hỏi ôn tập (Question Sets 1-3), và 10 bài tập thực hành (Practice Problems) sang tiếng Việt học thuật, giữ nguyên văn bản tiếng Anh của đề bài.
  - Bổ sung hướng dẫn bấm máy tính tài chính Texas Instruments BA II Plus chi tiết cho các phép toán phức tạp (như tính tỷ suất sinh lời trung bình hình học và độ lệch chuẩn).
- **Lược bỏ đường kẻ dọc trong bảng biểu:**
  - Loại bỏ hoàn toàn tất cả các đường kẻ dọc (`|`) trong toàn bộ các bảng biểu của Module 8 (Bảng LOS, Bảng 8.1, bảng dữ liệu ví dụ/bài tập) để tuân thủ thiết kế `booktabs` hiện đại và sạch sẽ.
- **Làm phong phú Ghi chú Giảng viên (Teacher Notes):**
  - Thêm mới và nâng cấp các ghi chú giảng viên màu xanh dương in nghiêng sử dụng đại từ chung "Chúng ta" kèm các câu hỏi gợi mở tư duy (ví dụ: so sánh bản chất rủi ro giữa CML và SML, ý nghĩa của Global MVP).
- **Biên dịch & Sửa lỗi cú pháp:**
  - Phát hiện và sửa lỗi thiếu ký tự đóng mở công thức toán học `$` trong lời giải bài tập 8.
  - Biên dịch thành công tài liệu lên 140 trang thông qua `latexmk` mà không gặp bất kỳ lỗi cú pháp nào. PDF thành phẩm đạt chất lượng xuất bản cao nhất.

### 2. Đề xuất cải tiến & Kế hoạch phiên tiếp theo (Next Session Plan)
- **Kế hoạch phiên tiếp theo:**
  - Tiến hành viết tiếp và biên dịch **Module 9** bám sát quy chuẩn LaTeX và rà soát ảnh đồ thị tương tự.

---

## 📅 Phiên làm việc 07: Tối ưu hóa Dung lượng trang qua việc Rút ngắn Ghi chú Giảng viên
*Thời gian hoàn thành: 25/06/2026 (Phiên chiều)*

### 1. Báo cáo công việc đã hoàn thành (Completed Tasks)
- **Rút gọn 56 Ghi chú Giảng viên:**
  - Viết lại toàn bộ 56 ghi chú của giảng viên (màu xanh dương in nghiêng) trên các file từ Module 1 đến Module 8 để tối giản từ ngữ, loại bỏ các từ đệm xã giao dư thừa nhưng vẫn giữ nguyên đại từ "Chúng ta" và các câu hỏi gợi mở cốt lõi.
  - Sửa lỗi cú pháp tại comment ID 46 (phần chứng minh phân phối Logistic trong `006_Module_6.tex`) bằng cách bọc chính xác các lệnh toán học `\text{Var}`, `\frac` và phương trình vào trong môi trường toán học inline `$ ... $`.
- **Tự động hóa thay thế:**
  - Triển khai thành công mã nguồn Python `replace_comments_by_order.py` để tự động hóa việc rà soát và thay thế chuẩn xác toàn bộ 56 ghi chú giảng viên theo thứ tự xuất hiện của các file.
- **Biên dịch & Xác thực PDF:**
  - Biên dịch dự án hoàn chỉnh sang PDF thông qua `latexmk` một cách trơn tru, không có bất kỳ cảnh báo/lỗi biên dịch nào.
  - Tải và lưu trữ PDF thành phẩm tại [005_product/QuantsLV1_2027.pdf](file:///d:/LaTeX/QuantsLV1_2027/005_product/QuantsLV1_2027.pdf).
  - **Kết quả giảm trang:** Tổng số trang của tài liệu đã được giảm thành công từ **140 trang xuống còn 138 trang** (giảm 2 trang) hoàn toàn sạch sẽ, không thay đổi bất kỳ tỷ lệ hình ảnh, cỡ chữ hay căn lề nào của định dạng tài liệu gốc.

### 2. Đề xuất cải tiến & Kế hoạch phiên tiếp theo (Next Session Plan)
- **Kế hoạch phiên tiếp theo:**
  - Tiếp tục phát triển và hoàn thiện **Module 9: Simple Linear Regression in Finance** ([009_Module_9.tex](file:///d:/LaTeX/QuantsLV1_2027/001_Module/003_inference_and_portfolios/009_Module_9.tex)). (Đã hoàn thành trong phiên 8)

---

## 📅 Phiên làm việc 08: Rút gọn & Tối ưu hóa Module 9
*Thời gian hoàn thành: 27/06/2026*

### 1. Báo cáo công việc đã hoàn thành (Completed Tasks)
- **Phục hồi & Đồng bộ Module 9:**
  - Trích xuất thành công các đoạn mã nguồn dựng trang từ tệp lịch sử để khôi phục cấu trúc ban đầu của [009_Module_9.tex](file:///d:/LaTeX/QuantsLV1_2027/001_Module/003_inference_and_portfolios/009_Module_9.tex) (1,719 dòng) bị mất do thao tác kiểm kho trước đó.
- **Rút gọn văn bản chương tối đa:**
  - Áp dụng thành công 25 khối thay thế để làm cô đọng các phần văn bản lý thuyết và ghi chú giảng viên dài dòng.
  - Dung lượng tệp nguồn `.tex` giảm từ **113KB xuống còn 75KB** (giảm khoảng **33%**).
  - Đảm bảo giữ nguyên các phần toán lý thuyết, bảng biểu, các bộ câu hỏi ôn tập (Question Sets 1-3) và lời giải chi tiết có hướng dẫn máy tính tài chính Texas Instruments BA II Plus.
- **Vá lỗi và Biên dịch dự án:**
  - Sửa lỗi cú pháp liên quan đến ký tự `\n` đặc biệt xuất hiện tại các dòng 58 và 702 trong tệp LaTeX.
  - Biên dịch toàn bộ tài liệu thành công đạt **170 trang** bằng `latexmk` mà không gặp bất kỳ lỗi cảnh báo hay lỗi cú pháp nào. Tệp PDF kết quả được lưu trữ tại [005_product/QuantsLV1_2027.pdf](file:///d:/LaTeX/QuantsLV1_2027/005_product/QuantsLV1_2027.pdf).
- **Dọn dẹp tệp rác hệ thống:**
  - Xóa bỏ toàn bộ các script tạm thời và các file txt hỗ trợ trong quá trình tối ưu để khôi phục trạng thái sạch sẽ cho thư mục làm việc.

### 2. Kế hoạch phiên tiếp theo (Next Session Plan)
- **Kế hoạch phiên tiếp theo:**
  - Bắt đầu triển khai và tối ưu hóa nội dung cho **Module 10: Applications of Simple Linear Regression in Finance** ([010_Module_10.tex](file:///d:/LaTeX/QuantsLV1_2027/001_Module/004_regression_and_data_science/010_Module_10.tex)). (Đã hoàn thành trong phiên 9)

---

## 📅 Phiên làm việc 09: Thiết kế & Biên soạn Module 10
*Thời gian hoàn thành: 29/06/2026*

### 1. Báo cáo công việc đã hoàn thành (Completed Tasks)
- **Đồng bộ và Commit thay đổi cũ:**
  - Commit toàn bộ các thay đổi chưa staged từ Phiên làm việc 08 liên quan đến Module 9 (`c955481`) để làm sạch kho mã nguồn làm việc.
- **Trích xuất và Xử lý hình ảnh đồ thị:**
  - Kết xuất (render) thành công các trang PDF chứa hình ảnh vector.
  - Sử dụng script Python `crop_all_images.py` để tự động cắt và lưu chính xác 5 đồ thị chất lượng cao dạng PNG vào thư mục `002_figs/010_Module_10/` (đặt tên: `10.1-Nonlinear.png`, `10.2-Interest vs Inflation.png`, `10.3-Residual Plots.png`, `10.4-Quarterly Rev vs Time.png`, `10.5-Residual Quarterly Rev vs Time.png`).
- **Soạn thảo và Hoàn thiện nội dung Module 10:**
  - Hoàn thành nội dung tệp `010_Module_10.tex` đáp ứng toàn bộ các mục tiêu học tập (LOS a, b, c, d).
  - Biên soạn lý thuyết chi tiết về ước lượng OLS, 5 giả định quan trọng của OLS, cách đọc bảng phân tích phương sai ANOVA (FIRN AG), khoảng dự báo (Prediction Interval), các dạng hàm phi tuyến Log-Lin, Lin-Log, Log-Log và ứng dụng CAPM thực tế (LVMH so với chỉ số CAC 40).
  - Tích hợp ghi chú giảng viên màu xanh dương in nghiêng và các tcolorbox bài tập/ví dụ có thuộc tính `breakable`.
- **Biên dịch & Xác thực PDF:**
  - Biên dịch thành công dự án lên **181 trang** bằng `latexmk` mà không gặp bất kỳ lỗi cú pháp nào. Tài liệu PDF kết quả lưu tại [005_product/QuantsLV1_2027.pdf](file:///d:/LaTeX/QuantsLV1_2027/005_product/QuantsLV1_2027.pdf).

### 2. Danh sách Git Commits trong phiên
- `c955481` feat(quants): sync and optimize Module 9, update session log for Session 8
- `2479676` feat(quants): implement Module 10 regression, extract figures, clean build

### 3. Đề xuất cải tiến & Kế hoạch phiên tiếp theo (Next Session Plan)
- **Kế hoạch phiên tiếp theo:**
  - Triển khai và tối ưu hóa nội dung cho **Module 11: Introduction to Financial Data Science** ([011_Module_11.tex](file:///d:/LaTeX/QuantsLV1_2027/001_Module/004_regression_and_data_science/011_Module_11.tex)). (Đã hoàn thành trong phiên 10)

---

## 📅 Phiên làm việc 10: Biên soạn & Hoàn thiện Module 11
*Thời gian hoàn thành: 29/06/2026*

### 1. Báo cáo công việc đã hoàn thành (Completed Tasks)
- **Chuẩn hóa định dạng Learning Outcomes:**
  - Định cấu hình lại các bảng Học tập ở cấp độ mục (`\section`) trong Module 9 và Module 10 để loại bỏ hoàn toàn tiêu đề "LEARNING OUTCOMES" và các đường kẻ ngang, đồng thời đồng bộ hóa dấu phân cách cột `|` như yêu cầu của Giảng viên.
- **Trích xuất và Xử lý hình ảnh đồ thị cho Module 11:**
  - Sử dụng script Python `crop_m11_images.py` để trích xuất 3 sơ đồ minh họa chất lượng cao trực tiếp từ PDF gốc vào [002_figs/011_Module_11/](file:///d:/LaTeX/QuantsLV1_2027/002_figs/011_Module_11/):
    - `11.1-Big Data Characteristics.png` (Đặc tính 3Vs của Big Data).
    - `11.2-Time vs Rolling.png` (Time-Based Split vs Rolling-Window Validation).
    - `11.3-Neural Network.png` (Mạng Nơ-ron Nhân tạo).
- **Soạn thảo và Hoàn thiện nội dung Module 11:**
  - Viết chi tiết toàn bộ nội dung tệp [011_Module_11.tex](file:///d:/LaTeX/QuantsLV1_2027/001_Module/004_regression_and_data_science/011_Module_11.tex) bám sát mục tiêu học tập (LOS a).
  - Phân tích chi tiết lý thuyết về Big Data, 4 Vs (Volume, Velocity, Variety, Veracity), nguồn Alternative Data (Individuals, Business Processes, Sensors/IoT), các thử thách của Big Data.
  - Giải thích Financial Data Science, các đặc tính riêng của dữ liệu tài chính (độ nhiễu, phi tĩnh, đuôi béo, phi tuyến - Copulas và Neural Networks, dữ liệu thưa thớt).
  - Phân tích cơ chế Machine Learning & AI, phân tách tập dữ liệu (huấn luyện, xác thực, kiểm thử) và kỹ thuật kiểm thử cho chuỗi thời gian (time-based, rolling-window).
  - Trình bày 4 phương thức học máy (Supervised, Unsupervised, Reinforcement, Deep Learning) dưới dạng bảng biểu `booktabs`.
  - Phân tích mạng nơ-ron (Forward pass, Backpropagation, Gradient descent, epochs), mạng GANs/VAEs, NLP & ứng dụng tài chính (sắc thái báo cáo, tuyên bố ngân hàng trung ương), LLMs (transformers, huấn luyện song miền, rủi ro ảo giác/sai số) và Generative AI.
  - Soạn thảo 8 câu hỏi trắc nghiệm tiếng Anh bám sát cấu trúc CFA kèm lời giải chi tiết tiếng Việt.
- **Biên dịch & Xác thực PDF:**
  - Biên dịch thành công dự án lên **189 trang** bằng `latexmk` mà không gặp bất kỳ lỗi cú pháp nào. Tệp PDF kết quả lưu tại [005_product/QuantsLV1_2027.pdf](file:///d:/LaTeX/QuantsLV1_2027/005_product/QuantsLV1_2027.pdf).
  - Tối ưu hóa chiều rộng các cột trong bảng `tab:ml_approaches` để tránh lỗi tràn lề trang (`Overfull \hbox`).

- **Quy hoạch học liệu (Phương án 1):**
  - Trích xuất toàn bộ các mục **Summary**, **Question Set**, và **Practice Problems & Solutions** từ Module 8, 9, 10, 11 ra khỏi các tệp gốc.
  - Sắp xếp và quy hoạch lại thành 3 chương phụ lục mới độc lập đặt ở cuối tài liệu:
    - [012_Summaries.tex](file:///d:/LaTeX/QuantsLV1_2027/001_Module/005_final_appendices/012_Summaries.tex) (Tóm tắt bài học).
    - [013_Question_Sets.tex](file:///d:/LaTeX/QuantsLV1_2027/001_Module/005_final_appendices/013_Question_Sets.tex) (Câu hỏi củng cố).
    - [014_Practice_Problems_and_Solutions.tex](file:///d:/LaTeX/QuantsLV1_2027/001_Module/005_final_appendices/014_Practice_Problems_and_Solutions.tex) (Bài tập ôn tập và Lời giải).
  - Cập nhật tệp [QuantsLV1_2027.tex](file:///d:/LaTeX/QuantsLV1_2027/QuantsLV1_2027.tex) để load các chương mới, tổng độ dài tài liệu PDF đạt **195 trang**.
  - Đã khắc phục triệt để cảnh báo trùng lặp nhãn (`multiply-defined labels`) bằng cách đổi tiền tố nhãn các câu hỏi trong phụ lục thành `app_` và cập nhật các liên kết dẫn hướng tương ứng.

### 2. Danh sách Git Commits trong phiên
- `cc9fa81` style(quants): standardize section-level learning outcomes format in Module 9 and 10
- `f187e84` style(quants): add vertical separator | to all learning outcomes tables in Module 8, 9, 10
- `8b552be` feat(quants): implement Module 11 data science, extract figures, resolve table layout (Phiên bản amend: `8b552be`)
- `1806183` refactor(quants): move Summaries, Question Sets, and Problems to final appendices

### 3. Đề xuất cải tiến & Kế hoạch phiên tiếp theo (Next Session Plan)
- **Kế hoạch phiên tiếp theo:**
  - Di chuyển các bài tập tự luyện của Module 1-7 sang phụ lục chuyên biệt (Đã hoàn thành trong phiên 11).

---

## 📅 Phiên làm việc 11: Di chuyển Bài tập thực hành Modules 1-7 & Chuẩn hóa
*Thời gian hoàn thành: 30/06/2026*

### 1. Báo cáo công việc đã hoàn thành (Completed Tasks)
- **Di chuyển & Chuẩn hóa bài tập ôn tập:**
  - Di chuyển thành công các bài tập ôn tập mẫu của Module 1, 2, 3, 4, và 5 từ tệp nháp `012_Practice.tex` vào tệp phụ lục chuyên biệt [014_Practice_Problems_and_Solutions.tex](file:///d:/LaTeX/QuantsLV1_2027/001_Module/005_final_appendices/014_Practice_Problems_and_Solutions.tex).
  - Dịch nghĩa và bổ sung phần giải thích tiếng Việt in nghiêng màu xanh dương (`\textcolor{blue}{\textit{...}}`) cho tất cả lời giải của các bài tập di chuyển.
- **Biên soạn mới bài tập bổ trợ:**
  - Biên soạn mới 2 bài tập cho Module 6 (độc lập, nhị thức và định lý Bayes) kèm lời giải chi tiết tiếng Việt.
  - Biên soạn mới 2 bài tập cho Module 7 (khoảng tin cậy dùng phân phối t và sai lầm Loại I/II trong kiểm định giả thuyết) kèm lời giải chi tiết tiếng Việt.
  - Khai báo các nhãn tham chiếu thích hợp ở đầu mỗi mục bài tập trong phụ lục để liên kết trực tiếp với các lệnh `\pageref` từ các Module tương ứng.
- **Hợp nhất Phụ lục Ôn tập & Thực hành:**
  - Hợp nhất thành công ba phần: Tóm tắt bài học (Summaries), Câu hỏi củng cố (Question Sets) và Bài tập ôn tập (Practice Problems) vào một tệp phụ lục hợp nhất duy nhất [012_Review_and_Practice.tex](file:///d:/LaTeX/QuantsLV1_2027/001_Module/005_final_appendices/012_Review_and_Practice.tex) dưới tiêu đề `\chapter{Tài liệu ôn tập và thực hành (Review and Practice Materials)}`.
  - Cập nhật định dạng phân cấp tiêu đề LaTeX (hạ từ `\chapter` $\rightarrow$ `\section` $\rightarrow$ `\subsection` $\rightarrow$ `\subsubsection`) để đảm bảo cấu trúc văn bản thống nhất mà không phá vỡ bất kỳ nhãn tham chiếu ngược nào.
- **Dọn dẹp & Xác thực:**
  - Xóa bỏ hoàn toàn tệp nháp cũ `001_Module/012_Practice.tex` và 3 file phụ lục cũ.
  - Biên dịch thành công dự án lên **209 trang** qua `latexmk` mà không gặp bất kỳ cảnh báo nào về các tham chiếu chưa định nghĩa (`undefined references`) hay lỗi hiển thị mục lục. PDF thành phẩm được cập nhật đầy đủ tại [005_product/QuantsLV1_2027.pdf](file:///d:/LaTeX/QuantsLV1_2027/005_product/QuantsLV1_2027.pdf).

### 2. Danh sách Git Commits trong phiên
- `ae8ce3f` refactor(quants): migrate Module 1-7 practice problems, add Module 6-7 problems, resolve references
- `d570875` refactor(quants): merge separate review appendices into a single appendix

### 3. Đề xuất cải tiến & Kế hoạch phiên tiếp theo (Next Session Plan)
- **Kế hoạch phiên tiếp theo:**
  - Rà soát toàn diện văn phong học thuật tiếng Việt và kiểm tra hiển thị hình ảnh trên toàn bộ tài liệu PDF.
