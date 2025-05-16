# CĐ1_JavaWeb_SmartphoneStore
📱 Smartphone Store – Dự án Website Bán Điện Thoại Java Spring Boot
Chào mừng đến với Smartphone Store, một ứng dụng web thương mại điện tử được xây dựng bằng Java Spring Boot kết hợp với MySQL, hỗ trợ bán điện thoại trực tuyến với tính năng quản lý sản phẩm, đơn hàng, người dùng và phân quyền rõ ràng.

🔗 Link GitHub dự án:
👉 https://github.com/tam150105/CD1_JavaWeb_SmartphoneStore.git

📚 Mục Lục

  🎯 Giới thiệu tính năng

  📁 Cấu trúc dự án

  🛠️ Công nghệ sử dụng

  ⚙️ Yêu cầu cài đặt

  🚀 Hướng dẫn cài đặt dự án

    Bước 1: Clone dự án

    Bước 2: Tạo cơ sở dữ liệu và cấu hình

    Bước 3: Build dự án bằng Maven

    Bước 4: Chạy ứng dụng

    Bước 5: Truy cập giao diện web

    Bước 6: Thêm dữ liệu mẫu (tuỳ chọn)


🎯 Giới thiệu tính năng
👤 Người dùng
  Đăng ký, đăng nhập với bảo mật (Spring Security)

  Cập nhật thông tin cá nhân, xem lịch sử đơn hàng

  Tìm kiếm sản phẩm theo từ khóa, hãng, mức giá

  Xem chi tiết sản phẩm (ảnh, thông số)

  Thêm vào giỏ hàng và đặt mua

🛒 Quản trị viên
Truy cập dashboard quản trị

Thêm / sửa / xóa sản phẩm

Quản lý đơn hàng và người dùng

Xem thống kê bán hàng

🌐 Giao diện
Giao diện responsive (hỗ trợ cả máy tính và điện thoại)

Giao diện KHÔNG dùng Thymeleaf (tách frontend)

🛠️ Công nghệ sử dụng
Backend: Java 17, Spring Boot, Spring Security, Spring MVC, JPA (Hibernate)

Database: MySQL 8+

Xây dựng: Maven

IDE: IntelliJ IDEA / Eclipse

Thư viện khác: Lombok, MySQL Connector/J

⚙️ Yêu cầu cài đặt
Trước khi cài đặt, đảm bảo bạn đã cài:

Công cụ	Phiên bản khuyến nghị
Java JDK	17 trở lên
Maven	3.8.x trở lên
MySQL Server	8.0 trở lên
MySQL Workbench	(tuỳ chọn)
IntelliJ IDEA / Eclipse	Mới nhất
Git	Mới nhất

🚀 Hướng dẫn cài đặt dự án
Bước 1: Clone dự án
bash
Sao chép
Chỉnh sửa
git clone https://github.com/tam150105/CD1_JavaWeb_SmartphoneStore.git
cd CD1_JavaWeb_SmartphoneStore
📷 Chèn ảnh: Terminal sau khi clone thành công.

Bước 2: Tạo cơ sở dữ liệu và cấu hình
Mở MySQL Workbench hoặc công cụ tương đương.

Tạo database:

sql
Sao chép
Chỉnh sửa
CREATE DATABASE smartphone_store;
Cấu hình file src/main/resources/application.properties:

properties
Sao chép
Chỉnh sửa
spring.datasource.url=jdbc:mysql://localhost:3306/smartphone_store
spring.datasource.username=your_username
spring.datasource.password=your_password
spring.jpa.hibernate.ddl-auto=update
✅ Nếu bạn dùng port khác (ví dụ 3307):

properties
Sao chép
Chỉnh sửa
spring.datasource.url=jdbc:mysql://localhost:3307/smartphone_store
📷 Chèn ảnh: File application.properties đã cập nhật (ẩn thông tin nhạy cảm).

Bước 3: Build dự án bằng Maven
bash
Sao chép
Chỉnh sửa
mvn clean install
📷 Chèn ảnh: Terminal hiển thị BUILD SUCCESS.

