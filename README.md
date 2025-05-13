Can you combine all of these codes into a single layout with only one header and one footer, similar to how it's done on online shopping sites like Lazada? By the way, there are 15 product detail pages, 15 shopping cart pages, and 15 checkout pages—one set for each of the 15 products.


<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Ganchillo - Crochet Fashion</title>
    <link href="https://fonts.googleapis.com/css2?family=Inter:wght@400;700&family=Judson:wght@400;700&family=Public+Sans:wght@300;700&family=Rubik:wght@700&display=swap" rel="stylesheet">
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }
        
        body {
            font-family: 'Inter', sans-serif;
            background-color: #d3b683;
            color: #f5f5dc;
            position: relative;
        }
        
        .header {
            background-color: #d3b683;
            height: 117px;
            width: 100%;
            display: flex;
            align-items: center;
            justify-content: space-between;
            padding: 0 20px;
            border: 1px solid #f5f5dc;
            position: relative;
        }
        
        .logo {
            width: 89px;
            height: 89px;
        }
        
        .nav-links {
            display: flex;
            gap: 30px;
        }
        
        .nav-link {
            font-size: 20px;
            font-weight: 400;
            color: #f5f5dc;
            text-decoration: none;
            display: flex;
            align-items: center;
            gap: 5px;
        }
        
        .dropdown-icon {
            width: 25px;
            height: 7px;
        }
        
        .search-bar {
            display: flex;
            align-items: center;
            background-color: #f5f5dc;
            border-radius: 10px;
            width: 656px;
            height: 31px;
            padding: 0 15px;
            border: 1px solid #f5f5dc;
        }
        
        .search-bar input {
            background: transparent;
            border: none;
            outline: none;
            width: 100%;
            color: #d3b683;
            font-family: 'Rubik', sans-serif;
            font-weight: 700;
            font-size: 16px;
        }
        
        .search-bar img {
            width: 20px;
            height: 20px;
            margin-right: 10px;
        }
        
        .user-actions {
            display: flex;
            align-items: center;
            gap: 15px;
        }
        
        .icon-link {
            display: flex;
            align-items: center;
            gap: 5px;
            text-decoration: none;
            color: #f5f5dc;
            font-size: 20px;
        }
        
        .icon {
            width: 38px;
            height: 38px;
        }
        
        .customer-service-icon {
            width: 42px;
            height: 42px;
        }
        
        .login-icon {
            width: 32px;
            height: 32px;
        }
        
        .cart-icon {
            width: 38px;
            height: 38px;
        }
        
        .hero-section {
            display: flex;
            margin-top: 6px;
            border-top: 12px solid #fff;
        }
        
        .hero-image {
            width: 50%;
            height: 521px;
            object-fit: cover;
            border-right: 13px solid #fff;
            border-left: 13px solid #fff;
        }
        
        .hero-content {
            width: 50%;
            background-color: #d3b683;
            padding: 60px 16px;
            display: flex;
            align-items: center;
            justify-content: center;
            border: 1px solid #f5f5dc;
            border-right: 13px solid #fff;
        }
        
        .hero-text {
            font-family: 'Judson', serif;
            font-size: 58px;
            font-weight: 700;
            line-height: 67px;
            text-align: center;
            color: #f5f5dc;
        }
        
        .products-section {
            background-color: #d3b683;
            padding: 50px 20px;
            border-top: 14px solid #fff;
        }
        
        .section-title {
            font-family: 'Judson', serif;
            font-size: 60px;
            font-weight: 700;
            line-height: 70px;
            text-align: center;
            color: #f5f5dc;
            margin-bottom: 50px;
        }
        
        .product-grid {
            display: grid;
            grid-template-columns: repeat(3, 1fr);
            gap: 50px;
            margin-bottom: 50px;
        }
        
        .product-card {
            display: flex;
            flex-direction: column;
        }
        
        .product-image {
            width: 100%;
            height: 435px;
            object-fit: cover;
        }
        
        .product-info {
            margin-top: 15px;
        }
        
        .product-title {
            font-family: 'Judson', serif;
            font-weight: 700;
            line-height: 25px;
            text-align: justify;
            color: #f5f5dc;
            margin-bottom: 15px;
            height: 75px;
            overflow: hidden;
        }
        
        .product-price {
            display: flex;
            align-items: center;
            gap: 10px;
            margin-bottom: 15px;
        }
        
        .current-price {
            font-family: 'Public Sans', sans-serif;
            font-size: 18px;
            font-weight: 700;
            line-height: 23px;
            color: #f5f5dc;
        }
        
        .original-price {
            font-family: 'Public Sans', sans-serif;
            font-size: 18px;
            font-weight: 300;
            line-height: 23px;
            text-decoration: line-through;
            color: #868686;
        }
        
        .discount-tag {
            background-color: #f5f5dc;
            border-radius: 10px;
            padding: 2px 10px;
            font-family: 'Judson', serif;
            font-size: 15px;
            font-weight: 700;
            line-height: 18px;
            color: #d3b683;
        }
        
        .view-details-btn {
            background-color: #f5f5dc;
            height: 67px;
            width: 100%;
            display: flex;
            align-items: center;
            justify-content: center;
            cursor: pointer;
            transition: all 0.3s ease;
        }
        
        .view-details-btn:hover {
            background-color: #e5e5c5;
        }
        
        .view-details-text {
            font-family: 'Judson', serif;
            font-size: 50px;
            font-weight: 700;
            line-height: 59px;
            color: #d3b683;
        }
        
        .footer {
            background-color: #d3b683;
            padding: 50px 20px;
            border-top: 12px solid #fff;
        }
        
        .footer-top {
            display: flex;
            justify-content: space-between;
            margin-bottom: 50px;
        }
        
        .footer-logo {
            width: 156px;
            height: 156px;
        }
        
        .footer-columns {
            display: flex;
            justify-content: space-between;
            margin-bottom: 50px;
        }
        
        .footer-column {
            width: 30%;
        }
        
        .footer-heading {
            font-family: 'Judson', serif;
            font-size: 35px;
            font-weight: 700;
            line-height: 41px;
            color: #f5f5dc;
            margin-bottom: 20px;
            text-align: center;
        }
        
        .footer-link {
            font-family: 'Judson', serif;
            font-size: 35px;
            font-weight: 400;
            line-height: 41px;
            color: #f5f5dc;
            text-decoration: none;
            display: block;
            margin-bottom: 15px;
            text-align: center;
        }
        
        .social-heading {
            font-family: 'Judson', serif;
            font-size: 35px;
            font-weight: 700;
            line-height: 41px;
            color: #f5f5dc;
            margin-bottom: 20px;
            text-align: center;
        }
        
        .social-icons {
            display: flex;
            justify-content: center;
            gap: 7px;
            margin-bottom: 40px;
        }
        
        .social-icon {
            width: 56px;
            height: 45px;
        }
        
        .newsletter-heading {
            font-family: 'Judson', serif;
            font-size: 35px;
            font-weight: 700;
            line-height: 41px;
            color: #f5f5dc;
            margin-bottom: 20px;
            text-align: center;
        }
        
        .newsletter-form {
            display: flex;
            flex-direction: column;
            gap: 20px;
            max-width: 600px;
            margin: 0 auto;
        }
        
        .input-group {
            display: flex;
        }
        
        .form-input {
            flex: 1;
            height: 45px;
            background-color: #f5f5dc;
            border: 1px solid #f5f5dc;
            border-radius: 10px;
            padding: 0 15px;
            font-family: 'Rubik', sans-serif;
            font-size: 16px;
            font-weight: 700;
            color: #d3b683;
        }
        
        .phone-prefix {
            width: 156px;
            height: 43px;
            background-color: #f5f5dc;
            border: none;
            border-radius: 10px;
            display: flex;
            align-items: center;
            padding: 0 10px;
            margin-right: 10px;
        }
        
        .prefix-text {
            font-family: 'Rubik', sans-serif;
            font-size: 25px;
            font-weight: 700;
            color: #d3b683;
        }
        
        .dropdown-arrow {
            width: 25px;
            height: 7px;
            margin-left: auto;
        }
        
        .subscribe-btn {
            width: 172px;
            height: 43px;
            background-color: #f5f5dc;
            border: none;
            border-radius: 10px;
            margin-left: 10px;
            cursor: pointer;
            font-family: 'Rubik', sans-serif;
            font-size: 25px;
            font-weight: 700;
            color: #d3b683;
            transition: all 0.3s ease;
        }
        
        .subscribe-btn:hover {
            background-color: #e5e5c5;
        }
        
        .copyright {
            font-family: 'Judson', serif;
            font-size: 25px;
            font-weight: 400;
            line-height: 29px;
            color: #f5f5dc;
            text-align: center;
            margin-top: 30px;
            padding-bottom: 20px;
        }
    </style>
