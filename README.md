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


🎯 Giới thiệu tính năng

  👤 Người dùng

    Đăng ký, đăng nhập với bảo mật (Spring Security)

    Cập nhật thông tin cá nhân, xem lịch sử đơn hàng

    Tìm kiếm sản phẩm theo từ khóa, hãng, mức giá

    Xem chi tiết sản phẩm (ảnh, thông số)

    Thêm vào giỏ hàng và đặt mua

    Xác thực tài khoản qua email: Gửi liên kết kích hoạt tài khoản khi người dùng đăng ký.

    Xác nhận đơn hàng qua email: Gửi chi tiết đơn hàng sau khi người dùng đặt mua thành công.

  🛒 Quản trị viên

    Truy cập dashboard quản trị

    Thêm / sửa / xóa sản phẩm

    Quản lý đơn hàng và người dùng

    Xem thống kê bán hàng
    
📁 Cấu trúc dự án

      CD1_JavaWeb_SmartphoneStore/
      ├── .mvn/                           # Maven Wrapper cấu hình
      │
      ├── src/
      │   └── main/
      │       ├── java/com/poly/app/     # Mã nguồn chính
      │       │   ├── Impl/              # Triển khai các lớp service (implements)
      │       │   ├── config/            # Cấu hình ứng dụng (Spring Config, Security, ...)
      │       │   ├── controller/        # Các controller xử lý request (Spring MVC)
      │       │   ├── dto/               # Các lớp Data Transfer Object (DTO)
      │       │   ├── entity/            # Các lớp Entity ánh xạ bảng CSDL (JPA/Hibernate)
      │       │   ├── repository/        # Interface tương tác với CSDL (Spring Data JPA)
      │       │   ├── service/           # Interface định nghĩa logic nghiệp vụ
      │       │   ├── util/              # Các lớp tiện ích dùng chung (Utils, Constants, ...)
      │       │   ├── AssignmentHtMobileApplication.java  # Lớp main khởi động Spring Boot
      │       │   └── ServletInitializer.java             # Khởi tạo servlet khi deploy WAR
      │
      │       └── resources/
      │           ├── i18n/              # Thư mục chứa file đa ngôn ngữ (quốc tế hóa)
      │           │   ├── layout.properties         # Tiếng Anh
      │           │   └── layout_vi.properties      # Tiếng Việt
      │           ├── static/            # Tài nguyên tĩnh (CSS/JS/JSP)
      │           │   └── css.jsp
      │           └── application.properties        # Cấu hình ứng dụng (port, db, mail,...)
      │
      │       └── webapp/                # Thư mục web root (dành cho JSP project)
      │           ├── WEB-INF/
      │           │   └── views/         # View JSP (trong WEB-INF, bảo mật không truy cập trực tiếp)
      │           ├── css/               # Tệp CSS giao diện
      │           ├── document/          # Tài liệu, PDF,...
      │           ├── fonts/             # Fonts giao diện
      │           ├── img/               # Ảnh giao diện
      │           ├── js/                # JavaScript
      │           └── taglib/            # Các taglib tuỳ chỉnh dùng trong JSP
      │
      ├── htmobilescript.sql             # Script tạo và khởi tạo CSDL
      ├── .gitignore                     # Loại trừ file/thư mục khi đẩy lên Git
      ├── README.md                      # Giới thiệu và hướng dẫn dự án
      └── pom.xml                        # Tệp khai báo dependencies và plugin Maven
      

🛠️ Công nghệ sử dụng

      Backend: Java 17, Spring Boot, Spring Security, JPA (Hibernate),Spring Mail(JavaMailSender)
      
      Frontend: JSP, HTML, CSS, JavaScript
      
      Database: SQL Server
  
      Xây dựng: Maven
  
      IDE: IntelliJ IDEA / Eclipse


