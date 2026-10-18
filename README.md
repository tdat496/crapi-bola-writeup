# Phân Tích Chuỗi 7 Lỗ Hổng BOLA Trên OWASP crAPI

**Tác giả:** Nguyễn Trung Đạt  
**Ngày công bố:** 18/10/2026  
**Mức độ nghiêm trọng:** Critical (CVSS 9.3)  

---

## Giới thiệu
Repository này chứa báo cáo kiểm thử bảo mật chi tiết về ứng dụng crAPI (Completely Ridiculous API) của OWASP. Báo cáo phân tích chuỗi 7 lỗ hổng **Broken Object Level Authorization (BOLA)** - formerly known as IDOR.

## Tóm tắt 7 lỗ hổng đã phát hiện

| # | Endpoint | Mức độ | Mô tả ngắn gọn |
|---|----------|--------|----------------|
| 1 | `/service-report` | Medium | BOLA trên Service Report API |
| 2 | `/vehicle-service-dashboard` | Medium | BOLA trên Vehicle Dashboard |
| 3 | `/workshop/api/shop/orders` | **Critical** | Lộ thông tin thẻ tín dụng (Vi phạm PCI DSS) |
| 4 | `/community/api/v2/community/posts/recent` | **High** | Mass PII Disclosure |
| 5 | `/community/api/v2/community/posts/{postId}` | Medium | BOLA trên Chi tiết bài post |
| 6 | `/contact-mechanic` | **High** | BOLA gửi yêu cầu mạo danh |
| 7 | `/identity/api/v2/vehicle/{vehicleId}/location` | **Critical** | Real-time GPS Tracking |

## Cấu trúc Repository
- `resources/`: Chứa file báo cáo đầy đủ định dạng PDF.
- `screenshots/`: Chứa các hình ảnh minh chứng (PoC) cho từng lỗ hổng.
- `README.md`: File tóm tắt này.

## Xem báo cáo đầy đủ
Bạn có thể tải xuống hoặc xem báo cáo chi tiết tại: [Bao_Cao_BOLA_crAPI.pdf](./resources/Bao_Cao_BOLA_crAPI.pdf)

## Responsible Disclosure
Báo cáo này được công bố với mục đích giáo dục và nâng cao nhận thức bảo mật. 

## Liên hệ
- **Email:** trungdatnguyen9@gmail.com
- **GitHub:** tdat496

---
© 2026 Nguyễn Trung Đạt. All rights reserved.