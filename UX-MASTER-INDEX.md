# UX MASTER INDEX — VINA Thảo Tâm Factory OS / Rubberwood ERP

Một cửa vào duy nhất cho toàn bộ tài liệu UX đã tổng hợp (cấu trúc hệ thống + kê khai nút).

**Công ty:** Công ty CP VINA Thảo Tâm · **Sản phẩm:** Rubberwood ERP / Factory OS  
**Ảnh chụp production + text công khai (ChatGPT không bị 403 Vercel):**  
https://github.com/DANIEL123352/vina-thao-tam-erp-ui-screenshots

---

## A. Mở trong Cursor (canvas cạnh chat)

| # | Nội dung | File |
|---|----------|------|
| 1 | **UX toàn hệ thống** — surface, vai trò, IA, auth, journey, pattern, ma trận, kê khai nút shell/login/`/m` | `canvases/rubberwood-erp-ux-overview.canvas.tsx` |
| 2 | **Catalog nút theo MODULE** — từng phân hệ (Hồ sơ ĐH → Approvals…) | `canvases/rubberwood-erp-module-buttons.canvas.tsx` |

Đường dẫn tuyệt đối workspace:

- `/Users/daniel/.cursor/projects/Users-daniel-Documents-New-project-2/canvases/rubberwood-erp-ux-overview.canvas.tsx`
- `/Users/daniel/.cursor/projects/Users-daniel-Documents-New-project-2/canvases/rubberwood-erp-module-buttons.canvas.tsx`

---

## B. Cho ChatGPT (raw GitHub — HTTP 200)

| # | File | URL raw |
|---|------|---------|
| 1 | UX toàn hệ thống (brief) | https://raw.githubusercontent.com/DANIEL123352/vina-thao-tam-erp-ui-screenshots/main/UX-TOAN-HE-THONG.md |
| 2 | Kê khai nút shell / login / `/m` / worker | https://raw.githubusercontent.com/DANIEL123352/vina-thao-tam-erp-ui-screenshots/main/UX-NUT-CTA-CATALOG.md |
| 3 | **Catalog nút từng MODULE (đầy đủ)** | https://raw.githubusercontent.com/DANIEL123352/vina-thao-tam-erp-ui-screenshots/main/UX-MODULE-BUTTONS.md |
| 4 | Index ảnh hệ thống | https://raw.githubusercontent.com/DANIEL123352/vina-thao-tam-erp-ui-screenshots/main/README.md |
| 5 | Repo ảnh | https://github.com/DANIEL123352/vina-thao-tam-erp-ui-screenshots |

### Ảnh production (raw)

- Login full: `.../main/01-login-full.jpg`
- Login preview A–E: `.../main/02-login-preview-A.jpg` … `E.jpg`
- Mobile `/m`: `.../main/03-mobile-m-login.jpg`
- Field chat: `.../main/04-mobile-field-chat.jpg`
- Logo: `.../main/00-logo.jpg`

### Prompt gợi ý dán ChatGPT

```
Đọc lần lượt các URL raw:
1) UX-TOAN-HE-THONG.md
2) UX-NUT-CTA-CATALOG.md
3) UX-MODULE-BUTTONS.md
và các ảnh 01–04 trong cùng repo.
Đây là UX thật của Rubberwood ERP / Factory OS (VINA Thảo Tâm).
Không dùng mock design-previews làm nguồn chính.
Tóm tắt lại cấu trúc + toàn bộ nút theo module, rồi đề xuất cải tiến UI mobile Giám đốc /m.
```

---

## C. Tóm tắt cấu trúc UX (1 trang)

### C1. Surface (cửa vào) — 10+

| Surface | Path | Ai dùng |
|---------|------|---------|
| Factory OS desktop | `RubberwoodDashboard` | GD · KT · TK · IT |
| Login Factory OS | `LoginScreen` | 4 TK nội bộ + QR NV |
| Login preview | `/login-preview` | Chọn mẫu A–E |
| Mobile Giám đốc | `/m` | Chỉ GD (PWA) |
| Tin hiện trường | `/mobile-field-chat` | Công nhân gửi · GD/KT nhận |
| Cổng công nhân | `/worker` | PIN/QR |
| Scan / Trace | `/scan` · `/trace` · `/t` | Public |
| Reset MK | `/auth/reset` | Token ~5’ |
| Verify HĐ | `/verify/invoice` | Public |
| Traffic Vision | `/` · `/traffic-vision` (local) | Camera AI — **tách khỏi ERP** |

**Lưu ý định tuyến:** Local `src/app/page.tsx` đang mount Traffic Vision. UX ERP đầy đủ nằm trong `RubberwoodDashboard` (có thể chưa gắn route local). Production từng phục vụ ERP login tại `/`.

