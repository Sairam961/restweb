# Ex.07 Restaurant Website
## Date:

## AIM:
To develop a static Restaurant website to display the food items and services provided by them.

## DESIGN STEPS:

### Step 1:
Requirement collection.

### Step 2:
Creating the layout using HTML and CSS.

### Step 3:
Updating the sample content.

### Step 4:
Choose the appropriate style and color scheme.

### Step 5:
Validate the layout in various browsers.

### Step 6:
Validate the HTML code.

### Step 7:
Publish the website in the given URL.

## PROGRAM:
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8" />
<title>FoodCart</title>
<meta name="viewport" content="width=960" />
<style>
    /* Colors */
    body {
        background: #f7f4ed;
        margin: 0;
        font-family: 'Georgia', serif;
        color: #222;
    }
    .header {
        text-align: center;
        padding: 20px 0 10px 0;
        background: #f7f4ed;
    }
    .header-logo {
        height: 60px;
        vertical-align: middle;
    }
    .header-title {
        display: inline-block;
        font-size: 2.6rem;
        color: #404040;
        margin-left: 18px;
        letter-spacing: 0.22rem;
        font-weight: 900;
        vertical-align: middle;
        font-family: 'Courier New', Courier, monospace;
    }
    nav {
        background: #404040;
    }
    nav ul {
        list-style: none;
        margin: 0;
        padding: 0;
        display: flex;
        justify-content: center;
    }
    nav li {
        margin: 0 24px;
    }
    nav a {
        display: inline-block;
        color: #fff;
        text-decoration: none;
        font-family: monospace;
        font-size: 1.2rem;
        padding: 12px 22px;
        border-radius: 7px 7px 0 0;
        letter-spacing: 1.6px;
        transition: background-color 0.3s;
    }
    nav a.active, nav a:hover {
        background: #2a2a2a;
    }
    .banner {
        position: relative;
        overflow: hidden;
        border-radius: 11px;
        margin: 34px auto 34px auto;
        max-width: 920px;
        min-height: 120px;
        background: #ddd;
        display: flex;
        align-items: flex-end;
        box-shadow: 0 4px 14px #dedede;
    }
    .banner img {
        width: 100%;
        height: 180px;
        object-fit: cover;
        display: block;
    }
    .banner-content {
        position: absolute;
        left: 0;
        top: 0;
        width: 100%;
        min-height: 100%;
        background: rgba(64,64,64,0.65);
        color: #ffffffde;
        padding: 20px 38px 16px 38px;
        display: flex;
        flex-direction: column;
        justify-content: flex-end;
    }
    .banner-content h2 {
        font-size: 2.05rem;
        margin: 0 0 18px 0;
        font-weight: 900;
        font-family: 'Courier New', Courier, monospace;
        letter-spacing: 0.05rem;
    }
    .banner-content p {
        font-size: 1rem;
        margin: 0;
        opacity: 0.94;
    }
    .main-cards {
        display: flex;
        justify-content: center;
        gap: 26px;
        margin: 0 auto 32px auto;
        max-width: 980px;
    }
    .card {
        background: #f2d18c;
        border-radius: 16px;
        padding: 22px;
        box-shadow: 2px 4px 14px #e2b65aaf;
        width: 295px;
    }
    .card h3 {
        font-size: 1.25rem;
        margin: 0 0 12px 0;
        font-family: 'Georgia', serif;
        font-weight: 700;
        color: #404040;
    }
    .card img {
        width: 100%;
        height: 120px;
        object-fit: cover;
        border-radius: 7px;
    }
    .card p {
        font-size: 1rem;
        margin: 13px 0;
        color: #333;
    }
    .card a {
        color: #404040;
        font-size: 1rem;
        text-decoration: underline;
        cursor: pointer;
    }
    /* MENU PAGE */
    .menu-section {
        display: flex;
        flex-wrap: wrap;
        gap: 22px;
        justify-content: center;
        max-width: 1000px;
        margin: 32px auto;
    }
    .menu-item {
        background: #f7e8b8;
        border-radius: 10px;
        box-shadow: 1px 2px 12px #f0d8798c;
        width: 200px;
        padding: 16px;
        text-align: center;
    }
    .menu-item img {
        width: 100%;
        height: 92px;
        object-fit: cover;
        border-radius: 8px;
    }
    .menu-item h4 {
        margin: 9px 0 6px 0;
        font-size: 1.12rem;
        color: #404040;
    }
    .menu-item p {
        margin: 0;
        font-size: 0.98rem;
    }
    /* ADMIN PAGE */
    .admin-section {
        display: flex;
        flex-wrap: wrap;
        gap: 23px;
        justify-content: center;
        max-width: 1100px;
        margin: 44px auto;
    }
    .admin-card {
        width: 220px;
        background: #f2d18c;
        border-radius: 12px;
        text-align: center;
        box-shadow: 0px 2px 10px #dfbe6569;
        padding: 20px 12px;
    }
    .admin-photo {
        width: 100px;
        height: 100px;
        border-radius: 50%;
        object-fit: cover;
        margin-bottom: 10px;
        margin-top: 3px;
    }
    .admin-card h4 {
        margin: 7px 0 3px 0;
        font-size: 1.1em;
        color: #404040;
    }
    .admin-card p {
        color: #222;
        margin: 0 0 7px 0;
        font-size: 1em;
    }
    /* CONTACT PAGE */
    .contact-block {
        background: #f7e8b8;
        border-radius: 14px;
        max-width: 650px;
        margin: 40px auto;
        padding: 28px 48px;
        box-shadow: 1px 3px 16px #f0d8799e;
        font-size: 1.1rem;
        color: #222;
    }
    .contact-block h2 {
        color: #404040;
        margin-bottom: 12px;
    }
    .footer {
        margin-top: 46px;
        text-align: center;
        color: #fff;
        background: #404040;
        font-size: 1.1rem;
        padding: 18px 0 10px 0;
        letter-spacing: 1.8px;
    }
    .footer .footer-logo {
        vertical-align: middle;
        height: 1.3em;
        margin-right: 15px;
    }
