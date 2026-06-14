# Bản Đồ Tham Chiếu Công Thức & Hình Ảnh Minh Họa

Tài liệu này quản lý danh sách hình ảnh minh họa và quy chuẩn đánh số/tham chiếu công thức toán học trong dự án để phục vụ việc rà soát học thuật.

---

## 1. Quy chuẩn Đánh số & Tham chiếu Công thức (Math Referencing Rules)

Để phục vụ việc kiểm duyệt (review) và đối chiếu chéo với tài liệu gốc:
- **Nguyên tắc:** 
  1. Tất cả các công thức toán học độc lập quan trọng bắt buộc phải nằm trong môi trường đánh số của LaTeX (`\begin{equation}` hoặc `\begin{alignedat}`).
  2. Ngay bên dưới công thức trong file `.tex` nguồn, Agent phải chèn một dòng chú thích `% Reference:` ghi rõ chương, phần và số trang của CFA Curriculum 2027 gốc.
- **Cú pháp ví dụ:**
  ```latex
  \begin{equation}
  PV = \frac{FV}{(1 + r)^n}
  \label{eq:pv_discounting}
  \end{equation}
  % Reference: CFA Curriculum 2027, Vol 1, Module 4: Time Value of Money, Section 1.2
  ```

---

## 2. Bản đồ Hình ảnh Minh họa trong dự án (Figure Mapping Table)

Dưới đây là danh sách toàn bộ hình ảnh minh họa hiện có trong `002_figs/` được gom nhóm theo từng Module và vị trí đề xuất chèn vào mã nguồn LaTeX:

### 001_returns_and_measures (Module 1, 2, 3)

| Tên tệp tin hình ảnh | Mô tả nội dung đồ thị | Module chèn | Vị trí đề xuất chèn trong mã nguồn |
| :--- | :--- | :--- | :--- |
| `002_figs/001_Module_1/exhibit_10.png` | Bảng mô tả tác động của tần suất ghép lãi (Compounding) | **Module 1** | Mục *Continuous Compounding* (phần so sánh ghép lãi rời rạc vs liên tục) |
| `002_figs/001_Module_1/exhibit_13.png` | Đồ thị cấu thành tỷ suất sinh lời yêu cầu (Required Rate of Return) | **Module 1** | Mục *The Required Rate of Return* (sơ đồ cấu thành và Risk Premia) |
| `002_figs/001_Module_1/exhibit_16.png` | Biểu đồ cột biểu diễn quan hệ Total Return vs Gross Return vs Net Return | **Module 1** | Mục *Gross and Net Return* (mô tả sự xói mòn do chi phí/phí quản lý) |
| `002_figs/001_Module_1/exhibit_18.png` | Đồ thị thể hiện mối quan hệ Payoff giữa cổ phiếu và quyền chọn (Leverage) | **Module 1** | Mục *Leveraged Returns* (đối chiếu suất sinh lời có đòn bẩy vs không đòn bẩy) |
| `002_figs/002_Module_2/exhibit_11.png` | Đồ thị cột biểu diễn quan hệ đánh đổi giữa Rủi ro và Tỷ suất sinh lời lịch sử (Risk-Return Trade-Off) | **Module 2** | Mục *The Risk-Return Trade-Off* (quan hệ giữa suất sinh lời bình quân và biến động) |
| `002_figs/003_Module_3/3.1-box and whisker.png` | Đồ thị hộp và râu (Box and Whisker Plot) | **Module 3** | Phần trực quan hóa thống kê mô tả |
| `002_figs/003_Module_3/3.2-Skewness.png` | So sánh đồ thị lệch trái, lệch phải và đối xứng | **Module 3** | Mục giải thích độ lệch (Skewness) |
| `002_figs/003_Module_3/3.3-Kurtosis.png` | Đồ thị ba loại độ nhọn (Lepto-, Platy-, Mesokurtic) | **Module 3** | Mục giải thích độ nhọn (Kurtosis) |
| `002_figs/003_Module_3/3.4-Scatter Plot.png` | Đồ thị phân tán biểu diễn mối quan hệ hai biến | **Module 3** | Mục trực quan hóa tương quan (Correlation) |

