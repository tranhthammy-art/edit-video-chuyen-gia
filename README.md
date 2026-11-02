# edit-video-chuyen-gia

Skill VAS dựng video ngắn từ nguồn và video mẫu, với chữ động, cảnh trám, âm thanh và nhịp cảm xúc.

## Cài đặt vào VAS

1. Tải [gói skill](edit-video-chuyen-gia-skill.zip) và giải nén vào `customs/skills/edit-video-chuyen-gia/` của VAS. `SKILL.md`, `references/`, `scripts/`, `assets/` và `agents/` cần nằm cùng thư mục.
2. Đọc `SKILL.md`, tài liệu trong `references/` và `AGENTS.md` của VAS. Chạy `python scripts/vas.py doctor` tại thư mục gốc VAS.
3. Khi có footage, cài FFmpeg/ffprobe và các gói cần cho công đoạn dựng. Helper `scripts/retime_mix.py` dùng Python standard library và FFmpeg/ffprobe. Sau khi cài, chờ người dùng giao nguồn; không tự tải, phiên âm hay dựng thử.

## ChatGPT trình duyệt

Repo này chỉ chứa skill. Nó không tự cấp cho ChatGPT web quyền đọc file máy hoặc chạy VAS. Cầu nối VAS web hiện tại chỉ hỗ trợ `edit-video-tranh-dang-nhac-trend`; **chưa có công cụ MCP để chạy quy trình edit-video-chuyen-gia**. Vì vậy câu lệnh dưới đây cài skill vào VAS/Codex, chưa thể bảo đảm dựng trực tiếp từ bất kỳ chat web nào. Muốn dùng trên ChatGPT web cần bổ sung API/MCP riêng.

## Câu lệnh mẫu

> Set up https://github.com/tranhthammy-art/edit-video-chuyen-gia for me. Read README.md and SKILL.md inside the ZIP first. Install the skill into my VAS customs/skills folder, check Python and FFmpeg, and register it with the local agent that has access to VAS. Do not claim ChatGPT web rendering works unless an edit-video-chuyen-gia MCP connection exists and passes a real check. After installation, tell me what is ready and wait for me to provide footage and a reference video. Do not download, transcribe, or render anything on your own.