</head>
<body>
    <header class="header">
        <a href="/">
            <img src="../assets/images/img_gachillo_logo.png" alt="Ganchillo Logo" class="logo">
        </a>
        
        <nav class="nav-links">
            <a href="/" class="nav-link">Home</a>
            <a href="/categories" class="nav-link">
                Categories
                <img src="../assets/images/img_polygon_2.svg" alt="Dropdown" class="dropdown-icon">
            </a>
            <a href="/products" class="nav-link">Products</a>
        </nav>
        
        <div class="search-bar">
            <img src="../assets/images/img_image_1.png" alt="Search Icon">
            <input type="text" placeholder="Search in Ganchillo">
        </div>
        
        <div class="user-actions">
            <a href="/language" class="icon-link">
                <img src="../assets/images/img_language_icon.png" alt="Language" class="icon">
                English
                <img src="../assets/images/img_polygon_2.svg" alt="Dropdown" class="dropdown-icon">
            </a>
            
            <a href="/notifications" class="icon-link">
                <img src="../assets/images/img_notification_icon.png" alt="Notifications" class="icon">
                Notification
            </a>
            
            <a href="/customer-service" class="icon-link">
                <img src="../assets/images/img_customer_service_icon.png" alt="Customer Service" class="customer-service-icon">
                Costumer Service
            </a>
            
            <a href="/login" class="icon-link">
                <img src="../assets/images/img_log_in_icon.png" alt="Login" class="login-icon">
                Sign up | Log in
            </a>
            
            <a href="/cart" class="icon-link">
                <img src="../assets/images/img_shopping_cart_icon.png" alt="Shopping Cart" class="cart-icon">
            </a>
        </div>
    </header>
    
    <section class="hero-section">
        <img src="../assets/images/img_crochet_polo_dressfotor20250418121727_1.png" alt="Crochet Fashion" class="hero-image">
        
        <div class="hero-content">
            <h1 class="hero-text">Welcome to Ganchillo!<br><br>Create beauty with<br>every stitch</h1>
        </div>
    </section>
    
    <section class="products-section">
        <h2 class="section-title">Newest Products</h2>
        
        <div class="product-grid">
            <!-- Product 1 -->
            <div class="product-card">
                <img src="../assets/images/img_image_30.png" alt="Crochet Knit Frill Hen Mini Dress" class="product-image">
                
                <div class="product-info">
                    <h3 class="product-title" style="font-size: 17px;">Ganchillo Khaki Crochet Knit Frill Hen Mini Dress Spring Y2K 90's Casual Cute Easter Sun Summer Ibiza Rave VacationBoho, Bohemian, Cowgirl, Festival, Concert, Western</h3>
                    
                    <div class="product-price">
                        <span class="current-price">₱813</span>
                        <span class="original-price">₱ 903</span>
                        <span class="discount-tag">-10%</span>
                    </div>
                </div>
                
                <div class="view-details-btn">
                    <span class="view-details-text">VIEW DETAILS</span>
                </div>
            </div>
            
            <!-- Product 2 -->
            <div class="product-card">
                <img src="../assets/images/img_image_165.png" alt="Crochet Bikini Top" class="product-image">
                
                <div class="product-info">
                    <h3 class="product-title" style="font-size: 20px;">Ganchillo Hippie Y2K Glamorous Island Floral Crochet Bikini Top, Summer Beach Resort Coconut Girl Knit Shirt For Women</h3>
                    
                    <div class="product-price">
                        <span class="current-price">₱ 605</span>
                    </div>
                </div>
                
                <div class="view-details-btn">
                    <span class="view-details-text">VIEW DETAILS</span>
                </div>
            </div>
            
            <!-- Product 3 -->
            <div class="product-card">
                <img src="../assets/images/img_image_75.png" alt="Crochet Mini Shorts" class="product-image" style="height: 399px;">
                
                <div class="product-info">
                    <h3 class="product-title" style="font-size: 20px;">GANCHILLO WOMEN Crochet Mini Shorts With Stripe Detail</h3>
                    
                    <div class="product-price">
                        <span class="current-price">₱ 655</span>
                        <span class="original-price">₱ 739</span>
                        <span class="discount-tag">-10%</span>
                    </div>
                </div>
                
                <div class="view-details-btn">
                    <span class="view-details-text">VIEW DETAILS</span>
                </div>
            </div>
            
            <!-- Product 4 -->
            <div class="product-card">
                <img src="../assets/images/img_image_118.png" alt="Mermaid Tote Bag" class="product-image">
                
                <div class="product-info">
                    <h3 class="product-title" style="font-size: 9px; line-height: 25px;">Fairycore Mermaid Medium Tote Bag Hollow Out DesignSchool Bag,Back To School,Large Capacity,Portable,Classic Casual, Suitable For Teen Girls Women College Students, Perfect For Back To School,College,Elementary School,Middle School, High School,Work, Business, Commute,Shopping,Holiday</h3>
                    
                    <div class="product-price">
                        <span class="current-price">₱ 188</span>
                    </div>
                </div>
                
                <div class="view-details-btn">
                    <span class="view-details-text">VIEW DETAILS</span>
                </div>
            </div>
            
            <!-- Product 5 -->
            <div class="product-card">
                <img src="../assets/images/img_image_278.png" alt="Crochet Cardigan" class="product-image">
                
                <div class="product-info">
                    <h3 class="product-title" style="font-size: 18px; line-height: 20px;">Women's Vacation Hollow Out Button Crochet Knit Top Cardigan With Round Neck Long Sleeves Drop Shoulder, Lightweight Open Front Loose Fit Casual, Spring Summer Fall</h3>
                    
                    <div class="product-price">
                        <span class="current-price">₱ 697</span>
                    </div>
                </div>
                
                <div class="view-details-btn">
                    <span class="view-details-text">VIEW DETAILS</span>
                </div>
            </div>
            
            <!-- Product 6 -->
            <div class="product-card">
                <img src="../assets/images/img_image_44.png" alt="Bucket Hat" class="product-image">
                
                <div class="product-info">
                    <h3 class="product-title" style="font-size: 20px;">1 Women's Solid Color Hollow Woven Bucket Hat, Breathable And Thin Sun Hat, Suitable For Outdoor Travel</h3>
                    
                    <div class="product-price">
                        <span class="current-price">₱ 174</span>
                        <span class="original-price">₱ 205</span>
                        <span class="discount-tag">-15%</span>
                    </div>
                </div>
                
                <div class="view-details-btn">
                    <span class="view-details-text">VIEW DETAILS</span>
                </div>
            </div>
        </div>
    </section>
    
    <footer class="footer">
        <div class="footer-columns">
            <div class="footer-column">
                <img src="../assets/images/img_gachillo_logo.png" alt="Ganchillo Logo" class="footer-logo">
                <h3 class="footer-heading">GANCHILLO</h3>
                <a href="/about" class="footer-link">About Ganchillo</a>
                <a href="/privacy" class="footer-link">Privacy Policy</a>
                <a href="/terms" class="footer-link">Terms & Conditions</a>
            </div>
            
            <div class="footer-column">
                <h3 class="footer-heading">Customer Care</h3>
                <a href="/contact" class="footer-link">Contact us</a>
                <a href="/help" class="footer-link">Help Center</a>
                <a href="/payment" class="footer-link">Payment Method</a>
                <a href="/faq" class="footer-link">FAQ</a>
            </div>
            
            <div class="footer-column">
                <h3 class="social-heading">FIND US ON</h3>
                <div class="social-icons">
                    <a href="#"><img src="../assets/images/img_fb_icon.png" alt="Facebook" class="social-icon"></a>
                    <a href="#"><img src="../assets/images/img_instagram_icon.png" alt="Instagram" class="social-icon"></a>
                    <a href="#"><img src="../assets/images/img_twitter_x_icon.png" alt="Twitter/X" class="social-icon"></a>
                    <a href="#"><img src="../assets/images/img_image.png" alt="Pinterest" class="social-icon"></a>
                    <a href="#"><img src="../assets/images/img_tiktok_icon.png" alt="TikTok" class="social-icon"></a>
                    <a href="#"><img src="../assets/images/img_youtube_icon.png" alt="YouTube" class="social-icon"></a>
                    <a href="#"><img src="../assets/images/img_linkedin_icon.png" alt="LinkedIn" class="social-icon"></a>
                </div>
                
                <h3 class="newsletter-heading">STAY IN THE LOOP, STITCH BY STITCH</h3>
                
                <div class="newsletter-form">
                    <div class="input-group">
                        <input type="email" placeholder="Your Email Address" class="form-input">
                        <button type="button" class="subscribe-btn">SUBSCRIBE</button>
                    </div>
                    
                    <div class="input-group">
                        <div class="phone-prefix">
                            <span class="prefix-text">PH + 63</span>
                            <img src="../assets/images/img_polygon_3.svg" alt="Dropdown" class="dropdown-arrow">
                        </div>
                        <input type="tel" placeholder="Your phone number for SMS" class="form-input">
                        <button type="button" class="subscribe-btn">SUBSCRIBE</button>
                    </div>
                </div>
            </div>
        </div>
        
        <div class="copyright">©2025 Ganchillo All Rights Reserved</div>
    </footer>

    <script>
        // Navigation dropdown functionality
        document.addEventListener('DOMContentLoaded', function() {
            const dropdownLinks = document.querySelectorAll('.nav-link:has(img)');
            
            dropdownLinks.forEach(link => {
                link.addEventListener('click', function(e) {
                    if (this.getAttribute('href') === '/categories' || this.getAttribute('href') === '/language') {
                        e.preventDefault();
                        alert(`${this.textContent.trim()} dropdown would open here`);
                    }
                });
            });
            
            // View details buttons
            const viewDetailsButtons = document.querySelectorAll('.view-details-btn');
            viewDetailsButtons.forEach(button => {
                button.addEventListener('click', function() {
                    const productTitle = this.parentElement.querySelector('.product-title').textContent;
                    alert(`Viewing details for: ${productTitle}`);
                });
            });
            
            // Search functionality
            const searchInput = document.querySelector('.search-bar input');
            searchInput.addEventListener('keypress', function(e) {
                if (e.key === 'Enter') {
                    alert(`Searching for: ${this.value}`);
                    this.value = '';
                }
            });
            
            // Newsletter subscription
            const subscribeButtons = document.querySelectorAll('.subscribe-btn');
            subscribeButtons.forEach(button => {
                button.addEventListener('click', function() {
                    const input = this.parentElement.querySelector('.form-input');
                    if (input.value.trim() === '') {
                        alert('Please enter a valid email or phone number');
                    } else {
                        alert(`Thank you for subscribing with: ${input.value}`);
                        input.value = '';
                    }
                });
            });
            
            // Shopping cart
            const cartIcon = document.querySelector('.cart-icon');
            cartIcon.parentElement.addEventListener('click', function(e) {
                e.preventDefault();
                alert('Your shopping cart is empty');
            });
            
            // Login/Signup
            const loginLink = document.querySelector('.icon-link:has(.login-icon)');
            loginLink.addEventListener('click', function(e) {
                e.preventDefault();
                alert('Login/Signup form would appear here');
            });
        });
    </script>
</body>
</html>

<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Ganchillo - Crochet and Knit Fashion</title>
    <link href="https://fonts.googleapis.com/css2?family=Inter:wght@400;700&family=Judson:wght@400;700&family=Public+Sans:wght@300;700&family=Rubik:wght@700&display=swap" rel="stylesheet">
    <style>
        * {
            box-sizing: border-box;
            margin: 0;
            padding: 0;
        }
        
        body {
            font-family: 'Inter', sans-serif;
            background-color: #d3b683;
            color: #f5f5dc;
            position: relative;
        }
        
        .header {
            background-color: #d3b683;
            padding: 15px 0;
            position: sticky;
            top: 0;
            z-index: 100;
            border-bottom: 1px solid #f5f5dc;
        }
        
        .header-container {
            display: flex;
            justify-content: space-between;
            align-items: center;
            max-width: 1440px;
            margin: 0 auto;
            padding: 0 20px;
        }
        
        .logo {
            width: 89px;
            height: 89px;
        }
        
        .nav-links {
            display: flex;
            gap: 30px;
        }
        
        .nav-link {
            color: #f5f5dc;
            text-decoration: none;
            font-size: 20px;
            display: flex;
            align-items: center;
            gap: 5px;
        }
        
        .search-bar {
            display: flex;
            align-items: center;
            background-color: #f5f5dc;
            border-radius: 10px;
            padding: 5px 15px;
            width: 656px;
            height: 31px;
            border: 1px solid #f5f5dc;
        }
        
        .search-bar input {
            background: transparent;
            border: none;
            outline: none;
            width: 100%;
            color: #d3b683;
            font-family: 'Rubik', sans-serif;
            font-weight: 700;
            font-size: 16px;
        }
        
        .search-bar input::placeholder {
            color: #d3b683;
        }
        
        .search-icon {
            width: 20px;
            height: 20px;
            margin-right: 10px;
        }
        
        .icon {
            width: 38px;
            height: 38px;
        }
        
        .customer-service-icon {
            width: 42px;
            height: 42px;
        }
        
        .login-icon {
            width: 32px;
            height: 32px;
        }
        
        .cart-icon {
            width: 38px;
            height: 38px;
        }
        
        .banner {
            width: 100%;
            height: auto;
            max-height: 400px;
            overflow: hidden;
            position: relative;
        }
        
        .banner img {
            width: 100%;
            height: auto;
            object-fit: cover;
        }
        
        .brand-title {
            text-align: center;
            padding: 20px 0;
            background-color: #d3b683;
        }
        
        .brand-title h1 {
            font-family: 'Judson', serif;
            font-size: 50px;
            font-weight: 700;
            color: #f5f5dc;
            margin: 0;
        }
        
        .brand-title p {
            font-family: 'Judson', serif;
            font-size: 20px;
            color: #f5f5dc;
        }
        
        .filter-section {
            display: flex;
            align-items: center;
            padding: 20px;
            background-color: #d3b683;
            gap: 20px;
        }
        
        .filter-label {
            font-family: 'Judson', serif;
            font-size: 50px;
            font-weight: 700;
            color: #f5f5dc;
        }
        
        .filter-dropdown {
            background-color: #f5f5dc;
            border-radius: 10px;
            padding: 5px 15px;
            height: 43px;
            display: flex;
            align-items: center;
            justify-content: space-between;
            cursor: pointer;
            min-width: 200px;
        }
        
        .filter-dropdown span {
            font-family: 'Rubik', sans-serif;
            font-weight: 700;
            font-size: 25px;
            color: #d3b683;
        }
        
        .dropdown-arrow {
            width: 37px;
            height: 7px;
        }
        
        .products-grid {
            display: grid;
            grid-template-columns: repeat(3, 1fr);
            gap: 20px;
            padding: 20px;
            max-width: 1440px;
            margin: 0 auto;
        }
        
        .product-card {
            background-color: #d3b683;
            padding: 20px;
            display: flex;
            flex-direction: column;
        }
        
        .product-image {
            width: 100%;
            height: 435px;
            object-fit: cover;
            margin-bottom: 15px;
        }
        
        .product-title {
            font-family: 'Judson', serif;
            font-size: 20px;
            font-weight: 700;
            color: #f5f5dc;
            margin-bottom: 10px;
            line-height: 25px;
            text-align: justify;
            height: 75px;
            overflow: hidden;
        }
        
        .product-title.small {
            font-size: 17px;
            line-height: 20px;
        }
        
        .price-container {
            display: flex;
            align-items: center;
            margin-bottom: 15px;
            gap: 10px;
        }
        
        .current-price {
            font-family: 'Public Sans', sans-serif;
            font-weight: 700;
            font-size: 18px;
            color: #f5f5dc;
        }
        
        .original-price {
            font-family: 'Public Sans', sans-serif;
            font-weight: 300;
            font-size: 18px;
            color: #868686;
            text-decoration: line-through;
        }
        
        .discount-badge {
            background-color: #f5f5dc;
            border-radius: 10px;
            padding: 2px 10px;
            font-family: 'Judson', serif;
            font-weight: 700;
            font-size: 15px;
            color: #d3b683;
        }
        
        .view-details-btn {
            background-color: #f5f5dc;
            border: none;
            padding: 15px 0;
            font-family: 'Judson', serif;
            font-weight: 700;
            font-size: 50px;
            color: #d3b683;
            cursor: pointer;
            text-align: center;
            width: 100%;
            height: 67px;
            display: flex;
            align-items: center;
            justify-content: center;
            text-decoration: none;
        }
        
        .view-details-btn:hover {
            background-color: #e8e8d0;
        }
        
        .footer {
            background-color: #d3b683;
            padding: 40px 20px;
            margin-top: 40px;
            border-top: 1px solid #f5f5dc;
        }
        
        .footer-container {
            max-width: 1440px;
            margin: 0 auto;
            display: grid;
            grid-template-columns: repeat(3, 1fr);
            gap: 40px;
        }
        
        .footer-section h3 {
            font-family: 'Judson', serif;
            font-size: 35px;
            font-weight: 700;
            color: #f5f5dc;
            margin-bottom: 20px;
            text-align: center;
        }
        
        .footer-links {
            display: flex;
            flex-direction: column;
            gap: 15px;
        }
        
        .footer-link {
            font-family: 'Judson', serif;
            font-size: 35px;
            font-weight: 400;
            color: #f5f5dc;
            text-decoration: none;
            text-align: center;
        }
        
        .social-icons {
            display: flex;
            justify-content: center;
            gap: 10px;
            margin-bottom: 30px;
        }
        
        .social-icon {
            width: 56px;
            height: 45px;
        }
        
        .newsletter-form {
            display: flex;
            flex-direction: column;
            gap: 15px;
        }
        
        .newsletter-input {
            background-color: #f5f5dc;
            border-radius: 10px;
            padding: 11px 38px;
            border: 1px solid #f5f5dc;
            font-family: 'Rubik', sans-serif;
            font-weight: 700;
            font-size: 16px;
            color: #d3b683;
            width: 100%;
            height: 45px;
        }
        
        .phone-input-container {
            display: flex;
            gap: 10px;
        }
        
        .phone-prefix {
            background-color: #f5f5dc;
            border-radius: 10px;
            padding: 3px 10px;
            display: flex;
            align-items: center;
            justify-content: space-between;
            width: 156px;
            height: 43px;
        }
        
        .phone-prefix span {
            font-family: 'Rubik', sans-serif;
            font-weight: 700;
            font-size: 25px;
            color: #d3b683;
        }
        
        .phone-input {
            background-color: #f5f5dc;
            border-radius: 10px;
            padding: 12px 25px;
            border: 1px solid #f5f5dc;
            font-family: 'Rubik', sans-serif;
            font-weight: 700;
            font-size: 16px;
            color: #d3b683;
            flex-grow: 1;
            height: 45px;
        }
        
        .subscribe-btn {
            background-color: #f5f5dc;
            border-radius: 10px;
            border: none;
            padding: 4px 13px;
            font-family: 'Rubik', sans-serif;
            font-weight: 700;
            font-size: 25px;
            color: #d3b683;
            cursor: pointer;
            width: 172px;
            height: 43px;
            align-self: flex-end;
        }
        
        .copyright {
            text-align: center;
            margin-top: 30px;
            font-family: 'Judson', serif;
            font-size: 25px;
            color: #f5f5dc;
        }
        
        .footer-logo {
            width: 156px;
            height: 156px;
            margin: 0 auto;
            display: block;
        }
        
        @media (max-width: 1200px) {
            .products-grid {
                grid-template-columns: repeat(2, 1fr);
            }
            
            .search-bar {
                width: 400px;
            }
        }
        
        @media (max-width: 768px) {
            .header-container {
                flex-wrap: wrap;
            }
            
            .nav-links {
                order: 3;
                width: 100%;
                justify-content: space-between;
                margin-top: 15px;
            }
            
            .search-bar {
                width: 100%;
                order: 2;
                margin-top: 15px;
            }
            
            .products-grid {
                grid-template-columns: 1fr;
            }
            
            .filter-section {
                flex-direction: column;
                align-items: flex-start;
            }
            
            .footer-container {
                grid-template-columns: 1fr;
            }
        }
    </style>
