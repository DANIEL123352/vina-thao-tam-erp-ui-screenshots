# → Mục lục tổng: [UX-MASTER-INDEX.md](./UX-MASTER-INDEX.md)

# UX toàn hệ thống — VINA Thảo Tâm Factory OS / Rubberwood ERP

Tài liệu tổng hợp UX từ code (LoginScreen, RubberwoodDashboard, /m, worker, field chat, trace).  
Không dùng mock `design-previews` làm nguồn chính.

**Lưu ý:** Local `src/app/page.tsx` có thể đang mount Traffic Vision CMS; UX ERP đầy đủ nằm trong `RubberwoodDashboard`.

---

## 1. Surface (cửa vào)

| Surface | Path | Ai dùng | Việc chính |
|---------|------|---------|------------|
| Factory OS desktop | RubberwoodDashboard | GD, KT, TK, IT | Sidebar + portal + overview CEO |
| Login Factory OS | LoginScreen | 4 TK nội bộ + QR NV | Hero kho · form · chat · footer |
| Login preview | /login-preview | Chọn mẫu | 5 mẫu A–E |
| Mobile Giám đốc | /m | Chỉ GD | PWA duyệt login + KPI + MK |
| Tin hiện trường | /mobile-field-chat | Công nhân gửi | Form public → inbox GD/KT |
| Cổng công nhân | /worker | PIN/QR | Quét lô · công đoạn |
| Scan / Trace | /scan · /trace · /t | Public | Tem QR provenance |
| Reset MK | /auth/reset | Token ~5’ | Câu hỏi bảo mật |
| Verify HĐ | /verify/invoice | Public | Xác minh GTGT |
| Traffic Vision | / · /traffic-vision | Camera AI | Tách khỏi ERP |

## 2. Personas

- **giam_doc**: toàn quyền + TOTP + Touch ID + duyệt thiết bị + /m + Approvals  
- **ke_toan**: tài chính/HĐ/HR/field chat; chat login + reset MK; không Approvals  
- **thu_kho**: kho/lô/QR/SX; chat login + reset; không HR/Hệ thống nhạy cảm  
- **it**: settings, device, data hub; login director-style  
- **worker / public**: /worker, /mobile-field-chat, /trace — không Factory OS  

## 3. IA sidebar

1. **Điều hành** — Tổng quan (Bàn Giám Đốc)  
2. **Kinh doanh** — Tài chính (DT·KT·HĐ) · Bán hàng · CRM/Hồ sơ ĐH · Mua hàng  
3. **Sản xuất** — Kho & SX (Kho·Lò·QR) · MRP · Chất lượng/Công đoạn QR  
4. **Quản trị** — Tài sản(+Bảo trì) · Nhân sự  
5. **Hệ thống** — Phê duyệt · Hoạt động TB · Tin hiện trường · Lịch sử chat · Data hub · Thiết lập  

## 4. Auth journey (Giám đốc)

1. MK → `/api/auth/login`  
2. (Nếu bật) TOTP 6 số  
3. (Máy mới) chờ duyệt thiết bị — tin cậy hoặc /m  
4. `loginSessionToken` → Supabase session + director session secret  

**KT/TK quên MK:** yêu cầu → GD duyệt → link 5’ → `/auth/reset` → câu hỏi bảo mật → MK mới.

## 5. Module catalog (24)

overview, order_dossier, sales, purchase, mrp, shopfloor, production, inventory, qr, accounting, invoice, revenue, bi, maintenance, assets, project, hr_payroll, field_chat, work_chat_history, device_activity, approvals, data_hub, settings, reports  

## 6. Mobile /m

Login GD → TOTP → approval wait → Home tabs: Tổng quan KPI · Duyệt login · Yêu cầu MK · Thêm. PWA. Deep link `?approveLogin=`.

## 7. Pattern UX

Shell Factory OS · portal tabs · ⌘K · drawer · toast · status footer · bottom nav ERP · Be Vietnam Pro · realtime badges · chặn private browsing.

## 8. Nguyên tắc

- Nhà máy thật — không marketing landing  
- Bảo mật GD nặng; hiện trường nhẹ  
- Một DB; mobile không tách data  
- Desktop dày → companion /m  

Ảnh: https://github.com/DANIEL123352/vina-thao-tam-erp-ui-screenshots


## 9. Kê khai nút UX

Xem file riêng: [UX-NUT-CTA-CATALOG.md](./UX-NUT-CTA-CATALOG.md)


## 10. Catalog nút theo MODULE

[UX-MODULE-BUTTONS.md](./UX-MODULE-BUTTONS.md) — toàn bộ CTA từng phân hệ.
