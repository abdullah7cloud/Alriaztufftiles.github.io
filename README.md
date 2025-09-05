<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Al Riaz Blocks and Tuftile | Premium Concrete Solutions</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <link href="https://fonts.googleapis.com/css2?family=Montserrat:wght@400;500;600;700&family=Roboto:wght@300;400;500&display=swap" rel="stylesheet">
    <link href="https://fonts.googleapis.com/css2?family=Noto+Nastaliq+Urdu&display=swap" rel="stylesheet">
    <style>
        :root {
            --primary: #2c3e50;
            --secondary: #e67e22;
            --accent: #3498db;
            --light: #ecf0f1;
            --dark: #2c3e50;
            --gray: #95a5a6;
            --concrete: #f5f5f5;
            --text: #333333;
            --transition: all 0.4s cubic-bezier(0.175, 0.885, 0.32, 1.275);
        }
        
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }
        
        body {
            font-family: 'Roboto', sans-serif;
            color: var(--text);
            line-height: 1.6;
            background-color: var(--concrete);
            position: relative;
            overflow-x: hidden;
        }
        
        .container {
            width: 100%;
            max-width: 1400px;
            margin: 0 auto;
            padding: 0 20px;
        }
        
        /* Header Styles */
        header {
            background-color: rgba(44, 62, 80, 0.95);
            color: white;
            padding: 15px 0;
            position: fixed;
            width: 100%;
            top: 0;
            z-index: 1000;
            box-shadow: 0 2px 30px rgba(0, 0, 0, 0.2);
            transition: var(--transition);
        }
        
        header.scrolled {
            padding: 10px 0;
            background-color: rgba(44, 62, 80, 0.98);
        }
        
        .header-container {
            display: flex;
            justify-content: space-between;
            align-items: center;
        }
        
        .logo {
            display: flex;
            align-items: center;
        }
        
        .logo h1 {
            font-family: 'Montserrat', sans-serif;
            font-size: 28px;
            font-weight: 700;
            background: linear-gradient(45deg, #fff, #e67e22);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
        }
        
        nav ul {
            display: flex;
            list-style: none;
        }
        
        nav ul li {
            margin-left: 30px;
        }
        
        nav ul li a {
            color: white;
            text-decoration: none;
            font-weight: 500;
            transition: var(--transition);
            position: relative;
            padding: 6px 0;
        }
        
        nav ul li a:after {
            content: '';
            position: absolute;
            width: 0;
            height: 2px;
            background: var(--secondary);
            left: 0;
            bottom: 0;
            transition: var(--transition);
        }
        
        nav ul li a:hover {
            color: var(--secondary);
        }
        
        nav ul li a:hover:after {
            width: 100%;
        }
        
        .mobile-menu-btn {
            display: none;
            font-size: 24px;
            background: none;
            border: none;
            color: white;
            cursor: pointer;
            z-index: 1001;
        }
        
        /* Hero Section */
        .hero {
            background: linear-gradient(rgba(0, 0, 0, 0.7), rgba(0, 0, 0, 0.7)), url('https://images.unsplash.com/photo-1503387762-592deb58ef4e?ixlib=rb-4.0.3&auto=format&fit=crop&w=1500&q=80');
            background-size: cover;
            background-position: center;
            background-attachment: fixed;
            height: 100vh;
            display: flex;
            align-items: center;
            text-align: center;
            color: white;
            position: relative;
            overflow: hidden;
        }
        
        .hero::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: linear-gradient(135deg, rgba(230, 126, 34, 0.2) 0%, rgba(44, 62, 80, 0.2) 100%);
            z-index: 1;
        }
        
        .hero-content {
            max-width: 900px;
            margin: 0 auto;
            padding: 20px;
            position: relative;
            z-index: 2;
            opacity: 0;
            transform: translateY(50px);
            animation: fadeInUp 1s forwards 0.5s;
        }
        
        .hero h2 {
            font-family: 'Montserrat', sans-serif;
            font-size: 4rem;
            margin-bottom: 20px;
            text-transform: uppercase;
            letter-spacing: 3px;
            text-shadow: 2px 2px 10px rgba(0, 0, 0, 0.3);
        }
        
        .hero p {
            font-size: 1.3rem;
            margin-bottom: 40px;
            max-width: 700px;
            margin-left: auto;
            margin-right: auto;
        }
        
        .btn {
            display: inline-block;
            padding: 15px 40px;
            background-color: var(--secondary);
            color: white;
            text-decoration: none;
            border-radius: 50px;
            font-weight: 600;
            transition: var(--transition);
            text-transform: uppercase;
            letter-spacing: 1px;
            position: relative;
            overflow: hidden;
            border: 2px solid var(--secondary);
        }
        
        .btn:hover {
            background-color: transparent;
            color: var(--secondary);
            transform: translateY(-5px);
            box-shadow: 0 10px 25px rgba(230, 126, 34, 0.3);
        }
        
        .btn::after {
            content: '';
            position: absolute;
            width: 100%;
            height: 100%;
            background: white;
            top: 0;
            left: -100%;
            transform: skewX(-30deg);
            transition: var(--transition);
            z-index: -1;
        }
        
        .btn:hover::after {
            left: 100%;
        }
        
        /* About Section */
        .section {
            padding: 100px 0;
        }
        
        .section-title {
            text-align: center;
            margin-bottom: 70px;
        }
        
        .section-title h2 {
            font-family: 'Montserrat', sans-serif;
            font-size: 2.8rem;
            color: var(--primary);
            position: relative;
            display: inline-block;
            padding-bottom: 15px;
        }
        
        .section-title h2:after {
            content: '';
            position: absolute;
            width: 50%;
            height: 4px;
            background: linear-gradient(to right, transparent, var(--secondary), transparent);
            bottom: 0;
            left: 25%;
        }
        
        .about-content {
            display: flex;
            flex-wrap: wrap;
            align-items: center;
            gap: 60px;
        }
        
        .about-text {
            flex: 1;
            min-width: 300px;
        }
        
        .about-text h3 {
            font-family: 'Montserrat', sans-serif;
            font-size: 2rem;
            margin-bottom: 25px;
            color: var(--primary);
        }
        
        .urdu-text {
            font-family: 'Noto Nastaliq Urdu', serif;
            direction: rtl;
            margin-top: 30px;
            padding: 20px;
            background: rgba(236, 240, 241, 0.5);
            border-right: 4px solid var(--secondary);
            border-radius: 5px;
        }
        
        .about-images {
            flex: 1;
            display: flex;
            flex-wrap: wrap;
            gap: 30px;
            min-width: 300px;
            perspective: 1000px;
        }
        
        .ceo-card {
            flex: 1;
            min-width: 250px;
            background: white;
            border-radius: 15px;
            overflow: hidden;
            box-shadow: 0 15px 30px rgba(0, 0, 0, 0.1);
            transition: var(--transition);
            transform-style: preserve-3d;
        }
        
        .ceo-card:hover {
            transform: translateY(-15px) rotateX(5deg);
            box-shadow: 0 20px 40px rgba(0, 0, 0, 0.15);
        }
        
        .ceo-img {
            width: 100%;
            height: 300px;
            overflow: hidden;
            position: relative;
        }
        
        .ceo-img img {
            width: 100%;
            height: 100%;
            object-fit: cover;
            transition: var(--transition);
        }
        
        .ceo-card:hover .ceo-img img {
            transform: scale(1.1);
        }
        
        .ceo-info {
            padding: 25px;
            text-align: center;
            background: linear-gradient(to bottom, var(--primary), #1a2530);
            color: white;
        }
        
        .ceo-info h4 {
            font-family: 'Montserrat', sans-serif;
            margin-bottom: 5px;
            font-size: 1.3rem;
        }
        
        .ceo-info p {
            color: var(--secondary);
            font-style: italic;
            font-weight: 500;
        }
        
        /* Tuftiles Section */
        .tuftiles {
            background: linear-gradient(to bottom, #f9f9f9, #ececec);
            position: relative;
            overflow: hidden;
        }
        
        .tuftiles::before {
            content: '';
            position: absolute;
            width: 100%;
            height: 100%;
            top: 0;
            left: 0;
            background-image: url('data:image/svg+xml;utf8,<svg xmlns="http://www.w3.org/2000/svg" width="100" height="100" viewBox="0 0 100 100"><rect fill-opacity="0.02" fill="%232c3e50" width="10" height="10"/></svg>');
            z-index: 0;
        }
        
        .tiles-content {
            display: flex;
            flex-wrap: wrap;
            gap: 50px;
            position: relative;
            z-index: 1;
        }
        
        .tiles-text {
            flex: 1;
            min-width: 300px;
        }
        
        .tiles-text h3 {
            font-family: 'Montserrat', sans-serif;
            font-size: 2rem;
            margin-bottom: 25px;
            color: var(--primary);
        }
        
        .features-grid {
            flex: 1;
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 20px;
            min-width: 300px;
            perspective: 1000px;
        }
        
        .feature-box {
            background: white;
            padding: 25px;
            border-radius: 10px;
            box-shadow: 0 10px 20px rgba(0, 0, 0, 0.05);
            transition: var(--transition);
            text-align: center;
            transform-style: preserve-3d;
        }
        
        .feature-box:hover {
            transform: translateY(-10px) rotateX(5deg);
            box-shadow: 0 15px 30px rgba(0, 0, 0, 0.1);
        }
        
        .feature-box i {
            font-size: 2.5rem;
            color: var(--secondary);
            margin-bottom: 15px;
        }
        
        .feature-box h4 {
            font-family: 'Montserrat', sans-serif;
            margin-bottom: 10px;
            color: var(--primary);
        }
        
        .types-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
            gap: 20px;
            margin-top: 50px;
        }
        
        .type-box {
            background: white;
            padding: 20px;
            border-radius: 10px;
            box-shadow: 0 10px 20px rgba(0, 0, 0, 0.05);
            transition: var(--transition);
            text-align: center;
            opacity: 0;
            transform: translateY(50px);
        }
        
        .type-box.visible {
            opacity: 1;
            transform: translateY(0);
        }
        
        .type-box:hover {
            transform: translateY(-5px);
            box-shadow: 0 15px 30px rgba(0, 0, 0, 0.1);
        }
        
        .type-box h4 {
            font-family: 'Montserrat', sans-serif;
            color: var(--primary);
            margin-top: 15px;
        }
        
        /* Products Section */
        .products {
            background: linear-gradient(to bottom, #f9f9f9, #ececec);
            position: relative;
            overflow: hidden;
        }
        
        .products::before {
            content: '';
            position: absolute;
            width: 100%;
            height: 100%;
            top: 0;
            left: 0;
            background-image: url('data:image/svg+xml;utf8,<svg xmlns="http://www.w3.org/2000/svg" width="100" height="100" viewBox="0 0 100 100"><rect fill-opacity="0.02" fill="%232c3e50" width="10" height="10"/></svg>');
            z-index: 0;
        }
        
        .products-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(350px, 1fr));
            gap: 40px;
            position: relative;
            z-index: 1;
        }
        
        .product-card {
            background: white;
            border-radius: 15px;
            overflow: hidden;
            box-shadow: 0 15px 30px rgba(0, 0, 0, 0.1);
            transition: var(--transition);
            transform: translateY(50px);
            opacity: 0;
        }
        
        .product-card.visible {
            transform: translateY(0);
            opacity: 1;
        }
        
        .product-card:hover {
            transform: translateY(-15px) scale(1.02);
            box-shadow: 0 25px 50px rgba(0, 0, 0, 0.15);
        }
        
        .product-img {
            height: 280px;
            overflow: hidden;
            position: relative;
        }
        
        .product-img img {
            width: 100%;
            height: 100%;
            object-fit: cover;
            transition: var(--transition);
        }
        
        .product-card:hover .product-img img {
            transform: scale(1.15);
        }
        
        .product-info {
            padding: 25px;
            background: white;
            position: relative;
        }
        
        .product-info h3 {
            font-family: 'Montserrat', sans-serif;
            margin-bottom: 15px;
            color: var(--primary);
            font-size: 1.5rem;
        }
        
        .product-info p {
            color: var(--gray);
            margin-bottom: 20px;
        }
        
        .product-link {
            display: inline-flex;
            align-items: center;
            color: var(--secondary);
            text-decoration: none;
            font-weight: 500;
            transition: var(--transition);
            cursor: pointer;
        }
        
        .product-link i {
            margin-left: 8px;
            transition: var(--transition);
        }
        
        .product-link:hover {
            color: var(--primary);
        }
        
        .product-link:hover i {
            transform: translateX(5px);
        }
        
        /* Contact Section */
        .contact-container {
            display: flex;
            flex-wrap: wrap;
            gap: 60px;
        }
        
        .contact-info {
            flex: 1;
            min-width: 300px;
        }
        
        .contact-info h3 {
            font-family: 'Montserrat', sans-serif;
            margin-bottom: 25px;
            color: var(--primary);
            font-size: 1.8rem;
        }
        
        .contact-details {
            margin-bottom: 40px;
        }
        
        .contact-details p {
            margin-bottom: 15px;
            display: flex;
            align-items: center;
            font-size: 1.1rem;
        }
        
        .contact-details i {
            margin-right: 15px;
            color: var(--secondary);
            width: 20px;
            font-size: 1.2rem;
        }
        
        .social-links {
            display: flex;
            gap: 15px;
        }
        
        .social-links a {
            display: inline-flex;
            align-items: center;
            justify-content: center;
            width: 50px;
            height: 50px;
            background: linear-gradient(135deg, var(--primary), #1a2530);
            color: white;
            border-radius: 50%;
            text-decoration: none;
            transition: var(--transition);
            font-size: 1.2rem;
        }
        
        .social-links a:hover {
            background: linear-gradient(135deg, var(--secondary), #e67e22);
            transform: translateY(-5px) rotate(5deg);
            box-shadow: 0 5px 15px rgba(230, 126, 34, 0.3);
        }
        
        .direct-contact {
            flex: 1;
            min-width: 300px;
            background: white;
            padding: 40px;
            border-radius: 15px;
            box-shadow: 0 15px 30px rgba(0, 0, 0, 0.1);
            text-align: center;
        }
        
        .direct-contact h3 {
            font-family: 'Montserrat', sans-serif;
            margin-bottom: 25px;
            color: var(--primary);
            font-size: 1.8rem;
        }
        
        .direct-contact p {
            margin-bottom: 30px;
            color: var(--gray);
        }
        
        .contact-options {
            display: flex;
            flex-direction: column;
            gap: 20px;
        }
        
        .contact-option {
            display: flex;
            align-items: center;
            padding: 20px;
            background: var(--light);
            border-radius: 10px;
            transition: var(--transition);
            text-decoration: none;
            color: var(--primary);
        }
        
        .contact-option:hover {
            background: var(--secondary);
            color: white;
            transform: translateY(-5px);
        }
        
        .contact-option i {
            font-size: 1.5rem;
            margin-right: 15px;
            width: 30px;
        }
        
        .contact-option span {
            font-weight: 500;
        }
        
        /* Footer */
        footer {
            background: linear-gradient(to right, #1a2530, var(--primary));
            color: white;
            padding: 80px 0 20px;
            position: relative;
        }
        
        .footer-content {
            display: flex;
            flex-wrap: wrap;
            gap: 50px;
            margin-bottom: 60px;
        }
        
        .footer-column {
            flex: 1;
            min-width: 250px;
        }
        
        .footer-column h3 {
            font-family: 'Montserrat', sans-serif;
            margin-bottom: 25px;
            position: relative;
            padding-bottom: 15px;
            font-size: 1.4rem;
        }
        
        .footer-column h3:after {
            content: '';
            position: absolute;
            width: 40px;
            height: 3px;
            background-color: var(--secondary);
            bottom: 0;
            left: 0;
        }
        
        .footer-column ul {
            list-style: none;
        }
        
        .footer-column ul li {
            margin-bottom: 12px;
        }
        
        .footer-column ul li a {
            color: #ddd;
            text-decoration: none;
            transition: var(--transition);
            display: inline-block;
        }
        
        .footer-column ul li a:hover {
            color: var(--secondary);
            transform: translateX(5px);
        }
        
        .copyright {
            text-align: center;
            padding-top: 30px;
            border-top: 1px solid rgba(255, 255, 255, 0.1);
            font-size: 0.9rem;
            color: #aaa;
        }
        
        .copyright a {
            color: var(--secondary);
            text-decoration: none;
            font-weight: 600;
        }
        
        /* Cookie Consent */
        .cookie-consent {
            position: fixed;
            bottom: 30px;
            left: 30px;
            right: 30px;
            background: linear-gradient(135deg, var(--primary), #1a2530);
            color: white;
            padding: 25px 30px;
            border-radius: 15px;
            box-shadow: 0 10px 30px rgba(0, 0, 0, 0.3);
            z-index: 1000;
            display: flex;
            flex-wrap: wrap;
            align-items: center;
            justify-content: space-between;
            gap: 20px;
            transform: translateY(150%);
            transition: var(--transition);
        }
        
        .cookie-consent.show {
            transform: translateY(0);
        }
        
        .cookie-text {
            flex: 1;
            min-width: 300px;
        }
        
        .cookie-text h4 {
            margin-bottom: 10px;
            font-family: 'Montserrat', sans-serif;
        }
        
        .cookie-buttons {
            display: flex;
            gap: 15px;
        }
        
        .cookie-btn {
            padding: 12px 25px;
            border: none;
            border-radius: 50px;
            cursor: pointer;
            font-weight: 500;
            transition: var(--transition);
        }
        
        .cookie-accept {
            background-color: var(--secondary);
            color: white;
        }
        
        .cookie-accept:hover {
            background-color: #d35400;
            transform: translateY(-3px);
        }
        
        .cookie-decline {
            background-color: transparent;
            color: white;
            border: 2px solid white;
        }
        
        .cookie-decline:hover {
            background-color: rgba(255, 255, 255, 0.1);
        }
        
        /* Animations */
        @keyframes fadeInUp {
            from {
                opacity: 0;
                transform: translateY(50px);
            }
            to {
                opacity: 1;
                transform: translateY(0);
            }
        }
        
        @keyframes pulse {
            0% {
                transform: scale(1);
            }
            50% {
                transform: scale(1.05);
            }
            to {
                transform: scale(1);
            }
        }
        
        .fade-in {
            animation: fadeInUp 1s ease forwards;
        }
        
        .pulse {
            animation: pulse 2s infinite ease-in-out;
        }
        
        /* Map */
        .map {
            height: 350px;
            margin-top: 40px;
            border-radius: 15px;
            overflow: hidden;
            box-shadow: 0 15px 30px rgba(0, 0, 0, 0.15);
        }
        
        .map iframe {
            width: 100%;
            height: 100%;
            border: none;
        }
        
        /* Responsive Design */
        @media (max-width: 992px) {
            .hero h2 {
                font-size: 3rem;
            }
            
            nav ul li {
                margin-left: 20px;
            }
        }
        
        @media (max-width: 768px) {
            .mobile-menu-btn {
                display: block;
            }
            
            nav {
                position: fixed;
                top: 0;
                left: -100%;
                width: 80%;
                max-width: 300px;
                height: 100vh;
                background-color: var(--primary);
                transition: var(--transition);
                z-index: 999;
                padding: 100px 30px 30px;
                box-shadow: 5px 0 15px rgba(0, 0, 0, 0.2);
            }
            
            nav.active {
                left: 0;
            }
            
            nav ul {
                flex-direction: column;
            }
            
            nav ul li {
                margin: 15px 0;
            }
            
            .hero h2 {
                font-size: 2.5rem;
            }
            
            .hero p {
                font-size: 1.1rem;
            }
            
            .section-title h2 {
                font-size: 2.2rem;
            }
            
            .cookie-consent {
                flex-direction: column;
                text-align: center;
            }
            
            .cookie-buttons {
                width: 100%;
                justify-content: center;
            }
            
            .contact-options {
                flex-direction: column;
            }
        }
        
        /* Particle Background */
        .particles-container {
            position: absolute;
            width: 100%;
            height: 100%;
            top: 0;
            left: 0;
            z-index: 0;
        }
        
        .particle {
            position: absolute;
            background-color: rgba(255, 255, 255, 0.1);
            border-radius: 50%;
        }
        
        /* Loading Screen */
        .loading-screen {
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: var(--primary);
            display: flex;
            align-items: center;
            justify-content: center;
            z-index: 9999;
            transition: opacity 0.5s ease;
        }
        
        .loader {
            width: 60px;
            height: 60px;
            border: 5px solid rgba(255, 255, 255, 0.2);
            border-radius: 50%;
            border-top-color: var(--secondary);
            animation: spin 1s linear infinite;
        }
        
        @keyframes spin {
            100% {
                transform: rotate(360deg);
            }
        }
        
        /* Scroll to Top Button */
        .scroll-to-top {
            position: fixed;
            bottom: 30px;
            right: 30px;
            width: 50px;
            height: 50px;
            background: linear-gradient(135deg, var(--secondary), #e67e22);
            color: white;
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            text-decoration: none;
            box-shadow: 0 5px 15px rgba(230, 126, 34, 0.3);
            transition: var(--transition);
            opacity: 0;
            visibility: hidden;
            z-index: 999;
        }
        
        .scroll-to-top.visible {
            opacity: 1;
            visibility: visible;
        }
        
        .scroll-to-top:hover {
            transform: translateY(-5px) rotate(5deg);
        }
        
        /* Modal */
        .modal {
            display: none;
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background-color: rgba(0, 0, 0, 0.8);
            z-index: 1000;
            overflow-y: auto;
            padding: 20px;
        }
        
        .modal-content {
            background-color: white;
            margin: 5% auto;
            padding: 40px;
            border-radius: 15px;
            max-width: 800px;
            position: relative;
            animation: modalFadeIn 0.5s;
        }
        
        @keyframes modalFadeIn {
            from {
                opacity: 0;
                transform: translateY(-50px);
            }
            to {
                opacity: 1;
                transform: translateY(0);
            }
        }
        
        .close-modal {
            position: absolute;
            top: 20px;
            right: 20px;
            font-size: 28px;
            cursor: pointer;
            color: var(--gray);
            transition: var(--transition);
            z-index: 1001;
        }
        
        .close-modal:hover {
            color: var(--secondary);
            transform: rotate(90deg);
        }
        
        .modal-header {
            margin-bottom: 30px;
        }
        
        .modal-header h3 {
            font-family: 'Montserrat', sans-serif;
            font-size: 2rem;
            color: var(--primary);
            margin-bottom: 10px;
        }
        
        .modal-body {
            display: flex;
            flex-wrap: wrap;
            gap: 30px;
        }
        
        .modal-image {
            flex: 1;
            min-width: 300px;
            border-radius: 10px;
            overflow: hidden;
        }
        
        .modal-image img {
            width: 100%;
            height: auto;
            display: block;
        }
        
        .modal-details {
            flex: 1;
            min-width: 300px;
        }
        
        .modal-details h4 {
            font-family: 'Montserrat', sans-serif;
            margin-bottom: 15px;
            color: var(--primary);
            font-size: 1.5rem;
        }
        
        .modal-features {
            margin-top: 20px;
        }
        
        .modal-features ul {
            list-style-type: none;
        }
        
        .modal-features li {
            margin-bottom: 10px;
            display: flex;
            align-items: center;
        }
        
        .modal-features li i {
            color: var(--secondary);
            margin-right: 10px;
        }
    </style>
</head>
<body>
    <!-- Loading Screen -->
    <div class="loading-screen">
        <div class="loader"></div>
    </div>

    <!-- Header -->
    <header>
        <div class="container header-container">
            <div class="logo">
                <h1>Al Riaz Blocks & Tuftile</h1>
            </div>
            <button class="mobile-menu-btn">
                <i class="fas fa-bars"></i>
            </button>
            <nav>
                <ul>
                    <li><a href="#home">Home</a></li>
                    <li><a href="#about">About</a></li>
                    <li><a href="#tuftiles">Tuftiles</a></li>
                    <li><a href="#products">Products</a></li>
                    <li><a href="#contact">Contact</a></li>
                </ul>
            </nav>
        </div>
    </header>

    <!-- Hero Section -->
    <section class="hero" id="home">
        <div class="particles-container" id="particles"></div>
        <div class="container hero-content">
            <h2>Building The Future With Quality</h2>
            <p>With over 30 years of experience in international construction, we deliver the highest quality concrete blocks and building materials for your projects.</p>
            <a href="#products" class="btn pulse">Explore Our Products</a>
        </div>
    </section>

    <!-- About Section -->
    <section class="section" id="about">
        <div class="container">
            <div class="section-title">
                <h2>About Us</h2>
            </div>
            <div class="about-content">
                <div class="about-text">
                    <h3>30 Years of Excellence</h3>
                    <p>Established in 2019, Al Riaz Blocks and Tuftile brings three decades of international construction expertise to Wazirabad, Pakistan. We specialize in manufacturing high-quality concrete products that meet international standards.</p>
                    <p>Our state-of-the-art factory produces a wide range of construction materials, from boundary walls and curb stones to hollow blocks and sewerage pipes, serving both residential and commercial projects.</p>
                    <p>Under the leadership of our visionary CEO, Ibrahim Sahi, and founded by Sajjad Sahi, we continue to innovate and expand our product line to meet the evolving needs of the construction industry.</p>
                    
                    <div class="urdu-text">
                        <h3>ہمارے بارے میں</h3>
                        <p>الریاز بلاکس اور ٹف ٹائل 2019 میں قائم کیا گیا، جو وازیرآباد، پاکستان میں تعمیرات کے شعبے میں تین دہائیوں کی بین الاقوامی مہارت لے کر آیا ہے۔ ہم بین الاقوامی معیارات پر پورا اترنے والے اعلیٰ معیار کے کنکریٹ مصنوعات کی تیاری میں مہارت رکھتے ہیں۔</p>
                        <p>ہمارا جدید ترین فیکٹری تعمیراتی مواد کی ایک وسیع رینج تیار کرتا ہے، جو رہائشی اور تجارتی دونوں منصوبوں کی خدمت کرتا ہے۔</p>
                    </div>
                </div>
                <div class="about-images">
                    <div class="ceo-card">
                        <div class="ceo-img">
                            <img src="https://i.ibb.co/273ZBP0h/CEO-Ibrahim-Sahi.jpg" alt="Ibrahim Sahi - CEO">
                        </div>
                        <div class="ceo-info">
                            <h4>Ibrahim Sahi</h4>
                            <p>Chief Executive Officer</p>
                        </div>
                    </div>
                    <div class="ceo-card">
                        <div class="ceo-img">
                            <img src="https://i.ibb.co/ZRQwhF1R/Founder-Sajjad-Sahi.jpg" alt="Sajjad Sahi - Founder">
                        </div>
                        <div class="ceo-info">
                            <h4>Sajjad Sahi</h4>
                            <p>Founder</p>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Tuftiles Section -->
    <section class="section tuftiles" id="tuftiles">
        <div class="container">
            <div class="section-title">
                <h2>Tuftiles Redefined</h2>
            </div>
            <div class="tiles-content">
                <div class="tiles-text">
                    <h3>Premium Quality Tuftiles</h3>
                    <p>Using hydraulic presses and strong eccentric vibrating forces, our tuftiles are designed for durability and visual appeal, with a specialized face mix that enhances their aesthetics. With a vast selection of colors, patterns, and shapes, Al Riaz tuftiles are ideal for driveways, walkways, patios, and other applications. Trust us for versatile, high-quality tuftiles that meet all your construction and landscaping needs.</p>
                    <p>Whether you are looking for tuftiles, Al
