# 🚀 Hướng Dẫn Thiết Lập 05tdhpython

## ✅ Đã Hoàn Thành

### 1. Tên Miền
- ✅ **Tên miền:** `tdhcv.anhlaptrinh.vn`
- ✅ **IP:** `194.59.165.104`
- ✅ **DNS Record:** Đã tạo thành công trên Cloudflare
- ✅ **Record ID:** `26b8900bb07275e9b27c4e80731f7166`

### 2. Cấu Hình Ứng Dụng
Ứng dụng đã được thiết lập tương tự như `01facebookads/` với đầy đủ các file:

#### Files Chính
- ✅ `index.html` - Trang chủ chính
- ✅ `device-emulator.html` - Device emulator
- ✅ `start-emulator.ps1` - Script khởi động (port 8007)
- ✅ `script.js` - JavaScript xử lý form đăng ký
- ✅ `style.css` - CSS styling
- ✅ `thanhtoan.html` - Trang thanh toán

#### Files Cấu Hình
- ✅ `email-config.js` - Cấu hình EmailJS
- ✅ `n8n-config.js` - Cấu hình n8n Webhook
- ✅ `logo.png` - Logo
- ✅ `ThuNhi_1450K_TDHCV343.png` - QR Code thanh toán

#### Tài Liệu
- ✅ `HUONG_DAN_CHAY_UNG_DUNG.md` - Hướng dẫn chi tiết
- ✅ `SETUP_DOMAIN.md` - Thông tin thiết lập tên miền
- ✅ `README_SETUP.md` - File này

## 🎯 So Sánh Với 01facebookads

| Tính năng | 01facebookads | 05tdhpython | Trạng thái |
|-----------|---------------|-------------|------------|
| Device Emulator | ✅ | ✅ | Hoàn thành |
| Form đăng ký | ✅ | ✅ | Hoàn thành |
| EmailJS | ✅ | ✅ | Hoàn thành |
| n8n Webhook | ✅ | ✅ | Hoàn thành |
| Trang thanh toán | ✅ | ✅ | Hoàn thành |
| Tên miền riêng | ❌ | ✅ `tdhcv.anhlaptrinh.vn` | **Hoàn thành** |

## 🚀 Cách Chạy

### Local Development

```powershell
cd /root/05tdhpython
.\start-emulator.ps1
```

Ứng dụng sẽ chạy tại: `http://localhost:8007/device-emulator.html`

### Production (Sau khi deploy)

Sau khi deploy lên server, ứng dụng sẽ có thể truy cập tại:
- `http://tdhcv.anhlaptrinh.vn`
- `https://tdhcv.anhlaptrinh.vn` (nếu đã cấu hình SSL)

## 📋 Thông Tin Cấu Hình

### EmailJS
- **Service ID:** `service_cdywck7`
- **Template ID:** `template_drxh4sf`
- **Email:** `nhuanlaptrinh@gmail.com`

### n8n Webhook
- **URL:** `https://vpsn8n.anhlaptrinh.vn/webhook/dangkypythontudonghoacv1`
- **Status:** Enabled

### Payment
- **Mã:** `TDHCV343`
- **Số tiền:** `1,450,000 VNĐ`

## 🔧 Công Cụ Tạo Tên Miền

Tên miền được tạo bằng công cụ tự động trong `00.SubDomain_Cloudflare/`:

```bash
cd /root/00.SubDomain_Cloudflare
python3 cloudflare_dns.py tdhcv.anhlaptrinh.vn
```

## 📝 Checklist Deploy

Trước khi deploy lên production:

- [x] DNS record đã được tạo
- [ ] Files đã được upload lên server
- [ ] Web server (Apache/Nginx) đã được cấu hình
- [ ] SSL certificate đã được cài đặt (nếu cần HTTPS)
- [ ] EmailJS và n8n webhook đã được test
- [ ] Form đăng ký đã được test
- [ ] Responsive design đã được test trên nhiều thiết bị

## 🆘 Troubleshooting

### DNS không hoạt động
1. Kiểm tra DNS record tại Cloudflare Dashboard
2. Đợi 5-10 phút để DNS propagate
3. Test: `ping tdhcv.anhlaptrinh.vn`

### Website không load
1. Kiểm tra web server đã chạy chưa
2. Kiểm tra firewall rules
3. Kiểm tra web server logs

### Form không gửi được
1. Kiểm tra EmailJS config trong `email-config.js`
2. Kiểm tra n8n webhook URL trong `n8n-config.js`
3. Kiểm tra console browser (F12) để xem lỗi

## 📞 Liên Hệ

- **Email:** contact@anhlaptrinh.vn
- **Website:** https://anhlaptrinh.vn

---

**Ngày thiết lập:** 2024
**Tên miền:** tdhcv.anhlaptrinh.vn
**IP Server:** 194.59.165.104


