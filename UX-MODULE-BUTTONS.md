# Catalog nút theo MODULE — VINA Thảo Tâm Factory OS

Nhãn UI (VI) → công dụng. Busy = chữ khi đang xử lý.  
Shell/Login/`/m` xem thêm: `UX-NUT-CTA-CATALOG.md`.

---

## Hồ sơ đơn hàng (Order Dossier)

| Vùng | Nhãn | Busy | Công dụng |
|------|------|------|-----------|
| Empty/form | Tạo hồ sơ | | Tạo company + SO nháp + pipeline + công nợ |
| Sidebar | Thêm khách hàng / Đóng form | | Mở/đóng form tạo KH |
| Danh sách | {tên công ty} | | Chọn KH |
| Mobile | Danh sách | | Đóng chi tiết |
| Quick | Tạo mới | | Menu tạo nhanh |
| Quick menu | Bán hàng · Mua hàng · Lệnh sản xuất · Chuẩn bị QR · Tạo chuyến · Hóa đơn nháp | | Tạo/jump module |
| Export | JSON / HTML | | Tải hồ sơ công ty |
| Toggle | Cost & Profit Engine | | Mở dải KPI giá thành |
| Tabs | Tổng quan · Bán hàng · Mua hàng · MRP/BoM · Lò sấy · QR · Hóa đơn · BL · Doanh thu · Ghi chú | | Đổi tab |
| Period | Tháng này | | Reset kỳ |
| Jump | Mở Bán hàng / Mua / MRP / Lò / QR / Doanh thu / Báo cáo | | Sang module |
| HĐ | Tải PDF · Tạo hóa đơn nháp | | PDF dossier / draft HĐ |
| Công nợ | Đã thu đủ · Thu một phần · Ghi nhận · Hủy | | Thanh toán receivable |
| Notes | Lưu note | | Lưu ghi chú |

## Bán hàng · Mua hàng · MRP

| Module | Nhãn | Công dụng |
|--------|------|-----------|
| Sales | Thêm đơn bán · Xóa dòng | Thêm/xóa SO |
| Purchase | Thêm đơn mua · Xóa dòng | Thêm/xóa PO |
| MRP | Thêm công thức BoM · Xóa công thức | Quản BoM |
| MRP | − / + định mức · Xóa thành phần | Sửa component |
| MRP | Thêm nguyên liệu · Thêm nhân công | Thêm dòng BoM |
| MRP | Lưu hồ sơ giá thành · Mở/Đóng nhóm · JSON/CSV/HTML · Xóa hồ sơ | Cost engine |
| ErpHub | Bộ lọc · Đồng bộ Odoo · Gỗ CN/Nội thất · quick modules | Hub nhảy phân hệ |

## Công đoạn QR (Shopfloor)

| Nhãn | Busy | Công dụng |
|------|------|-----------|
| Thêm khâu | | Thêm công đoạn |
| Gán vào team | Đang gán... | Phân công NV |
| Xóa | | Xóa phân công |
| Tạo pallet xử lý | | Tạo pallet từ QR/lô |
| Đang xử lý | | Start run |
| Tạm dừng / Tiếp tục | | Pause/resume |
| Hoàn thành | | Finish + qty/QC |

## Lò sấy

| Nhãn | Công dụng |
|------|-----------|
| + Thêm lò / lệnh · Thêm lệnh sấy | Thêm lệnh |
| Xóa dòng | Xóa lệnh |

## Kho & Lô (WMS)

| Vùng | Nhãn | Công dụng |
|------|------|-----------|
| Tabs | Tồn kho & SKU · Sổ phiếu kho | Đổi tab |
| Toolbar | Tạo phiếu kho | Modal phiếu |
| SKU | + Thêm SKU · Xóa SKU | CRUD SP |
| Filter SKU | Tất cả / Gỗ Tròn / Xẻ Sấy / Ghép Thanh / Phụ Phẩm | Lọc loại |
| Ledger filter | Nhập·Xuất·Chuyển·Điều chỉnh·Hao hụt · Chờ duyệt·Đã ghi sổ·Từ chối | Lọc phiếu |
| Export | Excel · PDF · phân trang | Xuất sổ |
| Pending GD | Duyệt · Từ chối | Phê duyệt phiếu |
| Posted | Đảo | Phiếu đảo |
| Modal | Huỷ · Ghi phiếu · Tạo phiếu đảo | Submit |

## QR Truy xuất

| Nhãn | Công dụng |
|------|-----------|
| {url} chip | Chọn public origin |
| Quét | Mở camera |
| Phát hành & lưu hồ sơ | Issue QR+barcode |
| Tải PNG QR / mã vạch · In tem | Download/in |
| Màn hình quét to | /scan/{lot} |
| Xuất bảng (Excel+HTML) | Export lịch sử |
| Xem · QR · 1D · In | Hàng lịch sử |
| Đóng camera | Đóng scanner |

