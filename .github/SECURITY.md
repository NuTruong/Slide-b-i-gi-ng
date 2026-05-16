# 🔒 Chính Sách Bảo Mật (Security Policy)

## 📋 Mục Đích

Tài liệu này mô tả chính sách bảo mật của dự án **Slide-b-i-gi-ng**, bao gồm cách chúng tôi xử lý các vấn đề bảo mật, quy trình báo cáo lỗi bảo mật, và các biện pháp bảo vệ được áp dụng.

---

## 🚨 Báo Cáo Lỗi Bảo Mật (Reporting Security Vulnerabilities)

### ⚠️ QUAN TRỌNG

**VUI LÒNG KHÔNG** tạo public issue để báo cáo lỗi bảo mật. Điều này có thể cho phép những người không lành mạnh khai thác lỗi trước khi chúng tôi có cơ hội fix.

### 📧 Cách Báo Cáo An Toàn

Nếu bạn phát hiện lỗi bảo mật, vui lòng báo cáo bằng cách gửi email **bí mật** tới:

**📧 Email:** `quynhluu869@gmail.com`

**Tiêu đề email nên bắt đầu với:** `[SECURITY]` hoặc `[BẢO MẬT]`

### 📝 Thông Tin Cần Cung Cấp

Vui lòng bao gồm các thông tin sau trong báo cáo:

1. **Mô tả lỗi** - Mô tả chi tiết về lỗi bảo mật là gì
2. **Ảnh hưởng** - Mức độ nghiêm trọng (Thấp, Trung, Cao, Tối cao)
3. **Cách tái hiện** - Các bước cụ thể để tái hiện lỗi
4. **Phiên bản bị ảnh hưởng** - Phiên bản nào của dự án bị ảnh hưởng
5. **Cách fix** - Nếu bạn có giải pháp được đề xuất
6. **Thông tin liên hệ** - Cách chúng tôi có thể liên lạc với bạn

### 📋 Mẫu Email Báo Cáo

```
To: quynhluu869@gmail.com
Subject: [SECURITY] Lỗi bảo mật trong Slide-b-i-gi-ng

Mô tả lỗi:
[Mô tả chi tiết]

Mức độ nghiêm trọng:
[Thấp / Trung / Cao / Tối cao]

Cách tái hiện:
1. Bước 1
2. Bước 2
3. Bước 3

Phiên bản bị ảnh hưởng:
[Ví dụ: v1.0.0 và các phiên bản trước]

Giải pháp được đề xuất:
[Nếu có]

Thông tin liên hệ:
[Tên, email, số điện thoại (tùy chọn)]
```

---

## ⏱️ Quy Trình Xử Lý (Response Process)

### Timeline Mong Đợi

| Giai Đoạn | Thời Gian | Mô Tả |
|-----------|----------|-------|
| **Xác Nhận** | 24-48 giờ | Chúng tôi sẽ xác nhận nhận được báo cáo của bạn |
| **Đánh Giá** | 1-3 ngày | Xác minh lỗi và đánh giá mức độ nghiêm trọng |
| **Phát Triển Fix** | 3-7 ngày | Phát triển và kiểm tra patch fix |
| **Phát Hành** | 7-14 ngày | Phát hành phiên bản patch/fix |
| **Công Bố** | Sau fix | Công bố chi tiết lỗi sau khi fix đã phát hành |

### Các Bước Chi Tiết

1. **Nhận Báo Cáo** 📥
   - Chúng tôi sẽ gửi email xác nhận
   - Gán một mã theo dõi (tracking ID)

2. **Xác Minh Lỗi** 🔍
   - Tái hiện lỗi trên các phiên bản khác nhau
   - Xác định phạm vi ảnh hưởng
   - Đánh giá mức độ nguy hiểm

3. **Phát Triển Patch** 🛠️
   - Tạo fix hoặc workaround
   - Kiểm tra kỹ lưỡng
   - Yêu cầu bạn xác minh fix (nếu có thể)

4. **Chuẩn Bị Phát Hành** 📦
   - Tạo patch/minor/major release tùy tình huống
   - Cập nhật CHANGELOG
   - Viết release notes

5. **Công Bố Lỗi** 📢
   - Công bố chi tiết lỗi sau khi fix phát hành
   - Ghi nhận người báo cáo (nếu đồng ý)

---

## 🔐 Biện Pháp Bảo Mật Hiện Tại (Current Security Measures)

### Phiên Bản Python
- ✅ Yêu cầu Python 3.7+ (có hỗ trợ bảo mật)
- ✅ Không hỗ trợ Python 2.7 (EOL)

### Quản Lý Dependencies
- ✅ Sử dụng `requirements.txt` để kiểm soát phiên bản
- ✅ Các package được chọn từ PyPI chính thức
- ✅ Tránh sử dụng package không đáng tin cậy

### Kiểm Tra Code
- ✅ Code review trước khi merge
- ✅ Tuân theo [CONTRIBUTING.md](../CONTRIBUTING.md)
- ✅ Kiểm tra code cho lỗi phổ biến

### Input Validation
- ✅ Kiểm tra định dạng file đầu vào (JSON, CSV, Markdown)
- ✅ Tránh SQL injection (không sử dụng SQL)
- ✅ Xử lý lỗi file safely

### Xử Lý Dữ Liệu
- ✅ Không lưu trữ dữ liệu nhạy cảm
- ✅ Dữ liệu được xử lý cục bộ
- ✅ Không gửi dữ liệu tới server bên thứ ba (ngoại trừ API công khai)

---

## 🆚 Các Phiên Bản Được Hỗ Trợ (Supported Versions)

