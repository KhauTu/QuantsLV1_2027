# Tra Cứu Thuật Ngữ & Công Thức CFA Quant (2027)

Tài liệu này hệ thống hóa các thuật ngữ và công thức cốt lõi của môn học **Quantitative Methods - CFA Level 1**. Sử dụng bảng này để đảm bảo dịch thuật tiếng Việt và ký hiệu LaTeX luôn đồng nhất.

---

## 1. Giá Trị Thời Gian Của Tiền (Time Value of Money - TVM)

| Thuật ngữ tiếng Anh | Dịch nghĩa tiếng Việt | Ký hiệu / Công thức LaTeX | Ghi chú |
| :--- | :--- | :--- | :--- |
| **Future Value (FV)** | Giá trị tương lai | `FV_n = PV(1 + r)^n` | Công thức cơ bản tích lũy lãi đơn/kép. |
| **Present Value (PV)** | Giá trị hiện tại | `PV = \frac{FV_n}{(1 + r)^n}` | Chiết khấu dòng tiền tương lai. |
| **Compounding Frequency** | Tần suất ghép lãi | `FV_n = PV \left(1 + \frac{r_s}{m}\right)^{m \times n}` | `m` là tần suất ghép lãi trong năm. |
| **Continuous Compounding** | Ghép lãi liên tục | `FV_n = PV \times e^{r \times n}` | Giới hạn khi `m \to \infty`. |
| **Stated Annual Interest Rate** | Lãi suất danh nghĩa năm | `r_s` | Chưa tính đến ghép lãi nhiều lần trong năm. |
| **Effective Annual Rate (EAR)** | Lãi suất hiệu dụng năm | `EAR = \left(1 + \frac{r_s}{m}\right)^m - 1` | Công thức tính lãi suất thực tế nhận được. |
| **Annuity** | Dòng tiền đều | - | Chia làm Dòng tiền đều cuối kỳ (Ordinary) và đầu kỳ (Annuity Due). |

---

## 2. Dòng Tiền & Đo Lường Suất Sinh Lời (Discounted Cash Flow & Return Measures)

| Thuật ngữ tiếng Anh | Dịch nghĩa tiếng Việt | Ký hiệu / Công thức LaTeX | Ghi chú |
| :--- | :--- | :--- | :--- |
| **Net Present Value (NPV)** | Giá trị hiện tại thuần | `NPV = \sum_{t=0}^{N} \frac{CF_t}{(1 + r)^t}` | Tiêu chuẩn ra quyết định đầu tư chính. |
| **Internal Rate of Return (IRR)** | Tỷ suất hoàn vốn nội bộ | `NPV = 0 \Rightarrow \sum_{t=0}^{N} \frac{CF_t}{(1 + \text{IRR})^t} = 0` | Mức lãi suất làm NPV của dự án bằng 0. |
| **Holding Period Return (HPR)** | Tỷ suất sinh lời thời kỳ nắm giữ | `HPR = \frac{P_{end} - P_{beg} + D}{P_{beg}}` | Tính cả chênh lệch giá và thu nhập cổ tức/tiền lãi. |
| **Money-Weighted Return** | Suất sinh lời bình quân gia quyền theo tiền | - | Thực chất là IRR tính trên toàn bộ dòng tiền của quỹ/tài khoản. |
| **Time-Weighted Return** | Suất sinh lời bình quân gia quyền theo thời gian | - | Tính bằng tích hình học của HPR các tiểu kỳ độc lập. |
| **Bank Discount Yield (BDY)** | Tỷ suất chiết khấu ngân hàng | `r_{BD} = \frac{D}{F} \times \frac{360}{t}` | Dùng cho T-bill, tính dựa trên mệnh giá `F` và năm 360 ngày. |
| **Holding Period Yield (HPY)** | Tỷ suất sinh lời kỳ nắm giữ | `HPY = \frac{F - P_0}{P_0}` | Suất sinh lời thực tế không chuẩn hóa theo năm. |
| **Money Market Yield (MMY)** | Tỷ suất thị trường tiền tệ | `r_{MM} = \frac{360 \times r_{BD}}{360 - (t \times r_{BD})}` | Hoặc `HPY \times \frac{360}{t}` (còn gọi là CD Equivalent Yield). |

---

## 3. Thống Kê Mô Tả (Descriptive Statistics)

- **Arithmetic Mean (Trung bình cộng):**
  $$\mu = \frac{\sum_{i=1}^{N} X_i}{N} \quad \text{hoặc} \quad \bar{X} = \frac{\sum_{i=1}^{n} X_i}{n}$$
- **Geometric Mean (Trung bình hình học):**
  $$R_G = \left[ \prod_{t=1}^{T} (1 + R_t) \right]^{\frac{1}{T}} - 1$$
- **Harmonic Mean (Trung bình điều hòa):**
  $$\bar{X}_H = \frac{N}{\sum_{i=1}^{N} \frac{1}{X_i}}$$
  *(Thường dùng để tính chi phí mua trung bình cho chiến lược dollar-cost averaging)*.
- **Variance (Phương sai):**
  $$\sigma^2 = \frac{\sum_{i=1}^{N} (X_i - \mu)^2}{N} \quad \text{(Tổng thể)} \quad s^2 = \frac{\sum_{i=1}^{n} (X_i - \bar{X})^2}{n - 1} \quad \text{(Mẫu)}$$
- **Standard Deviation (Độ lệch chuẩn):**
  $$s = \sqrt{s^2}$$
