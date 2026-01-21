# 📋 Hướng Dẫn Sao Chép Website (Nội Dung Thay Đổi)

## 🎯 Mục Đích

Hướng dẫn này giúp bạn tạo một website mới dựa trên website mẫu (`01facebookads/`) với:
- ✅ Giao diện và màu sắc giống hệt website mẫu
- ✅ Nội dung thay đổi theo yêu cầu
- ✅ Trang thanh toán tương tự
- ✅ Gửi email và Zalo bot hoàn toàn tương tự
- ✅ Chạy trên port riêng

---

## 📝 Quy Trình Thực Hiện

### Bước 1: Chuẩn Bị Thư Mục

1. Tạo thư mục mới cho website (ví dụ: `05tdhpython/`)
2. Đảm bảo thư mục mẫu (`01facebookads/`) đã có đầy đủ file

### Bước 2: Tạo File index.html

**Nội dung cần thay đổi:**
- `<title>`: Tiêu đề trang
- Hero section: Tagline, title, subtitle, description
- Main content: Nội dung chính về khóa học/sản phẩm
- Course content: Danh sách nội dung khóa học
- Instructor section: Thông tin giảng viên (có thể giữ nguyên hoặc thay đổi)
- Footer: Có thể giữ nguyên

**Cấu trúc giữ nguyên:**
- Header và navigation
- Các class CSS
- Cấu trúc HTML
- Links đến các file CSS, JS

**File mẫu:** `01facebookads/index.html`

### Bước 3: Copy style.css

**Lệnh:**
```powershell
Copy-Item "D:\98. Cursor\01. Web_Ban_Hang\01facebookads\style.css" -Destination "D:\98. Cursor\01. Web_Ban_Hang\[THƯ_MỤC_MỚI]\style.css"
```

**Hoặc:** Copy toàn bộ nội dung từ `01facebookads/style.css` sang file mới

**Lưu ý:** Không cần thay đổi gì trong file này

### Bước 4: Tạo script.js

**Copy từ:** `01facebookads/script.js`

**Nội dung cần thay đổi:**
- Dòng 64: `course_name: 'Khóa Tự Động Hóa Facebook Ads'` → Thay bằng tên khóa học mới
- Dòng 99: `course_name: 'Khóa Tự Động Hóa Facebook Ads'` → Thay bằng tên khóa học mới

**Ví dụ:**
```javascript
course_name: 'Khóa Tự Động Hóa Công Việc Với Python',
```

**Các phần khác giữ nguyên:**
- Validation form
- Gửi email qua EmailJS
- Gửi Zalo notification qua n8n
- Mobile menu toggle
- Floating CTA button
- Tất cả các function khác

### Bước 5: Tạo thanhtoan.html

**Copy từ:** `01facebookads/thanhtoan.html`

**Nội dung cần thay đổi:**
- Dòng 1032: `<p>Kỹ Thuật Tự Động Hóa Quảng Cáo Facebook Ads Với Ai Automation</p>` → Thay bằng mô tả khóa học mới

**Ví dụ:**
```html
<p>Tự Động Hóa Công Việc Với Python: Vướng Đâu - Gỡ Đó</p>
```

**Các phần khác giữ nguyên:**
- Cấu trúc HTML
- CSS styles
- JavaScript functions
- Thông tin ngân hàng
- QR code

### Bước 6: Copy Các File Cấu Hình

**1. email-config.js:**
```powershell
Copy-Item "D:\98. Cursor\01. Web_Ban_Hang\01facebookads\email-config.js" -Destination "D:\98. Cursor\01. Web_Ban_Hang\[THƯ_MỤC_MỚI]\email-config.js"
```
**Lưu ý:** Không cần thay đổi gì, file này dùng chung cho tất cả website

**2. n8n-config.js:**
```powershell
Copy-Item "D:\98. Cursor\01. Web_Ban_Hang\01facebookads\n8n-config.js" -Destination "D:\98. Cursor\01. Web_Ban_Hang\[THƯ_MỤC_MỚI]\n8n-config.js"
```
**Lưu ý:** Không cần thay đổi gì, file này dùng chung cho tất cả website

### Bước 7: Copy Logo Và Hình Ảnh

**1. logo.png:**
```powershell
Copy-Item "D:\98. Cursor\01. Web_Ban_Hang\01facebookads\logo.png" -Destination "D:\98. Cursor\01. Web_Ban_Hang\[THƯ_MỤC_MỚI]\logo.png"
```

**2. QR Code thanh toán (nếu dùng chung):**
```powershell
Copy-Item "D:\98. Cursor\01. Web_Ban_Hang\01facebookads\ThuNhi_1450K_TDHCV343.png" -Destination "D:\98. Cursor\01. Web_Ban_Hang\[THƯ_MỤC_MỚI]\ThuNhi_1450K_TDHCV343.png"
```

**Lưu ý:** Nếu có QR code riêng, thay thế file này

### Bước 8: Copy Device Emulator

**device-emulator.html:**
```powershell
Copy-Item "D:\98. Cursor\01. Web_Ban_Hang\01facebookads\device-emulator.html" -Destination "D:\98. Cursor\01. Web_Ban_Hang\[THƯ_MỤC_MỚI]\device-emulator.html"
```

