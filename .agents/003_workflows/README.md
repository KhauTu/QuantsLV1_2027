# Quy Trình Làm Việc & Mô Hình Cộng Tác (Workflows & Collaboration Models)

Tài liệu này định nghĩa các **Mô hình làm việc hiệu quả** giữa Giảng viên Trustville và AI Agent, đồng thời tổng hợp các quy trình làm việc chi tiết từng bước được lưu trữ dưới dạng các tệp `.md` được đánh số.

---

## 1. Gợi ý các Mô hình làm việc hiệu quả (Recommended Collaboration Models)

Để tối ưu hóa thời gian soạn bài giảng của Giảng viên và tận dụng tối đa năng lực lập trình/dịch thuật của AI, chúng ta sẽ áp dụng 3 mô hình làm việc chính tùy thuộc vào trạng thái của bài học:

### 💡 Mô hình A: "Phác thảo từ Ý tưởng thô" (Drafting from Scratch)
*Áp dụng khi Giảng viên chuẩn bị viết một chủ đề hoàn toàn mới hoặc chưa có cấu trúc LaTeX.*
1. **Bước 1 (Giảng viên):** Gửi các gạch đầu dòng ý tưởng chính bằng tiếng Việt và copy đoạn văn bản tiếng Anh tương ứng từ CFA Curriculum (nếu có).
2. **Bước 2 (Agent):** Xây dựng dàn ý chi tiết (Outline) bao gồm:
   - Cách tổ chức các đề mục (Section/Subsection).
   - Phần toán học cần chứng minh (ở mức độ phổ thông).
   - Đề xuất câu hỏi gợi mở của giảng viên (Blue Italic) và nội dung đóng khung Exam Tips.
3. **Bước 3 (Thảo luận & Phê duyệt):** Giảng viên đánh giá dàn ý, yêu cầu tăng/giảm độ khó hoặc đổi ví dụ.
4. **Bước 4 (Triển khai):** Sau khi giảng viên duyệt, Agent tiến hành viết code LaTeX hoàn chỉnh vào file Module tương ứng và chạy compile kiểm tra.

### 🔍 Mô hình B: "Đồng nghiệp kiểm duyệt & Tối ưu" (Review & Refine)
*Áp dụng khi Giảng viên đã tự soạn thảo trước mã nguồn LaTeX nhưng cần kiểm tra chất lượng.*
1. **Bước 1 (Giảng viên):** Gửi file LaTeX hoặc chỉ định file cần rà soát.
2. **Bước 2 (Agent):** Chạy quy trình **`002_review_content`** để:
   - Kiểm tra lỗi cú pháp LaTeX (thiếu dấu `$`, sai thẻ đóng ngoặc).
   - Tối ưu hóa bảng biểu sang dạng `booktabs` (không dòng kẻ dọc).
   - Rà soát tính chính xác của công thức toán học và các bước bấm máy BA II Plus.
3. **Bước 3 (Agent đề xuất):** Đưa ra các gợi ý thay đổi cụ thể (diff block) kèm theo lý do để giảng viên duyệt.

### 📋 Mô hình C: "Đối chiếu và Đảm bảo chất lượng CFA" (Curriculum Alignment Audit)
*Áp dụng trước khi xuất bản một Module hoàn chỉnh để đảm bảo học viên không bị thiếu kiến thức thi.*
1. **Bước 1 (Agent):** Đối chiếu danh sách các mục tiêu học tập (Learning Outcomes Statements - LOS) của CFA 2027 với nội dung thực tế trong Module.
2. **Bước 2 (Agent):** Phát hiện và cảnh báo nếu có phần kiến thức trọng tâm nào của CFA bị bỏ sót hoặc chưa giải thích đủ sâu.
3. **Bước 3 (Giảng viên & Agent):** Bổ sung phần thiếu sót thông qua Mô hình A.

---

## 2. Danh sách các Quy trình Chi tiết (Workflow Documents)

Để xem hướng dẫn chi tiết cho từng tác vụ, vui lòng mở các tệp tin tương ứng:

1. **[001_publish_module.md](file:///d:/LaTeX/QuantsLV1_2027/.agents/003_workflows/001_publish_module.md)**: Quy trình soạn thảo, kiểm tra cấu trúc, định dạng và xuất bản một Module kiến thức mới hoặc cập nhật.
2. **[002_review_content.md](file:///d:/LaTeX/QuantsLV1_2027/.agents/003_workflows/002_review_content.md)**: Quy trình rà soát học thuật (chứng minh toán, tính toán, kiểm tra bước bấm máy BA II Plus, kiểm tra tính tương tác của lời giảng).
3. **[003_release_pdf.md](file:///d:/LaTeX/QuantsLV1_2027/.agents/003_workflows/003_release_pdf.md)**: Quy trình đóng gói, kiểm tra hiển thị visual của PDF, dọn dẹp cache và phát hành tài liệu PDF phiên bản Trustville.
