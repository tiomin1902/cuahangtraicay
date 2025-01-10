<!DOCTYPE html>
<html lang="vi">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Cửa Hàng Trái Cây Tươi</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            margin: 0;
            padding: 0;
            background-color: #f4f4f9;
        }

        header {
            background-color: #d9534f; /* Màu đỏ */
            color: white;
            text-align: center;
            padding: 20px 0;
        }

        nav {
            background-color: #c9302c; /* Màu đỏ */
            overflow: hidden;
        }

        nav a {
            color: white;
            padding: 14px 20px;
            text-decoration: none;
            float: left;
        }

        nav a:hover {
            background-color: #f0ad4e; /* Màu vàng khi hover */
            color: black;
        }

        .container {
            width: 80%;
            margin: 0 auto;
        }

        .banner {
            width: 100%;
            height: 300px;
            background-image: url('banner.jpg'); /* Hình ảnh banner */
            background-size: cover;
            background-position: center;
            text-align: center;
            color: white;
            padding-top: 100px;
            font-size: 40px;
        }

        .banner h1 {
            font-size: 50px;
            margin: 0;
        }

        .products {
            display: flex;
            justify-content: space-between;
            margin-top: 30px;
        }

        .product {
            background-color: white;
            border-radius: 8px;
            box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
            overflow: hidden;
            width: 30%;
            text-align: center;
            padding: 10px;
            transition: transform 0.3s ease;
        }

        .product:hover {
            transform: scale(1.05);
        }

        .product img {
            width: 100%;
            height: 200px;
            object-fit: cover;
        }

        .product h2 {
            color: #333;
            font-size: 20px;
        }

        .product p {
            font-size: 16px;
            color: #777;
        }

        .product .price {
            font-size: 18px;
            color: #d9534f; /* Màu đỏ cho giá */
            font-weight: bold;
        }

        .product .order-btn {
            background-color: #f0ad4e; /* Màu vàng cho nút Đặt hàng */
            color: white;
            padding: 10px 20px;
            border: none;
            cursor: pointer;
            font-size: 16px;
            margin-top: 15px;
        }

        .product .order-btn:hover {
            background-color: #c9302c; /* Màu đỏ khi hover */
        }

        .order-form {
            display: none;
            margin-top: 20px;
            text-align: left;
            width: 80%;
            margin-left: auto;
            margin-right: auto;
            padding: 20px;
            background-color: #f9f9f9;
            border-radius: 8px;
            box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
        }

        .order-form input, .order-form textarea {
            width: 100%;
            padding: 10px;
            margin: 10px 0;
            border: 1px solid #ddd;
            border-radius: 4px;
        }

        .order-form button {
            background-color: #f0ad4e; /* Màu vàng cho nút Gửi đơn hàng */
            color: white;
            padding: 10px 20px;
            border: none;
            cursor: pointer;
            font-size: 16px;
        }

        .order-form button:hover {
            background-color: #c9302c; /* Màu đỏ khi hover */
        }

        .success-message {
            display: none;
            margin-top: 20px;
            padding: 15px;
            background-color: #d9534f; /* Màu đỏ cho thông báo thành công */
            color: white;
            text-align: center;
            border-radius: 8px;
        }

        footer {
            background-color: #c9302c; /* Màu đỏ cho footer */
            color: white;
            text-align: center;
            padding: 10px;
            margin-top: 30px;
        }
    </style>
</head>
<body>

    <header>
        <h1>Cửa Hàng Trái Cây Tươi</h1>
        <p>Trái cây tươi ngon mỗi ngày - Giao hàng tận nơi</p>
    </header>

    <nav>
        <a href="#">Trang Chủ</a>
        <a href="#">Sản Phẩm</a>
        <a href="#">Giới Thiệu</a>
        <a href="#">Blog</a>
        <a href="#">Liên Hệ</a>
    </nav>

    <div class="container">
        <!-- Banner -->
        <div class="banner">
            <h1>Trái Cây Tươi Ngon Mỗi Ngày</h1>
        </div>

        <!-- Sản phẩm nổi bật -->
        <div class="products">
            <div class="product">
                <img src="triquangdangghet.jpg" alt="Sầu riêng">
                <h2>Sầu riêng</h2>
                <p>Sầu riêng</p>
                <p class="price">150.000 VNĐ</p>
                <button class="order-btn">Đặt hàng</button>
            </div>
            <div class="product">
                <img src="apple-kiwi.jpg" alt="Dâu tây">
                <h2>Dâu tây</h2>
                <p>Dâu tây</p>
                <p class="price">120.000 VNĐ</p>
                <button class="order-btn">Đặt hàng</button>
            </div>
            <div class="product">
                <img src="fruit-health.webp" alt="Kiwi">
                <h2>Kiwi</h2>
                <p>Kiwi</p>
                <p class="price">180.000 VNĐ</p>
                <button class="order-btn">Đặt hàng</button>
            </div>
        </div>

        <!-- Form đặt hàng -->
        <div class="order-form">
            <h3>Điền thông tin để đặt hàng</h3>
            <form id="orderForm">
                <label for="name">Họ và Tên:</label>
                <input type="text" id="name" name="name" required>

                <label for="address">Địa chỉ giao hàng:</label>
                <input type="text" id="address" name="address" required>

                <label for="phone">Số điện thoại:</label>
                <input type="text" id="phone" name="phone" required>

                <button type="submit">Gửi đơn hàng</button>
            </form>
        </div>

        <!-- Thông báo thành công -->
        <div class="success-message">
            Đơn hàng của bạn đã được đặt thành công!
        </div>
    </div>

    <footer>
        <p>&copy; 2025 Cửa Hàng Trái Cây Tươi. Tất cả quyền lợi được bảo vệ.</p>
    </footer>

    <script>
        // JavaScript để hiển thị form đặt hàng khi nhấn nút "Đặt hàng"
        const orderButtons = document.querySelectorAll('.order-btn');
        const orderForm = document.querySelector('.order-form');
        const successMessage = document.querySelector('.success-message');

        orderButtons.forEach(button => {
            button.addEventListener('click', () => {
                orderForm.style.display = 'block';
            });
        });

        // Xử lý gửi đơn hàng
        document.getElementById('orderForm').addEventListener('submit', function (e) {
            e.preventDefault();
            orderForm.style.display = 'none';
            successMessage.style.display = 'block';
        });
    </script>

</body>
</html>