</style>
</head>
<body>

<div class="header">
    <img src="5.jpg" alt="FoodCart Logo" class="header-logo" width="60" height="60" />
    <span class="header-title">FOODCART</span>
</div>
<nav>
    <ul>
        <li><a href="#" class="active" onclick="showTab('home')">Home</a></li>
        <li><a href="#" onclick="showTab('menu')">Menu</a></li>
        <li><a href="#" onclick="showTab('admin')">Administration</a></li>
        <li><a href="#" onclick="showTab('contact')">Contact Us</a></li>
    </ul>
</nav>

<!-- HOME PAGE -->
<section id="homeTab">
    <div class="banner">
        <img src="4.jpg" alt="Featuring Today's Specials" width="100%" height="180" />
        <div class="banner-content">
            <h2>Delicious Meals, Every Day</h2>
            <p>Welcome to FoodCart, your neighborhood place for fresh ingredients and hearty flavors. Enjoy complimentary appetizers when you dine in this weekend. We’re committed to exceptional quality and friendly service.</p>
        </div>
    </div>
    <div class="main-cards">
        <div class="card">
            <h3>Chef’s Picks</h3>
            <img src="1.jpg" alt="Chef's Picks Image" width="100%" height="120" />
            <p>Our top recommendations crafted with passion and fresh produce sourced locally.</p>
            <a href="#" onclick="showTab('menu')">Browse our selections</a>
        </div>
        <div class="card">
            <h3>Reserve a Table</h3>
            <img src="2.jpg" alt="Table Reservation" width="100%" height="120" />
            <p>Book your spot with ease. Perfect for celebrations and gatherings.</p>
            <a href="#">Make a reservation</a>
        </div>
        <div class="card">
            <h3>Opening Hours</h3>
            <img src="3.jpg" alt="Open Kitchen" width="100%" height="120" />
            <p>We open daily with flexible meal times. Come taste the best local dishes!</p>
            <b>Mon - Fri:</b> 11am - 9pm<br />
            <b>Sat - Sun:</b> 12pm - 11pm
        </div>
    </div>
</section>