Bước 4: Chạy ứng dụng
bash
Sao chép
Chỉnh sửa
mvn spring-boot:run
Hoặc chạy file SmartphoneStoreApplication.java từ IDE.

📷 Chèn ảnh: Console IDE hoặc terminal hiển thị Started SmartphoneStoreApplication.

Bước 5: Truy cập giao diện web
Mở trình duyệt:

arduino
Sao chép
Chỉnh sửa
http://localhost:8080
Nếu frontend dùng riêng (React/Vue/HTML), hãy build hoặc mở frontend theo hướng dẫn của bạn.

Đăng nhập bằng tài khoản đã có trong DB hoặc tự đăng ký.

📷 Chèn ảnh: Giao diện trang chủ website trên trình duyệt.

Bước 6: Thêm dữ liệu mẫu (tuỳ chọn)
Có thể thêm dữ liệu vào DB thủ công hoặc thông qua giao diện admin.

Nếu có file data.sql, dữ liệu mẫu sẽ tự động import.

📷 Chèn ảnh: Sản phẩm mẫu hiển thị trong DB hoặc admin dashboard.

📁 Cấu trúc dự án
bash
Sao chép
Chỉnh sửa
├── src
│   ├── main
│   │   ├── java/com/example/smartphonestore
│   │   │   ├── config         # Cấu hình Spring
│   │   │   ├── controller     # Controller xử lý yêu cầu
│   │   │   ├── model          # Entity JPA
│   │   │   ├── repository     # Giao tiếp DB (JPA)
│   │   │   ├── service        # Xử lý nghiệp vụ
│   │   │   └── SmartphoneStoreApplication.java
│   │   └── resources
│   │       ├── static         # Tài nguyên tĩnh (nếu có)
│   │       ├── application.properties
│   │       └── data.sql       # Dữ liệu mẫu (tuỳ chọn)
├── pom.xml                   # Quản lý dependencies
└── README.md                 # Tài liệu hướng dẫn
🧑‍💻 Hướng dẫn sử dụng
👤 Người dùng
Truy cập website, đăng ký tài khoản

Tìm kiếm, chọn sản phẩm

Thêm vào giỏ, đặt hàng, xem lịch sử đơn

🛠️ Admin
Truy cập /admin để:

Quản lý sản phẩm

Xử lý đơn hàng

Quản lý người dùng

Xem báo cáo thống kê

📷 Chèn ảnh: Giao diện người dùng và giao diện admin.

🤝 Đóng góp
Chào mừng mọi đóng góp!
Các bước thực hiện:

bash
Sao chép
Chỉnh sửa
# 1. Fork dự án
# 2. Tạo nhánh mới
git checkout -b feature/ten-tinh-nang

# 3. Commit thay đổi
git commit -m "Thêm tính năng abc"

# 4. Push lên GitHub
git push origin feature/ten-tinh-nang

# 5. Tạo Pull Request
📄 Giấy phép
Dự án sử dụng MIT License – tự do sử dụng, sửa đổi, phân phối.

Nếu bạn cần mình xuất file README.md gốc, hoặc tạo bộ ảnh minh họa mẫu để bạn dán vào, chỉ cần nói nhé!







Bạn đã nói:
ứng dụng tôi có tính năng gởi mnail xác nhận đặt hành thành công cũng như xác thực tài khoản nữa


ChatGPT đã nói:
Đã cập nhật bộ nhớ đã lưu
Tuyệt vời! Dưới đây là phần cập nhật cho mục Giới thiệu tính năng và các phần liên quan trong file README.md để thể hiện rõ rằng ứng dụng có hỗ trợ:

✅ Gửi email xác nhận đơn hàng sau khi đặt hàng thành công.

✅ Gửi email xác thực tài khoản khi đăng ký.

🎯 Giới thiệu tính năng (bổ sung)
📧 Email xác nhận & xác thực
Xác thực tài khoản qua email: Gửi liên kết kích hoạt tài khoản khi người dùng đăng ký.

Xác nhận đơn hàng qua email: Gửi chi tiết đơn hàng sau khi người dùng đặt mua thành công.

