# 🛍️ ShopthoitrangT - Hệ Thống Quản Lý Cửa Hàng Thời Trang

## 📋 Mô Tả Dự Án

ShopthoitrangT là một hệ thống quản lý cửa hàng thời trang hoàn chỉnh bao gồm:
- **Giao diện khách hàng**: Website mua sắm trực tuyến
- **Giao diện quản trị**: Dashboard quản lý cửa hàng
- **Backend API**: Hệ thống API RESTful

## 🏗️ Kiến Trúc Dự Án

```
ShopthoitrangT/
├── client-admin/          # Giao diện quản trị (React)
├── client-customer/       # Giao diện khách hàng (React)
└── server/               # Backend API (Node.js + Express)
```

## 🚀 Công Nghệ Sử Dụng

### Frontend
- **React.js 18.2.0** - Framework JavaScript
- **React Router DOM** - Điều hướng
- **Axios** - HTTP Client
- **React Bootstrap** - UI Components (client-customer)
- **React Slick** - Carousel/Slider
- **React Toastify** - Thông báo

### Backend
- **Node.js** - Runtime JavaScript
- **Express.js** - Web Framework
- **MongoDB** - Cơ sở dữ liệu
- **Mongoose** - ODM cho MongoDB
- **JWT** - Xác thực
- **Nodemailer** - Gửi email
- **Crypto** - Mã hóa

## 📦 Cài Đặt Và Chạy Dự Án

### Yêu Cầu Hệ Thống
- Node.js (phiên bản 14 trở lên)
- MongoDB
- Git

### Bước 1: Clone Dự Án
```bash
git clone <repository-url>
cd ShopthoitrangT
```

### Bước 2: Cài Đặt Dependencies

#### Cài đặt Backend
```bash
cd server
npm install
```

#### Cài đặt Frontend Admin
```bash
cd ../client-admin
npm install
```

#### Cài đặt Frontend Customer
```bash
cd ../client-customer
npm install
```

### Bước 3: Cấu Hình Database
1. Đảm bảo MongoDB đang chạy
2. Cập nhật connection string trong `server/utils/MongooseUtil.js`

### Bước 4: Chạy Dự Án

#### Phương Pháp 1: Chạy Riêng Lẻ
```bash
# Terminal 1 - Backend
cd server
npm start

# Terminal 2 - Admin Interface
cd client-admin
npm start

# Terminal 3 - Customer Interface
cd client-customer
npm start
```

#### Phương Pháp 2: Build và Deploy
```bash
# Build toàn bộ dự án
cd server
npm run build

# Chạy server (sẽ serve cả admin và customer)
npm start
```

## 🌐 Truy Cập Ứng Dụng

- **Giao diện khách hàng**: http://localhost:3000
- **Giao diện quản trị**: http://localhost:3000/admin

## 📁 Cấu Trúc Thư Mục

### Backend (`server/`)
```
server/
├── api/
│   ├── admin.js          # API cho admin
│   └── customer.js       # API cho customer
├── models/
│   ├── AdminDAO.js       # Quản lý admin
│   ├── CategoryDAO.js    # Quản lý danh mục
│   ├── ContactDAO.js     # Quản lý liên hệ
│   ├── CustomerDAO.js    # Quản lý khách hàng
│   ├── NotificationDAO.js # Quản lý thông báo
│   ├── OrderDAO.js       # Quản lý đơn hàng
│   ├── ProductDAO.js     # Quản lý sản phẩm
│   ├── ProductFavoriteDAO.js # Quản lý sản phẩm yêu thích
│   ├── SizeDAO.js        # Quản lý kích thước
│   └── SliderDAO.js      # Quản lý slider
├── utils/
│   ├── CryptoUtil.js     # Tiện ích mã hóa
│   ├── EmailUtil.js      # Tiện ích email
│   ├── JwtUtil.js        # Tiện ích JWT
│   ├── MongooseUtil.js   # Kết nối MongoDB
│   └── MyConstants.js    # Hằng số
└── index.js              # Entry point
```

