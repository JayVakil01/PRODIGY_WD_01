# PRODIGY_WD_01
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Responsive Landing Page</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
        }

        html {
            scroll-behavior: smooth;
        }

        nav {
            position: fixed;
            top: 0;
            width: 100%;
            padding: 20px 50px;
            display: flex;
            justify-content: space-between;
            align-items: center;
            background-color: transparent; 
            transition: background-color 0.4s ease, padding 0.4s ease;
            z-index: 1000;
        }

        nav.scrolled {
            background-color: #1a1a1a; 
            padding: 15px 50px;
            box-shadow: 0 5px 15px rgba(0,0,0,0.3);
        }

        nav .logo {
            color: #fff;
            font-size: 24px;
            font-weight: bold;
            text-decoration: none;
            letter-spacing: 2px;
        }

        nav ul {
            list-style: none;
            display: flex;
        }

        nav ul li {
            margin-left: 30px;
        }

        nav ul li a {
            text-decoration: none;
            color: #fff;
            font-size: 16px;
            font-weight: 500;
            transition: color 0.3s ease;
        }

        nav ul li a:hover {
            color: #00d2ff; 
        }

        section {
            height: 100vh;
            display: flex;
            flex-direction: column;
            justify-content: center;
            align-items: center;
            text-align: center;
            padding: 0 20px;
        }

        #home {
            background: linear-gradient(135deg, #3a7bd5, #3a6073);
            color: white;
        }

        #home h1 {
            font-size: 3rem;
            margin-bottom: 20px;
        }

        #home p {
            font-size: 1.2rem;
            max-width: 600px;
        }

        #about { background-color: #f4f4f4; color: #333; }
        #services { background-color: #e2e2e2; color: #333; }
        #contact { background-color: #d1d1d1; color: #333; }

        section h2 { font-size: 2.5rem; margin-bottom: 15px; }

        @media (max-width: 768px) {
            nav {
                flex-direction: column;
                padding: 15px 20px;
            }

            nav.scrolled {
                padding: 15px 20px;
            }

            nav ul {
                margin-top: 15px;
                flex-wrap: wrap;
                justify-content: center;
            }

            nav ul li {
                margin: 5px 10px;
            }

            #home h1 {
                font-size: 2rem;
            }
        }
    </style>
</head>
<body>

    <nav id="navbar">
        <a href="#home" class="logo">PRODIGY</a>
        <ul>
            <li><a href="#home">Home</a></li>
            <li><a href="#about">About</a></li>
            <li><a href="#services">Services</a></li>
            <li><a href="#contact">Contact</a></li>
        </ul>
    </nav>

    <section id="home">
        <h1>Welcome to Task 01</h1>
        <p>This is a fully responsive landing page. Scroll down to see the navigation menu change its background color dynamically.</p>
    </section>

    <section id="about">
        <h2>About Section</h2>
        <p>The navigation bar remains fixed at the top of the screen.</p>
    </section>

    <section id="services">
        <h2>Services Section</h2>
        <p>Hover over the links in the menu above to see the color change effect.</p>
    </section>

    <section id="contact">
        <h2>Contact Section</h2>
        <p>This layout adapts to both desktop and mobile screens.</p>
    </section>

    <script>
        const navbar = document.getElementById('navbar');

        window.addEventListener('scroll', () => {
            if (window.scrollY > 50) {
                navbar.classList.add('scrolled');
            } else {
                navbar.classList.remove('scrolled');
            }
        });
    </script>

</body>
</html>
