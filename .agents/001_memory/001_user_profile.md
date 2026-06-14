# Thông Tin Cá Nhân & Phong Cách Làm Việc (User Profile)

*Tài liệu này ghi nhớ thông tin về phong cách tương tác và thói quen của bạn để Agent tối ưu hóa phản hồi.*

## 1. Thông tin cá nhân & Chuyên môn
- **Vai trò:** Giảng viên biên soạn tài liệu giảng dạy trực tiếp tại Trung tâm luyện thi CFA **Trustville** (trustville.vn).
- **Nền tảng chuyên môn:** CFA Charterholder, chuyên gia về quản trị rủi ro trong chứng khoán và đầu tư.
- **Mức độ quen thuộc với LaTeX:** Người dùng đưa ra ý tưởng thô; Agent chịu trách nhiệm hoàn thiện nội dung chi tiết, viết toàn bộ mã nguồn LaTeX và đề xuất phương án chỉnh sửa.
- **Ngôn ngữ ưu tiên:** Tiếng Việt giải thích nghĩa, Tiếng Anh cho thuật ngữ chuyên ngành CFA và nguyên văn đề bài tập mẫu.

## 2. Phong cách tương tác & Tông giọng mong muốn
- **Tông giọng của Agent:** Hướng học thuật (academic), diễn đạt đơn giản hóa kiến thức phức tạp nhưng đi sâu vào bản chất và logic rõ ràng. Ngôi xưng hô thân thiện, gần gũi như "**Chúng ta**".
- **Cơ chế ra quyết định (Workflow ý tưởng):** 
  1. Người dùng đưa ra các gạch đầu dòng ý tưởng thô.
  2. Agent phản hồi và phác thảo chi tiết hơn.
  3. Cả hai cùng thảo luận kỹ lưỡng.
  4. Người dùng duyệt phương án trước khi Agent chính thức triển khai viết code.
- **Thói quen chú thích & Trình bày đặc biệt:**
  - Sử dụng ghi chú chữ in nghiêng màu xanh dương (`\textcolor{blue}{\textit{...}}`) cho giải thích của giảng viên, ưu tiên **đặt các câu hỏi gợi mở** để tăng tính tương tác của học viên.
  - Các mẹo thi cử (**Exam Tips**) hoặc lưu ý quan trọng cần được đóng khung viền riêng biệt trong LaTeX để làm nổi bật.

## 3. Quy chuẩn Toán học, Bài tập & Tích hợp thực tế
- **Chứng minh Toán học (Proofs):** Trình bày đầy đủ các bước chứng minh toán học của công thức, nhưng đơn giản hóa cách diễn đạt sao cho người có trình độ toán phổ thông có thể hiểu được bản chất.
- **Đề bài tập:** Giữ nguyên văn tiếng Anh (đúng chuẩn độ khó đề thi thật của CFA).
- **Lời giải bài tập:** Trình bày rõ công thức toán học đồng thời hướng dẫn từng bước bấm máy tính tài chính (Texas Instruments BA II Plus) qua các phím bấm cụ thể (ví dụ: `[PV]`, `[FV]`, `[N]`, `[I/Y]`).
- **Tích hợp kiến thức thực tế:** Các góc nhìn nâng cao về quản trị rủi ro và đầu tư được lồng ghép dưới dạng các **Footnote (chú thích chân trang) ngắn gọn**, tránh làm phân tâm luồng ôn thi chính nhưng vẫn đảm bảo tính ứng dụng.

## 4. Định dạng Thương hiệu (Trustville Brand Guidelines)
- **Màu sắc chủ đạo (lấy theo Logo):** Sử dụng tông màu xanh lam và xanh lá của logo Trustville làm màu sắc cho các đề mục chính (Section/Subsection titles) trong tài liệu.
  - *Màu xanh lam (Primary Blue):* `\definecolor{trustvilleblue}{HTML}{1D70B8}`
  - *Màu xanh lá (Primary Green):* `\definecolor{trustvillegreen}{HTML}{0F8A5F}`
- **Logo chân trang:** Chèn logo Trustville (`figs/logo Trustville + text.png`) vào chân trang (footer) của tài liệu một cách chuyên nghiệp.

## 5. Quy tắc tương tác cốt lõi (Core Interaction Rules)
- **Tập trung vào giá trị cốt lõi:** Luôn trao đổi và thống nhất về mặt mục tiêu, định hướng và tư duy trước; bỏ qua hoặc lùi lại các chi tiết kỹ thuật ad-hoc (như biên dịch LaTeX, cấu hình file PDF) cho đến khi khung cốt lõi đã rõ ràng.
- **Hỏi theo cụm chuyên đề:** Khi cần thông tin từ người dùng, hãy gom các câu hỏi liên quan thành một cụm lớn có tính hệ thống để người dùng trả lời một lượt, tránh hỏi lắt nhắt từng câu đơn lẻ.
- **Làm việc bài bản & ngăn nắp:** Tổ chức cấu trúc thư mục, tệp tin và các bước thực hiện rõ ràng, có đánh số thứ tự `xxx_` và giải thích lý do cụ thể trước khi thực hiện.
- **Giới hạn số lượng tệp tin (Max 10 items per folder):** Mỗi thư mục không được chứa quá 10 tệp tin hoặc thư mục con. Nếu vượt quá số lượng này, bắt buộc phải phân loại và gom nhóm chúng thành các thư mục con theo chủ đề hoặc tính chất tương đồng.
- **Quy trình quản lý Git (Git Commit & Push Rules):**
  - Trước khi đẩy code lên GitHub, bắt buộc phải chia nhỏ các lần commit theo từng nội dung cụ thể (atomic commits), tuyệt đối không gộp chung toàn bộ thay đổi lớn vào một commit duy nhất. Mỗi commit phải có thông điệp (commit message) rõ ràng, mang tính mô tả cao (ví dụ: `feat:`, `docs:`, `asset:`, `ci:`).
  - Sau khi thực hiện lệnh `git push`, Agent phải cung cấp lại bảng danh sách tổng hợp các commit đã thực hiện trong phiên làm việc đó cho giảng viên để dễ theo dõi tiến độ.
- **Báo cáo & Khởi tạo phiên làm việc (Session Initialization & Logging):**
  - **Khởi tạo phiên:** Đầu mỗi phiên làm việc mới, Agent phải tự động đọc tệp `005_session_log.md` để: (1) Báo cáo tóm tắt các việc đã hoàn thành ở phiên trước, và (2) Đề xuất giải pháp cải tiến & lập kế hoạch chi tiết cho phiên hiện tại.
  - **Kết thúc phiên:** Cuối mỗi phiên làm việc, Agent có trách nhiệm ghi nhận lại lịch sử công việc đã làm và danh sách các commit đã thực hiện trong phiên đó vào tệp `005_session_log.md` để lưu trữ lâu dài.
