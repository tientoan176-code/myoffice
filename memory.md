# Memory — bộ nhớ dự án

Mỗi dòng: `- YYYY-MM-DD: nội dung`. Mới nhất ở dưới cùng.

## Quyết định đã chốt
- 2026-09-27: Đặt CLAUDE.md trong `.claude/` (bỏ bản ở gốc) để chỉ có một CLAUDE.md duy nhất.

## Lỗi đã gặp & cách sửa
- 2026-09-27: Máy không có `jq` nên hook đọc JSON bằng Node (`.claude/hooks/post-edit.js`) thay vì `jq`.
- 2026-09-27: Hook gọi formatter với `shell: true` làm đường dẫn có dấu cách (`D:\AI CLAUDE`) bị tách đôi → bỏ shell, gọi prettier bằng `node prettier.cjs`.

## Thói quen làm việc của mình
- 2026-09-27: Muốn Claude kiểm tra lại kết quả nhiều lần trước khi báo xong.