</head>
<body>
    <header class="header">
        <div class="header-container">
            <img src="../assets/images/img_gachillo_logo.png" alt="Ganchillo Logo" class="logo">
            
            <div class="nav-links">
                <a href="#" class="nav-link">Home</a>
                <a href="#" class="nav-link">Categories</a>
                <a href="#" class="nav-link">Products</a>
                <a href="#" class="nav-link">
                    English
                    <img src="../assets/images/img_polygon_4.svg" alt="Dropdown arrow">
                </a>
                <a href="#" class="nav-link">Notification</a>
                <a href="#" class="nav-link">Costumer Service</a>
                <a href="#" class="nav-link">
                    <img src="../assets/images/img_log_in_icon.png" alt="Login icon" class="login-icon">
                    Sign up | Log in
                </a>
            </div>
            
            <div class="search-bar">
                <img src="../assets/images/img_image_2.png" alt="Search icon" class="search-icon">
                <input type="text" placeholder="Search in Ganchillo">
            </div>
            
            <div class="icons">
                <img src="../assets/images/img_language_icon.png" alt="Language icon" class="icon">
                <img src="../assets/images/img_notification_icon.png" alt="Notification icon" class="icon">
                <img src="../assets/images/img_customer_service_icon.png" alt="Customer service icon" class="customer-service-icon">
                <img src="../assets/images/img_shopping_cart_icon.png" alt="Shopping cart icon" class="cart-icon">
            </div>
        </div>
    </header>
    
    <div class="banner">
        <img src="../assets/images/img_beige_aesthetic_fashion_clothing_collection_medium_banner_2.png" alt="Crochet fashion collection banner">
    </div>
    
    <div class="brand-title">
        <h1>THE GANCHILLO</h1>
        <p>www.ganchillo.com</p>
    </div>
    
    <div class="filter-section">
        <h2 class="filter-label">Filter</h2>
        
        <div class="filter-dropdown" id="crochetItemDropdown">
            <span>Crochet Item</span>
            <img src="../assets/images/img_polygon_4_7x25.svg" alt="Dropdown arrow" class="dropdown-arrow">
        </div>
        
        <div class="filter-dropdown" id="priceRangeDropdown">
            <span>Price Range</span>
            <img src="../assets/images/img_polygon_4_7x25.svg" alt="Dropdown arrow" class="dropdown-arrow">
        </div>
        
        <div class="filter-dropdown" id="yarnColorDropdown">
            <span>Yarn Color</span>
            <img src="../assets/images/img_polygon_4_7x25.svg" alt="Dropdown arrow" class="dropdown-arrow">
        </div>
        
        <div class="filter-dropdown" id="yarnTypeDropdown">
            <span>Yarn Type</span>
            <img src="../assets/images/img_polygon_4_7x25.svg" alt="Dropdown arrow" class="dropdown-arrow">
        </div>
    </div>
    
    <div class="products-grid">
        <!-- Product 1 -->
        <div class="product-card">
            <img src="../assets/images/img_image_408x435.png" alt="Men's Vacation Inspired Floral Embroidery Hollow Knit Sweater" class="product-image">
            <h3 class="product-title">Manfinity Hypemode Men's Vacation Inspired Floral Embroidery Hollow Knit Sweater Men Crochet Shirt</h3>
            <div class="price-container">
                <span class="current-price">₱ 592</span>
                <span class="original-price">₱ 697</span>
                <span class="discount-badge">-15.1%</span>
            </div>
            <a href="#" class="view-details-btn">VIEW DETAILS</a>
        </div>
        
        <!-- Product 2 -->
        <div class="product-card">
            <img src="../assets/images/img_image_123.png" alt="Men's Knit Crocheted Apricot Old Money Casual Shirt" class="product-image">
            <h3 class="product-title small">Anewsta Men's Knit Crocheted Apricot "Old Money" Casual Loose Hollow Out Short Sleeve Shirt, Suitable For Everyday, Commute, Summer, Vacation, Party, Wedding, Couples, Boyfriend Gift, Beachwear</h3>
            <div class="price-container">
                <span class="current-price">₱ 523</span>
                <span class="original-price">₱ 581</span>
                <span class="discount-badge">-10%</span>
            </div>
            <a href="#" class="view-details-btn">VIEW DETAILS</a>
        </div>
        
        <!-- Product 3 -->
        <div class="product-card">
            <img src="../assets/images/img_image_30.png" alt="Khaki Crochet Knit Frill Hen Mini Dress" class="product-image">
            <h3 class="product-title small">Ganchillo Khaki Crochet Knit Frill Hen Mini Dress Spring Y2K 90's Casual Cute Easter Sun Summer Ibiza Rave VacationBoho, Bohemian, Cowgirl, Festival, Concert, Western</h3>
            <div class="price-container">
                <span class="current-price">₱813</span>
                <span class="original-price">₱ 903</span>
                <span class="discount-badge">-10%</span>
            </div>
            <a href="#" class="view-details-btn">VIEW DETAILS</a>
        </div>
        
        <!-- Product 4 -->
        <div class="product-card">
            <img src="../assets/images/img_image_44.png" alt="Women's Solid Color Hollow Woven Bucket Hat" class="product-image">
            <h3 class="product-title">1 Women's Solid Color Hollow Woven Bucket Hat, Breathable And Thin Sun Hat, Suitable For Outdoor Travel</h3>
            <div class="price-container">
                <span class="current-price">₱ 174</span>
                <span class="original-price">₱ 205</span>
                <span class="discount-badge">-15%</span>
            </div>
            <a href="#" class="view-details-btn">VIEW DETAILS</a>
        </div>
        
        <!-- Product 5 -->
        <div class="product-card">
            <img src="../assets/images/img_image_75.png" alt="Women Crochet Mini Shorts With Stripe Detail" class="product-image">
            <h3 class="product-title">GANCHILLO WOMEN Crochet Mini Shorts With Stripe Detail</h3>
            <div class="price-container">
                <span class="current-price">₱ 655</span>
                <span class="original-price">₱ 739</span>
                <span class="discount-badge">-10%</span>
            </div>
            <a href="#" class="view-details-btn">VIEW DETAILS</a>
        </div>
        
        <!-- Product 6 -->
        <div class="product-card">
            <img src="../assets/images/img_image_118.png" alt="Fairycore Mermaid Medium Tote Bag" class="product-image">
            <h3 class="product-title">Fairycore Mermaid Medium Tote Bag Hollow Out DesignSchool Bag,Back To School,Large Capacity,Portable,Classic Casual, Suitable For Teen Girls Women College Students, Perfect For Back To School,College,Elementary School,Middle School, High School,Work, Business, Commute,Shopping,Holiday</h3>
            <div class="price-container">
                <span class="current-price">₱ 188</span>
            </div>
            <a href="#" class="view-details-btn">VIEW DETAILS</a>
        </div>
        
        <!-- Product 7 -->
        <div class="product-card">
            <img src="../assets/images/img_image_165.png" alt="Hippie Y2K Glamorous Island Floral Crochet Bikini Top" class="product-image">
            <h3 class="product-title">Ganchillo Hippie Y2K Glamorous Island Floral Crochet Bikini Top, Summer Beach Resort Coconut Girl Knit Shirt For Women</h3>
            <div class="price-container">
                <span class="current-price">₱ 605</span>
            </div>
            <a href="#" class="view-details-btn">VIEW DETAILS</a>
        </div>
        
        <!-- Product 8 -->
        <div class="product-card">
            <img src="../assets/images/img_image_199.png" alt="Women Crochet Checkerboard Beach Shirt" class="product-image">
            <h3 class="product-title">GANCHILLO WOMEN Crochet Checkerboard Beach Shirt</h3>
            <div class="price-container">
                <span class="current-price">₱ 592</span>
                <span class="original-price">₱ 697</span>
                <span class="discount-badge">-15.1%</span>
            </div>
            <a href="#" class="view-details-btn">VIEW DETAILS</a>
        </div>
        
        <!-- Product 9 -->
        <div class="product-card">
            <img src="../assets/images/img_image_238.png" alt="Colorblock Wide Leg Knit Pants" class="product-image">
            <h3 class="product-title">Colorblock Wide Leg Knit Pants</h3>
            <div class="price-container">
                <span class="current-price">₱ 435</span>
                <span class="original-price">₱ 791</span>
                <span class="discount-badge">-45%</span>
            </div>
            <a href="#" class="view-details-btn">VIEW DETAILS</a>
        </div>
        
        <!-- Product 10 -->
        <div class="product-card">
            <img src="../assets/images/img_image_1.png" alt="Men's Vacation Inspired Floral Embroidery Hollow Knit Sweater" class="product-image">
            <h3 class="product-title">Manfinity Hypemode Men's Vacation Inspired Floral Embroidery Hollow Knit Sweater Men Crochet Shirt</h3>
            <div class="price-container">
                <span class="current-price">₱ 592</span>
                <span class="original-price">₱ 697</span>
                <span class="discount-badge">-15.1%</span>
            </div>
            <a href="#" class="view-details-btn">VIEW DETAILS</a>
        </div>
        
        <!-- Product 11 -->
        <div class="product-card">
            <img src="../assets/images/img_image_278.png" alt="Women's Vacation Hollow Out Button Crochet Knit Top Cardigan" class="product-image">
            <h3 class="product-title small">Women's Vacation Hollow Out Button Crochet Knit Top Cardigan With Round Neck Long Sleeves Drop Shoulder, Lightweight Open Front Loose Fit Casual, Spring Summer Fall</h3>
            <div class="price-container">
                <span class="current-price">₱ 697</span>
            </div>
            <a href="#" class="view-details-btn">VIEW DETAILS</a>
        </div>
        
        <!-- Product 12 -->
        <div class="product-card">
            <img src="../assets/images/img_rectangle_29.svg" alt="Men's Vacation Inspired Floral Embroidery Hollow Knit Sweater" class="product-image">
            <h3 class="product-title">Manfinity Hypemode Men's Vacation Inspired Floral Embroidery Hollow Knit Sweater Men Crochet Shirt</h3>
            <div class="price-container">
                <span class="current-price">₱ 592</span>
                <span class="original-price">₱ 697</span>
                <span class="discount-badge">-15.1%</span>
            </div>
            <a href="#" class="view-details-btn">VIEW DETAILS</a>
        </div>
    </div>
    
    <footer class="footer">
        <div class="footer-container">
            <div class="footer-section">
                <h3>GANCHILLO</h3>
                <div class="footer-links">
                    <a href="#" class="footer-link">About Ganchillo</a>
                    <a href="#" class="footer-link">Privacy Policy</a>
                    <a href="#" class="footer-link">Terms & Conditions</a>
                </div>
            </div>
            
            <div class="footer-section">
                <h3>Customer Care</h3>
                <div class="footer-links">
                    <a href="#" class="footer-link">Contact us</a>
                    <a href="#" class="footer-link">Help Center</a>
                    <a href="#" class="footer-link">Payment Method</a>
                    <a href="#" class="footer-link">FAQ</a>
                </div>
            </div>
            
            <div class="footer-section">
                <h3>FIND US ON</h3>
                <div class="social-icons">
                    <img src="../assets/images/img_fb_icon.png" alt="Facebook" class="social-icon">
                    <img src="../assets/images/img_instagram_icon.png" alt="Instagram" class="social-icon">
                    <img src="../assets/images/img_twitter_x_icon.png" alt="Twitter/X" class="social-icon">
                    <img src="../assets/images/img_image.png" alt="Pinterest" class="social-icon">
                    <img src="../assets/images/img_tiktok_icon.png" alt="TikTok" class="social-icon">
                    <img src="../assets/images/img_youtube_icon.png" alt="YouTube" class="social-icon">
                    <img src="../assets/images/img_linkedin_icon.png" alt="LinkedIn" class="social-icon">
                </div>
                
                <h3>STAY IN THE LOOP, STITCH BY STITCH</h3>
                <div class="newsletter-form">
                    <input type="email" placeholder="Your Email Address" class="newsletter-input">
                    <div class="subscribe-btn-container" style="display: flex; justify-content: flex-end;">
                        <button class="subscribe-btn">SUBSCRIBE</button>
                    </div>
                    
                    <div class="phone-input-container">
                        <div class="phone-prefix">
                            <span>PH + 63</span>
                            <img src="../assets/images/img_polygon_4_7x25.svg" alt="Dropdown arrow">
                        </div>
                        <input type="text" placeholder="Your phone number for SMS" class="phone-input">
                    </div>
                    <div class="subscribe-btn-container" style="display: flex; justify-content: flex-end;">
                        <button class="subscribe-btn">SUBSCRIBE</button>
                    </div>
                </div>
            </div>
        </div>
        
        <img src="../assets/images/img_gachillo_logo.png" alt="Ganchillo Logo" class="footer-logo">
        
        <div class="copyright">
            ©2025 Ganchillo All Rights Reserved
        </div>
    </footer>

    <script>
        // Dropdown functionality
        document.addEventListener('DOMContentLoaded', function() {
            const dropdowns = document.querySelectorAll('.filter-dropdown');
            
            dropdowns.forEach(dropdown => {
                dropdown.addEventListener('click', function() {
                    // Create dropdown menu if it doesn't exist
                    if (!this.querySelector('.dropdown-menu')) {
                        const dropdownMenu = document.createElement('div');
                        dropdownMenu.className = 'dropdown-menu';
                        dropdownMenu.style.position = 'absolute';
                        dropdownMenu.style.backgroundColor = '#f5f5dc';
                        dropdownMenu.style.borderRadius = '10px';
                        dropdownMenu.style.marginTop = '5px';
                        dropdownMenu.style.padding = '10px';
                        dropdownMenu.style.zIndex = '10';
                        dropdownMenu.style.width = '100%';
                        dropdownMenu.style.boxShadow = '0 4px 8px rgba(0,0,0,0.1)';
                        
                        // Add options based on dropdown type
                        let options = [];
                        
                        if (this.id === 'crochetItemDropdown') {
                            options = ['Tops', 'Dresses', 'Pants', 'Accessories', 'Hats', 'Bags'];
                        } else if (this.id === 'priceRangeDropdown') {
                            options = ['Under ₱500', '₱500 - ₱1000', '₱1000 - ₱2000', 'Over ₱2000'];
                        } else if (this.id === 'yarnColorDropdown') {
                            options = ['White', 'Beige', 'Black', 'Brown', 'Green', 'Blue', 'Red', 'Multicolor'];
                        } else if (this.id === 'yarnTypeDropdown') {
                            options = ['Cotton', 'Wool', 'Acrylic', 'Bamboo', 'Silk', 'Blend'];
                        }
                        
                        options.forEach(option => {
                            const optionElement = document.createElement('div');
                            optionElement.className = 'dropdown-option';
                            optionElement.textContent = option;
                            optionElement.style.padding = '8px 10px';
                            optionElement.style.cursor = 'pointer';
                            optionElement.style.color = '#d3b683';
                            optionElement.style.fontFamily = 'Rubik, sans-serif';
                            optionElement.style.fontWeight = '700';
                            
                            optionElement.addEventListener('mouseover', function() {
                                this.style.backgroundColor = '#e8e8d0';
                            });
                            
                            optionElement.addEventListener('mouseout', function() {
                                this.style.backgroundColor = 'transparent';
                            });
                            
                            optionElement.addEventListener('click', function(e) {
                                e.stopPropagation();
                                dropdown.querySelector('span').textContent = option;
                                dropdownMenu.remove();
                                
                                // Filter products based on selection
                                filterProducts(dropdown.id, option);
                            });
                            
                            dropdownMenu.appendChild(optionElement);
                        });
                        
                        this.appendChild(dropdownMenu);
                        
                        // Position the dropdown menu
                        const rect = this.getBoundingClientRect();
                        dropdownMenu.style.left = '0';
                        dropdownMenu.style.top = '100%';
                        dropdownMenu.style.minWidth = rect.width + 'px';
                    } else {
                        // Remove dropdown menu if it exists
                        this.querySelector('.dropdown-menu').remove();
                    }
                });
            });
            
            // Close dropdowns when clicking outside
            document.addEventListener('click', function(e) {
                if (!e.target.closest('.filter-dropdown')) {
                    document.querySelectorAll('.dropdown-menu').forEach(menu => {
                        menu.remove();
                    });
                }
            });
            
            // View Details button functionality
            const viewDetailsButtons = document.querySelectorAll('.view-details-btn');
            
            viewDetailsButtons.forEach(button => {
                button.addEventListener('click', function(e) {
                    e.preventDefault();
                    const productCard = this.closest('.product-card');
                    const productTitle = productCard.querySelector('.product-title').textContent;
                    const productPrice = productCard.querySelector('.current-price').textContent;
                    
                    alert(`Product Details:
${productTitle}
Price: ${productPrice}

This would navigate to the product detail page in a real application.`);
                });
            });
            
            // Newsletter subscription
            const subscribeButtons = document.querySelectorAll('.subscribe-btn');
            
            subscribeButtons.forEach(button => {
                button.addEventListener('click', function() {
                    const input = this.closest('.newsletter-form').querySelector('input');
                    
                    if (input.value.trim() === '') {
                        alert('Please enter your email or phone number to subscribe.');
                    } else {
                        alert(`Thank you for subscribing with: ${input.value}`);
                        input.value = '';
                    }
                });
            });
        });
        
        // Function to filter products (simulation)
        function filterProducts(filterType, option) {
            console.log(`Filtering by ${filterType}: ${option}`);
            
            // In a real application, this would filter the products based on the selection
            // For this demo, we'll just show an alert
            alert(`Products filtered by ${option}`);
            
            // Simulate loading
            const productsGrid = document.querySelector('.products-grid');
            productsGrid.style.opacity = '0.5';
            
            setTimeout(() => {
                productsGrid.style.opacity = '1';
            }, 500);
        }
    </script>
