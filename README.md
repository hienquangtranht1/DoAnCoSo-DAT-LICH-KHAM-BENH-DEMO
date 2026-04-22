<div align="center">
  <h1>🏥 Hệ Thống Đặt Lịch Khám Bệnh Trực Tuyến</h1>
  <p><i>(Hospitals Booking System)</i></p>
  
  <br />

  <img src="https://img.shields.io/badge/PHP-777BB4?style=for-the-badge&logo=php&logoColor=white" alt="PHP" />
  <img src="https://img.shields.io/badge/MySQL-005C84?style=for-the-badge&logo=mysql&logoColor=white" alt="MySQL" />
  <img src="https://img.shields.io/badge/HTML5-E34F26?style=for-the-badge&logo=html5&logoColor=white" alt="HTML5" />
  <img src="https://img.shields.io/badge/CSS3-1572B6?style=for-the-badge&logo=css3&logoColor=white" alt="CSS3" />
  <img src="https://img.shields.io/badge/JavaScript-F7DF1E?style=for-the-badge&logo=javascript&logoColor=black" alt="JavaScript" />

</div>

---

## 📖 Mô tả dự án

**Hospitals Booking System** là một ứng dụng web toàn diện được thiết kế nhằm số hóa quy trình đặt lịch khám bệnh, kết nối bệnh nhân và cơ sở y tế một cách hiệu quả. Hệ thống tập trung vào việc tối ưu hóa trải nghiệm người dùng trong việc tìm kiếm chuyên khoa, đặt lịch và tương tác trực tiếp với đội ngũ y bác sĩ, chăm sóc khách hàng.

---

## 📑 Mục lục
- [Các tính năng cốt lõi](#-các-tính-năng-cốt-lõi)
- [Công nghệ sử dụng](#-công-nghệ-sử-dụng)
- [Cấu trúc thư mục (MVC)](#-cấu-trúc-thư-mục-mvc)
- [Vai trò trong dự án](#-vai-trò-trong-dự-án)
- [Hướng dẫn cài đặt](#-hướng-dẫn-cài-đặt)

---

## ✨ Các tính năng cốt lõi

### 📅 1. Quản lý đặt lịch (Booking Management)
- Bệnh nhân có thể tra cứu và chọn chuyên khoa *(Tim mạch, Khám tổng quát...)*.
- Chủ động chọn ngày, giờ khám bệnh phù hợp với lịch trình cá nhân.
- Gửi yêu cầu và nhận xác nhận đặt lịch khám trực tuyến nhanh chóng.

### 🤖 2. Hệ thống tương tác thông minh
- **Chatbot tự động:** Hỗ trợ giải đáp các thắc mắc thường gặp 24/7.
- **Hỏi đáp với bác sĩ (QA Doctor):** Nền tảng cho phép bệnh nhân đặt câu hỏi và nhận tư vấn chuyên môn trực tiếp.
- **Trò chuyện trực tuyến (Customer Chat):** Kênh giao tiếp thời gian thực giữa bệnh nhân và bộ phận CSKH để hỗ trợ ngay lập tức.

### 🔐 3. Quản lý người dùng & Bảo mật
- Hệ thống Auth hoàn chỉnh: Đăng ký, Đăng nhập, Quên mật khẩu.
- Xác thực tài khoản an toàn qua mã xác minh (Verify).
- Phân quyền chặt chẽ các vai trò: **User (Bệnh nhân)**, **CSKH (Nhân viên)**, **Bác sĩ**.
- Quản lý hồ sơ cá nhân và cập nhật thông tin sức khỏe bảo mật.

### 📢 4. Thông báo & Truyền thông
- **Email tự động:** Tích hợp `PHPMailer` gửi email thông báo xác nhận lịch hẹn, mã xác thực tài khoản.
- **Blog Y tế:** Không gian chia sẻ các bài viết, tin tức y khoa chuyên sâu giúp nâng cao nhận thức sức khỏe cộng đồng.

---

## 💻 Công nghệ sử dụng

| Phân lớp | Công nghệ / Thư viện |
| :--- | :--- |
| **Ngôn ngữ** | PHP (Core) |
| **Frontend** | HTML5, CSS3, Vanilla JavaScript |
| **Database** | MySQL |
| **Thư viện** | `PHPMailer` (Gửi Email), `Composer` (Quản lý thư viện) |
| **Máy chủ** | Apache (Cấu hình qua file `.htaccess` để tối ưu SEO & bảo mật) |
| **Kiến trúc** | MVC (Model - View - Controller) |

---

## 📂 Cấu trúc thư mục (MVC)

Dự án được xây dựng theo mô hình **MVC** chuẩn mực, giúp dễ dàng mở rộng và bảo trì:

```text
├── config/
│   └── config.php               # Cấu hình Database & hệ thống
├── controller/
│   ├── BookingController.php    # Xử lý logic đặt lịch
│   ├── CSKHController.php       # Xử lý logic nhân viên hỗ trợ
│   ├── ChatController.php       # Xử lý logic trò chuyện
│   ├── QAController.php         # Xử lý logic hỏi đáp bác sĩ
│   └── UserController.php       # Xử lý xác thực, người dùng
├── model/
│   ├── Database.php             # Kết nối PDO/MySQLi
│   ├── ChatModel.php, QAModel...# Truy vấn DB tương ứng
├── view/
│   ├── header.php, footer.php   # Layout dùng chung
│   ├── login.php, register.php  # Giao diện Auth
│   ├── customer_chat.php        # Giao diện Chat
│   └── ...
├── public/                      # Chứa tài nguyên tĩnh (Assets)
│   ├── css/
│   ├── js/
│   └── images/
├── vendor/                      # Thư viện Composer (PHPMailer...)
├── .htaccess                    # Rewrite URL
└── index.php                    # Router chính của ứng dụng

```

---


## 👨‍💻 Vai trò trong dự án
📐 Thiết kế & Kiến trúc: Trực tiếp phân tích, thiết kế cấu trúc Cơ sở dữ liệu và xây dựng core code theo mô hình MVC.

🎨 Phát triển Frontend: Chuyển đổi thiết kế thành giao diện thực tế (Responsive Layout), đảm bảo tương thích đa thiết bị.

⚙️ Phát triển Tính năng: Lập trình các tính năng phức tạp như hệ thống Real-time Chat, Hỏi đáp bác sĩ (QA), cấu hình luồng gửi Email tự động và bảo mật .htaccess.

---

## 🚀 Hướng dẫn cài đặt
Để chạy thử dự án trên môi trường Local (XAMPP/MAMP/Laragon), vui lòng làm theo các bước sau:

Clone dự án về máy:

Bash
git clone [https://github.com/hienquangtranht1/doancoso-dat-lich-kham-benh-demo.git](https://github.com/hienquangtranht1/doancoso-dat-lich-kham-benh-demo.git)
Cài đặt thư viện:
Di chuyển vào thư mục dự án và chạy lệnh (yêu cầu máy đã cài Composer):

Bash
composer install
Cấu hình Cơ sở dữ liệu:

Tạo một Database mới trong MySQL (ví dụ: hospital_booking).

Import file .sql (nếu có) vào database vừa tạo.

Mở file config/config.php và cập nhật thông tin kết nối DB của bạn:

PHP
define('DB_HOST', 'localhost');
define('DB_USER', 'root');
define('DB_PASS', '');
define('DB_NAME', 'hospital_booking');
Khởi chạy ứng dụng:

Khởi động Apache và MySQL.

Truy cập vào trình duyệt với đường dẫn: http://localhost/doancoso-dat-lich-kham-benh-demo/
