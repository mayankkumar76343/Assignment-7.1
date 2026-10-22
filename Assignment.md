 Assignment 7.1 — Responsive Navigation Bar1. HTML file — Assignment-7.1.html

<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Assignment 7.1 - Responsive Navbar</title>
    <link rel="stylesheet" href="style.css">
</head>
<body>

    <header class="header">
        <nav class="navbar">

            <!-- Website Logo -->
            <a href="#" class="logo">MyWebsite</a>

            <!-- Navigation Links -->
            <ul class="nav-links">
                <li><a href="#home">Home</a></li>
                <li><a href="#about">About</a></li>
                <li><a href="#services">Services</a></li>
                <li><a href="#contact">Contact</a></li>
            </ul>

            <!-- Navigation Button -->
            <a href="#get-started" class="nav-button">Get Started</a>

        </nav>
    </header>

    <main>
        <section class="hero" id="home">
            <h1>Welcome to MyWebsite</h1>
            <p>
                Explore our website to learn more about our services
                and what we offer.
            </p>
            <a href="#services" class="hero-button">Explore More</a>
        </section>

        <section class="content-section" id="about">
            <h2>About Us</h2>
            <p>We create simple, modern, and user-friendly websites.</p>
        </section>

        <section class="content-section" id="services">
            <h2>Our Services</h2>
            <p>We offer web design, development, and responsive layouts.</p>
        </section>

        <section class="content-section" id="contact">
            <h2>Contact Us</h2>
            <p>Get in touch with us to learn more.</p>
        </section>
    </main>

</body>
</html>
2. CSS file — style.css

css

/* Reset */
* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
}

html {
    scroll-behavior: smooth;
}

body {
    font-family: Arial, sans-serif;
    color: #1e293b;
    background-color: #f8fafc;
}

/* Header */
.header {
    width: 100%;
    background-color: #1e293b;
}

/* Flexbox navigation bar */
.navbar {
    display: flex;
    justify-content: space-between;
    align-items: center;
    max-width: 1200px;
    min-height: 75px;
    margin: 0 auto;
    padding: 15px 25px;
    gap: 25px;
}

/* Logo */
.logo {
    color: #38bdf8;
    font-size: 26px;
    font-weight: bold;
    text-decoration: none;
    white-space: nowrap;
}

/* Navigation links */
.nav-links {
    display: flex;
    align-items: center;
    justify-content: center;
    gap: 25px;
    list-style: none;
}

.nav-links a {
    color: #ffffff;
    text-decoration: none;
    font-size: 16px;
    transition: color 0.3s;
}

.nav-links a:hover {
    color: #38bdf8;
}

/* Get Started button */
.nav-button {
    display: inline-block;
    padding: 11px 18px;
    background-color: #0284c7;
    color: #ffffff;
    border-radius: 7px;
    text-decoration: none;
    font-weight: bold;
    white-space: nowrap;
    transition: background-color 0.3s;
}

.nav-button:hover {
    background-color: #0369a1;
}

/* Hero section */
.hero {
    min-height: 300px;
    padding: 80px 20px;
    text-align: center;
    background-color: #e0f2fe;
}

.hero h1 {
    margin-bottom: 15px;
    font-size: 36px;
}

.hero p {
    margin-bottom: 25px;
    color: #475569;
    line-height: 1.6;
}

.hero-button {
    display: inline-block;
    padding: 12px 22px;
    background-color: #0284c7;
    color: white;
    border-radius: 7px;
    text-decoration: none;
}

.hero-button:hover {
    background-color: #0369a1;
}

/* Content sections */
.content-section {
    max-width: 900px;
    margin: 25px auto;
    padding: 35px 20px;
    text-align: center;
}

.content-section h2 {
    margin-bottom: 12px;
    color: #0369a1;
}

/* Responsive layout */
@media (max-width: 768px) {
    .navbar {
        flex-wrap: wrap;
        justify-content: center;
        gap: 18px;
    }

    .nav-links {
        order: 3;
        width: 100%;
        flex-wrap: wrap;
        gap: 18px;
    }

    .logo {
        margin-right: auto;
    }
}

@media (max-width: 480px) {
    .navbar {
        padding: 15px;
        gap: 15px;
    }

    .logo {
        font-size: 22px;
    }

    .nav-button {
        padding: 9px 12px;
        font-size: 13px;
    }

    .nav-links {
        gap: 12px 18px;
    }

    .nav-links a {
        font-size: 14px;
    }

    .hero {
        padding: 60px 15px;
    }

    .hero h1 {
        font-size: 28px;
    }
}