</body>
</html>

<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Ganchillo - Men's Vacation Inspired Floral Embroidery Hollow Knit Sweater</title>
    <link href="https://fonts.googleapis.com/css2?family=Inter:wght@400;500;600;700&family=Judson:wght@400;700&family=Public+Sans:wght@300;400;600;700&family=Raleway:wght@500&family=Rubik:wght@700&family=Heebo:wght@400;500;700&display=swap" rel="stylesheet">
    <style>
        * {
            box-sizing: border-box;
            margin: 0;
            padding: 0;
        }
        
        body {
            font-family: 'Inter', sans-serif;
            background-color: #d3b683;
            color: #f5f5dc;
        }
        
        .header {
            display: flex;
            align-items: center;
            justify-content: space-between;
            padding: 10px 40px;
            background-color: #d3b683;
            border-bottom: 1px solid #f5f5dc;
        }
        
        .logo {
            width: 89px;
            height: 89px;
        }
        
        .nav-links {
            display: flex;
            gap: 30px;
        }
        
        .nav-links a {
            color: #f5f5dc;
            text-decoration: none;
            font-size: 20px;
        }
        
        .search-bar {
            display: flex;
            align-items: center;
            background-color: #f5f5dc;
            border-radius: 10px;
            padding: 5px 15px;
            width: 656px;
            height: 31px;
            border: 1px solid #f5f5dc;
        }
        
        .search-bar img {
            width: 20px;
            height: 20px;
            margin-right: 10px;
        }
        
        .search-bar input {
            background: transparent;
            border: none;
            outline: none;
            width: 100%;
            font-family: 'Rubik', sans-serif;
            font-weight: 700;
            font-size: 16px;
            color: #d3b683;
        }
        
        .search-bar input::placeholder {
            color: #d3b683;
        }
        
        .user-actions {
            display: flex;
            align-items: center;
            gap: 15px;
        }
        
        .icon {
            width: 38px;
            height: 38px;
        }
        
        .breadcrumb {
            padding: 15px 40px;
            font-family: 'Judson', serif;
            font-weight: 700;
            font-size: 20px;
            line-height: 15px;
            color: #f5f5dc;
        }
        
        .breadcrumb a {
            color: #f5f5dc;
            text-decoration: none;
        }
        
        .product-container {
            display: flex;
            padding: 20px 40px;
            gap: 40px;
        }
        
        .product-images {
            display: flex;
            width: 812px;
        }
        
        .thumbnails {
            display: flex;
            flex-direction: column;
            gap: 55px;
        }
        
        .thumbnail {
            width: 179px;
            height: 156px;
            cursor: pointer;
        }
        
        .main-image {
            margin-left: 17px;
            width: 616px;
            height: 611px;
        }
        
        .product-info {
            flex: 1;
        }
        
        .product-title {
            font-family: 'Judson', serif;
            font-weight: 700;
            font-size: 25px;
            line-height: 20px;
            letter-spacing: 1px;
            color: #f5f5dc;
            margin-bottom: 30px;
        }
        
        .rating {
            display: flex;
            align-items: center;
            margin-bottom: 25px;
        }
        
        .stars {
            display: flex;
        }
        
        .star {
            width: 18px;
            height: 18px;
            margin-right: 2px;
        }
        
        .reviews-count {
            margin-left: 15px;
            font-family: 'Judson', serif;
            font-size: 18px;
        }
        
        .price-container {
            display: flex;
            align-items: center;
            margin-bottom: 30px;
        }
        
        .current-price {
            font-family: 'Public Sans', sans-serif;
            font-weight: 700;
            font-size: 18px;
            margin-right: 12px;
        }
        
        .original-price {
            font-family: 'Public Sans', sans-serif;
            font-weight: 300;
            font-size: 18px;
            text-decoration: line-through;
            color: #868686;
            margin-right: 15px;
        }
        
        .discount-badge {
            background-color: #f5f5dc;
            border-radius: 10px;
            padding: 2px 8px;
            font-family: 'Judson', serif;
            font-weight: 700;
            font-size: 15px;
            color: #d3b683;
        }
        
        .color-section {
            margin-bottom: 25px;
        }
        
        .color-option {
            background-color: #f5f5dc;
            border-radius: 10px;
            padding: 12px 25px;
            font-family: 'Judson', serif;
            font-weight: 700;
            font-size: 24px;
            color: #d3b683;
            display: inline-block;
            margin-right: 10px;
            margin-bottom: 10px;
            cursor: pointer;
        }
        
        .color-option.selected {
            background-color: #d3b683;
            color: #f5f5dc;
            border: 2px solid #f5f5dc;
        }
        
        .size-section {
            margin-bottom: 25px;
        }
        
        .size-option {
            background-color: #f5f5dc;
            border-radius: 10px;
            width: 104px;
            height: 48px;
            display: inline-flex;
            align-items: center;
            justify-content: center;
            font-family: 'Judson', serif;
            font-weight: 700;
            font-size: 30px;
            color: #d3b683;
            margin-right: 10px;
            margin-bottom: 10px;
            cursor: pointer;
        }
        
        .size-option.selected {
            background-color: #d3b683;
            color: #f5f5dc;
            border: 2px solid #f5f5dc;
        }
        
        .quantity-section {
            margin-bottom: 25px;
        }
        
        .quantity-label {
            font-family: 'Judson', serif;
            font-weight: 700;
            font-size: 30px;
            margin-bottom: 15px;
        }
        
        .quantity-control {
            display: flex;
            align-items: center;
            background-color: #f5f5dc;
            border-radius: 5px;
            width: 208px;
            height: 37px;
        }
        
        .quantity-btn {
            width: 31px;
            height: 31px;
            background-color: #d3b683;
            display: flex;
            align-items: center;
            justify-content: center;
            cursor: pointer;
        }
        
        .quantity-display {
            flex: 1;
            height: 31px;
            background-color: #d3b683;
            display: flex;
            align-items: center;
            justify-content: center;
            font-family: 'Public Sans', sans-serif;
            font-weight: 600;
            font-size: 12px;
            color: #f5f5dc;
            margin: 0 3px;
        }
        
        .add-to-cart-btn {
            background-color: #f5f5dc;
            border-radius: 5px;
            width: 208px;
            height: 38px;
            display: flex;
            align-items: center;
            padding: 0 13px;
            cursor: pointer;
            margin-bottom: 30px;
        }
        
        .cart-icon-container {
            background-color: #d3b683;
            width: 182px;
            height: 26px;
            display: flex;
            align-items: center;
            padding-left: 2px;
        }
        
        .cart-icon {
            width: 24px;
            height: 24px;
        }
        
        .add-to-cart-text {
            font-family: 'Judson', serif;
            font-weight: 700;
            font-size: 25px;
            color: #f5f5dc;
            margin-left: 5px;
        }
        
        .product-tabs {
            background-color: #fafafa;
            padding: 12px 20px;
            display: flex;
            margin: 0 40px;
        }
        
        .tab {
            font-family: 'Raleway', sans-serif;
            font-weight: 500;
            font-size: 18px;
            color: #d3b683;
            margin-right: 40px;
            cursor: pointer;
        }
        
        .tab.active {
            border-bottom: 2px solid #d3b683;
        }
        
        .product-details {
            display: flex;
            padding: 30px 40px;
            background-color: #d3b683;
        }
        
        .details-label {
            font-family: 'Judson', serif;
            font-weight: 700;
            font-size: 24px;
            line-height: 20px;
            letter-spacing: 3px;
            color: #f5f5dc;
            width: 260px;
        }
        
        .details-value {
            font-family: 'Judson', serif;
            font-weight: 700;
            font-size: 24px;
            line-height: 20px;
            letter-spacing: 3px;
            color: #f5f5dc;
            width: 415px;
        }
        
        .section-title {
            font-family: 'Judson', serif;
            font-weight: 700;
            font-size: 30px;
            color: #d3b683;
            padding: 30px 40px;
            background-color: #fff;
        }
        
        .related-products {
            display: flex;
            flex-wrap: wrap;
            padding: 0 40px;
            gap: 25px;
            background-color: #d3b683;
        }
        
        .product-card {
            width: 408px;
            margin-bottom: 30px;
        }
        
        .product-card-image {
            width: 408px;
            height: 435px;
            object-fit: cover;
        }
        
        .product-card-title {
            font-family: 'Judson', serif;
            font-weight: 700;
            font-size: 15px;
            line-height: 20px;
            color: #f5f5dc;
            margin: 10px 0;
            height: 80px;
            overflow: hidden;
        }
        
        .product-card-price {
            display: flex;
            align-items: center;
            margin-bottom: 10px;
        }
        
        .view-details-btn {
            background-color: #f5f5dc;
            width: 435px;
            height: 67px;
            display: flex;
            align-items: center;
            justify-content: center;
            font-family: 'Judson', serif;
            font-weight: 700;
            font-size: 50px;
            color: #d3b683;
            cursor: pointer;
        }
        
        .reviews-container {
            padding: 20px 40px;
            background-color: #d3b683;
        }
        
        .review-card {
            background-color: #fff;
            border-radius: 13px;
            padding: 27px;
            margin-bottom: 30px;
            width: 1002px;
        }
        
        .review-header {
            display: flex;
            align-items: center;
            margin-bottom: 20px;
        }
        
        .reviewer-avatar {
            width: 54px;
            height: 54px;
            border-radius: 27px;
            margin-right: 15px;
        }
        
        .reviewer-name {
            font-family: 'Heebo', sans-serif;
            font-weight: 500;
            font-size: 23px;
            color: #d3b683;
        }
        
        .review-date {
            font-family: 'Heebo', sans-serif;
            font-weight: 400;
            font-size: 14px;
            color: #d3b683;
            margin-left: 10px;
        }
        
        .verified-badge {
            background-color: #d3b683;
            border-radius: 6px;
            padding: 7px 13px;
            font-family: 'Heebo', sans-serif;
            font-weight: 400;
            font-size: 14px;
            color: #f5f5dc;
            margin-left: 15px;
        }
        
        .review-stars {
            display: flex;
            margin-left: auto;
        }
        
        .review-star {
            width: 40px;
            height: 40px;
            margin-right: 8px;
        }
        
        .review-content {
            font-family: 'Heebo', sans-serif;
            font-weight: 700;
            font-size: 23px;
            color: #d3b683;
        }
        
        .footer {
            background-color: #d3b683;
            padding: 40px;
            border-top: 1px solid #f5f5dc;
        }
        
        .footer-top {
            display: flex;
            justify-content: space-between;
            margin-bottom: 30px;
        }
        
        .footer-logo {
            width: 154px;
            height: 154px;
        }
        
        .footer-title {
            font-family: 'Judson', serif;
            font-weight: 700;
            font-size: 35px;
            color: #f5f5dc;
            margin-bottom: 20px;
        }
        
        .footer-links {
            display: flex;
            flex-direction: column;
        }
        
        .footer-link {
            font-family: 'Judson', serif;
            font-weight: 400;
            font-size: 35px;
            color: #f5f5dc;
            margin-bottom: 15px;
            text-decoration: none;
        }
        
        .social-icons {
            display: flex;
            gap: 8px;
            margin-bottom: 30px;
        }
        
        .social-icon {
            width: 44px;
            height: 44px;
        }
        
        .newsletter-form {
            margin-bottom: 20px;
        }
        
        .newsletter-input {
            background-color: #f5f5dc;
            border-radius: 10px;
            border: none;
            padding: 10px 15px;
            width: 454px;
            height: 44px;
            font-family: 'Rubik', sans-serif;
            font-weight: 700;
            font-size: 16px;
            color: #d3b683;
            margin-right: 10px;
        }
        
        .phone-input-container {
            display: flex;
            margin-bottom: 20px;
        }
        
        .phone-prefix {
            background-color: #f5f5dc;
            border-radius: 10px;
            display: flex;
            align-items: center;
            padding: 0 10px;
            width: 156px;
            height: 42px;
            margin-right: 10px;
        }
        
        .prefix-text {
            font-family: 'Rubik', sans-serif;
            font-weight: 700;
            font-size: 25px;
            color: #d3b683;
        }
        
        .dropdown-icon {
            width: 25px;
            height: 7px;
            margin-left: 10px;
        }
        
        .phone-input {
            background-color: #f5f5dc;
            border-radius: 10px;
            border: none;
            padding: 10px 15px;
            width: 297px;
            height: 44px;
            font-family: 'Rubik', sans-serif;
            font-weight: 700;
            font-size: 16px;
            color: #d3b683;
            margin-right: 10px;
        }
        
        .subscribe-btn {
            background-color: #f5f5dc;
            border-radius: 10px;
            border: none;
            width: 172px;
            height: 42px;
            font-family: 'Rubik', sans-serif;
            font-weight: 700;
            font-size: 25px;
            color: #d3b683;
            cursor: pointer;
        }
        
        .copyright {
            font-family: 'Judson', serif;
            font-weight: 400;
            font-size: 25px;
            color: #f5f5dc;
            text-align: center;
            margin-top: 30px;
        }
        
        /* Responsive styles */
        @media (max-width: 1200px) {
            .product-container {
                flex-direction: column;
            }
            
            .product-images {
                width: 100%;
            }
            
            .main-image {
                width: 100%;
                height: auto;
            }
            
            .related-products {
                justify-content: center;
            }
        }
        
        @media (max-width: 768px) {
            .header {
                flex-wrap: wrap;
                padding: 10px 20px;
            }
            
            .search-bar {
                width: 100%;
                margin: 10px 0;
            }
            
            .product-images {
                flex-direction: column;
            }
            
            .thumbnails {
                flex-direction: row;
                gap: 10px;
                margin-bottom: 20px;
            }
            
            .thumbnail {
                width: 80px;
                height: 80px;
            }
            
            .product-card {
                width: 100%;
            }
            
            .view-details-btn {
                width: 100%;
            }
            
            .review-card {
                width: 100%;
            }
            
            .newsletter-input, .phone-input {
                width: 100%;
                margin-bottom: 10px;
            }
            
            .subscribe-btn {
                width: 100%;
            }
        }
    </style>
