# new-coding
new repo
html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <link rel="stylesheet" href="styles.css">
    <title>Interactive Navigation Menu</title>
</head>
<body>
    <nav id="navbar">
        <ul>
            <li><a href="#home">Home</a></li>
            <li><a href="#about">About</a></li>
            <li><a href="#services">Services</a></li>
            <li><a href="#contact">Contact</a></li>
        </ul>
    </nav>
    <div class="content">
        <h1>Welcome to Our Website</h1>
        <p>Scroll down to see the effect.</p>
        <div style="height: 1500px;"></div> <!-- Just to create scrollable content -->
    </div>
    <script src="script.js"></script>
</body>
</html>


### CSS (styles.css)

css
body {
    margin: 0;
    font-family: Arial, sans-serif;
}

#navbar {
    position: fixed;
    width: 100%;
    background-color: #333;
    color: white;
    padding: 15px 0;
    transition: background-color 0.3s, color 0.3s;
}

#navbar ul {
    list-style-type: none;
    margin: 0;
    padding: 0;
    display: flex;
    justify-content: center;
}

#navbar li {
    margin: 0 20px;
}

#navbar a {
    color: white;
    text-decoration: none;
    font-size: 18px;
    transition: color 0.3s;
}

#navbar a:hover {
    color: #ff6347; /* Change color on hover */
}

.scrolled {
    background-color: #222; /* Darker background when scrolled */
    color: #ff6347; /* Change text color when scrolled */
}


### JavaScript (script.js)

javascript
window.onscroll = function() {
    const navbar = document.getElementById("navbar");
    if (document.body.scrollTop > 50 || document.documentElement.scrollTop > 50) {
        navbar.classList.add("scrolled");
    } else {
        navbar.classList.remove("scrolled");
    }
};

