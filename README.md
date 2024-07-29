# electronic-shop-dashboard
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Electronic Shop Dashboard</title>
    <style>
        body, html {
            height: 100%;
            margin: 0;
            font-family: Arial, sans-serif;
            color: #fff;
        }
        .bg {
            background-image: url("images/electronic6.jpeg"); /* Replace with your image path */
            height: 100%;
            background-position: center;
            background-repeat: no-repeat;
            background-size: cover;
        }
        .content {
            position: absolute;
            top: 50%;
            left: 50%;
            transform: translate(-50%, -50%);
            text-align: center;
        }
        .content h1 {
            font-size: 50px;
            margin: 0;
        }
        .content p {
            font-size: 24px;
            margin: 10px 0;
        }
        .content a {
            display: inline-block;
            margin-top: 20px;
            padding: 10px 20px;
            background-color: #5cb85c;
            color: #fff;
            text-decoration: none;
            border-radius: 4px;
            transition: background-color 0.3s ease;
        }
        .content a:hover {
            background-color: #4cae4c;
        }
        .topbar {
            position: fixed;
            top: 0;
            width: 100%;
            background-color: rgba(0, 0, 0, 0.7);
            padding: 10px;
            display: flex;
            justify-content: space-between;
            align-items: center;
            z-index: 1000;
        }
        .menu-icon {
            font-size: 24px;
            cursor: pointer;
        }
        .dropdown {
            display: none;
            position: absolute;
            top: 50px;
            right: 10px;
            background-color: rgba(0, 0, 0, 0.9);
            border-radius: 4px;
            padding: 10px;
            box-shadow: 0 0 10px rgba(0, 0, 0, 0.5);
        }
        .dropdown a {
            display: block;
            color: #fff;
            padding: 10px;
            text-decoration: none;
            transition: background-color 0.3s ease;
        }
        .dropdown a:hover {
            background-color: #575757;
        }
    </style>
    <script>
        function toggleDropdown() {
            var dropdown = document.getElementById("dropdown");
            if (dropdown.style.display === "none" || dropdown.style.display === "") {
                dropdown.style.display = "block";
            } else {
                dropdown.style.display = "none";
            }
        }

        function loadContent(page) {
            // Example: assuming page content is fetched dynamically
            var contentDiv = document.getElementById("content");
            contentDiv.innerHTML = "<h1>" + page + "</h1><p>This is the " + page + " page content.</p>";
        }
    </script>
</head>
<body>
    <div class="bg">
        <div class="topbar">
            <div class="menu-icon" onclick="toggleDropdown()">&#9776;</div>
            <div class="dropdown" id="dropdown">
                <a href="#" onclick="loadContent('Home')">Home</a>
                <a href="#" onclick="loadContent('Products')">Products</a>
                <a href="about_us.php" onclick="loadContent('About Us')">About Us</a>
                <a href="#" onclick="loadContent('Contact')">Contact</a>
                <a href="#" onclick="loadContent('Register')">Register</a>
                <a href="#" onclick="loadContent('Login')">Login</a>
            </div>
        </div>
        <div class="content" id="content">
            <h1>Welcome to Electronic Shop</h1>
            <p>Your one-stop shop for the latest electronics</p>
            <a href="#">View Products</a>
        </div>
    </div>
</body>
</html>