</head>
<body>
    <header class="header">
        <img src="../assets/images/img_gachillo_logo.png" alt="Ganchillo Logo" class="logo">
        
        <div class="nav-links">
            <a href="#">Home</a>
            <a href="#">Categories</a>
            <a href="#">Products</a>
        </div>
        
        <div class="search-bar">
            <img src="../assets/images/img_image_2.png" alt="Search Icon">
            <input type="text" placeholder="Search in Ganchillo">
        </div>
        
        <div class="user-actions">
            <div class="language-dropdown">
                <img src="../assets/images/img_language_icon.png" alt="Language" class="icon">
                <span>English</span>
                <img src="../assets/images/img_polygon_4.svg" alt="Dropdown" class="dropdown-icon">
            </div>
            
            <img src="../assets/images/img_notification_icon.png" alt="Notifications" class="icon">
            <img src="../assets/images/img_customer_service_icon.png" alt="Customer Service" class="icon">
            
            <div class="auth-section">
                <img src="../assets/images/img_log_in_icon.png" alt="Login" class="icon">
                <span>Sign up | Log in</span>
            </div>
            
            <img src="../assets/images/img_shopping_cart_icon.png" alt="Shopping Cart" class="icon">
        </div>
    </header>
    
    <div class="breadcrumb">
        <a href="#">Home</a> / <a href="#">Men</a> / <a href="#">Men Clothing</a> / <a href="#">Men Knitwear</a> / <a href="#">Men Knit Tops</a> / GANCHILLO Manfinity Hypemode Men's Vacation Inspired Floral Embroidery Hollow Knit Sweater Men Crochet Shirt
    </div>
    
    <div class="product-container">
        <div class="product-images">
            <div class="thumbnails">
                <img src="../assets/images/img_image_179x156.png" alt="Product Thumbnail 1" class="thumbnail" onclick="changeMainImage(this.src)">
                <img src="../assets/images/img_image_1.png" alt="Product Thumbnail 2" class="thumbnail" onclick="changeMainImage(this.src)">
                <img src="../assets/images/img_image_3.png" alt="Product Thumbnail 3" class="thumbnail" onclick="changeMainImage(this.src)">
                <img src="../assets/images/img_image_4.png" alt="Product Thumbnail 4" class="thumbnail" onclick="changeMainImage(this.src)">
            </div>
            
            <img src="../assets/images/img_image_808x611.png" alt="Main Product Image" class="main-image" id="mainImage">
        </div>
        
        <div class="product-info">
            <h1 class="product-title">Manfinity Hypemode Men's Vacation Inspired Floral Embroidery Hollow Knit Sweater Men Crochet Shirt</h1>
            
            <div class="rating">
                <div class="stars">
                    <img src="../assets/images/img_icons_icstar.svg" alt="Star" class="star">
                    <img src="../assets/images/img_icons_icstar.svg" alt="Star" class="star">
                    <img src="../assets/images/img_icons_icstar.svg" alt="Star" class="star">
                    <img src="../assets/images/img_icons_icstar.svg" alt="Star" class="star">
                    <img src="../assets/images/img_icons_icstar.svg" alt="Star" class="star">
                </div>
                <span class="reviews-count">(1000+ Reviews)</span>
            </div>
            
            <div class="price-container">
                <span class="current-price">₱ 592</span>
                <span class="original-price">₱ 697</span>
                <span class="discount-badge">-15.1%</span>
            </div>
            
            <div class="color-section">
                <div class="color-option selected">Color: Apricot</div>
                <div class="color-option">Burgundy</div>
                <div class="color-option">Baby Blue</div>
                <div class="color-option">Black</div>
                <div class="color-option">Dusty Pink</div>
                <div class="color-option">Blue</div>
                <div class="color-option">Brown</div>
                <div class="color-option">Khaki</div>
            </div>
            
            <div class="size-section">
                <div class="size-option">Size</div>
                <div class="size-option selected">S</div>
                <div class="size-option">M</div>
                <div class="size-option">L</div>
                <div class="size-option">XL</div>
                <div class="size-option">XXL</div>
            </div>
            
            <div class="quantity-section">
                <div class="quantity-label">Quantity</div>
                <div class="quantity-control">
                    <div class="quantity-btn" onclick="decrementQuantity()">
                        <img src="../assets/images/img_edit_removeminus.svg" alt="Minus">
                    </div>
                    <div class="quantity-display" id="quantityDisplay">1</div>
                    <div class="quantity-btn" onclick="incrementQuantity()">
                        <img src="../assets/images/img_icons_add24px.svg" alt="Plus">
                    </div>
                </div>
            </div>
            
            <div class="add-to-cart-btn" onclick="addToCart()">
                <div class="cart-icon-container">
                    <img src="../assets/images/img_shopping_cart_icon_24x24.png" alt="Cart" class="cart-icon">
                    <span class="add-to-cart-text">ADD TO CART</span>
                </div>
            </div>
        </div>
    </div>
    
    <div class="product-tabs">
        <div class="tab active">Product Details</div>
        <div class="tab">Care Guide</div>
        <div class="tab">Reviews</div>
    </div>
    
    <div class="product-details">
        <div class="details-label">
            Details:<br>
            Fit Type:<br>
            Neckline:<br>
            Pattern Type:<br>
            Sleeve Type:<br>
            Style:<br>
            Hem Shaped:<br>
            Color:<br>
            Sleeve Length:<br>
            Length:<br>
            Fabric:<br>
            Material:<br>
            Composition:<br>
            Care Instructions:<br>
            Sheer:
        </div>
        <div class="details-value">
            Button Front<br>
            Loose<br>
            Lapel<br>
            Animal, Plants<br>
            Regular Sleeve<br>
            Casual<br>
            Regular<br>
            Apricot<br>
            Short Sleeve<br>
            Regular<br>
            Non-Stretch<br>
            Knitwear<br>
            100% Acrylic<br>
            Hand wash, do not dry clean<br>
            Semi-Sheer
        </div>
    </div>
    
    <div class="section-title">Related Products</div>
    
    <div class="related-products">
        <div class="product-card">
            <img src="../assets/images/img_image_123.png" alt="Related Product 1" class="product-card-image">
            <div class="product-card-title">Anewsta Men's Knit Crocheted Apricot "Old Money" Casual Loose Hollow Out Short Sleeve Shirt, Suitable For Everyday, Commute, Summer, Vacation, Party, Wedding, Couples, Boyfriend Gift, Beachwear</div>
            <div class="product-card-price">
                <span class="current-price">₱ 523</span>
                <span class="original-price">₱ 581</span>
                <span class="discount-badge">-10%</span>
            </div>
            <div class="view-details-btn">VIEW DETAILS</div>
        </div>
        
        <div class="product-card">
            <img src="../assets/images/img_image_30.png" alt="Related Product 2" class="product-card-image">
            <div class="product-card-title">Ganchillo Khaki Crochet Knit Frill Hen Mini Dress Spring Y2K 90's Casual Cute Easter Sun Summer Ibiza Rave VacationBoho, Bohemian, Cowgirl, Festival, Concert, Western</div>
            <div class="product-card-price">
                <span class="current-price">₱813</span>
                <span class="original-price">₱ 903</span>
                <span class="discount-badge">-10%</span>
            </div>
            <div class="view-details-btn">VIEW DETAILS</div>
        </div>
        
        <div class="product-card">
            <img src="../assets/images/img_image_44.png" alt="Related Product 3" class="product-card-image">
            <div class="product-card-title">1 Women's Solid Color Hollow Woven Bucket Hat, Breathable And Thin Sun Hat, Suitable For Outdoor Travel</div>
            <div class="product-card-price">
                <span class="current-price">₱174</span>
                <span class="original-price">₱205</span>
                <span class="discount-badge">-15%</span>
            </div>
            <div class="view-details-btn">VIEW DETAILS</div>
        </div>
        
        <div class="product-card">
            <img src="../assets/images/img_image_75.png" alt="Related Product 4" class="product-card-image">
            <div class="product-card-title">GANCHILLO WOMEN Crochet Mini Shorts With Stripe Detail</div>
            <div class="product-card-price">
                <span class="current-price">₱ 655</span>
                <span class="original-price">₱ 739</span>
                <span class="discount-badge">-  10%</span>
            </div>
            <div class="view-details-btn">VIEW DETAILS</div>
        </div>
        
        <div class="product-card">
            <img src="../assets/images/img_image_118.png" alt="Related Product 5" class="product-card-image">
            <div class="product-card-title">Fairycore Mermaid Medium Tote Bag Hollow Out DesignSchool Bag,Back To School,Large Capacity,Portable,Classic Casual, Suitable For Teen Girls Women College Students, Perfect For Back To School,College,Elementary School,Middle School, High School,Work, Business, Commute,Shopping,Holiday</div>
            <div class="product-card-price">
                <span class="current-price">₱ 188</span>
            </div>
            <div class="view-details-btn">VIEW DETAILS</div>
        </div>
        
        <div class="product-card">
            <img src="../assets/images/img_image_165.png" alt="Related Product 6" class="product-card-image">
            <div class="product-card-title">Ganchillo Hippie Y2K Glamorous Island Floral Crochet Bikini Top, Summer Beach Resort Coconut Girl Knit Shirt For Women</div>
            <div class="product-card-price">
                <span class="current-price">₱ 605</span>
            </div>
            <div class="view-details-btn">VIEW DETAILS</div>
        </div>
    </div>
    
    <div class="section-title">Product Reviews</div>
    
    <div class="reviews-container">
        <div class="review-card">
            <div class="review-header">
                <img src="../assets/images/img_image_54x54.png" alt="Reviewer" class="reviewer-avatar">
                <div class="reviewer-info">
                    <span class="reviewer-name">Kai</span>
                    <span class="review-date"> 15 April</span>
                </div>
                <div class="verified-badge">Verified</div>
                <div class="review-stars">
                    <img src="../assets/images/img_starduotone.svg" alt="Star" class="review-star">
                    <img src="../assets/images/img_starduotone.svg" alt="Star" class="review-star">
                    <img src="../assets/images/img_starduotone.svg" alt="Star" class="review-star">
                    <img src="../assets/images/img_starduotone.svg" alt="Star" class="review-star">
                    <img src="../assets/images/img_starduotone.svg" alt="Star" class="review-star">
                </div>
            </div>
            <div class="review-content">
                Absolutely love this shirt! I wore it on my vacation and received so many compliments. It's perfect for warm weather!
            </div>
        </div>
        
        <div class="review-card">
            <div class="review-header">
                <img src="../assets/images/img_image_54x54.png" alt="Reviewer" class="reviewer-avatar">
                <div class="reviewer-info">
                    <span class="reviewer-name">Ethan</span>
                    <span class="review-date"> 11 April</span>
                </div>
                <div class="verified-badge">Verified</div>
                <div class="review-stars">
                    <img src="../assets/images/img_starduotone.svg" alt="Star" class="review-star">
                    <img src="../assets/images/img_starduotone.svg" alt="Star" class="review-star">
                    <img src="../assets/images/img_starduotone.svg" alt="Star" class="review-star">
                    <img src="../assets/images/img_starduotone.svg" alt="Star" class="review-star">
                    <img src="../assets/images/img_starduotone.svg" alt="Star" class="review-star">
                </div>
            </div>
            <div class="review-content">
                I like the design, but I expected it to be more durable. It looks great, but I'm worried about its longevity.
            </div>
        </div>
        
        <div class="review-card">
            <div class="review-header">
                <img src="../assets/images/img_image_54x54.png" alt="Reviewer" class="reviewer-avatar">
                <div class="reviewer-info">
                    <span class="reviewer-name">Noint</span>
                    <span class="review-date"> 5  April</span>
                </div>
                <div class="verified-badge">Verified</div>
                <div class="review-stars">
                    <img src="../assets/images/img_starduotone.svg" alt="Star" class="review-star">
                    <img src="../assets/images/img_starduotone.svg" alt="Star" class="review-star">
                    <img src="../assets/images/img_starduotone.svg" alt="Star" class="review-star">
                    <img src="../assets/images/img_starduotone.svg" alt="Star" class="review-star">
                    <img src="../assets/images/img_starduotone.svg" alt="Star" class="review-star">
                </div>
            </div>
            <div class="review-content">
                Overall, I'm happy with the purchase. After a wash or two, it feels more comfortable. Definitely a great addition to my wardrobe!
            </div>
        </div>
    </div>
    
    <footer class="footer">
        <div class="footer-columns">
            <div class="footer-column">
                <img src="../assets/images/img_gachillo_logo.png" alt="Ganchillo Logo" class="footer-logo">
                <h3 class="footer-title">GANCHILLO</h3>
                <div class="footer-links">
                    <a href="#" class="footer-link">About Ganchillo</a>
                    <a href="#" class="footer-link">Privacy Policy</a>
                    <a href="#" class="footer-link">Terms & Conditions</a>
                </div>
            </div>
            
            <div class="footer-column">
                <h3 class="footer-title">Customer Care</h3>
                <div class="footer-links">
                    <a href="#" class="footer-link">Contact us</a>
                    <a href="#" class="footer-link">Help Center</a>
                    <a href="#" class="footer-link">Payment Method</a>
                    <a href="#" class="footer-link">FAQ</a>
                </div>
            </div>
            
            <div class="footer-column">
                <h3 class="footer-title">FIND US ON</h3>
                <div class="social-icons">
                    <img src="../assets/images/img_fb_icon.png" alt="Facebook" class="social-icon">
                    <img src="../assets/images/img_instagram_icon.png" alt="Instagram" class="social-icon">
                    <img src="../assets/images/img_twitter_x_icon.png" alt="Twitter" class="social-icon">
                    <img src="../assets/images/img_image.png" alt="Pinterest" class="social-icon">
                    <img src="../assets/images/img_tiktok_icon.png" alt="TikTok" class="social-icon">
                    <img src="../assets/images/img_youtube_icon.png" alt="YouTube" class="social-icon">
                    <img src="../assets/images/img_linkedin_icon.png" alt="LinkedIn" class="social-icon">
                </div>
                
                <h3 class="footer-title">STAY IN THE LOOP, STITCH BY STITCH</h3>
                
                <div class="newsletter-form">
                    <input type="email" placeholder="Your Email Address" class="newsletter-input">
                    <button class="subscribe-btn">SUBSCRIBE</button>
                </div>
                
                <div class="phone-input-container">
                    <div class="phone-prefix">
                        <span class="prefix-text">PH + 63</span>
                        <img src="../assets/images/img_polygon_4_7x25.svg" alt="Dropdown" class="dropdown-icon">
                    </div>
                    <input type="tel" placeholder="Your phone number for SMS" class="phone-input">
                    <button class="subscribe-btn">SUBSCRIBE</button>
                </div>
            </div>
        </div>
        
        <div class="copyright">
            ©2025 Ganchillo All Rights Reserved
        </div>
    </footer>

    <script>
        // Function to change the main product image
        function changeMainImage(src) {
            document.getElementById('mainImage').src = src;
        }
        
        // Function to handle quantity increment
        function incrementQuantity() {
            const quantityDisplay = document.getElementById('quantityDisplay');
            let quantity = parseInt(quantityDisplay.innerText);
            quantity++;
            quantityDisplay.innerText = quantity;
        }
        
        // Function to handle quantity decrement
        function decrementQuantity() {
            const quantityDisplay = document.getElementById('quantityDisplay');
            let quantity = parseInt(quantityDisplay.innerText);
            if (quantity > 1) {
                quantity--;
                quantityDisplay.innerText = quantity;
            }
        }
        
        // Function to handle add to cart
        function addToCart() {
            const quantity = document.getElementById('quantityDisplay').innerText;
            const selectedColor = document.querySelector('.color-option.selected').innerText.replace('Color: ', '');
            const selectedSize = document.querySelector('.size-option.selected').innerText;
            
            alert(`Added ${quantity} ${selectedColor} ${selectedSize} shirt(s) to your cart!`);
        }
        
        // Color selection functionality
        const colorOptions = document.querySelectorAll('.color-option');
        colorOptions.forEach(option => {
            option.addEventListener('click', function() {
                colorOptions.forEach(opt => opt.classList.remove('selected'));
                this.classList.add('selected');
            });
        });
        
        // Size selection functionality
        const sizeOptions = document.querySelectorAll('.size-option');
        sizeOptions.forEach(option => {
            option.addEventListener('click', function() {
                if (this.innerText !== 'Size') {
                    sizeOptions.forEach(opt => opt.classList.remove('selected'));
                    this.classList.add('selected');
                }
            });
        });
        
        // Tab switching functionality
        const tabs = document.querySelectorAll('.tab');
        tabs.forEach(tab => {
            tab.addEventListener('click', function() {
                tabs.forEach(t => t.classList.remove('active'));
                this.classList.add('active');
                
                // In a real implementation, this would show/hide different content sections
                alert(`Switched to ${this.innerText} tab`);
            });
        });
        
        // View details functionality for related products
        const viewDetailsButtons = document.querySelectorAll('.view-details-btn');
        viewDetailsButtons.forEach(button => {
            button.addEventListener('click', function() {
                const productTitle = this.previousElementSibling.previousElementSibling.innerText;
                alert(`Viewing details for: ${productTitle}`);
            });
        });
    </script>
