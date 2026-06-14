---
name: clean-latex-cache
description: Dọn dẹp các tệp trung gian biên dịch LaTeX bằng cách xóa toàn bộ thư mục 004_intermediate để giải phóng bộ nhớ.
---

# Hướng dẫn Dọn dẹp Cache Biên dịch LaTeX

Kỹ năng này giúp Agent xóa bỏ toàn bộ thư mục chứa các file trung gian sinh ra trong quá trình biên dịch.

## 1. Các tệp cần dọn dẹp
Toàn bộ các file trung gian như `.aux`, `.log`, `.toc`, `.lof`, `.lot`, `.synctex.gz`, v.v. đều được lưu tập trung trong thư mục:
- `004_intermediate/`

## 2. Quy trình Thực hiện

> [!IMPORTANT]
> Theo quy tắc **GEMINI.md**, Agent cần xin sự đồng ý của người dùng trước khi dọn dẹp các thư mục biên dịch.

1. **Xin xác nhận:** Hỏi người dùng xem họ có muốn dọn dẹp các file cache biên dịch hay không.
2. **Thực thi lệnh dọn dẹp:** Sau khi được đồng ý, chạy lệnh PowerShell sau trong thư mục gốc của dự án để xóa bỏ toàn bộ thư mục `004_intermediate`:
   ```powershell
   Remove-Item -Path 004_intermediate -Recurse -Force -ErrorAction SilentlyContinue
   ```
3. **Báo cáo kết quả:** Thông báo cho người dùng biết thư mục file rác trung gian đã được dọn dẹp sạch sẽ.
