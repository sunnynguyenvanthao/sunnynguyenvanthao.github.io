# CLAUDE.md — sunnynguyenvanthao.github.io

Hướng dẫn cho Claude và các cloud session khi làm việc với repo này.

## Bối cảnh

- Landing page tĩnh của BS. Bùi Thị Kim Phượng (chăm sóc sức khỏe chủ động), dành cho khách muốn đăng ký tư vấn. Không có build, không có framework: một file `index.html` chứa HTML, CSS và JS.
- GitHub Pages phát hành từ `main`, nên `main` chính là trang đang chạy thật tại https://sunnynguyenvanthao.github.io/.
- File: `index.html` (trang), `bs/index.html` (chuyển hướng `/bs`), `bs-phuong-*.png` (ảnh).
- Xem thử: `python3 -m http.server 8000` rồi mở http://localhost:8000/.

## Quy tắc bắt buộc

1. Mỗi việc làm trên một nhánh riêng (`claude/...`) và kết thúc bằng pull request. Không bao giờ push hoặc merge thẳng vào `main`.
2. Không thay đổi nội dung y khoa, tuyên bố về sức khỏe, lời khuyên, giá hoặc phạm vi dịch vụ khi chưa có chủ sở hữu duyệt. Giữ nguyên phần "Lưu ý y khoa".
3. Ảnh phải tối ưu trước khi commit: WebP hoặc JPEG, cạnh dài tối đa 1600 px, mục tiêu dưới 300 KB mỗi ảnh. Không nhúng thêm ảnh base64 vào HTML.
4. Không commit khóa bí mật, token, mật khẩu hay dữ liệu cá nhân thật của khách. `FORM_ENDPOINT` chỉ điền khi chủ sở hữu cung cấp.
5. Không đổi tên file ảnh hoặc đường dẫn `/bs` khi chưa kiểm tra mọi tham chiếu.
6. Trước khi mở PR: mở trang cục bộ, kiểm tra ảnh, liên kết neo, biểu mẫu và giao diện điện thoại.

## Tình trạng kiểm tra gần nhất (26/10/2026)

- Tham chiếu nội bộ: `bs-phuong-hero.png`, `bs-phuong-3.png`, `bs-phuong-4.png` đều tồn tại; các neo `#main #top #phuongphap #dichvu #bacsi #faq #dangky` đều có đích. Không có tham chiếu hỏng.
- Dịch vụ bên ngoài: chỉ Google Fonts (`fonts.googleapis.com`, `fonts.gstatic.com`). Không có analytics, pixel hay script CDN.
- Biểu mẫu `#lead-form`: `FORM_ENDPOINT` để trống (`index.html:296`), nên form chạy chế độ demo, không gửi dữ liệu đi đâu và báo lỗi cho người dùng. Trang hiện không thu được lead.
- Khóa bí mật: không tìm thấy.
- Ảnh: 5 file PNG, tổng ~9,5 MB. Lớn nhất: `bs-phuong-5.png` 1,96 MB, `bs-phuong-2.png` 1,91 MB, `bs-phuong-4.png` 1,89 MB. `bs-phuong-2.png` và `bs-phuong-5.png` không được dùng.
- `index.html` nặng 1,37 MB vì chứa 4 ảnh base64 (~1 MB; ảnh chân dung 470×588 lặp 2 lần). Ở hero, "Về bác sĩ" và bài viết nổi bật, mỗi khung có cả `<img>` PNG lẫn `<img>` base64 liền nhau, nên trình duyệt tải cả hai. Cần chủ sở hữu chọn giữ ảnh nào trước khi dọn.
- `bs/index.html` chuyển hướng (meta refresh) về trang chủ, hoạt động đúng.