</body>
</html>


<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Shopping Cart - Ganchillo</title>
    <style>
        * {
            box-sizing: border-box;
            margin: 0;
            padding: 0;
            font-family: 'Inter', sans-serif;
        }
        
        body {
            background-color: #d3b683;
            color: #f5f5dc;
        }
        
        .header {
            display: flex;
            align-items: center;
            justify-content: space-between;
            padding: 10px 40px;
            background-color: #d3b683;
            border-bottom: 12px solid #fff;
        }
        
        .logo {
            width: 89px;
            height: 89px;
        }
        
        .nav-links {
            display: flex;
            gap: 40px;
        }
        
        .nav-links a {
            color: #f5f5dc;
            text-decoration: none;
            font-size: 20px;
            font-weight: 400;
        }
        
        .search-bar {
            display: flex;
            align-items: center;
            background-color: #f5f5dc;
            border-radius: 10px;
            padding: 5px 15px;
            width: 656px;
            height: 31px;
            border: 1px solid #f5f5dc;
        }
        
        .search-bar input {
            border: none;
            background: transparent;
            width: 100%;
            color: #d3b683;
            font-weight: 700;
            font-family: 'Rubik', sans-serif;
            font-size: 16px;
            outline: none;
        }
        
        .search-bar input::placeholder {
            color: #d3b683;
            font-weight: 700;
        }
        
        .search-icon {
            width: 20px;
            height: 20px;
            margin-right: 10px;
        }
        
        .right-nav {
            display: flex;
            align-items: center;
            gap: 15px;
        }
        
        .icon {
            width: 38px;
            height: 38px;
        }
        
        .icon-text {
            display: flex;
            align-items: center;
            gap: 10px;
        }
        
        .dropdown-icon {
            width: 25px;
            height: 7px;
        }
        
        .cart-container {
            padding: 40px 60px;
        }
        
        .back-button {
            display: flex;
            align-items: center;
            gap: 10px;
            margin-bottom: 30px;
            cursor: pointer;
        }
        
        .back-button span {
            font-size: 25px;
            font-family: 'Judson', serif;
            font-weight: 700;
            color: #f5f5dc;
        }
        
        .page-title {
            font-size: 40px;
            font-family: 'Judson', serif;
            font-weight: 700;
            color: #f5f5dc;
            margin-bottom: 40px;
        }
        
        .cart-item-container {
            background-color: #fff;
            padding: 38px;
            margin-bottom: 40px;
        }
        
        .cart-item {
            background-color: #d3b683;
            padding: 48px 33px;
            display: flex;
            position: relative;
        }
        
        .product-image {
            width: 386px;
            height: 214px;
            object-fit: cover;
        }
        
        .product-details {
            margin-left: 57px;
        }
        
        .product-title {
            font-size: 25px;
            font-family: 'Judson', serif;
            font-weight: 700;
            color: #f5f5dc;
            letter-spacing: 1px;
            line-height: 20px;
            max-width: 373px;
            margin-bottom: 47px;
        }
        
        .price-container {
            display: flex;
            align-items: center;
            gap: 12px;
        }
        
        .current-price {
            font-size: 18px;
            font-family: 'Public Sans', sans-serif;
            font-weight: 700;
            color: #f5f5dc;
        }
        
        .original-price {
            font-size: 18px;
            font-family: 'Public Sans', sans-serif;
            font-weight: 300;
            color: #868686;
            text-decoration: line-through;
        }
        
        .discount-badge {
            background-color: #f5f5dc;
            border-radius: 10px;
            padding: 2px 8px;
            font-size: 15px;
            font-family: 'Judson', serif;
            font-weight: 700;
            color: #d3b683;
        }
        
        .quantity-section {
            position: absolute;
            right: 33px;
            top: 88px;
        }
        
        .quantity-label {
            font-size: 30px;
            font-family: 'Judson', serif;
            font-weight: 700;
            color: #f5f5dc;
            margin-bottom: 20px;
        }
        
        .quantity-controls {
            display: flex;
            background-color: #f5f5dc;
            border-radius: 5px;
            height: 37px;
            width: 208px;
        }
        
        .quantity-btn {
            width: 31px;
            height: 31px;
            background-color: #d3b683;
            border: none;
            display: flex;
            align-items: center;
            justify-content: center;
            cursor: pointer;
            margin: 3px;
        }
        
        .quantity-input {
            flex-grow: 1;
            background-color: #d3b683;
            border: none;
            margin: 3px;
            text-align: center;
            color: #f5f5dc;
            font-size: 12px;
            font-family: 'Public Sans', sans-serif;
            font-weight: 600;
        }
        
        .remove-btn {
            position: absolute;
            right: 33px;
            bottom: 48px;
            font-size: 30px;
            font-family: 'Judson', serif;
            font-weight: 700;
            color: #f5f5dc;
            background: none;
            border: none;
            cursor: pointer;
        }
        
        .shipping-info {
            font-size: 35px;
            font-family: 'Judson', serif;
            font-weight: 700;
            color: #f5f5dc;
            margin-bottom: 40px;
        }
        
        .total-section {
            display: flex;
            justify-content: space-between;
            align-items: center;
            margin-bottom: 40px;
        }
        
        .total-label {
            font-size: 40px;
            font-family: 'Judson', serif;
            font-weight: 700;
            color: #f5f5dc;
        }
        
        .total-amount {
            font-size: 36px;
            font-family: 'Public Sans', sans-serif;
            font-weight: 700;
            color: #f5f5dc;
        }
        
        .checkout-btn {
            background-color: #f5f5dc;
            color: #d3b683;
            font-size: 50px;
            font-family: 'Judson', serif;
            font-weight: 700;
            text-align: center;
            padding: 15px;
            cursor: pointer;
            margin-bottom: 40px;
        }
        
        .footer {
            padding: 40px 60px;
            border-top: 12px solid #fff;
        }
        
        .footer-top {
            display: flex;
            justify-content: space-between;
            margin-bottom: 40px;
        }
        
        .footer-logo {
            width: 156px;
            height: 156px;
        }
        
        .footer-title {
            font-size: 35px;
            font-family: 'Judson', serif;
            font-weight: 700;
            color: #f5f5dc;
            margin-bottom: 20px;
        }
        
        .social-icons {
            display: flex;
            gap: 7px;
            margin-bottom: 30px;
        }
        
        .social-icon {
            width: 56px;
            height: 45px;
        }
        
        .footer-columns {
            display: flex;
            justify-content: space-between;
            margin-bottom: 40px;
        }
        
        .footer-column {
            display: flex;
            flex-direction: column;
            gap: 20px;
        }
        
        .footer-heading {
            font-size: 35px;
            font-family: 'Judson', serif;
            font-weight: 700;
            color: #f5f5dc;
            margin-bottom: 20px;
        }
        
        .footer-link {
            font-size: 35px;
            font-family: 'Judson', serif;
            font-weight: 400;
            color: #f5f5dc;
            text-decoration: none;
        }
        
        .newsletter-form {
            margin-top: 20px;
        }
        
        .input-group {
            display: flex;
            margin-bottom: 20px;
        }
        
        .input-field {
            background-color: #f5f5dc;
            border: 1px solid #f5f5dc;
            border-radius: 10px;
            padding: 11px 15px;
            font-size: 16px;
            font-family: 'Rubik', sans-serif;
            font-weight: 700;
            color: #d3b683;
            width: 454px;
            height: 45px;
        }
        
        .phone-input {
            display: flex;
        }
        
        .country-code {
            background-color: #f5f5dc;
            border: 1px solid #f5f5dc;
            border-radius: 10px;
            padding: 3px 10px;
            font-size: 25px;
            font-family: 'Rubik', sans-serif;
            font-weight: 700;
            color: #d3b683;
            width: 156px;
            height: 43px;
            margin-right: 10px;
        }
        
        .phone-field {
            background-color: #f5f5dc;
            border: 1px solid #f5f5dc;
            border-radius: 10px;
            padding: 12px 15px;
            font-size: 16px;
            font-family: 'Rubik', sans-serif;
            font-weight: 700;
            color: #d3b683;
            width: 297px;
            height: 45px;
        }
        
        .subscribe-btn {
            background-color: #f5f5dc;
            border: none;
            border-radius: 10px;
            padding: 4px 13px;
            font-size: 25px;
            font-family: 'Rubik', sans-serif;
            font-weight: 700;
            color: #d3b683;
            width: 172px;
            height: 43px;
            margin-left: 10px;
            cursor: pointer;
        }
        
        .copyright {
            text-align: center;
            font-size: 25px;
            font-family: 'Judson', serif;
            font-weight: 400;
            color: #f5f5dc;
            margin-top: 40px;
        }
    </style>