### 002_tvm_and_statistics (Module 4, 5, 6)

| Tên tệp tin hình ảnh | Mô tả nội dung đồ thị | Module chèn | Vị trí đề xuất chèn trong mã nguồn |
| :--- | :--- | :--- | :--- |
| `002_figs/004_Module_4/4.1-BankCorp Forecasted EPS.png` | Sơ đồ cây xác suất dự báo EPS BankCorp | **Module 4** | Phần ví dụ xác suất có điều kiện |
| `002_figs/004_Module_4/4.2-Bayes formula.png` | Sơ đồ cây áp dụng công thức Bayes | **Module 4** | Phần công thức Bayes |
| `002_figs/004_Module_4/4.3-Tree Map.png` | Tổng quan sơ đồ cây xác suất đầy đủ | **Module 4** | Phần giới thiệu sơ đồ cây (Probability Trees) |
| `002_figs/006_Module_6/6.1-lognormal.jpg` | Đồ thị so sánh phân phối Normal và Lognormal | **Module 6** | Mục giải thích phân phối Lognormal trong đầu tư |
| `002_figs/006_Module_6/6.2-Monte Carlo.png` | Sơ đồ quy trình mô phỏng Monte Carlo | **Module 6** | Mục giới thiệu phương pháp Monte Carlo |

### 003_inference_and_portfolios (Module 7, 8, 9)

| Tên tệp tin hình ảnh | Mô tả nội dung đồ thị | Module chèn | Vị trí đề xuất chèn trong mã nguồn |
| :--- | :--- | :--- | :--- |
| `002_figs/007_Module_7/6.3-Bootstrap.png` | Sơ đồ quy trình lấy mẫu lặp Bootstrap | **Module 7** | Mục phương pháp lấy mẫu phi tham số (Bootstrap) |
| `002_figs/007_Module_7/7.1-Probability Sampling.png` | Bản đồ phân loại các kỹ thuật lấy mẫu xác suất | **Module 7** | Mục giới thiệu phương pháp lấy mẫu (Sampling) |
| `002_figs/008_Module_8/8.1-Hypo Test Process.png` | Sơ đồ quy trình 7 bước kiểm định giả thuyết | **Module 8** | Phần giới thiệu quy trình kiểm định giả thuyết |

### 004_regression_and_data_science (Module 10, 11)

| Tên tệp tin hình ảnh | Mô tả nội dung đồ thị | Module chèn | Vị trí đề xuất chèn trong mã nguồn |
| :--- | :--- | :--- | :--- |
| `002_figs/010_Module_10/10.1-Nonlinear.jpg` | Đồ thị mối quan hệ phi tuyến giữa các biến | **Module 10** | Mục giới hạn của hồi quy tuyến tính đơn |
| `002_figs/010_Module_10/10.2-Interest vs Inflation.png` | Đường hồi quy thực tế giữa Lãi suất và Lạm phát | **Module 10** | Mục ví dụ thực tế về mô hình hồi quy tuyến tính |
| `002_figs/010_Module_10/10.3-Residual Plots.png` | Đồ thị phân tán của phần dư (Residual Plot) | **Module 10** | Mục kiểm tra giả định hồi quy (Residual Analysis) |
| `002_figs/010_Module_10/10.4-Quarterly Rev vs Time.png` | Đồ thị doanh thu theo quý biến động theo thời gian | **Module 10** | Mục phân tích hồi quy chuỗi thời gian |
| `002_figs/010_Module_10/10.5-Residual Quarterly Rev vs Time.png` | Đồ thị phần dư doanh thu theo quý theo thời gian | **Module 10** | Mục phân tích phần dư chuỗi thời gian |