**Lưu ý:** Không cần thay đổi gì, file này dùng chung

### Bước 9: Tạo start-emulator.ps1

**Copy từ:** `01facebookads/start-emulator.ps1`

**Nội dung cần thay đổi:**

1. **Dòng 5:** Tiêu đề
```powershell
Write-Host "  Device Emulator - [TÊN_APP]" -ForegroundColor Cyan
```

2. **Dòng 23:** Port (thay 8000 bằng port mới, ví dụ: 8007)
```powershell
$portInUse = Get-NetTCPConnection -LocalPort 8007 -ErrorAction SilentlyContinue
```

3. **Dòng 41:** Port trong thông báo
```powershell
Write-Host "🚀 Đang khởi động HTTP Server trên port 8007..." -ForegroundColor Cyan
```

4. **Dòng 47:** Port trong lệnh Python
```powershell
python -m http.server 8007
```

5. **Dòng 54:** Port trong kiểm tra server
```powershell
$serverRunning = Get-NetTCPConnection -LocalPort 8007 -ErrorAction SilentlyContinue
```

6. **Dòng 69:** Port trong URL
```powershell
$emulatorUrl = "http://localhost:8007/device-emulator.html"
```

### Bước 10: Tạo HUONG_DAN_CHAY_UNG_DUNG.md

**Copy từ:** `01facebookads/HUONG_DAN_CHAY_UNG_DUNG.md`

**Nội dung cần thay đổi:**

1. **Dòng 1:** Tiêu đề
```markdown
# 📱 Hướng Dẫn Chạy Ứng Dụng Website [TÊN_APP]
```

2. **Dòng 11:** Đường dẫn thư mục
```markdown
cd "D:\98. Cursor\01. Web_Ban_Hang\[THƯ_MỤC_MỚI]"
```

3. **Tất cả các chỗ có port 8000:** Thay bằng port mới (ví dụ: 8007)
   - Dòng 59: `python -m http.server 8007`
   - Dòng 64: `http://localhost:8007/device-emulator.html`
   - Dòng 79: `http://localhost:8007/index.html`
   - Dòng 84: `http://localhost:8007/index.html?mobile=1`
   - Dòng 117: `netstat -ano | findstr :8007`
   - Dòng 134: `http://localhost:8007/device-emulator.html`
   - Dòng 157: Cấu trúc file (thư mục mới)
   - Dòng 212: `Port 8007 không bị chiếm dụng`
   - Dòng 231: Đường dẫn thư mục
   - Dòng 236: `http://localhost:8007/device-emulator.html`

---

## 📋 Checklist Hoàn Thành

Sau khi hoàn thành, kiểm tra các file sau:

- [ ] `index.html` - Nội dung đã thay đổi, cấu trúc giữ nguyên
- [ ] `style.css` - Copy từ mẫu, không thay đổi
- [ ] `script.js` - Đã cập nhật tên khóa học (2 chỗ)
- [ ] `thanhtoan.html` - Đã cập nhật mô tả khóa học
- [ ] `email-config.js` - Copy từ mẫu, không thay đổi
- [ ] `n8n-config.js` - Copy từ mẫu, không thay đổi
- [ ] `logo.png` - Copy từ mẫu hoặc thay bằng logo mới
- [ ] `ThuNhi_1450K_TDHCV343.png` - Copy từ mẫu hoặc thay bằng QR code mới
- [ ] `device-emulator.html` - Copy từ mẫu, không thay đổi
- [ ] `start-emulator.ps1` - Đã cập nhật port và tên app
- [ ] `HUONG_DAN_CHAY_UNG_DUNG.md` - Đã cập nhật port và đường dẫn

---

## 🎯 Lệnh Nhanh Để Tạo Website Mới

Khi bạn muốn tạo website mới, chỉ cần nói:

**"Bạn dựa vào app này @01facebookads/ này, để tạo cho tôi một @[THƯ_MỤC_MỚI]/ với giao diện và màu sắc tương tự @01facebookads/, còn nội dung thì là [MÔ TẢ NỘI DUNG], trang thanh toán thì tương tự @01facebookads/, sử dụng gởi email và zalo bot hoàn toàn tương tự nữa nhé, tạo cho tôi app này nhé"**

**Và thêm:**
**"Bạn dựa vào file này @HUONG_DAN_CHAY_UNG_DUNG để chạy app port thì bạn lấy [PORT], nhớ là chạy ứng dụng @[THƯ_MỤC_MỚI]/, logo, set up bạn làm tương tự ứng dụng @01facebookads/ (bạn có thể copy các nội dung (không phải nội dung web) ứng dụng này qua @[THƯ_MỤC_MỚI]/ để chạy)"**

---

## 📝 Ví Dụ Cụ Thể

### Ví dụ 1: Tạo website cho khóa học Python