📷 Chèn ảnh: Email xác thực tài khoản trong hộp thư đến & email xác nhận đơn hàng với thông tin chi tiết.

⚙️ Yêu cầu thêm
Đảm bảo cấu hình SMTP trong application.properties để gửi email, ví dụ với Gmail:

properties
Sao chép
Chỉnh sửa
spring.mail.host=smtp.gmail.com
spring.mail.port=587
spring.mail.username=your_email@gmail.com
spring.mail.password=your_app_password
spring.mail.properties.mail.smtp.auth=true
spring.mail.properties.mail.smtp.starttls.enable=true
💡 Lưu ý: Không sử dụng mật khẩu Gmail thật. Tạo App Password nếu dùng Gmail.

📷 Chèn ảnh: Màn hình cấu hình email trong application.properties.

Nếu bạn muốn, mình có thể giúp bạn viết lại đoạn README hoàn chỉnh với phần gửi email tích hợp, hoặc tạo file cấu hình mẫu cho phần xác nhận/SMTP. Bạn cần không?







Bạn đã nói:
hãy viết lại 1 file readme hoàn chỉnh


ChatGPT đã nói:
Dưới đây là nội dung hoàn chỉnh của file README.md dành cho dự án Web bán điện thoại - Java Spring Boot, không sử dụng Thymeleaf, có hỗ trợ gửi email xác nhận đơn hàng và xác thực tài khoản. Phần nội dung được trình bày rõ ràng, sinh động, có chỗ để bạn dán ảnh minh họa:

📱 Smartphone Store - Ứng dụng web bán điện thoại bằng Java Spring Boot
Chào mừng bạn đến với Smartphone Store – một ứng dụng thương mại điện tử được xây dựng với Java Spring Boot. Ứng dụng cung cấp nền tảng quản lý và bán điện thoại trực tuyến hiện đại, dễ sử dụng, bảo mật cao, có tích hợp tính năng gửi email xác nhận đơn hàng và xác thực tài khoản người dùng.

🔗 Link GitHub: https://github.com/tam150105/CD1_JavaWeb_SmartphoneStore.git

📚 Mục lục
🎯 Giới thiệu dự án

🚀 Tính năng

🧰 Công nghệ sử dụng

⚙️ Yêu cầu hệ thống

🛠️ Hướng dẫn cài đặt

📂 Cấu trúc dự án

💡 Sử dụng

🤝 Đóng góp

📄 Giấy phép

🎯 Giới thiệu dự án
Smartphone Store là một ứng dụng web thương mại điện tử với đầy đủ chức năng: đăng ký, đăng nhập, duyệt sản phẩm, giỏ hàng, đặt hàng, quản trị sản phẩm & đơn hàng, và gửi email xác nhận.

Ứng dụng không sử dụng Thymeleaf – frontend được triển khai qua API REST và giao diện riêng (có thể tích hợp frontend như React, Vue hoặc HTML/CSS/JS thuần).

🚀 Tính năng
👤 Quản lý người dùng
Đăng ký tài khoản có xác thực email.

Đăng nhập bảo mật.

Cập nhật thông tin cá nhân.

Xem lịch sử đơn hàng.

📷 Chèn ảnh: giao diện đăng ký và email xác thực tài khoản.

📱 Quản lý sản phẩm
Duyệt danh sách điện thoại.

Lọc theo hãng, giá, cấu hình.

Xem chi tiết sản phẩm.

Thêm vào giỏ hàng / yêu thích.

📷 Chèn ảnh: giao diện trang sản phẩm và chi tiết sản phẩm.

🛒 Quản lý đơn hàng
Đặt hàng nhanh chóng.

Gửi email xác nhận đơn hàng.

Xem chi tiết và trạng thái đơn hàng.

📷 Chèn ảnh: email xác nhận đơn hàng và giao diện đơn hàng.

🔐 Bảo mật & phân quyền
Spring Security + mã hóa mật khẩu.

Phân quyền người dùng và admin.

🛠️ Trang quản trị (Admin)
Thêm / sửa / xóa sản phẩm.

Quản lý đơn hàng và người dùng.