### C2. Personas

| Role | Trọng tâm UX |
|------|----------------|
| `giam_doc` | Toàn quyền · TOTP · Touch ID · duyệt thiết bị · `/m` · Approvals |
| `ke_toan` | Tài chính · HĐ · HR · field chat · chat login + reset MK |
| `thu_kho` | Kho · lô · QR · SX · chat login + reset |
| `it` | Settings · device · data hub · login director-style |
| worker / public | `/worker` · field chat · `/trace` — không Factory OS |

### C3. Information Architecture — 5 rail → 24 module

1. **Điều hành** — Tổng quan (Bàn Giám Đốc)  
2. **Kinh doanh** — Tài chính (DT · KT · HĐ) · Bán hàng · CRM/Hồ sơ ĐH · Mua hàng  
3. **Sản xuất** — Kho & SX (Kho · Lò · QR) · MRP · Chất lượng / Công đoạn QR  
4. **Quản trị** — Tài sản (+ Bảo trì) · Nhân sự  
5. **Hệ thống** — Phê duyệt · Hoạt động TB · Tin hiện trường · Lịch sử chat · Data hub · Thiết lập  

(+ `reports`, `bi`, `project` trong catalog module)

### C4. Auth journey

1. Mật khẩu → `/api/auth/login`  
2. (GD) TOTP / Passkey nếu bật  
3. (Máy mới) chờ duyệt thiết bị — máy tin cậy hoặc `/m`  
4. `loginSessionToken` → Supabase + director session  

**KT/TK quên MK:** yêu cầu → GD Approvals → link 5’ → `/auth/reset` + câu hỏi bảo mật → MK mới.

### C5. Nguyên tắc sản phẩm

- Nhà máy / số liệu / lô / QR thật — không landing marketing  
- GD bảo mật nặng · hiện trường nhẹ (PIN/QR/chat)  
- Một DB (Supabase/Firestore) — mobile không DB riêng  
- Desktop dày → companion `/m` cho GD đi đường  

---

## D. Kê khai nút — hai lớp

### D1. Shell · Login · `/m` · Worker · Reset  
→ File: `UX-NUT-CTA-CATALOG.md` · Canvas UX mục 11  

Nhóm: Login/TOTP/Touch ID/QR · Shell sidebar/header/⌘K · Overview KPI · Approvals/2FA · `/m`/Field/Worker · `/auth/reset` · pattern Lưu/Xuất/Import

### D2. Từng MODULE (đầy đủ)  
→ File: `UX-MODULE-BUTTONS.md` · Canvas `rubberwood-erp-module-buttons`  

| Module | Nút chính (rút gọn) |
|--------|---------------------|
| Hồ sơ ĐH | Tạo hồ sơ · quick menu · tabs · công nợ · note · jump module |
| Bán / Mua / MRP | Thêm/xóa đơn · BoM · giá thành · ErpHub |
| Công đoạn QR | Thêm khâu · gán team · start/pause/finish |
| Lò sấy | Thêm/xóa lệnh |
| Kho & Lô | SKU · phiếu · duyệt/đảo · Excel/PDF |
| QR | Phát hành · tải PNG · in · /scan |
| Hóa đơn | PDF/CSV · mẫu GTGT · Gmail |
| Doanh thu | Tabs · draft HĐ · jump |
| Bảo trì / Tài sản | Thêm lịch · xóa dòng |
| Dự án / BI / KT giá thành | Không nút (read-only / blur-save) |
| Tin hiện trường | Copy link · Đang/Đã xử lý · Lưu trữ |
| Nhân sự | NV · PIN · import chấm công · xuất CSV |
| Data Hub | Xuất/nhập JSON·CSV · mẫu gốc |
| Lịch sử chat | TXT/HTML/JSON · Xóa |
| Phê duyệt + Touch ID + 2FA | Đầy đủ |
| Hoạt động TB / Thiết lập / Báo cáo | Filter · Khóa/Mở · reports tĩnh |

---

## E. File local trong repo dự án

| File | Vai trò |
|------|---------|
| `docs/UX-MASTER-INDEX.md` | **File này** — mục lục tổng |
| `docs/UX-TOAN-HE-THONG.md` | Brief UX (nếu đã copy) |
| `docs/UX-NUT-CTA-CATALOG.md` | Nút shell/login |
| `docs/UX-MODULE-BUTTONS.md` | Nút theo module |
| `docs/system-screenshots/` | Ảnh chụp local |
| `docs/chatgpt-ui-samples-brief.html` | Brief HTML sớm hơn (login A–E) |

---

*Cập nhật khi tổng hợp lại toàn bộ UX + catalog nút module.*