**Lệnh:**
```
Bạn dựa vào app này @01facebookads/ này, để tạo cho tôi một @05tdhpython/ với giao diện và màu sắc tương tự @01facebookads/, còn nội dung thì là về khóa học Tự Động Hóa Công Việc Với Python, trang thanh toán thì tương tự @01facebookads/, sử dụng gởi email và zalo bot hoàn toàn tương tự nữa nhé, tạo cho tôi app này nhé

Bạn dựa vào file này @HUONG_DAN_CHAY_UNG_DUNG để chạy app port thì bạn lấy 8007, nhớ là chạy ứng dụng @05tdhpython/, logo, set up bạn làm tương tự ứng dụng @01facebookads/ (bạn có thể copy các nội dung (không phải nội dung web) ứng dụng này qua @05tdhpython/ để chạy)
```

**Kết quả:**
- Website mới trong `05tdhpython/`
- Nội dung về Python automation
- Chạy trên port 8007
- Tất cả tính năng tương tự website mẫu

---

## 🔍 Các File Quan Trọng Cần Kiểm Tra

### 1. script.js - 2 chỗ cần thay đổi

**Tìm và thay:**
```javascript
// Dòng ~64
course_name: 'Khóa Tự Động Hóa Facebook Ads',
// Thay thành:
course_name: 'Khóa [TÊN_KHÓA_HỌC_MỚI]',

// Dòng ~99
course_name: 'Khóa Tự Động Hóa Facebook Ads',
// Thay thành:
course_name: 'Khóa [TÊN_KHÓA_HỌC_MỚI]',
```

### 2. thanhtoan.html - 1 chỗ cần thay đổi

**Tìm và thay:**
```html
<!-- Dòng ~1032 -->
<p>Kỹ Thuật Tự Động Hóa Quảng Cáo Facebook Ads Với Ai Automation</p>
<!-- Thay thành: -->
<p>[MÔ TẢ_KHÓA_HỌC_MỚI]</p>
```

### 3. start-emulator.ps1 - 6 chỗ cần thay đổi

**Tìm và thay tất cả:**
- `8000` → `[PORT_MỚI]` (6 chỗ)
- `Facebook Ads App` → `[TÊN_APP_MỚI]` (1 chỗ)

### 4. HUONG_DAN_CHAY_UNG_DUNG.md - Nhiều chỗ

**Tìm và thay:**
- `01facebookads` → `[THƯ_MỤC_MỚI]` (nhiều chỗ)
- `8000` → `[PORT_MỚI]` (nhiều chỗ)
- `Facebook Ads` → `[TÊN_APP]` (nhiều chỗ)

---

## ✅ Kiểm Tra Sau Khi Hoàn Thành

1. **Chạy thử app:**
   ```powershell
   cd "D:\98. Cursor\01. Web_Ban_Hang\[THƯ_MỤC_MỚI]"
   .\start-emulator.ps1
   ```

2. **Kiểm tra:**
   - [ ] Website hiển thị đúng
   - [ ] Nội dung đã thay đổi
   - [ ] Form đăng ký hoạt động
   - [ ] Chuyển đến trang thanh toán
   - [ ] Email và Zalo notification hoạt động (nếu đã cấu hình)

3. **Test trên mobile:**
   - Truy cập: `http://localhost:[PORT]/index.html?mobile=1`
   - Kiểm tra responsive

---

## 🎨 Màu Sắc Và Giao Diện

**Màu chính:** `#00786a` (teal/green)
**Màu nền:** `rgb(225, 247, 250)` (light teal)
**Gradient hero:** `linear-gradient(135deg, #1b877b 0%, #00786a 100%)`

**Giữ nguyên tất cả màu sắc và style từ website mẫu!**

---

## 📞 Lưu Ý Quan Trọng

1. **Không thay đổi:**
   - Cấu trúc HTML
   - Class CSS
   - JavaScript logic (chỉ thay tên khóa học)
   - Cấu hình email và n8n
   - Thông tin ngân hàng (trừ khi có yêu cầu)

2. **Chỉ thay đổi:**
   - Nội dung text trong HTML
   - Tên khóa học trong script.js (2 chỗ)
   - Mô tả trong thanhtoan.html (1 chỗ)
   - Port trong start-emulator.ps1 và HUONG_DAN_CHAY_UNG_DUNG.md
   - Đường dẫn thư mục trong các file hướng dẫn

3. **Copy nguyên:**
   - style.css
   - email-config.js
   - n8n-config.js
   - device-emulator.html
   - logo.png (hoặc thay bằng logo mới)
   - QR code (hoặc thay bằng QR code mới)

---

## 🚀 Tóm Tắt Nhanh

**Để tạo website mới:**

1. Tạo thư mục mới
2. Copy tất cả file từ `01facebookads/`
3. Thay đổi nội dung trong `index.html`
4. Cập nhật tên khóa học trong `script.js` (2 chỗ)
5. Cập nhật mô tả trong `thanhtoan.html` (1 chỗ)
6. Cập nhật port trong `start-emulator.ps1` (6 chỗ)
7. Cập nhật port và đường dẫn trong `HUONG_DAN_CHAY_UNG_DUNG.md`
8. Chạy thử và kiểm tra

**Xong!** 🎉

---

*Tạo bởi: Auto (Cursor AI)*
*Ngày: 2024*
*Dựa trên: 01facebookads/ → 05tdhpython/*

