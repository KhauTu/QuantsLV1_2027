# Kỹ Năng Của Agent (Agent Skills)

Thư mục này chứa các kỹ năng (skills) chuyên biệt do người dùng định nghĩa để mở rộng khả năng hoạt động của AI Agent. Mỗi kỹ năng là một thư mục riêng chứa tệp hướng dẫn cốt lõi `SKILL.md`.

## Cấu trúc của một Skill

Một kỹ năng hợp lệ cần có cấu trúc như sau:
```text
skills/
└── ten-ky-nang/
    └── SKILL.md
```

Tệp `SKILL.md` bắt đầu bằng phần YAML frontmatter bắt buộc:
```markdown
---
name: ten-ky-nang
description: Mô tả ngắn gọn về chức năng của kỹ năng này để Agent nhận diện khi nào cần dùng.
---

# Nội dung hướng dẫn chi tiết...
```

## Danh sách kỹ năng hiện tại

1. **`001_compile-latex`**: Biên dịch toàn bộ tài liệu dự án từ mã nguồn LaTeX sang tệp PDF sử dụng `latexmk` hoặc `pdflatex`, đồng thời tự động phân tích tệp `.log` để chẩn đoán và báo cáo lỗi cú pháp.
2. **`002_clean-latex-cache`**: Quét và dọn dẹp các tệp trung gian do trình biên dịch LaTeX sinh ra (như `.aux`, `.log`, `.synctex.gz`, v.v.) một cách an toàn sau khi nhận được xác nhận từ người dùng.

## Cách tạo mới một Skill

1. Tạo thư mục mới mang tên của kỹ năng dưới thư mục `skills/` (viết thường, phân cách bằng dấu gạch ngang, ví dụ: `my-custom-skill`).
2. Tạo tệp `SKILL.md` bên trong thư mục vừa tạo.
3. Định nghĩa phần frontmatter `name` trùng tên thư mục và viết phần `description` thật chi tiết để Agent tự động hiểu và sử dụng khi gặp bài toán liên quan.