## Hóa đơn

| Nhãn | Busy | Công dụng |
|------|------|-----------|
| Bộ lọc · Đồng bộ | | Chrome / sync |
| Tải PDF / In | Đang tạo PDF… | Xuất PDF |
| Xuất CSV · Thao tác | | Export / menu |
| HĐ GTGT (01/GTGT) · GTGT ngoại tệ · HĐ bán hàng (02GTTT3/001) | | Đổi mẫu |
| Gửi Gmail (PDF đính kèm) | | Email kèm PDF |

## Doanh thu

| Nhãn | Công dụng |
|------|-----------|
| Tabs Tổng quan · Theo KH · Lô/SKU · Dự báo | Đổi tab |
| Xem chi tiết · {KH} · Mở | Chọn KH |
| Mở Hồ sơ ĐH · Tạo HĐ theo DT · Đối chiếu công nợ · Xem lô kho | Jump / draft |
| Mở Kho · Mở MRP · Mở hóa đơn (alerts) | Jump cảnh báo |

## Bảo trì · Tài sản · Dự án · BI · Kế toán

| Module | Nút | Ghi chú |
|--------|-----|---------|
| Bảo trì | Thêm lịch bảo trì · Xóa dòng | EditableTable |
| Tài sản | Xóa dòng | Có quyền sửa |
| Dự án | — | Cards read-only |
| BI | — | KPI only |
| Kế toán giá thành | — | Blur-save, không button |

## Tin hiện trường (inbox)

| Nhãn | Công dụng |
|------|-----------|
| Sao chép link mobile | Copy /mobile-field-chat |
| Làm mới | Reload queue |
| {sender} row | Chọn tin |
| Đang xử lý · Đã xử lý · Lưu trữ (GD) | Đổi status |

## Nhân sự & Lương

| Nhãn | Busy | Công dụng |
|------|------|-----------|
| Refresh icon | | Reload HR |
| Tabs Danh mục · Chấm công · Tổng giờ | | Đổi tab |
| Thêm nhân viên | Đang lưu… | addEmployee |
| Import CSV · Đặt lại danh sách | | Import/reset |
| Cấp MK · Xóa MK · Mở khóa · Khóa · Xóa | | Worker access |
| Chọn file chấm công | Đang import… | Fingerprint CSV |
| Lưu ngày công | | saveAttendanceDay |
| Xuất CSV tháng | | exportSummaryCsv |

## Data Hub

| Nhãn | Công dụng |
|------|-----------|
| Xuất JSON · CSV (bảo trì·giá·kho) | Export |
| Sao chép tóm tắt · Nhập JSON · Mẫu gốc | Clipboard / import / reset |

## Lịch sử chat công việc

| Nhãn | Công dụng |
|------|-----------|
| {tiêu đề phiên} | Expand |
| TXT · HTML · JSON (GD) | Download |
| Xóa | Xóa phiên |

## Phê duyệt · Passkey · 2FA

| Nhãn | Busy | Công dụng |
|------|------|-----------|
| Duyệt · Từ chối | | Yêu cầu MK |
| Lưu tên & chức danh | Đang lưu… | Profile |
| Thêm/Bỏ câu hỏi · Lưu tất cả | Đang lưu… | Q&A |
| Xóa tất cả · Tải vào form · Lưu/Xóa TR · Đưa vào form | | Lịch sử Q&A |
| Gửi link đặt MK (5 phút) | Đang tạo link… | Reset URL |
| Mở khóa / Khóa truy cập | Đang mở khóa… | Lock |
| Gửi phản hồi | | Chat GD→NV |
| Thêm Touch ID | Đang chờ Touch ID… | WebAuthn |
| Bật thông báo phê duyệt | Đang đăng ký… | Web Push |
| Xóa (passkey) | | Xóa device |
| Tạo QR 2FA · Sao chép secret · Bật 2FA · Tắt 2FA | | TOTP |

## Hoạt động TB · Thiết lập · Báo cáo · CRM table

| Module | Nhãn | Công dụng |
|--------|------|-----------|
| Device | Hôm nay | Filter ngày |
| Settings | Khóa / Mở | GD khóa TK nội bộ |
| Reports | — | Bảng lịch tĩnh |
| CrmCustomerTable | Sắp xếp cột · Mặc định · lên/xuống cột · click hàng | Column UX / select |

---

Ảnh + brief UX: https://github.com/DANIEL123352/vina-thao-tam-erp-ui-screenshots