</head>
<body>
    <header class="header">
        <img src="../assets/images/img_gachillo_logo.png" alt="Ganchillo Logo" class="logo">
        
        <div class="nav-links">
            <a href="#">Home</a>
            <a href="#">Categories</a>
            <a href="#">Products</a>
        </div>
        
        <div class="search-bar">
            <img src="../assets/images/img_image_2.png" alt="Search Icon" class="search-icon">
            <input type="text" placeholder="Search in Ganchillo">
        </div>
        
        <div class="right-nav">
            <div class="icon-text">
                <img src="../assets/images/img_language_icon.png" alt="Language Icon" class="icon">
                <span>English</span>
                <img src="../assets/images/img_polygon_4.svg" alt="Dropdown Icon" class="dropdown-icon">
            </div>
            
            <div class="icon-text">
                <img src="../assets/images/img_notification_icon.png" alt="Notification Icon" class="icon">
                <span>Notification</span>
            </div>
            
            <div class="icon-text">
                <img src="../assets/images/img_customer_service_icon.png" alt="Customer Service Icon" class="icon">
                <span>Costumer Service</span>
            </div>
            
            <div class="icon-text">
                <img src="../assets/images/img_log_in_icon.png" alt="Login Icon" class="icon">
                <span>Sign up | Log in</span>
            </div>
            
            <img src="../assets/images/img_shopping_cart_icon.png" alt="Shopping Cart Icon" class="icon">
        </div>
    </header>
    
    <main class="cart-container">
        <div class="back-button">
            <img src="../assets/images/img_fluentiosarrow24regular.svg" alt="Back Arrow" width="24" height="24">
            <span>Back</span>
        </div>
        
        <h1 class="page-title">Shopping Cart</h1>
        
        <div class="cart-item-container">
            <div class="cart-item">
                <img src="../assets/images/img_image.png" alt="Crochet Shirt" class="product-image">
                
                <div class="product-details">
                    <h2 class="product-title">Manfinity Hypemode Men's Vacation Inspired Floral Embroidery Hollow Knit Sweater Men Crochet Shirt</h2>
                    
                    <div class="price-container">
                        <span class="current-price">₱ 592</span>
                        <span class="original-price">₱ 697</span>
                        <span class="discount-badge">-15.1%</span>
                    </div>
                </div>
                
                <div class="quantity-section">
                    <div class="quantity-label">Quantity:</div>
                    <div class="quantity-controls">
                        <button class="quantity-btn decrease-btn">
                            <img src="../assets/images/img_edit_removeminus.svg" alt="Decrease" width="18" height="18">
                        </button>
                        <input type="text" value="1" class="quantity-input" readonly>
                        <button class="quantity-btn increase-btn">
                            <img src="../assets/images/img_icons_add24px.svg" alt="Increase" width="18" height="18">
                        </button>
                    </div>
                </div>
                
                <button class="remove-btn">Remove</button>
            </div>
        </div>
        
        <div class="shipping-info">
            Is your cart eligible for free shipping? Enter your zip code Find out.
        </div>
        
        <div class="total-section">
            <div class="total-label">Total</div>
            <div class="total-amount">₱ 592</div>
        </div>
        
        <div class="checkout-btn">Proceed to Checkout</div>
    </main>
    
    <footer class="footer">
        <div class="footer-top">
            <div class="footer-left">
                <img src="../assets/images/img_gachillo_logo.png" alt="Ganchillo Logo" class="footer-logo">
                <h3 class="footer-title">GANCHILLO</h3>
                
                <div class="footer-columns">
                    <div class="footer-column">
                        <a href="#" class="footer-link">About Ganchillo</a>
                        <a href="#" class="footer-link">Privacy Policy</a>
                        <a href="#" class="footer-link">Terms & Conditions</a>
                    </div>
                    
                    <div class="footer-column">
                        <h3 class="footer-heading">Customer Care</h3>
                        <a href="#" class="footer-link">Contact us</a>
                        <a href="#" class="footer-link">Help Center</a>
                        <a href="#" class="footer-link">Payment Method</a>
                        <a href="#" class="footer-link">FAQ</a>
                    </div>
                </div>
            </div>
            
            <div class="footer-right">
                <h3 class="footer-title">FIND US ON</h3>
                
                <div class="social-icons">
                    <img src="../assets/images/img_fb_icon.png" alt="Facebook" class="social-icon">
                    <img src="../assets/images/img_instagram_icon.png" alt="Instagram" class="social-icon">
                    <img src="../assets/images/img_twitter_x_icon.png" alt="Twitter" class="social-icon">
                    <img src="../assets/images/img_image_45x56.png" alt="Pinterest" class="social-icon">
                    <img src="../assets/images/img_tiktok_icon.png" alt="TikTok" class="social-icon">
                    <img src="../assets/images/img_youtube_icon.png" alt="YouTube" class="social-icon">
                    <img src="../assets/images/img_linkedin_icon.png" alt="LinkedIn" class="social-icon">
                </div>
                
                <h3 class="footer-title">STAY IN THE LOOP, STITCH BY STITCH</h3>
                
                <div class="newsletter-form">
                    <div class="input-group">
                        <input type="email" placeholder="Your Email Address" class="input-field">
                        <button class="subscribe-btn">SUBSCRIBE</button>
                    </div>
                    
                    <div class="input-group phone-input">
                        <div class="country-code">PH + 63</div>
                        <input type="tel" placeholder="Your phone number for SMS" class="phone-field">
                        <button class="subscribe-btn">SUBSCRIBE</button>
                    </div>
                </div>
            </div>
        </div>
        
        <div class="copyright">©2025 Ganchillo All Rights Reserved</div>
    </footer>

    <script>
        document.addEventListener('DOMContentLoaded', function() {
            // Quantity controls
            const decreaseBtn = document.querySelector('.decrease-btn');
            const increaseBtn = document.querySelector('.increase-btn');
            const quantityInput = document.querySelector('.quantity-input');
            const removeBtn = document.querySelector('.remove-btn');
            const checkoutBtn = document.querySelector('.checkout-btn');
            const backButton = document.querySelector('.back-button');
            
            // Initialize quantity
            let quantity = 1;
            
            // Decrease quantity
            decreaseBtn.addEventListener('click', function() {
                if (quantity > 1) {
                    quantity--;
                    quantityInput.value = quantity;
                    updateTotal();
                }
            });
            
            // Increase quantity
            increaseBtn.addEventListener('click', function() {
                quantity++;
                quantityInput.value = quantity;
                updateTotal();
            });
            
            // Remove item
            removeBtn.addEventListener('click', function() {
                const cartItem = document.querySelector('.cart-item');
                cartItem.style.display = 'none';
                
                // Update total to zero
                document.querySelector('.total-amount').textContent = '₱ 0';
                
                // Show empty cart message
                const cartContainer = document.querySelector('.cart-item-container');
                const emptyMessage = document.createElement('div');
                emptyMessage.textContent = 'Your cart is empty';
                emptyMessage.style.padding = '30px';
                emptyMessage.style.textAlign = 'center';
                emptyMessage.style.fontSize = '24px';
                emptyMessage.style.color = '#d3b683';
                cartContainer.appendChild(emptyMessage);
            });
            
            // Update total based on quantity
            function updateTotal() {
                const basePrice = 592;
                const total = basePrice * quantity;
                document.querySelector('.total-amount').textContent = `₱ ${total}`;
                document.querySelector('.current-price').textContent = `₱ ${total}`;
            }
            
            // Checkout button
            checkoutBtn.addEventListener('click', function() {
                alert('Proceeding to checkout...');
            });
            
            // Back button
            backButton.addEventListener('click', function() {
                alert('Going back to previous page...');
            });
            
            // Shipping eligibility
            const shippingInfo = document.querySelector('.shipping-info');
            shippingInfo.addEventListener('click', function() {
                const zipCode = prompt('Enter your zip code:');
                if (zipCode) {
                    if (zipCode.length === 5 && !isNaN(zipCode)) {
                        alert('Congratulations! Your order is eligible for free shipping.');
                    } else {
                        alert('Please enter a valid 5-digit zip code.');
                    }
                }
            });
            
            // Newsletter subscription
            const subscribeBtns = document.querySelectorAll('.subscribe-btn');
            subscribeBtns.forEach(btn => {
                btn.addEventListener('click', function() {
                    const input = this.previousElementSibling;
                    if (input.value.trim() !== '') {
                        alert('Thank you for subscribing!');
                        input.value = '';
                    } else {
                        alert('Please enter a valid email or phone number.');
                    }
                });
            });
        });
    </script>
</body>
</html>

