# Crochet Main Service

## Giới thiệu

**Crochet Main Service** là hệ thống backend phục vụ cho ứng dụng web quản lý, bán sản phẩm và chia sẻ mẫu chart về đan/móc len (“Crochet”) – dành cho cộng đồng và cửa hàng Tieuphuong Crochet.

## Tính năng nổi bật

- Quản lý sản phẩm, thể loại, mẫu sản phẩm (products, categories, patterns)
- Quản lý mẫu chart miễn phí & trả phí (free/premium patterns)
- Xử lý đơn hàng, bình luận, bộ sưu tập, banner, thông báo
- Xác thực người dùng, phân quyền (OAuth2, JWT), xác minh email, đăng nhập qua Google, Facebook,...
- Quản lý hình ảnh, dữ liệu file qua Firebase Storage
- RESTful API tài liệu sẵn với Swagger UI (OpenAPI)
- Hỗ trợ bộ nhớ đệm, lịch trình tự động, gửi email, phân trang
- Dễ dàng tích hợp với microservices khác (Blog Service, ...)
- Đóng gói – triển khai nhanh qua Docker

## Công nghệ sử dụng

- **Java 21**, Spring Boot 3, Spring Data JPA, Spring Security, OAuth2
- **MySQL 8**, Hibernate, MapStruct, Caffeine Cache
- **JWT**, Firebase Admin, Resilience4j
- **Docker, Docker Compose** đóng gói toàn bộ services (MySQL, app backend)
- **Gradle** quản lý dự án/build
- **Swagger/OpenAPI** tài liệu hóa API tự động

## Hướng dẫn cài đặt & chạy nhanh

### 1. Yêu cầu môi trường

- Docker & Docker Compose
- (Tuỳ chọn) Java 21, MySQL 8 nếu chạy riêng lẻ

### 2. Chạy với Docker Compose

```bash
docker-compose up --build
```

- Ứng dụng backend lắng nghe tại: http://localhost:8081
- MySQL service: port 3306, user/pass: root/root, dbname: crochet_db

### 3. Xây dựng & chạy thủ công

```bash
./gradlew bootJar
java -jar build/libs/crochet.jar
```

### 4. Truy cập tài liệu API

Sau khi chạy thành công truy cập:

- Swagger: http://localhost:8081/swagger-ui.html

## Thông tin liên hệ

- Website: [https://www.tieuphuongcrochet.com](https://www.tieuphuongcrochet.com)
- Email hỗ trợ: thamphuong.crochet@gmail.com

---

> ⓘ Đóng góp mã nguồn và phản hồi xin gửi GitHub hoặc qua email liên hệ bên trên!
