# PRODIGY_WD_01
TASK 1-Create an interactive navigation menu
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Interactive Navigation Menu</title>
    <link rel="stylesheet" href="styles.css">
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

    <div id="content">
        <section id="home">
            <h1>Home</h1>
            <p>Welcome to the homepage.</p>
        </section>
        <section id="about">
            <h1>About</h1>
            <p>Learn more about us.</p>
        </section>
        <section id="services">
            <h1>Services</h1>
            <p>Discover our services.</p>
        </section>
        <section id="contact">
            <h1>Contact</h1>
            <p>Get in touch with us.</p>
        </section>
    </div>

    <script src="script.js"></script>
</body>
</html>

body {
    font-family: Arial, sans-serif;
    margin: 0;
    padding: 0;
}

nav {
    position: fixed;
    top: 0;
    width: 100%;
    background-color: #333;
    color: white;
    z-index: 1000;
    transition: background-color 0.3s;
}

nav ul {
    list-style: none;
    padding: 0;
    margin: 0;
    display: flex;
    justify-content: center;
}

nav ul li {
    margin: 0 15px;
}

nav ul li a {
    text-decoration: none;
    color: white;
    padding: 15px 20px;
    display: block;
    transition: background-color 0.3s, color 0.3s;
}

nav ul li a:hover {
    background-color: #555;
    color: #fff;
}

#content {
    padding-top: 60px; /* to prevent content from being hidden under the fixed navbar */
}

section {
    padding: 50px;
    margin: 50px 0;
    background-color: #f4f4f4;
    border: 1px solid #ddd;
    border-radius: 5px;
}

window.addEventListener('scroll', function() {
    var navbar = document.getElementById('navbar');
    if (window.scrollY > 50) {
        navbar.style.backgroundColor = '#222';
    } else {
        navbar.style.backgroundColor = '#333';
    }
});
