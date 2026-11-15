# AI CLAUDE — Bộ não thứ hai & sân tập Claude Code

## Tổng quan
Dự án có 2 mục đích:
1. **Học cấu hình Claude Code**: thử nghiệm CLAUDE.md, rules, settings, hooks, agents, skills.
2. **Trợ lý "bộ não thứ hai"**: nơi làm việc cá nhân (ghi chú, nghiên cứu, mua sắm, script tự động hóa nhỏ).

Công nghệ: Markdown (tài liệu), Python 3.12 và Node.js 24 (script). Chi tiết ở `rules/tech-defaults.md`.

## Lệnh
Hiện chưa có code nên chưa có lệnh build/test. Khi có thì dùng:

| Việc | Python | Node.js |
|------|--------|---------|
| Cài thư viện | `pip install -r requirements.txt` | `npm install` |
| Chạy | `python <file>.py` | `node <file>.js` hoặc `npm run dev` |
| Test | `python -m pytest` | `npm test` |
| Lint / format | `ruff check .` / `ruff format .` | `npm run lint` / `npx prettier --write .` |

Khi thêm lệnh thật cho dự án, cập nhật bảng này.

## Thư mục chính
- `.claude/` — cấu hình Claude Code (rules, agents, skills, hooks, settings)
- `.claude/hooks/` — script hook (`post-edit.js`: format + ghi log sau mỗi lần sửa file)
- `.claude/logs/` — log do hook ghi (không commit)
- `photo/` — ảnh và tài liệu tham khảo khi học

## Quy tắc cốt lõi
1. Làm chính xác trước, nhanh sau. Chưa rõ yêu cầu thì hỏi lại, không đoán.
2. Kiểm tra lại kết quả trước khi báo xong: đọc lại file vừa sửa, chạy lệnh/test nếu có.
3. Báo cáo trung thực: nói rõ phần nào đã kiểm tra, phần nào chưa, phần nào còn lỗi.
4. Thay đổi nhỏ, từng bước. Không sửa những thứ ngoài phạm vi được yêu cầu.
5. Không đọc hay in nội dung `.env`, `.env.*`, `secrets/`.
6. Không ghi đè file đã có mà chưa đọc; với file quan trọng, đề xuất trước rồi mới sửa.
7. Sau khi viết/sửa code, dùng agent `reviewer` để rà soát.

## Bộ nhớ dự án
Khi chốt một quyết định quan trọng hoặc sửa xong một lỗi khó, thêm **1 dòng có ngày** (YYYY-MM-DD) vào đúng mục trong `memory.md`.

@memory.md
