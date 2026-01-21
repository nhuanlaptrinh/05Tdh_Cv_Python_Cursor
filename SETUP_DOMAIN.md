# 🌐 Thiết Lập Tên Miền cho 05tdhpython

## ✅ Đã Hoàn Thành

### 1. Tên Miền Đã Được Tạo
- **Tên miền:** `tdhcv.anhlaptrinh.vn`
- **Loại record:** A
- **IP Address:** `194.59.165.104`
- **Record ID:** `26b8900bb07275e9b27c4e80731f7166`
- **Trạng thái:** ✅ Đã tạo thành công trên Cloudflare

### 2. Cấu Hình Ứng Dụng
Ứng dụng `05tdhpython/` đã được thiết lập tương tự như `01facebookads/` với:

- ✅ `index.html` - Trang chủ
- ✅ `device-emulator.html` - Device emulator để xem trên nhiều thiết bị
- ✅ `start-emulator.ps1` - Script khởi động (port 8007)
- ✅ `script.js` - JavaScript xử lý form
- ✅ `style.css` - CSS styling
- ✅ `email-config.js` - Cấu hình EmailJS
- ✅ `n8n-config.js` - Cấu hình n8n Webhook
- ✅ `thanhtoan.html` - Trang thanh toán
- ✅ `HUONG_DAN_CHAY_UNG_DUNG.md` - Hướng dẫn sử dụng

## 🚀 Cách Sử Dụng

### Chạy Ứng Dụng Local

```powershell
cd /root/05tdhpython
.\start-emulator.ps1
```

Ứng dụng sẽ chạy tại: `http://localhost:8007/device-emulator.html`

### Deploy Lên Server

Để deploy ứng dụng lên server và sử dụng tên miền `tdhcv.anhlaptrinh.vn`:

1. **Upload files lên server:**
   - Upload toàn bộ thư mục `05tdhpython/` lên server tại IP `194.59.165.104`
   - Đảm bảo web server (Apache/Nginx) đã được cấu hình

2. **Cấu hình Web Server:**
   - Cấu hình virtual host trỏ đến thư mục `05tdhpython/`
   - Đảm bảo domain `tdhcv.anhlaptrinh.vn` trỏ đến đúng thư mục

3. **Kiểm tra DNS:**
   - DNS record đã được tạo tự động qua Cloudflare API
   - Có thể kiểm tra tại: Cloudflare Dashboard → DNS Records

## 📋 Thông Tin Cấu Hình

### EmailJS Config
- **Service ID:** `service_cdywck7`
- **Template ID:** `template_drxh4sf`
- **Email nhận thông báo:** `nhuanlaptrinh@gmail.com`

### n8n Webhook Config
- **Webhook URL:** `https://vpsn8n.anhlaptrinh.vn/webhook/dangkypythontudonghoacv1`
- **Zalo Notification:** Enabled

### Payment Code
- **Mã chuyển khoản:** `TDHCV343`
- **Số tiền:** `1,450,000 VNĐ`

## 🔧 Công Cụ Cloudflare

Tên miền được tạo bằng công cụ tự động trong `00.SubDomain_Cloudflare/`:

```bash
cd /root/00.SubDomain_Cloudflare
python3 cloudflare_dns.py tdhcv.anhlaptrinh.vn
```

## 📝 Lưu Ý

1. **DNS Propagation:** Sau khi tạo DNS record, có thể mất vài phút để DNS propagate. Thường là 1-5 phút.

2. **SSL Certificate:** Nếu cần HTTPS, cần cấu hình SSL certificate (Let's Encrypt) trên web server.

3. **Firewall:** Đảm bảo port 80 (HTTP) và 443 (HTTPS) đã được mở trên server.

4. **Backup:** Nên backup các file cấu hình trước khi deploy lên production.

## ✅ Checklist Trước Khi Deploy

- [ ] DNS record đã được tạo (✅ Đã hoàn thành)
- [ ] Files đã được upload lên server
- [ ] Web server đã được cấu hình đúng
- [ ] SSL certificate đã được cài đặt (nếu cần HTTPS)
- [ ] EmailJS và n8n webhook đã được cấu hình đúng
- [ ] Đã test form đăng ký hoạt động
- [ ] Đã test trên nhiều thiết bị (desktop, mobile)

## 📞 Hỗ Trợ

Nếu gặp vấn đề:
1. Kiểm tra DNS record tại Cloudflare Dashboard
2. Kiểm tra web server logs
3. Kiểm tra firewall rules
4. Test kết nối: `ping tdhcv.anhlaptrinh.vn`

---

**Ngày tạo:** $(date)
**Tên miền:** tdhcv.anhlaptrinh.vn
**IP Server:** 194.59.165.104