### Frontend Admin (`client-admin/`)
```
client-admin/src/
├── components/
│   ├── CategoryComponent/     # Quản lý danh mục
│   ├── ContactComponent/      # Quản lý liên hệ
│   ├── CustomerComponent/     # Quản lý khách hàng
│   ├── LoginComponent/        # Đăng nhập
│   ├── NotificationComponent/ # Quản lý thông báo
│   ├── OrderComponent/        # Quản lý đơn hàng
│   ├── ProductComponent/      # Quản lý sản phẩm
│   ├── SizeComponent/         # Quản lý kích thước
│   ├── SliderComponent/       # Quản lý slider
│   └── StatisticsComponent/   # Thống kê
└── contexts/
    ├── MyContext.js
    └── MyProvider.js
```

### Frontend Customer (`client-customer/`)
```
client-customer/src/
├── components/
│   ├── AboutComponent/        # Thông tin sản phẩm
│   ├── ActiveComponent/       # Kích hoạt tài khoản
│   ├── AddressComponent/      # Quản lý địa chỉ
│   ├── ContactInfoComponent/  # Thông tin liên hệ
│   ├── FooterComponent/       # Footer
│   ├── HomeComponent/         # Trang chủ
│   ├── InformComponent/       # Thông báo
│   ├── LoginComponent/        # Đăng nhập
│   ├── MenuComponent/         # Menu
│   ├── MycartComponent/       # Giỏ hàng
│   ├── MyordersComponent/     # Đơn hàng của tôi
│   ├── MyProductFavoriteComponent/ # Sản phẩm yêu thích
│   ├── MyprofileComponent/    # Hồ sơ cá nhân
│   ├── ProductComponent/      # Sản phẩm
│   ├── ResetPasswordComponent/ # Đặt lại mật khẩu
│   ├── SignupComponent/       # Đăng ký
│   └── TawkMessengerComponent/ # Chat hỗ trợ
└── utils/
    ├── CartUtil.js
    └── withRouter.js
```

## 🔧 Tính Năng Chính

### Giao Diện Khách Hàng
- ✅ Đăng ký/Đăng nhập tài khoản
- ✅ Xem danh sách sản phẩm
- ✅ Tìm kiếm và lọc sản phẩm
- ✅ Xem chi tiết sản phẩm
- ✅ Thêm vào giỏ hàng
- ✅ Quản lý giỏ hàng
- ✅ Đặt hàng
- ✅ Xem lịch sử đơn hàng
- ✅ Quản lý hồ sơ cá nhân
- ✅ Sản phẩm yêu thích
- ✅ Chat hỗ trợ (Tawk.to)

### Giao Diện Quản Trị
- ✅ Đăng nhập admin
- ✅ Quản lý danh mục sản phẩm
- ✅ Quản lý sản phẩm
- ✅ Quản lý kích thước
- ✅ Quản lý đơn hàng
- ✅ Quản lý khách hàng
- ✅ Quản lý liên hệ
- ✅ Quản lý thông báo
- ✅ Quản lý slider
- ✅ Thống kê bán hàng

## 🔐 Bảo Mật

- JWT Authentication
- Mã hóa mật khẩu với Crypto
- Validation dữ liệu đầu vào
- CORS protection

## 📧 Email

Hệ thống sử dụng Nodemailer để gửi email:
- Email xác nhận đăng ký
- Email đặt lại mật khẩu
- Email thông báo đơn hàng

## 🚀 Deployment

### Build Production
```bash
cd server
npm run build
```

### Environment Variables
Tạo file `.env` trong thư mục `server/`:
```
PORT=3000
MONGODB_URI=mongodb://localhost:27017/shopthoitrang
JWT_SECRET=your_jwt_secret
EMAIL_USER=your_email@gmail.com
EMAIL_PASS=your_email_password
```

## 👥 Đóng Góp

1. Fork dự án
2. Tạo feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit thay đổi (`git commit -m 'Add some AmazingFeature'`)
4. Push to branch (`git push origin feature/AmazingFeature`)
5. Mở Pull Request

## 📄 Giấy Phép

Dự án này được phân phối dưới giấy phép ISC.

## 📞 Liên Hệ

- **Email**: [your-email@example.com]
- **GitHub**: [your-github-username]

---

⭐ Nếu dự án này hữu ích, hãy cho chúng tôi một ngôi sao! 
