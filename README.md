# sunnynguyenvanthao.github.io

Landing page giới thiệu **BS. Bùi Thị Kim Phượng — Chăm sóc sức khỏe chủ động**: tư vấn 1:1, lộ trình đồng hành 12 tuần, coaching theo nhóm, kèm biểu mẫu đăng ký tư vấn.

- Đối tượng: người muốn cải thiện sức khỏe qua dinh dưỡng, giấc ngủ, vận động và tinh thần; khách hàng tiềm năng của bác sĩ.
- Nơi chạy: GitHub Pages (user site), phát hành trực tiếp từ nhánh `main` tại https://sunnynguyenvanthao.github.io/. Mọi thay đổi trên `main` lên trang thật ngay.

## Cấu trúc thư mục

| Đường dẫn | Vai trò |
|---|---|
| `index.html` | Toàn bộ trang: HTML, CSS và JS nội tuyến (~1,4 MB vì có ảnh base64) |
| `bs/index.html` | Trang chuyển hướng `/bs` về trang chủ |
| `bs-phuong-hero.png`, `bs-phuong-3.png`, `bs-phuong-4.png` | Ảnh đang được `index.html` dùng |
| `bs-phuong-2.png`, `bs-phuong-5.png` | Ảnh chưa được trang nào dùng |
| `CLAUDE.md` | Quy tắc cho cloud session và kết quả kiểm tra gần nhất |

## Xem thử trên máy

```bash
python3 -m http.server 8000
# mở http://localhost:8000/ và http://localhost:8000/bs/
```

Không cần build hay cài đặt gì thêm.

## Tình trạng ngắn gọn (26/10/2026)

- Không có liên kết hay ảnh hỏng; không có khóa bí mật trong repo.
- Biểu mẫu đăng ký đang ở chế độ demo (`FORM_ENDPOINT` để trống), chưa thu được lead.
- Ảnh PNG chưa tối ưu (~9,5 MB). Chi tiết trong `CLAUDE.md`.

## Đóng góp

Làm trên nhánh riêng và mở pull request; không đẩy thẳng lên `main`. Không sửa nội dung y khoa, cam kết sức khỏe hay giá khi chưa có chủ sở hữu duyệt.