⚙️ Yêu cầu cài đặt

  Trước khi cài đặt, đảm bảo bạn đã cài:

  | 🛠️ Công cụ                             | ✅ Phiên bản khuyến nghị | 📌 Ghi chú                                 |
  | --------------------------------------- | ----------------------- | ------------------------------------------ |
  | **Java JDK**                            | 17 trở lên              | Bắt buộc, nên dùng bản LTS                 |
  | **Maven**                               | 3.8.x trở lên           | Dùng để quản lý thư viện và build dự án    |
  | **SQL Server**                          | 2019 hoặc 2022          | Dùng làm cơ sở dữ liệu chính               |
  | **SQL Server Management Studio (SSMS)** | Mới nhất                | Tuỳ chọn nhưng rất hữu ích để quản lý CSDL |
  | **IntelliJ IDEA / Eclipse**             | Mới nhất                | Dùng để lập trình Java Spring Boot         |
  | **Git**                                 | Mới nhất                | Clone source code từ GitHub                |
  


🚀 Hướng dẫn cài đặt dự án

  Bước 1: Clone dự án
  
        git clone https://github.com/tam150105/CD1_JavaWeb_SmartphoneStore.git
        cd CD1_JavaWeb_SmartphoneStore
    
  Bước 2: Tạo cơ sở dữ liệu và cấu hình
  
   Tạo database:
    
        Bước 1: Mở SQL Server Management Studio (SSMS) hoặc công cụ tương đương.
        Bước 2: Mở file htmobilescript.sql (có sẵn trong dự án) bằng SSMS.
        Nước 3: Chạy toàn bộ script để tạo bảng, quan hệ và dữ liệu mẫu.
        
   Cấu hình file src/main/resources/application.properties:

    server.port = your_post
    spring.datasource.url=jdbc:sqlserver://localhost:your_port;databaseName=HTMOBILE;encrypt=true;trustServerCertificate=true
    spring.datasource.username=your_username
    spring.datasource.password=your_password_here

   Giải thích:
   
    server.port: Thay bằng số cổng mà bạn muốn ứng dụng Spring Boot sẽ chạy (ví dụ: 8080, 8081,...).
    your_port: Thay bằng số cổng SQL Server của bạn (mặc định là 1433).
    your_username: Thay bằng tên đăng nhập SQL Server.
    your_password_here: Thay bằng mật khẩu tương ứng.

   Ví dụ: 
   
    server.port = 8081
    spring.datasource.url = jdbc:sqlserver://localhost:1433;databaseName=HTMOBILE ;encrypt=true;trustServerCertificate=true
    spring.datasource.username = sa
    spring.datasource.password = 15012005


![Screenshot 2025-05-16 225539](https://github.com/user-attachments/assets/71d97253-d155-410c-a762-0913910e2df9)


Bước 3: Build dự án bằng Maven
Cách thực hiện:
Mở Terminal (Linux/macOS) hoặc Command Prompt (Windows).

Dùng lệnh cd để chuyển vào thư mục chứa dự án.

    cd đường_dẫn_đến_thư_mục_dự_án

Ví dụ:

    cd C:\Users\Bạn\Projects\CD1_JavaWeb_SmartphoneStore
Sau đó chạy lệnh:

    mvn clean install

Bước 4: Chạy ứng dụng

Mở Eclipse IDE/IntelliJ IDEA và chạy file SmartphoneStoreApplication.java. 


![Screenshot 2025-05-16 231202](https://github.com/user-attachments/assets/1eaf36b6-4b11-4bcd-83f6-419a005b6d7e)


Bước 5: Truy cập giao diện web
Mở trình duyệt và tìm kiếm:

    http://localhost:8080


🤝 Đóng góp
Chào mừng mọi đóng góp!
Các bước thực hiện:

# 1. Fork dự án
# 2. Tạo nhánh mới
    git checkout -b feature/ten-tinh-nang

# 3. Commit thay đổi
    git commit -m "Thêm tính năng abc"

# 4. Push lên GitHub
    git push origin feature/ten-tinh-nang

# 5. Tạo Pull Request





