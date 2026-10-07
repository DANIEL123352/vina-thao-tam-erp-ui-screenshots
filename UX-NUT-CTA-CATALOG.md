# Kê khai nút UX — VINA Thảo Tâm Factory OS

Nhãn UI → công dụng. Kind: primary | secondary | icon | nav | tab | kpi | link | danger.

## Login + chờ duyệt

| Vùng | Nhãn | Loại | Công dụng |
|------|------|------|-----------|
| header | Thông báo đăng nhập | icon | Mở/đóng panel sự kiện bảo mật |
| header | Đặt lại biểu mẫu | icon | Reset form; hủy TOTP / chờ duyệt |
| hint | Mở app Giám đốc (/m) | link | Sang PWA /m |
| MK | Đăng nhập | primary | Gửi MK → phiên / TOTP |
| MK | Đăng nhập bằng Touch ID | primary | WebAuthn Touch ID |
| MK | Hủy Touch ID | secondary | Hủy passkey đang chờ |
| MK | Yêu cầu cấp / reset mật khẩu | secondary | GD/IT xin reset |
| MK | Quên mật khẩu / yêu cầu mã mới | secondary | KT/TK quên MK |
| MK | Yêu cầu mở quyền truy cập | secondary | TK bị khóa xin mở |
| MK | Hiện / Ẩn mật khẩu | icon | Toggle hiển thị MK |
| TOTP | Xác nhận đăng nhập | primary | Gửi mã 2FA |
| TOTP | Quay lại nhập mật khẩu | secondary | Thoát 2FA |
| QR/PIN | Xác nhận QR / PIN | primary | Login công nhân → /worker |
| chat | Đặt mật khẩu mới | link | Mở link reset còn hạn |
| chat | Gửi tin nhắn hỗ trợ | icon | Chat tới Giám đốc |
| chờ duyệt | Đây là máy chính — cho phép đăng nhập | primary | Self-grant |
| chờ duyệt | Hủy và đăng nhập lại | secondary | Hủy pending |

## Shell Factory OS

| Vùng | Nhãn | Loại | Công dụng |
|------|------|------|-----------|
| sidebar | Tổng quan … Hệ thống | nav | Mở rail / portal tương ứng |
| header | Tìm kiếm chứng từ… | search | Command palette ⌘K |
| header | Thông báo | icon | Công nợ quá hạn + yêu cầu MK |
| header | Tin nhắn công việc | icon | Chat GD/KT/TK |
| header | Trợ giúp | icon | Toast hướng dẫn IT |
| header | Đăng xuất | secondary | Logout |
| footer | Làm mới | secondary | Refresh data |
| ⌘K | Mở đơn trễ hạn / Xem cảnh báo QC | quick | Jump có filter |
| mobile nav | Tổng quan · Hồ sơ ĐH · Công đoạn QR · Kho · MRP · Hóa đơn | tab | Bottom nav ERP |
| chấm công | Clock in / break / Clock out | primary | Attendance KT/TK |

## Overview KPI

| Nhãn | Công dụng |
|------|-----------|
| Doanh thu (Tháng) | → Doanh thu |
| Lợi nhuận gộp | → Kế toán |
| Lợi nhuận ròng | → Doanh thu |
| Công nợ phải thu | → CRM / Hồ sơ ĐH |
| Đơn hàng mở / Giao hàng đúng hạn | → Bán hàng |
| Pipeline stages | → CRM |
| In tem QR / Mở phân hệ / Đóng chi tiết | Drawer |

## Approvals · Passkey · 2FA

| Nhãn | Công dụng |
|------|-----------|
| Duyệt / Từ chối | Xử lý yêu cầu reset MK |
| Xác nhận từ chối | Từ chối có lý do |
| Cho phép / Từ chối (banner) | Duyệt login thiết bị mới |
| Lưu tên & chức danh | Profile NV |
| Thêm/Bỏ/Lưu câu hỏi | Q&A bảo mật |
| Gửi link đặt mật khẩu (5 phút) | Issue reset URL |
| Mở khóa / Khóa truy cập | Lock account |
| Gửi phản hồi | Chat trả lời NV |
| Thêm Touch ID / Bật push / Xóa | Passkey + Web Push |
| Tạo QR 2FA / Sao chép secret / Bật / Tắt 2FA | TOTP |

## /m · Field · Worker

| Vùng | Nhãn | Công dụng |
|------|------|-----------|
| /m | Đăng nhập · Xác nhận 2FA · Quay lại | Auth mobile GD |
| /m | Cho phép / Từ chối | Duyệt login máy mới |
| /m | Duyệt / Từ chối (MK) | Duyệt yêu cầu đặt MK |
| /m | Tổng quan · Duyệt · MK · Thêm | Bottom nav |
| /m | Mở ERP đầy đủ · Đăng xuất | More |
| Field | Admin/GD · Kế toán | Chọn người nhận |
| Field | Gắn GPS · Gửi tin hiện trường | Gửi tin |
| Worker | Quét tem QR · Tải công đoạn | Scan lô |
| Worker | Bắt đầu xử lý pallet · Hoàn thành công đoạn | Run shopfloor |
| Worker | Đăng xuất · Đóng camera | Session / UI |

## /auth/reset

| Nhãn | Công dụng |
|------|-----------|
| Xác nhận tất cả câu trả lời | Verify Q&A → hiện MK |
| Sao chép mật khẩu | Copy MK |
| Về trang đăng nhập | Về `/` |

## Pattern module sâu (lặp)

Lưu/Cập nhật · Tạo mới · Xóa · Xuất PDF/CSV/JSON · Import · Sync · Duyệt phiếu kho · Phát hành tem QR · Gửi Gmail HĐ · Đánh dấu tin hiện trường.

Chi tiết đầy đủ trong Cursor canvas UX + ảnh: https://github.com/DANIEL123352/vina-thao-tam-erp-ui-screenshots