Xem báo cáo doanh thu.

📷 Chèn ảnh: giao diện admin quản lý sản phẩm và đơn hàng.

🧰 Công nghệ sử dụng
Thành phần	Công nghệ
Ngôn ngữ	Java 17
Backend	Spring Boot, Spring MVC, Spring Security, Spring Data JPA
Giao tiếp frontend	RESTful API
Cơ sở dữ liệu	MySQL 8+
Build Tool	Maven
IDE đề xuất	IntelliJ IDEA
Khác	Hibernate, Lombok, JavaMailSender

⚙️ Yêu cầu hệ thống
Java JDK 17+

Maven 3.8+

MySQL 8.0+

Git

IDE (IntelliJ IDEA / Eclipse / VS Code)

MySQL Workbench (tùy chọn)

🛠️ Hướng dẫn cài đặt
Bước 1: Clone dự án
bash
Sao chép
Chỉnh sửa
git clone https://github.com/tam150105/CD1_JavaWeb_SmartphoneStore.git
cd CD1_JavaWeb_SmartphoneStore
📷 Chèn ảnh: clone repo thành công trong terminal.

Bước 2: Cấu hình CSDL
Tạo CSDL smartphone_store bằng MySQL Workbench hoặc dòng lệnh:

sql
Sao chép
Chỉnh sửa
CREATE DATABASE smartphone_store;
Cập nhật thông tin kết nối trong src/main/resources/application.properties:

properties
Sao chép
Chỉnh sửa
spring.datasource.url=jdbc:mysql://localhost:3306/smartphone_store
spring.datasource.username=your_username
spring.datasource.password=your_password
spring.jpa.hibernate.ddl-auto=update
📌 Nếu dùng cổng khác (ví dụ 3307):

properties
Sao chép
Chỉnh sửa
spring.datasource.url=jdbc:mysql://localhost:3307/smartphone_store
📷 Chèn ảnh: file application.properties có phần cấu hình CSDL.

Bước 3: Cấu hình gửi email
Thêm thông tin cấu hình SMTP để gửi email xác nhận:

properties
Sao chép
Chỉnh sửa
spring.mail.host=smtp.gmail.com
spring.mail.port=587
spring.mail.username=your_email@gmail.com
spring.mail.password=your_app_password
spring.mail.properties.mail.smtp.auth=true
spring.mail.properties.mail.smtp.starttls.enable=true
📷 Chèn ảnh: giao diện email xác nhận đơn hàng và email kích hoạt tài khoản.

⚠️ Lưu ý: Dùng App Password nếu sử dụng Gmail, không dùng mật khẩu tài khoản chính.

Bước 4: Build dự án
bash
Sao chép
Chỉnh sửa
mvn clean install
📷 Chèn ảnh: terminal hiển thị build thành công.

Bước 5: Chạy ứng dụng
bash
Sao chép
Chỉnh sửa
mvn spring-boot:run
Hoặc chạy SmartphoneStoreApplication.java từ IDE.

Ứng dụng mặc định chạy tại: http://localhost:8080

📷 Chèn ảnh: console log “Started SmartphoneStoreApplication”.

Bước 6: Nhập dữ liệu mẫu (tuỳ chọn)
Chạy script SQL trong src/main/resources/data.sql

Hoặc dùng giao diện admin để thêm dữ liệu.

📷 Chèn ảnh: dữ liệu sản phẩm hiển thị trong admin.

📂 Cấu trúc dự án
bash
Sao chép
Chỉnh sửa
src
├── main
│   ├── java/com/example/smartphonestore
│   │   ├── config         # Cấu hình Spring
│   │   ├── controller     # Controller REST/API
│   │   ├── model          # Entity JPA
│   │   ├── repository     # Repository JPA
│   │   ├── service        # Business logic
│   │   └── SmartphoneStoreApplication.java
│   └── resources
│       ├── static         # Tài nguyên tĩnh (nếu có)
│       ├── application.properties
│       └── data.sql       # Dữ liệu mẫu (tuỳ chọn)
└── pom.xml                # Maven cấu hình