### Bảo Mật Patch

| Phiên Bản | Trạng Thái | Kết Thúc Hỗ Trợ |
|-----------|----------|----------------|
| **1.x.x** | ✅ Hoạt Động | Đang hỗ trợ |
| **0.9.x** | ⚠️ Cũ | 3 tháng kể từ bây giờ |
| **0.8.x** | ❌ EOL | Không còn hỗ trợ |
| **< 0.8** | ❌ EOL | Không còn hỗ trợ |

**Chú ý:** Chúng tôi chỉ phát hành bảo mật patch cho phiên bản hiện tại và phiên bản trước gần đây nhất.

---

## 🛡️ Các Lỗi Bảo Mật Phổ Biến (Common Vulnerabilities)

### Lỗi Chúng Tôi Theo Dõi

1. **Path Traversal** 🚫
   - Kiểm tra: Đầu vào không hợp lệ không thể truy cập các file ngoài thư mục cho phép
   - Status: Được kiểm tra ✅

2. **Command Injection** 🚫
   - Kiểm tra: Không thực hiện shell commands với input từ user
   - Status: Được kiểm tra ✅

3. **XML External Entity (XXE)** 🚫
   - Kiểm tra: XML parsing không cho phép external entities
   - Status: Không áp dụng (không dùng XML) ✅

4. **Insecure Deserialization** 🚫
   - Kiểm tra: Không dùng pickle hoặc cơ chế deserialization không an toàn
   - Status: Được kiểm tra ✅

5. **Hardcoded Credentials** 🚫
   - Kiểm tra: Không có password hoặc key được hardcode
   - Status: Được kiểm tra ✅

---

## 🔄 Cập Nhật Bảo Mật (Security Updates)

### Khi Có Lỗi Bảo Mật

1. **Patch Release** 🔧
   - Phát hành patch (v1.0.x → v1.0.x+1)
   - Ưu tiên cao
   - Khuyến cáo tất cả người dùng nâng cấp

2. **Thông Báo** 📢
   - GitHub Security Advisory
   - Release notes
   - Email tới followers (nếu có)

3. **Documentation** 📝
   - CHANGELOG cập nhật
   - Hướng dẫn upgrade
   - Workaround (nếu có)

### Cách Nâng Cấp

```bash
# Cập nhật đến phiên bản mới nhất
git pull origin main
pip install --upgrade -r requirements.txt
```

---

## 📋 Checklist Bảo Mật (Security Checklist)

### Trước Mỗi Release

- [ ] Kiểm tra tất cả dependencies có cập nhật bảo mật
- [ ] Chạy linter và static analysis
- [ ] Kiểm tra không có hardcoded credentials
- [ ] Xem xét tất cả thay đổi code
- [ ] Cập nhật CHANGELOG với các sửa chữa bảo mật
- [ ] Kiểm tra file permissions
- [ ] Xóa debug code
- [ ] Kiểm tra error handling

### Bảo Mật Cộng Đồng

- [ ] Tuân thủ [Code of Conduct](../CODE_OF_CONDUCT.md)
- [ ] Kiểm tra không có malware hoặc code độc hại
- [ ] Xác minh source code
- [ ] Kiểm tra pull request trước merge

---

## 🔗 Liên Kết Liên Quan (Related Resources)

### Bảo Mật Python
- [Python Security Warnings](https://docs.python.org/3/library/security_warnings.html)
- [OWASP Top 10](https://owasp.org/www-project-top-ten/)
- [CWE Top 25](https://cwe.mitre.org/top25/)

### GitHub Security
- [GitHub Security Best Practices](https://docs.github.com/en/code-security)
- [GitHub Security Advisory](https://docs.github.com/en/code-security/repository-security-advisories)
- [Dependabot](https://docs.github.com/en/code-security/dependabot)

### Cộng Đồng Python
- [PyPI Security](https://pypi.org/security/)
- [Python Package Security](https://www.python.org/dev/peps/pep-0426/)

---

## 💬 FAQ Bảo Mật (Security FAQ)

### Q: Dữ liệu của tôi có được gửi tới server bên thứ ba không?
**A:** Không. Dữ liệu được xử lý hoàn toàn cục bộ. Chúng tôi không gửi dữ liệu của bạn tới bất kỳ server nào ngoại trừ:
- GitHub (để lưu trữ code)
- PyPI (để tải package)
- (Tùy chọn) External APIs nếu bạn cấu hình (ví dụ: API hình ảnh)

### Q: Dự án này có được audit bảo mật không?
**A:** Hiện tại chưa. Nhưng chúng tôi đón chào security audit từ cộng đồng.

### Q: Tôi phát hiện lỗi bảo mật, phải làm gì?
**A:** Gửi email bí mật tới `quynhluu869@gmail.com` với tiêu đề `[SECURITY]`

### Q: Tôi có thể lên lịch security call không?
**A:** Có, vui lòng email tới `quynhluu869@gmail.com` để yêu cầu.

### Q: Bạn có bug bounty program không?
**A:** Hiện tại không, nhưng chúng tôi sẽ ghi nhận công việc của bạn trong CHANGELOG.

---

## 🤝 Cảm Ơn

Cảm ơn bạn vì quan tâm đến bảo mật của dự án **Slide-b-i-gi-ng**. Bảo mật là trách nhiệm chung của chúng ta, và chúng tôi đánh giá cao sự giúp đỡ của bạn.

---

**Phiên bản:** 1.0  
**Cập nhật lần cuối:** 2026-05-16  
**Liên hệ:** quynhluu869@gmail.com
