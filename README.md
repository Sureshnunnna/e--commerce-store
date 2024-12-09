# E-Commerce Website

Description:
This project is a simple e-commerce website prototype designed to simulate the basic functionality of an online store.
The platform allows users to browse products, add them to a shopping cart, and view their selections dynamically.
It uses front-end technologies like HTML, CSS, and JavaScript for structure, design, and interactivity.
The website features responsive design elements to ensure accessibility across different devices.

Key Features:

Product Listings: Display of product details, including images, names, and prices.
Shopping Cart: Users can add items to the cart and view them dynamically updated.
Interactive UI: A lightweight and responsive user interface built with HTML and CSS.
JavaScript Functionality: Dynamic cart management using JavaScript.



<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>E-Commerce Store</title>
    <style>
        body { font-family: Arial, sans-serif; margin: 0; padding: 20px; background-color: #f4f4f4; }
        h1 { text-align: center; }
        .product-container { display: flex; flex-wrap: wrap; justify-content: center; }
        .product { border: 1px solid #ddd; border-radius: 5px; padding: 16px; margin: 16px; background-color: white; width: 200px; box-shadow: 0 2px 5px rgba(0,0,0,0.1); }
        .product img { width: 100%; height: auto; border-radius: 5px; }
        .cart { margin-top: 20px; padding: 10px; background-color: #fff; border-radius: 5px; box-shadow: 0 2px 5px rgba(0,0,0,0.1); }
        button { padding: 10px; background-color: #28a745; color: white; border: none; border-radius: 5px; cursor: pointer; }
        button:hover { background-color: #218838; }
    </style>
</head>
<body>
    <h1>Welcome to the E-Commerce Store</h1>
    <div class="product-container">
        <div class="product">
            <img src="product1.jpg" alt="Product 1">
            <h2>Product 1</h2>
            <p>Price: $10</p>
            <button onclick="addToCart('Product 1')">Add to Cart</button>
        </div>
        <div class="product">
            <img src="product2.jpg" alt="Product 2">
            <h2>Product 2</h2>
            <p>Price: $15</p>
            <button onclick="addToCart('Product 2')">Add to Cart</button>
        </div>
        <div class="product">
            <img src="product3.jpg" alt="Product 3">
            <h2>Product 3</h2>
            <p>Price: $20</p>
            <button onclick="addToCart('Product 3')">Add to Cart</button>
        </div>
    </div>

    <div class="cart" id="cart">
        <h3>Your Cart</h3>
        <p id="cart-items">Cart is empty.</p>
    </div>

    <script>
        const cart = [];

        function addToCart(product) {
            cart.push(product);
            updateCartDisplay();
        }

        function updateCartDisplay() {
            const cartItems = document.getElementById("cart-items");
            if (cart.length === 0) {
                cartItems.innerText = "Cart is empty.";
            } else {
                cartItems.innerText = "Cart: " + cart.join(", ") + " (Total items: " + cart.length + ")";
            }
        }
    </script>
</body>
</html>





![image](https://github.com/user-attachments/assets/6f8ea788-684d-4742-ad24-a4931e7cdc64)