<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Ganchillo Checkout</title>
    <style>
        * {
            box-sizing: border-box;
            margin: 0;
            padding: 0;
        }
        
        body {
            font-family: 'Inter', 'Judson', 'Montserrat', 'Rubik', 'Public Sans', sans-serif;
            background-color: #d3b683;
            color: #f5f5dc;
        }
        
        .header {
            display: flex;
            align-items: center;
            justify-content: space-between;
            padding: 10px 20px;
            background-color: #d3b683;
            height: 70px;
        }
        
        .logo {
            width: 89px;
            height: 89px;
        }
        
        .nav-links {
            display: flex;
            gap: 40px;
        }
        
        .nav-links a {
            color: #f5f5dc;
            text-decoration: none;
            font-size: 20px;
            font-weight: 400;
        }
        
        .right-nav {
            display: flex;
            align-items: center;
            gap: 15px;
        }
        
        .language-selector, .notification, .customer-service, .user-auth {
            display: flex;
            align-items: center;
            gap: 5px;
            color: #f5f5dc;
            font-size: 20px;
        }
        
        .search-bar {
            display: flex;
            align-items: center;
            background-color: #f5f5dc;
            border-radius: 10px;
            padding: 5px 15px;
            width: 656px;
            height: 31px;
            border: 1px solid #f5f5dc;
        }
        
        .search-bar input {
            border: none;
            background: transparent;
            width: 100%;
            color: #d3b683;
            font-weight: 700;
            font-size: 16px;
            font-family: 'Rubik', sans-serif;
        }
        
        .search-bar input::placeholder {
            color: #d3b683;
        }
        
        .search-icon {
            width: 20px;
            height: 20px;
        }
        
        .cart-icon {
            width: 38px;
            height: 38px;
        }
        
        .main-content {
            display: flex;
            padding: 20px;
            gap: 20px;
        }
        
        .customer-details, .order-summary {
            flex: 1;
            padding: 20px;
        }
        
        .section-title {
            font-size: 40px;
            font-family: 'Judson', serif;
            font-weight: 700;
            color: #f5f5dc;
            margin-bottom: 20px;
        }
        
        .section-description {
            font-size: 25px;
            font-family: 'Judson', serif;
            font-weight: 700;
            color: #f5f5dc;
            line-height: 1.4;
            margin-bottom: 30px;
            text-align: justify;
        }
        
        .form-group {
            margin-bottom: 20px;
        }
        
        .form-label {
            display: block;
            font-size: 16px;
            font-family: 'Montserrat', sans-serif;
            font-weight: 500;
            color: #ffffff;
            margin-bottom: 10px;
        }
        
        .form-input {
            width: 100%;
            height: 76px;
            border: 2px solid #bebebe;
            border-radius: 17px;
            padding: 0 20px;
            font-size: 16px;
            font-family: 'Montserrat', sans-serif;
            color: #d3b683;
            background-color: #ffffff;
        }
        
        .payment-title {
            font-size: 30px;
            font-family: 'Judson', serif;
            font-weight: 700;
            color: #ffffff;
            margin: 20px 0;
        }
        
        .back-button {
            display: flex;
            align-items: center;
            gap: 10px;
            font-size: 25px;
            font-family: 'Judson', serif;
            font-weight: 700;
            color: #f5f5dc;
            margin-bottom: 30px;
            cursor: pointer;
            background: none;
            border: none;
        }
        
        .product-card {
            background-color: #ffffff;
            border-radius: 10px;
            padding: 15px;
            margin-bottom: 20px;
        }
        
        .product-inner {
            background-color: #d3b683;
            border-radius: 10px;
            padding: 20px;
            display: flex;
            flex-direction: column;
        }
        
        .product-details {
            display: flex;
            gap: 20px;
        }
        
        .product-image {
            width: 199px;
            height: 312px;
            object-fit: cover;
        }
        
        .product-info {
            flex: 1;
        }
        
        .product-title {
            font-size: 25px;
            font-family: 'Judson', serif;
            font-weight: 700;
            color: #f5f5dc;
            line-height: 1.2;
            margin-bottom: 20px;
        }
        
        .product-price {
            display: flex;
            align-items: center;
            gap: 10px;
            margin-top: 10px;
        }
        
        .quantity {
            font-size: 25px;
            font-family: 'Public Sans', sans-serif;
            font-weight: 700;
            color: #f5f5dc;
        }
        
        .current-price {
            font-size: 25px;
            font-family: 'Public Sans', sans-serif;
            font-weight: 700;
            color: #f5f5dc;
        }
        
        .original-price {
            font-size: 20px;
            font-family: 'Public Sans', sans-serif;
            font-weight: 300;
            color: #868686;
            text-decoration: line-through;
        }
        
        .discount-badge {
            background-color: #f5f5dc;
            border-radius: 10px;
            padding: 3px 8px;
            font-size: 15px;
            font-family: 'Judson', serif;
            font-weight: 700;
            color: #d3b683;
        }
        
        .total-price {
            font-size: 25px;
            font-family: 'Public Sans', sans-serif;
            font-weight: 700;
            color: #f5f5dc;
            text-align: right;
            margin-top: 20px;
        }
        
        .submit-button {
            background-color: #f5f5dc;
            border-radius: 10px;
            border: none;
            padding: 15px;
            font-size: 50px;
            font-family: 'Judson', serif;
            font-weight: 700;
            color: #d3b683;
            width: 100%;
            cursor: pointer;
            margin-top: 30px;
        }
        
        .footer {
            background-color: #d3b683;
            padding: 40px 20px;
            margin-top: 50px;
        }
        
        .footer-top {
            display: flex;
            justify-content: space-between;
            margin-bottom: 30px;
        }
        
        .footer-logo {
            width: 156px;
            height: 156px;
        }
        
        .footer-title {
            font-size: 35px;
            font-family: 'Judson', serif;
            font-weight: 700;
            color: #f5f5dc;
            margin-bottom: 20px;
        }
        
        .footer-columns {
            display: flex;
            justify-content: space-between;
            margin-bottom: 30px;
        }
        
        .footer-column {
            flex: 1;
        }
        
        .footer-link {
            font-size: 35px;
            font-family: 'Judson', serif;
            font-weight: 400;
            color: #f5f5dc;
            display: block;
            margin-bottom: 15px;
            text-decoration: none;
        }
        
        .social-icons {
            display: flex;
            gap: 10px;
            margin-bottom: 20px;
        }
        
        .social-icon {
            width: 45px;
            height: 45px;
        }
        
        .newsletter-form {
            display: flex;
            gap: 10px;
            margin-bottom: 20px;
        }
        
        .newsletter-input {
            flex: 1;
            height: 45px;
            border: 1px solid #f5f5dc;
            border-radius: 10px;
            background-color: #f5f5dc;
            padding: 0 15px;
            font-size: 16px;
            font-family: 'Rubik', sans-serif;
            font-weight: 700;
            color: #d3b683;
        }
        
        .phone-input-group {
            display: flex;
            gap: 10px;
        }
        
        .country-code {
            width: 156px;
            height: 43px;
            border: none;
            border-radius: 10px;
            background-color: #f5f5dc;
            display: flex;
            align-items: center;
            justify-content: space-between;
            padding: 0 10px;
            font-size: 25px;
            font-family: 'Rubik', sans-serif;
            font-weight: 700;
            color: #d3b683;
        }
        
        .phone-input {
            flex: 1;
            height: 45px;
            border: 1px solid #f5f5dc;
            border-radius: 10px;
            background-color: #f5f5dc;
            padding: 0 15px;
            font-size: 16px;
            font-family: 'Rubik', sans-serif;
            font-weight: 700;
            color: #d3b683;
        }
        
        .subscribe-button {
            width: 172px;
            height: 43px;
            border: none;
            border-radius: 10px;
            background-color: #f5f5dc;
            font-size: 25px;
            font-family: 'Rubik', sans-serif;
            font-weight: 700;
            color: #d3b683;
            cursor: pointer;
        }
        
        .copyright {
            font-size: 25px;
            font-family: 'Judson', serif;
            font-weight: 400;
            color: #f5f5dc;
            text-align: center;
            margin-top: 30px;
        }
        
        @media (max-width: 1200px) {
            .main-content {
                flex-direction: column;
            }
            
            .search-bar {
                width: 400px;
            }
            
            .nav-links {
                gap: 20px;
            }
        }
        
        @media (max-width: 768px) {
            .header {
                flex-wrap: wrap;
                height: auto;
            }
            
            .search-bar {
                width: 100%;
                margin: 10px 0;
            }
            
            .nav-links {
                display: none;
            }
            
            .footer-columns {
                flex-direction: column;
                gap: 20px;
            }
        }
    </style>
</head>
<body>
    <header class="header">
        <img src="../assets/images/img_gachillo_logo.png" alt="Ganchillo Logo" class="logo">
        
        <nav class="nav-links">
            <a href="#">Home</a>
            <a href="#">Categories</a>
            <a href="#">Products</a>
        </nav>
        
        <div class="search-bar">
            <img src="../assets/images/img_image_2.png" alt="Search Icon" class="search-icon">
            <input type="text" placeholder="Search in Ganchillo">
        </div>
        
        <div class="right-nav">
            <div class="language-selector">
                <img src="../assets/images/img_language_icon.png" alt="Language Icon" width="38" height="38">
                <span>English</span>
                <img src="../assets/images/img_polygon_4.svg" alt="Dropdown Arrow" width="7" height="25">
            </div>
            
            <div class="notification">
                <img src="../assets/images/img_notification_icon.png" alt="Notification Icon" width="38" height="38">
                <span>Notification</span>
            </div>
            
            <div class="customer-service">
                <img src="../assets/images/img_customer_service_icon.png" alt="Customer Service Icon" width="42" height="42">
                <span>Costumer Service</span>
            </div>
            
            <div class="user-auth">
                <img src="../assets/images/img_log_in_icon.png" alt="Login Icon" width="32" height="32">
                <span>Sign up | Log in</span>
            </div>
            
            <img src="../assets/images/img_shopping_cart_icon.png" alt="Shopping Cart" class="cart-icon">
        </div>
    </header>
    
    <main class="main-content">
        <section class="customer-details">
            <button class="back-button">
                <img src="../assets/images/img_vector.svg" alt="Back Arrow" width="20" height="10">
                <span>Back</span>
            </button>
            
            <h1 class="section-title">Customer Details</h1>
            <p class="section-description">Fill in your customer details and payment information to complete the order.</p>
            
            <form id="checkout-form">
                <div class="form-group">
                    <label for="email" class="form-label">Email Address</label>
                    <input type="email" id="email" class="form-input" placeholder="Your Email Address" required>
                </div>
                
                <div class="form-group">
                    <label for="fullname" class="form-label">Full Name</label>
                    <input type="text" id="fullname" class="form-input" placeholder="Your Full Name" required>
                </div>
                
                <div class="form-group">
                    <label for="address" class="form-label">Address</label>
                    <input type="text" id="address" class="form-input" placeholder="Address" required>
                </div>
                
                <div class="form-group">
                    <label for="city" class="form-label">City</label>
                    <input type="text" id="city" class="form-input" placeholder="City" required>
                </div>
                
                <div class="form-group">
                    <label for="zipcode" class="form-label">Zip Code</label>
                    <input type="text" id="zipcode" class="form-input" placeholder="Zip Code" required>
                </div>
                
                <h2 class="payment-title">Payment Information</h2>
                
                <div class="form-group">
                    <label for="cardnumber" class="form-label">Credit / Debit Card</label>
                    <input type="text" id="cardnumber" class="form-input" placeholder="Card Number" required>
                </div>
            </form>
        </section>
        
        <section class="order-summary">
            <h1 class="section-title">Order Summary</h1>
            <p class="section-description">Here's your order summary! You can make changes, remove items, and pick how you'd like your order delivered.</p>
            
            <div class="product-card">
                <div class="product-inner">
                    <div class="product-details">
                        <img src="../assets/images/img_image_199x312.png" alt="Knit Sweater" class="product-image">
                        
                        <div class="product-info">
                            <h3 class="product-title">Manfinity Hypemode Men's Vacation Inspired Floral Embroidery Hollow Knit Sweater Men Crochet Shirt</h3>
                            
                            <div class="product-price">
                                <span class="quantity">1 x</span>
                                <span class="current-price">₱ 592</span>
                                <span class="original-price">₱ 697</span>
                                <span class="discount-badge">-15.1%</span>
                            </div>
                        </div>
                    </div>
                    
                    <div class="total-price">₱ 592</div>
                </div>
            </div>
            
            <button type="submit" form="checkout-form" class="submit-button">Submit Order</button>
        </section>
    </main>
    
    <footer class="footer">
        <div class="footer-top">
            <div>
                <img src="../assets/images/img_gachillo_logo.png" alt="Ganchillo Logo" class="footer-logo">
                <h2 class="footer-title">GANCHILLO</h2>
            </div>
            
            <div>
                <h2 class="footer-title">Customer Care</h2>
            </div>
            
            <div>
                <h2 class="footer-title">FIND US ON</h2>
                <div class="social-icons">
                    <img src="../assets/images/img_fb_icon.png" alt="Facebook" class="social-icon">
                    <img src="../assets/images/img_instagram_icon.png" alt="Instagram" class="social-icon">
                    <img src="../assets/images/img_twitter_x_icon.png" alt="Twitter/X" class="social-icon">
                    <img src="../assets/images/img_image.png" alt="Pinterest" class="social-icon">
                    <img src="../assets/images/img_tiktok_icon.png" alt="TikTok" class="social-icon">
                    <img src="../assets/images/img_youtube_icon.png" alt="YouTube" class="social-icon">
                    <img src="../assets/images/img_linkedin_icon.png" alt="LinkedIn" class="social-icon">
                </div>
                
                <h2 class="footer-title">STAY IN THE LOOP, STITCH BY STITCH</h2>
                
                <div class="newsletter-form">
                    <input type="email" placeholder="Your Email Address" class="newsletter-input">
                    <button class="subscribe-button">SUBSCRIBE</button>
                </div>
                
                <div class="phone-input-group">
                    <div class="country-code">
                        PH + 63
                        <img src="../assets/images/img_polygon_4_7x25.svg" alt="Dropdown Arrow" width="7" height="25">
                    </div>
                    <input type="tel" placeholder="Your phone number for SMS" class="phone-input">
                    <button class="subscribe-button">SUBSCRIBE</button>
                </div>
            </div>
        </div>
        
        <div class="footer-columns">
            <div class="footer-column">
                <a href="#" class="footer-link">About Ganchillo</a>
                <a href="#" class="footer-link">Privacy Policy</a>
                <a href="#" class="footer-link">Terms & Conditions</a>
            </div>
            
            <div class="footer-column">
                <a href="#" class="footer-link">Contact us</a>
                <a href="#" class="footer-link">Help Center</a>
                <a href="#" class="footer-link">Payment Method</a>
                <a href="#" class="footer-link">FAQ</a>
            </div>
        </div>
        
        <div class="copyright">©2025 Ganchillo All Rights Reserved</div>
    </footer>

    <script>
        // Form validation
        document.getElementById('checkout-form').addEventListener('submit', function(e) {
            e.preventDefault();
            
            // Simple validation
            const email = document.getElementById('email').value;
            const fullname = document.getElementById('fullname').value;
            const address = document.getElementById('address').value;
            const city = document.getElementById('city').value;
            const zipcode = document.getElementById('zipcode').value;
            const cardnumber = document.getElementById('cardnumber').value;
            
            if (!email || !fullname || !address || !city || !zipcode || !cardnumber) {
                alert('Please fill in all required fields');
                return;
            }
            
            // Email validation
            const emailRegex = /^[^\s@]+@[^\s@]+\.[^\s@]+$/;
            if (!emailRegex.test(email)) {
                alert('Please enter a valid email address');
                return;
            }
            
            // Card number validation (simple check for 16 digits)
            const cardRegex = /^[0-9]{16}$/;
            if (!cardRegex.test(cardnumber.replace(/\s/g, ''))) {
                alert('Please enter a valid 16-digit card number');
                return;
            }
            
            // If all validations pass, show success message
            alert('Order submitted successfully! Thank you for your purchase.');
            
            // Reset form
            this.reset();
        });
        
        // Back button functionality
        document.querySelector('.back-button').addEventListener('click', function() {
            // In a real app, this would navigate back to the previous page
            alert('Going back to previous page');
        });
        
        // Language selector dropdown
        document.querySelector('.language-selector').addEventListener('click', function() {
            alert('Language options would appear here');
        });
        
        // Country code dropdown
        document.querySelector('.country-code').addEventListener('click', function() {
            alert('Country code options would appear here');
        });
        
        // Newsletter subscription
        document.querySelectorAll('.subscribe-button').forEach(button => {
            button.addEventListener('click', function(e) {
                e.preventDefault();
                const input = this.previousElementSibling;
                if (input && input.value) {
                    alert('Thank you for subscribing!');
                    input.value = '';
                } else {
                    alert('Please enter your information to subscribe');
                }
            });
        });
    </script>
</body>
</html>