<!-- MENU PAGE -->
<section id="menuTab" style="display:none;">
    <h2 style="text-align:center; margin:34px 0 20px 0;color:#404040;">Our Menu</h2>
    <div class="menu-section">
        <div class="menu-item"><img src="" alt="Grilled Chicken" width="200" height="92" /><h4>Grilled Chicken Salad</h4><p>Marinated chicken with mixed greens.</p></div>
        <div class="menu-item"><img src="" alt="Vegan Burger" width="200" height="92" /><h4>Vegan Burger</h4><p>Plant-based patty with avocado.</p></div>
        <div class="menu-item"><img src="" alt="Pasta Primavera" width="200" height="92" /><h4>Pasta Primavera</h4><p>Fresh veggies in light sauce.</p></div>
        <div class="menu-item"><img src="" alt="Roast Beef" width="200" height="92" /><h4>Roast Beef</h4><p>Slow-roasted tender slices.</p></div>
        <div class="menu-item"><img src="" alt="Seafood Paella" width="200" height="92" /><h4>Seafood Paella</h4><p>Saffron rice with fresh catch.</p></div>
        <div class="menu-item"><img src="" alt="Tomato Soup" width="200" height="92" /><h4>Tomato Basil Soup</h4><p>Classic comforting tomato soup.</p></div>
        <div class="menu-item"><img src="" alt="Stuffed Peppers" width="200" height="92" /><h4>Stuffed Bell Peppers</h4><p>Filled with rice and herbs.</p></div>
        <div class="menu-item"><img src="" alt="BBQ Ribs" width="200" height="92" /><h4>BBQ Ribs</h4><p>Smoked with our secret sauce.</p></div>
        <div class="menu-item"><img src="" alt="Garden Salad" width="200" height="92" /><h4>Garden Salad</h4><p>Seasonal greens and vinaigrette.</p></div>
        <div class="menu-item"><img src="" alt="Fruit Tart" width="200" height="92" /><h4>Fruit Tart</h4><p>Mixed berries on flaky crust.</p></div>
        <div class="menu-item"><img src="" alt="Chocolate Cake" width="200" height="92" /><h4>Chocolate Cake</h4><p>Rich and moist with ganache.</p></div>
        <div class="menu-item"><img src="" alt="Vanilla Ice Cream" width="200" height="92" /><h4>Vanilla Ice Cream</h4><p>Creamy and classic frozen dessert.</p></div>
    </div>
</section>

<!-- ADMIN PAGE -->
<section id="adminTab" style="display:none;">
    <h2 style="text-align:center; margin:34px 0 24px;color:#404040;">Administration Team</h2>
    <div class="admin-section">
        <div class="admin-card">
            <img src="" alt="Liam Hughes" class="admin-photo" width="100" height="100" />
            <h4>Liam Hughes</h4>
            <p>General Manager</p>
        </div>
        <div class="admin-card">
            <img src="" alt="Emma Walker" class="admin-photo" width="100" height="100" />
            <h4>Emma Walker</h4>
            <p>Head Chef</p>
        </div>
        <div class="admin-card">
            <img src="" alt="Noah Lee" class="admin-photo" width="100" height="100" />
            <h4>Noah Lee</h4>
            <p>Sous Chef</p>
        </div>
        <div class="admin-card">
            <img src="" alt="Ava Martinez" class="admin-photo" width="100" height="100" />
            <h4>Ava Martinez</h4>
            <p>Pastry Specialist</p>
        </div>
        <div class="admin-card">
            <img src="" alt="Ethan Perez" class="admin-photo" width="100" height="100" />
            <h4>Ethan Perez</h4>
            <p>Front-of-House Lead</p>
        </div>
        <div class="admin-card">
            <img src="" alt="Sophia Adams" class="admin-photo" width="100" height="100" />
            <h4>Sophia Adams</h4>
            <p>Customer Relations</p>
        </div>
    </div>
</section>

<!-- CONTACT PAGE -->
<section id="contactTab" style="display:none;">
    <div class="contact-block">
        <h2>Contact Us</h2>
        <p>
        <b>Address:</b> 45 Market Street, Downtown City, Country<br />
        <b>Phone:</b> +123 456 7890<br />
        <b>Email:</b> contact@foodcart.com
        </p>
        <p>
        For reservations or inquiries, please call or email us anytime. We look forward to serving you!
        </p>
    </div>
</section>

<footer class="footer">
    FOODCART developed by R.Sairam
</footer>

<script>
    // Tab navigation script
    function showTab(tabName) {
        const tabs = ['homeTab','menuTab','adminTab','contactTab'];
        tabs.forEach(id => {
            document.getElementById(id).style.display = (id === tabName + 'Tab') ? 'block' : 'none';
        });
        // Update active nav link
        const navLinks = document.querySelectorAll('nav a');
        navLinks.forEach(link => link.classList.remove('active'));
        switch(tabName) {
            case 'home': navLinks[0].classList.add('active'); break;
            case 'menu': navLinks[1].classList.add('active'); break;
            case 'admin': navLinks[2].classList.add('active'); break;
            case 'contact': navLinks[3].classList.add('active'); break;
        }
        window.scrollTo(0,0);
    }
    // show home by default
    showTab('home');
</script>

</body>
</html>



## OUTPUT:


## RESULT:
The program for designing software company website using HTML and CSS is completed successfully.
