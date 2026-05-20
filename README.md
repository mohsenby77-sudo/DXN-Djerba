<!DOCTYPE html>
<html lang="ar" dir="rtl">
<head>
    <meta charset="utf-8">
    <meta http-equiv="Content-Type" content="text/html; charset=utf-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>DXN Djerba - متجر منتجات DXN الصحية في جربة تونس</title>
    <link href="https://fonts.googleapis.com/css2?family=Cairo:wght@300;400;600;700;800;900&display=swap" rel="stylesheet">
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <style>
        :root {
            --primary: #1a7a1a;
            --primary-dark: #0d5a0d;
            --primary-light: #2ecc71;
            --secondary: #f39c12;
            --accent: #e74c3c;
            --dark: #1a1a2e;
            --light: #f8f9fa;
            --gray: #6c757d;
            --white: #ffffff;
            --shadow: 0 10px 40px rgba(0,0,0,0.1);
            --shadow-hover: 0 20px 60px rgba(0,0,0,0.15);
            --gradient: linear-gradient(135deg, var(--primary), var(--primary-light));
            --gradient-gold: linear-gradient(135deg, #f39c12, #e67e22);
        }

        * { margin: 0; padding: 0; box-sizing: border-box; }

        body {
            font-family: 'Cairo', sans-serif;
            background: var(--light);
            color: var(--dark);
            overflow-x: hidden;
        }

        ::-webkit-scrollbar { width: 8px; }
        ::-webkit-scrollbar-track { background: #f1f1f1; }
        ::-webkit-scrollbar-thumb { background: var(--primary); border-radius: 10px; }

        /* TOP BAR */
        .top-bar {
            background: var(--dark);
            color: white;
            padding: 8px 0;
            font-size: 13px;
        }
        .top-bar .container {
            display: flex;
            justify-content: space-between;
            align-items: center;
        }
        .top-bar a {
            color: #ccc;
            text-decoration: none;
            margin: 0 10px;
            transition: 0.3s;
        }
        .top-bar a:hover { color: var(--primary-light); }

        /* HEADER */
        .header {
            background: white;
            box-shadow: 0 2px 20px rgba(0,0,0,0.08);
            position: sticky;
            top: 0;
            z-index: 1000;
            transition: 0.3s;
        }
        .header.scrolled { box-shadow: 0 5px 30px rgba(0,0,0,0.15); }
        .header .container {
            display: flex;
            justify-content: space-between;
            align-items: center;
            padding: 15px 20px;
        }
        .logo {
            display: flex;
            align-items: center;
            gap: 12px;
            text-decoration: none;
        }
        .logo-icon {
            width: 55px;
            height: 55px;
            background: var(--gradient);
            border-radius: 15px;
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 18px;
            color: white;
            font-weight: 900;
            box-shadow: 0 5px 15px rgba(26,122,26,0.3);
        }
        .logo-text h1 { font-size: 24px; font-weight: 900; color: var(--primary); line-height: 1; }
        .logo-text span { font-size: 11px; color: var(--gray); letter-spacing: 2px; }

        .nav-menu { display: flex; list-style: none; gap: 5px; }
        .nav-menu a {
            text-decoration: none;
            color: var(--dark);
            padding: 10px 18px;
            border-radius: 10px;
            font-weight: 600;
            font-size: 15px;
            transition: 0.3s;
        }
        .nav-menu a:hover, .nav-menu a.active {
            background: var(--primary);
            color: white;
        }

        .header-actions { display: flex; align-items: center; gap: 15px; }

        .search-box { position: relative; }
        .search-box input {
            padding: 10px 45px 10px 20px;
            border: 2px solid #e0e0e0;
            border-radius: 25px;
            font-family: 'Cairo';
            font-size: 14px;
            width: 220px;
            transition: 0.3s;
            outline: none;
        }
        .search-box input:focus { border-color: var(--primary); width: 280px; }
        .search-box button {
            position: absolute;
            right: 12px;
            top: 50%;
            transform: translateY(-50%);
            background: none;
            border: none;
            color: var(--gray);
            cursor: pointer;
            font-size: 16px;
        }

        .cart-btn {
            position: relative;
            background: var(--gradient);
            color: white;
            border: none;
            width: 45px;
            height: 45px;
            border-radius: 12px;
            font-size: 20px;
            cursor: pointer;
            transition: 0.3s;
            box-shadow: 0 4px 15px rgba(26,122,26,0.3);
        }
        .cart-btn:hover { transform: translateY(-2px); box-shadow: 0 6px 20px rgba(26,122,26,0.4); }
        .cart-count {
            position: absolute;
            top: -8px;
            left: -8px;
            background: var(--accent);
            color: white;
            width: 22px;
            height: 22px;
            border-radius: 50%;
            font-size: 12px;
            font-weight: 700;
            display: flex;
            align-items: center;
            justify-content: center;
            border: 2px solid white;
        }

        .mobile-toggle {
            display: none;
            background: none;
            border: none;
            font-size: 24px;
            color: var(--dark);
            cursor: pointer;
        }

        .container { max-width: 1280px; margin: 0 auto; padding: 0 20px; }

        /* HERO */
        .hero {
            background: linear-gradient(135deg, #0a3d0a 0%, #1a7a1a 50%, #2ecc71 100%);
            padding: 80px 0;
            position: relative;
            overflow: hidden;
            min-height: 600px;
            display: flex;
            align-items: center;
        }
        .hero::before {
            content: '';
            position: absolute;
            top: -50%;
            right: -20%;
            width: 600px;
            height: 600px;
            background: rgba(255,255,255,0.05);
            border-radius: 50%;
        }
        .hero::after {
            content: '';
            position: absolute;
            bottom: -30%;
            left: -10%;
            width: 400px;
            height: 400px;
            background: rgba(255,255,255,0.03);
            border-radius: 50%;
        }
        .hero .container {
            display: flex;
            align-items: center;
            justify-content: space-between;
            position: relative;
            z-index: 2;
        }
        .hero-content { flex: 1; color: white; }
        .hero-badge {
            display: inline-block;
            background: rgba(255,255,255,0.15);
            backdrop-filter: blur(10px);
            padding: 8px 20px;
            border-radius: 50px;
            font-size: 14px;
            margin-bottom: 20px;
            border: 1px solid rgba(255,255,255,0.2);
        }
        .hero-content h2 {
            font-size: 52px;
            font-weight: 900;
            line-height: 1.2;
            margin-bottom: 20px;
            text-shadow: 0 2px 10px rgba(0,0,0,0.2);
        }
        .hero-content h2 span { color: var(--secondary); }
        .hero-content p {
            font-size: 18px;
            opacity: 0.9;
            margin-bottom: 35px;
            max-width: 500px;
            line-height: 1.8;
        }
        .hero-buttons { display: flex; gap: 15px; flex-wrap: wrap; }

        .btn {
            padding: 14px 35px;
            border: none;
            border-radius: 12px;
            font-family: 'Cairo';
            font-size: 16px;
            font-weight: 700;
            cursor: pointer;
            transition: all 0.3s;
            text-decoration: none;
            display: inline-flex;
            align-items: center;
            gap: 8px;
        }
        .btn-primary {
            background: var(--secondary);
            color: var(--dark);
            box-shadow: 0 5px 20px rgba(243,156,18,0.4);
        }
        .btn-primary:hover { transform: translateY(-3px); box-shadow: 0 8px 30px rgba(243,156,18,0.5); }
        .btn-outline {
            background: transparent;
            color: white;
            border: 2px solid rgba(255,255,255,0.5);
        }
        .btn-outline:hover { background: white; color: var(--primary); border-color: white; }

        .hero-image { flex: 1; display: flex; justify-content: center; position: relative; }
        .hero-product-card {
            background: rgba(255,255,255,0.1);
            backdrop-filter: blur(20px);
            border-radius: 30px;
            padding: 40px;
            border: 1px solid rgba(255,255,255,0.2);
            text-align: center;
            width: 380px;
            color: white;
            animation: float 3s ease-in-out infinite;
        }
        @keyframes float {
            0%, 100% { transform: translateY(0); }
            50% { transform: translateY(-15px); }
        }
        .hero-product-card .product-emoji {
            font-size: 120px;
            display: block;
            margin-bottom: 20px;
            filter: drop-shadow(0 10px 20px rgba(0,0,0,0.2));
        }
        .hero-product-card h3 { font-size: 24px; margin-bottom: 10px; }
        .hero-product-card .price { font-size: 32px; font-weight: 900; color: var(--secondary); }

        .hero-stats { display: flex; gap: 40px; margin-top: 40px; }
        .stat-item { text-align: center; }
        .stat-item .number { font-size: 32px; font-weight: 900; color: var(--secondary); }
        .stat-item .label { font-size: 13px; opacity: 0.8; }

        /* FEATURES BAR */
        .features-bar {
            background: white;
            padding: 30px 0;
            position: relative;
            z-index: 5;
        }
        .features-grid { display: grid; grid-template-columns: repeat(4, 1fr); gap: 30px; }
        .feature-item {
            display: flex;
            align-items: center;
            gap: 15px;
            padding: 20px;
            border-radius: 15px;
            transition: 0.3s;
        }
        .feature-item:hover { background: var(--light); }
        .feature-icon {
            width: 55px;
            height: 55px;
            background: linear-gradient(135deg, rgba(26,122,26,0.1), rgba(46,204,113,0.1));
            border-radius: 15px;
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 24px;
            color: var(--primary);
            flex-shrink: 0;
        }
        .feature-item h4 { font-size: 15px; margin-bottom: 3px; }
        .feature-item p { font-size: 13px; color: var(--gray); }

        /* SECTION HEADERS */
        .section-header { text-align: center; margin-bottom: 50px; }
        .section-header .badge {
            display: inline-block;
            background: linear-gradient(135deg, rgba(26,122,26,0.1), rgba(46,204,113,0.1));
            color: var(--primary);
            padding: 6px 20px;
            border-radius: 50px;
            font-size: 14px;
            font-weight: 700;
            margin-bottom: 15px;
        }
        .section-header h2 { font-size: 38px; font-weight: 900; color: var(--dark); margin-bottom: 15px; }
        .section-header h2 span { color: var(--primary); }
        .section-header p { font-size: 16px; color: var(--gray); max-width: 600px; margin: 0 auto; }

        /* CATEGORIES */
        .categories { padding: 80px 0; }
        .categories-grid { display: grid; grid-template-columns: repeat(6, 1fr); gap: 20px; }
        .category-card {
            background: white;
            border-radius: 20px;
            padding: 30px 15px;
            text-align: center;
            cursor: pointer;
            transition: all 0.3s;
            box-shadow: 0 5px 20px rgba(0,0,0,0.05);
            border: 2px solid transparent;
        }
        .category-card:hover, .category-card.active {
            border-color: var(--primary);
            transform: translateY(-5px);
            box-shadow: 0 15px 40px rgba(26,122,26,0.15);
        }
        .category-card .cat-icon { font-size: 45px; margin-bottom: 15px; display: block; }
        .category-card h4 { font-size: 14px; color: var(--dark); margin-bottom: 5px; }
        .category-card span { font-size: 12px; color: var(--gray); }

        /* PRODUCTS */
        .products { padding: 80px 0; background: linear-gradient(180deg, #f8f9fa, #ffffff); }
        .products-grid { display: grid; grid-template-columns: repeat(4, 1fr); gap: 25px; }
        .product-card {
            background: white;
            border-radius: 20px;
            overflow: hidden;
            box-shadow: 0 5px 20px rgba(0,0,0,0.05);
            transition: all 0.3s;
            position: relative;
        }
        .product-card:hover { transform: translateY(-8px); box-shadow: var(--shadow-hover); }

        .product-badge {
            position: absolute;
            top: 15px;
            right: 15px;
            padding: 5px 12px;
            border-radius: 8px;
            font-size: 12px;
            font-weight: 700;
            z-index: 2;
        }
        .badge-sale { background: var(--accent); color: white; }
        .badge-new { background: var(--primary); color: white; }
        .badge-best { background: var(--secondary); color: var(--dark); }

        .product-wishlist {
            position: absolute;
            top: 15px;
            left: 15px;
            width: 38px;
            height: 38px;
            background: white;
            border: none;
            border-radius: 50%;
            font-size: 16px;
            color: #ccc;
            cursor: pointer;
            transition: 0.3s;
            z-index: 2;
            box-shadow: 0 2px 10px rgba(0,0,0,0.1);
        }
        .product-wishlist:hover, .product-wishlist.active { color: var(--accent); }

        .product-image {
            background: linear-gradient(135deg, #f5f5f5, #e8f5e9);
            height: 220px;
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 100px;
            position: relative;
            overflow: hidden;
        }
        .product-image::after {
            content: '';
            position: absolute;
            bottom: 0;
            left: 0;
            right: 0;
            height: 50%;
            background: linear-gradient(transparent, rgba(255,255,255,0.5));
        }

        .product-actions {
            position: absolute;
            bottom: -50px;
            left: 50%;
            transform: translateX(-50%);
            display: flex;
            gap: 8px;
            transition: 0.3s;
            z-index: 3;
        }
        .product-card:hover .product-actions { bottom: 15px; }
        .product-actions button {
            width: 40px;
            height: 40px;
            border-radius: 10px;
            border: none;
            background: white;
            color: var(--dark);
            font-size: 16px;
            cursor: pointer;
            transition: 0.3s;
            box-shadow: 0 3px 10px rgba(0,0,0,0.15);
        }
        .product-actions button:hover { background: var(--primary); color: white; }

        .product-info { padding: 20px; }
        .product-category { font-size: 12px; color: var(--primary); font-weight: 600; margin-bottom: 5px; }
        .product-info h3 { font-size: 16px; font-weight: 700; margin-bottom: 8px; line-height: 1.4; }
        .product-info .description {
            font-size: 13px;
            color: var(--gray);
            margin-bottom: 12px;
            line-height: 1.6;
            display: -webkit-box;
            -webkit-line-clamp: 2;
            -webkit-box-orient: vertical;
            overflow: hidden;
        }

        .product-rating { display: flex; align-items: center; gap: 5px; margin-bottom: 12px; }
        .stars { color: #ffc107; font-size: 13px; }
        .rating-count { font-size: 12px; color: var(--gray); }

        .product-footer { display: flex; justify-content: space-between; align-items: center; }
        .product-price { display: flex; flex-direction: column; }
        .current-price { font-size: 22px; font-weight: 900; color: var(--primary); }
        .old-price { font-size: 14px; color: #ccc; text-decoration: line-through; }

        .add-cart-btn {
            background: var(--gradient);
            color: white;
            border: none;
            padding: 10px 20px;
            border-radius: 10px;
            font-family: 'Cairo';
            font-weight: 700;
            font-size: 14px;
            cursor: pointer;
            transition: 0.3s;
            display: flex;
            align-items: center;
            gap: 6px;
        }
        .add-cart-btn:hover { transform: scale(1.05); box-shadow: 0 5px 20px rgba(26,122,26,0.3); }

        /* SPECIAL OFFER */
        .special-offer { padding: 80px 0; }
        .offer-card {
            background: var(--gradient);
            border-radius: 30px;
            padding: 60px;
            display: flex;
            align-items: center;
            justify-content: space-between;
            color: white;
            position: relative;
            overflow: hidden;
        }
        .offer-card::before {
            content: '';
            position: absolute;
            top: -100px;
            right: -100px;
            width: 300px;
            height: 300px;
            background: rgba(255,255,255,0.08);
            border-radius: 50%;
        }
        .offer-content { position: relative; z-index: 2; }
        .offer-content .offer-badge {
            display: inline-block;
            background: var(--accent);
            padding: 5px 15px;
            border-radius: 8px;
            font-size: 14px;
            font-weight: 700;
            margin-bottom: 15px;
        }
        .offer-content h2 { font-size: 42px; font-weight: 900; margin-bottom: 15px; }
        .offer-content p { font-size: 16px; opacity: 0.9; margin-bottom: 25px; }

        .countdown { display: flex; gap: 15px; margin-bottom: 25px; }
        .countdown-item {
            background: rgba(255,255,255,0.15);
            backdrop-filter: blur(10px);
            padding: 15px 20px;
            border-radius: 15px;
            text-align: center;
            min-width: 80px;
        }
        .countdown-item .num { font-size: 28px; font-weight: 900; display: block; }
        .countdown-item .label { font-size: 12px; opacity: 0.8; }
        .offer-image { position: relative; z-index: 2; font-size: 150px; animation: float 3s ease-in-out infinite; }

        /* WHY DXN */
        .why-dxn { padding: 80px 0; background: white; }
        .why-grid { display: grid; grid-template-columns: repeat(3, 1fr); gap: 30px; }
        .why-card {
            text-align: center;
            padding: 40px 30px;
            border-radius: 20px;
            transition: 0.3s;
            border: 2px solid #f0f0f0;
        }
        .why-card:hover { border-color: var(--primary); box-shadow: var(--shadow); transform: translateY(-5px); }
        .why-card .icon {
            width: 80px;
            height: 80px;
            background: linear-gradient(135deg, rgba(26,122,26,0.1), rgba(46,204,113,0.1));
            border-radius: 20px;
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 35px;
            margin: 0 auto 20px;
        }
        .why-card h3 { font-size: 20px; margin-bottom: 12px; }
        .why-card p { color: var(--gray); font-size: 14px; line-height: 1.8; }

        /* TESTIMONIALS */
        .testimonials { padding: 80px 0; background: var(--light); }
        .testimonials-grid { display: grid; grid-template-columns: repeat(3, 1fr); gap: 30px; }
        .testimonial-card {
            background: white;
            padding: 35px;
            border-radius: 20px;
            box-shadow: 0 5px 20px rgba(0,0,0,0.05);
            position: relative;
        }
        .testimonial-card .quote-icon {
            position: absolute;
            top: 20px;
            left: 20px;
            font-size: 40px;
            color: rgba(26,122,26,0.1);
        }
        .testimonial-stars { color: #ffc107; margin-bottom: 15px; }
        .testimonial-card p { font-size: 15px; line-height: 1.8; color: var(--gray); margin-bottom: 20px; }
        .testimonial-author { display: flex; align-items: center; gap: 12px; }
        .author-avatar {
            width: 50px;
            height: 50px;
            background: var(--gradient);
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            color: white;
            font-weight: 700;
            font-size: 18px;
        }
        .author-info h4 { font-size: 15px; }
        .author-info span { font-size: 13px; color: var(--gray); }

        /* JOIN SECTION */
        .join-section { padding: 80px 0; background: white; }
        .join-card {
            background: linear-gradient(135deg, #1a1a2e, #16213e);
            border-radius: 30px;
            padding: 60px;
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 60px;
            align-items: center;
            color: white;
        }
        .join-content h2 { font-size: 36px; font-weight: 900; margin-bottom: 15px; }
        .join-content h2 span { color: var(--primary-light); }
        .join-content p { opacity: 0.8; margin-bottom: 25px; line-height: 1.8; }
        .join-benefits { list-style: none; }
        .join-benefits li { display: flex; align-items: center; gap: 10px; padding: 8px 0; font-size: 15px; }
        .join-benefits li i { color: var(--primary-light); font-size: 18px; }

        .join-form {
            background: rgba(255,255,255,0.05);
            backdrop-filter: blur(10px);
            padding: 40px;
            border-radius: 20px;
            border: 1px solid rgba(255,255,255,0.1);
        }
        .join-form h3 { font-size: 22px; margin-bottom: 25px; text-align: center; }
        .form-group { margin-bottom: 18px; }
        .form-group label { display: block; margin-bottom: 6px; font-size: 14px; opacity: 0.9; }
        .form-group input,
        .form-group select {
            width: 100%;
            padding: 12px 18px;
            background: rgba(255,255,255,0.08);
            border: 1px solid rgba(255,255,255,0.15);
            border-radius: 10px;
            color: white;
            font-family: 'Cairo';
            font-size: 14px;
            outline: none;
            transition: 0.3s;
        }
        .form-group input:focus, .form-group select:focus {
            border-color: var(--primary-light);
            background: rgba(255,255,255,0.12);
        }
        .form-group input::placeholder { color: rgba(255,255,255,0.4); }
        .form-group select option { background: #1a1a2e; color: white; }
        .submit-btn {
            width: 100%;
            padding: 14px;
            background: var(--gradient);
            color: white;
            border: none;
            border-radius: 10px;
            font-family: 'Cairo';
            font-size: 16px;
            font-weight: 700;
            cursor: pointer;
            transition: 0.3s;
        }
        .submit-btn:hover { transform: translateY(-2px); box-shadow: 0 10px 30px rgba(26,122,26,0.4); }

        /* NEWSLETTER */
        .newsletter { padding: 60px 0; background: var(--gradient); }
        .newsletter .container { text-align: center; color: white; }
        .newsletter h2 { font-size: 32px; margin-bottom: 10px; }
        .newsletter p { opacity: 0.9; margin-bottom: 25px; }
        .newsletter-form { display: flex; max-width: 500px; margin: 0 auto; gap: 10px; }
        .newsletter-form input {
            flex: 1;
            padding: 14px 20px;
            border: none;
            border-radius: 12px;
            font-family: 'Cairo';
            font-size: 15px;
            outline: none;
        }
        .newsletter-form button {
            padding: 14px 30px;
            background: var(--secondary);
            color: var(--dark);
            border: none;
            border-radius: 12px;
            font-family: 'Cairo';
            font-weight: 700;
            font-size: 15px;
            cursor: pointer;
            transition: 0.3s;
        }
        .newsletter-form button:hover { transform: scale(1.05); }

        /* FOOTER */
        .footer { background: var(--dark); color: white; padding: 60px 0 0; }
        .footer-grid {
            display: grid;
            grid-template-columns: 2fr 1fr 1fr 1fr;
            gap: 40px;
            padding-bottom: 40px;
            border-bottom: 1px solid rgba(255,255,255,0.1);
        }
        .footer-about p { color: #999; font-size: 14px; line-height: 1.8; margin-bottom: 20px; margin-top: 15px; }
        .footer-social { display: flex; gap: 10px; }
        .footer-social a {
            width: 40px;
            height: 40px;
            background: rgba(255,255,255,0.08);
            border-radius: 10px;
            display: flex;
            align-items: center;
            justify-content: center;
            color: #999;
            text-decoration: none;
            transition: 0.3s;
        }
        .footer-social a:hover { background: var(--primary); color: white; }
        .footer h4 { font-size: 18px; margin-bottom: 20px; }
        .footer-links { list-style: none; }
        .footer-links li { margin-bottom: 10px; }
        .footer-links a {
            color: #999;
            text-decoration: none;
            font-size: 14px;
            transition: 0.3s;
            display: flex;
            align-items: center;
            gap: 8px;
        }
        .footer-links a:hover { color: var(--primary-light); padding-right: 5px; }
        .footer-contact { list-style: none; }
        .footer-contact li { display: flex; align-items: center; gap: 12px; margin-bottom: 15px; color: #999; font-size: 14px; }
        .footer-contact li i { color: var(--primary-light); font-size: 18px; }
        .footer-bottom {
            padding: 20px 0;
            display: flex;
            justify-content: space-between;
            align-items: center;
            color: #666;
            font-size: 14px;
        }
        .payment-methods { display: flex; gap: 10px; }
        .payment-methods span {
            background: rgba(255,255,255,0.08);
            padding: 5px 12px;
            border-radius: 6px;
            font-size: 12px;
        }

        /* CART SIDEBAR */
        .cart-overlay {
            position: fixed;
            top: 0; left: 0; right: 0; bottom: 0;
            background: rgba(0,0,0,0.5);
            z-index: 9999;
            opacity: 0;
            visibility: hidden;
            transition: 0.3s;
        }
        .cart-overlay.active { opacity: 1; visibility: visible; }
        .cart-sidebar {
            position: fixed;
            top: 0;
            left: -420px;
            width: 400px;
            height: 100%;
            background: white;
            z-index: 10000;
            transition: 0.4s cubic-bezier(0.16, 1, 0.3, 1);
            display: flex;
            flex-direction: column;
            box-shadow: 10px 0 40px rgba(0,0,0,0.2);
        }
        .cart-sidebar.active { left: 0; }
        .cart-header {
            padding: 20px 25px;
            border-bottom: 1px solid #eee;
            display: flex;
            justify-content: space-between;
            align-items: center;
        }
        .cart-header h3 { font-size: 20px; display: flex; align-items: center; gap: 8px; }
        .cart-close { background: none; border: none; font-size: 24px; cursor: pointer; color: var(--gray); transition: 0.3s; }
        .cart-close:hover { color: var(--accent); }
        .cart-items { flex: 1; overflow-y: auto; padding: 20px; }
        .cart-item {
            display: flex;
            gap: 15px;
            padding: 15px;
            background: var(--light);
            border-radius: 15px;
            margin-bottom: 12px;
            align-items: center;
        }
        .cart-item-image {
            width: 65px;
            height: 65px;
            background: white;
            border-radius: 12px;
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 35px;
        }
        .cart-item-details { flex: 1; }
        .cart-item-details h4 { font-size: 14px; margin-bottom: 5px; }
        .cart-item-details .cart-item-price { color: var(--primary); font-weight: 700; }
        .qty-controls { display: flex; align-items: center; gap: 8px; margin-top: 5px; }
        .qty-controls button {
            width: 28px;
            height: 28px;
            border-radius: 8px;
            border: 1px solid #ddd;
            background: white;
            cursor: pointer;
            font-weight: 700;
            transition: 0.3s;
        }
        .qty-controls button:hover { background: var(--primary); color: white; border-color: var(--primary); }
        .qty-controls span { font-weight: 700; min-width: 25px; text-align: center; }
        .remove-item { background: none; border: none; color: #ccc; font-size: 18px; cursor: pointer; transition: 0.3s; }
        .remove-item:hover { color: var(--accent); }
        .cart-footer { padding: 20px 25px; border-top: 1px solid #eee; }
        .cart-total { display: flex; justify-content: space-between; align-items: center; margin-bottom: 15px; font-size: 18px; font-weight: 700; }
        .cart-total .total-amount { color: var(--primary); font-size: 24px; }
        .checkout-btn {
            width: 100%;
            padding: 14px;
            background: var(--gradient);
            color: white;
            border: none;
            border-radius: 12px;
            font-family: 'Cairo';
            font-size: 16px;
            font-weight: 700;
            cursor: pointer;
            transition: 0.3s;
        }
        .checkout-btn:hover { transform: translateY(-2px); box-shadow: 0 10px 30px rgba(26,122,26,0.3); }
        .empty-cart { text-align: center; padding: 60px 20px; }
        .empty-cart i { font-size: 60px; color: #ddd; margin-bottom: 15px; }
        .empty-cart p { color: var(--gray); font-size: 16px; }

        /* WHATSAPP FLOAT */
        .whatsapp-float { position: fixed; bottom: 25px; left: 25px; z-index: 999; }
        .whatsapp-float a {
            display: flex;
            align-items: center;
            gap: 10px;
            background: #25d366;
            color: white;
            padding: 12px 25px;
            border-radius: 50px;
            text-decoration: none;
            font-weight: 700;
            font-size: 15px;
            box-shadow: 0 5px 25px rgba(37,211,102,0.4);
            transition: 0.3s;
        }
        .whatsapp-float a:hover { transform: translateY(-3px); box-shadow: 0 8px 35px rgba(37,211,102,0.5); }

        /* SCROLL TOP */
        .scroll-top {
            position: fixed;
            bottom: 25px;
            right: 25px;
            width: 50px;
            height: 50px;
            background: var(--gradient);
            color: white;
            border: none;
            border-radius: 15px;
            font-size: 20px;
            cursor: pointer;
            z-index: 999;
            opacity: 0;
            visibility: hidden;
            transition: 0.3s;
            box-shadow: 0 5px 20px rgba(26,122,26,0.3);
        }
        .scroll-top.active { opacity: 1; visibility: visible; }
        .scroll-top:hover { transform: translateY(-3px); }

        /* TOAST */
        .toast {
            position: fixed;
            top: 100px;
            left: 50%;
            transform: translateX(-50%) translateY(-100px);
            background: white;
            padding: 15px 30px;
            border-radius: 12px;
            box-shadow: 0 10px 40px rgba(0,0,0,0.15);
            z-index: 99999;
            display: flex;
            align-items: center;
            gap: 10px;
            font-weight: 600;
            transition: 0.4s cubic-bezier(0.16, 1, 0.3, 1);
            opacity: 0;
        }
        .toast.show { transform: translateX(-50%) translateY(0); opacity: 1; }
        .toast i { color: var(--primary); font-size: 20px; }

        /* ADMIN PANEL */
        .admin-btn {
            position: fixed;
            bottom: 90px;
            right: 25px;
            width: 50px;
            height: 50px;
            background: linear-gradient(135deg, #1a1a2e, #16213e);
            color: white;
            border: none;
            border-radius: 15px;
            font-size: 20px;
            cursor: pointer;
            z-index: 999;
            box-shadow: 0 5px 20px rgba(0,0,0,0.3);
            transition: 0.3s;
        }
        .admin-btn:hover { transform: translateY(-3px); }

        .admin-overlay {
            position: fixed;
            top: 0; left: 0; right: 0; bottom: 0;
            background: rgba(0,0,0,0.7);
            z-index: 99998;
            opacity: 0;
            visibility: hidden;
            transition: 0.3s;
            backdrop-filter: blur(5px);
        }
        .admin-overlay.active { opacity: 1; visibility: visible; }

        .admin-login {
            position: fixed;
            top: 50%;
            left: 50%;
            transform: translate(-50%, -50%) scale(0.9);
            background: white;
            border-radius: 25px;
            padding: 50px 40px;
            z-index: 99999;
            width: 400px;
            box-shadow: 0 30px 80px rgba(0,0,0,0.3);
            opacity: 0;
            visibility: hidden;
            transition: 0.4s cubic-bezier(0.16, 1, 0.3, 1);
            text-align: center;
        }
        .admin-login.active {
            opacity: 1;
            visibility: visible;
            transform: translate(-50%, -50%) scale(1);
        }
        .admin-login .lock-icon {
            width: 80px;
            height: 80px;
            background: linear-gradient(135deg, #1a1a2e, #16213e);
            border-radius: 20px;
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 35px;
            margin: 0 auto 20px;
            color: white;
        }
        .admin-login h3 { font-size: 24px; margin-bottom: 8px; }
        .admin-login p { color: var(--gray); font-size: 14px; margin-bottom: 25px; }
        .admin-login input {
            width: 100%;
            padding: 14px 18px;
            border: 2px solid #e0e0e0;
            border-radius: 12px;
            font-family: 'Cairo';
            font-size: 15px;
            outline: none;
            margin-bottom: 15px;
            text-align: center;
            letter-spacing: 3px;
            transition: 0.3s;
        }
        .admin-login input:focus { border-color: var(--primary); }
        .admin-login .login-btn {
            width: 100%;
            padding: 14px;
            background: var(--gradient);
            color: white;
            border: none;
            border-radius: 12px;
            font-family: 'Cairo';
            font-size: 16px;
            font-weight: 700;
            cursor: pointer;
            transition: 0.3s;
            margin-bottom: 10px;
        }
        .admin-login .login-btn:hover { transform: translateY(-2px); box-shadow: 0 8px 25px rgba(26,122,26,0.3); }
        .admin-login .cancel-btn {
            width: 100%;
            padding: 12px;
            background: #f5f5f5;
            color: var(--gray);
            border: none;
            border-radius: 12px;
            font-family: 'Cairo';
            font-size: 15px;
            cursor: pointer;
            transition: 0.3s;
        }
        .admin-login .cancel-btn:hover { background: #eee; }
        .admin-login .error-msg {
            color: var(--accent);
            font-size: 13px;
            margin-top: 10px;
            display: none;
        }

        /* ADMIN PANEL DASHBOARD */
        .admin-panel {
            position: fixed;
            top: 0;
            right: -100%;
            width: 100%;
            height: 100%;
            background: white;
            z-index: 99997;
            transition: 0.4s cubic-bezier(0.16, 1, 0.3, 1);
            overflow-y: auto;
        }
        .admin-panel.active { right: 0; }

        .admin-panel-header {
            background: linear-gradient(135deg, #1a1a2e, #16213e);
            padding: 20px 30px;
            display: flex;
            justify-content: space-between;
            align-items: center;
            color: white;
            position: sticky;
            top: 0;
            z-index: 10;
        }
        .admin-panel-header h2 { font-size: 22px; display: flex; align-items: center; gap: 10px; }
        .close-admin {
            background: rgba(255,255,255,0.1);
            border: none;
            color: white;
            width: 40px;
            height: 40px;
            border-radius: 10px;
            font-size: 20px;
            cursor: pointer;
            transition: 0.3s;
        }
        .close-admin:hover { background: var(--accent); }

        .admin-content { padding: 30px; }

        .admin-stats {
            display: grid;
            grid-template-columns: repeat(4, 1fr);
            gap: 20px;
            margin-bottom: 35px;
        }
        .admin-stat-card {
            background: linear-gradient(135deg, #f8f9fa, white);
            border-radius: 20px;
            padding: 25px;
            border: 2px solid #f0f0f0;
            text-align: center;
        }
        .admin-stat-card .stat-icon { font-size: 35px; margin-bottom: 10px; }
        .admin-stat-card .stat-number { font-size: 28px; font-weight: 900; color: var(--primary); }
        .admin-stat-card .stat-label { font-size: 13px; color: var(--gray); }

        .admin-section { margin-bottom: 35px; }
        .admin-section h3 {
            font-size: 20px;
            margin-bottom: 20px;
            padding-bottom: 10px;
            border-bottom: 2px solid #f0f0f0;
            display: flex;
            align-items: center;
            gap: 8px;
        }

        .orders-table {
            width: 100%;
            border-collapse: collapse;
            font-size: 14px;
        }
        .orders-table th {
            background: #f8f9fa;
            padding: 12px 15px;
            text-align: right;
            font-weight: 700;
            color: var(--gray);
        }
        .orders-table td { padding: 12px 15px; border-bottom: 1px solid #f0f0f0; }
        .orders-table tr:hover { background: #fafafa; }

        .status-badge {
            padding: 4px 12px;
            border-radius: 8px;
            font-size: 12px;
            font-weight: 700;
        }
        .status-new { background: rgba(26,122,26,0.1); color: var(--primary); }
        .status-pending { background: rgba(243,156,18,0.1); color: var(--secondary); }
        .status-done { background: rgba(108,117,125,0.1); color: var(--gray); }

        .admin-products-grid {
            display: grid;
            grid-template-columns: repeat(4, 1fr);
            gap: 15px;
        }
        .admin-product-item {
            background: #f8f9fa;
            border-radius: 15px;
            padding: 15px;
            display: flex;
            flex-direction: column;
            gap: 8px;
        }
        .admin-product-item .prod-emoji { font-size: 30px; text-align: center; }
        .admin-product-item .prod-name { font-size: 13px; font-weight: 700; text-align: center; }
        .admin-product-item .prod-price { font-size: 15px; font-weight: 900; color: var(--primary); text-align: center; }
        .admin-product-item input {
            width: 100%;
            padding: 6px 10px;
            border: 1px solid #ddd;
            border-radius: 8px;
            font-family: 'Cairo';
            font-size: 13px;
            text-align: center;
            outline: none;
        }
        .admin-product-item .save-price {
            background: var(--gradient);
            color: white;
            border: none;
            padding: 7px;
            border-radius: 8px;
            font-family: 'Cairo';
            font-size: 12px;
            cursor: pointer;
        }

        .settings-grid { display: grid; grid-template-columns: repeat(2, 1fr); gap: 20px; }
        .setting-item label { display: block; font-size: 14px; color: var(--gray); margin-bottom: 6px; }
        .setting-item input {
            width: 100%;
            padding: 10px 15px;
            border: 2px solid #e0e0e0;
            border-radius: 10px;
            font-family: 'Cairo';
            font-size: 14px;
            outline: none;
            transition: 0.3s;
        }
        .setting-item input:focus { border-color: var(--primary); }
        .save-settings {
            background: var(--gradient);
            color: white;
            border: none;
            padding: 12px 30px;
            border-radius: 10px;
            font-family: 'Cairo';
            font-size: 15px;
            font-weight: 700;
            cursor: pointer;
            margin-top: 15px;
            transition: 0.3s;
        }
        .save-settings:hover { transform: translateY(-2px); }

        /* RESPONSIVE */
        @media (max-width: 1024px) {
            .products-grid { grid-template-columns: repeat(3, 1fr); }
            .categories-grid { grid-template-columns: repeat(3, 1fr); }
            .hero-content h2 { font-size: 38px; }
            .footer-grid { grid-template-columns: repeat(2, 1fr); }
            .admin-stats { grid-template-columns: repeat(2, 1fr); }
            .admin-products-grid { grid-template-columns: repeat(3, 1fr); }
        }
        @media (max-width: 768px) {
            .mobile-toggle { display: block; }
            .nav-menu {
                display: none;
                position: absolute;
                top: 100%;
                left: 0; right: 0;
                background: white;
                flex-direction: column;
                padding: 20px;
                box-shadow: 0 10px 30px rgba(0,0,0,0.1);
            }
            .nav-menu.active { display: flex; }
            .search-box { display: none; }
            .hero .container { flex-direction: column; text-align: center; }
            .hero-content h2 { font-size: 32px; }
            .hero-image { margin-top: 40px; }
            .hero-product-card { width: 300px; }
            .hero-stats { justify-content: center; }
            .hero-buttons { justify-content: center; }
            .products-grid { grid-template-columns: repeat(2, 1fr); }
            .categories-grid { grid-template-columns: repeat(3, 1fr); }
            .features-grid { grid-template-columns: repeat(2, 1fr); }
            .offer-card { flex-direction: column; text-align: center; padding: 40px 25px; }
            .why-grid { grid-template-columns: 1fr; }
            .testimonials-grid { grid-template-columns: 1fr; }
            .join-card { grid-template-columns: 1fr; padding: 40px 25px; }
            .footer-grid { grid-template-columns: 1fr; }
            .footer-bottom { flex-direction: column; gap: 10px; text-align: center; }
            .cart-sidebar { width: 100%; left: -100%; }
            .top-bar { display: none; }
            .admin-stats { grid-template-columns: repeat(2, 1fr); }
            .admin-products-grid { grid-template-columns: repeat(2, 1fr); }
            .settings-grid { grid-template-columns: 1fr; }
            .admin-login { width: 90%; }
        }
        @media (max-width: 480px) {
            .products-grid { grid-template-columns: 1fr; }
            .categories-grid { grid-template-columns: repeat(2, 1fr); }
            .features-grid { grid-template-columns: 1fr; }
            .newsletter-form { flex-direction: column; }
            .countdown { flex-wrap: wrap; justify-content: center; }
            .admin-stats { grid-template-columns: repeat(2, 1fr); }
            .admin-products-grid { grid-template-columns: repeat(2, 1fr); }
        }
    </style>
</head>
<body>

<!-- Top Bar -->
<div class="top-bar">
    <div class="container">
        <div>
            <a href="tel:+21622750578"><i class="fas fa-phone"></i> +216 22 750 578</a>
            <a href="mailto:mohsen.by77@yahoo.fr"><i class="fas fa-envelope"></i> mohsen.by77@yahoo.fr</a>
        </div>
        <div>
            <span>تابعنا: </span>
            <a href="#"><i class="fab fa-facebook-f"></i></a>
            <a href="#"><i class="fab fa-instagram"></i></a>
            <a href="#"><i class="fab fa-youtube"></i></a>
            <a href="https://wa.me/21622750578" target="_blank"><i class="fab fa-whatsapp"></i></a>
        </div>
    </div>
</div>

<!-- Header -->
<header class="header" id="header">
    <div class="container">
        <a href="#" class="logo">
            <div class="logo-icon">DXN</div>
            <div class="logo-text">
                <h1>DXN Djerba</h1>
                <span>HEALTHY LIFESTYLE</span>
            </div>
        </a>
        <ul class="nav-menu" id="navMenu">
            <li><a href="#" class="active">الرئيسية</a></li>
            <li><a href="#products">المنتجات</a></li>
            <li><a href="#categories">الأقسام</a></li>
            <li><a href="#about">عن DXN</a></li>
            <li><a href="#join">انضم إلينا</a></li>
            <li><a href="#contact">تواصل معنا</a></li>
        </ul>
        <div class="header-actions">
            <div class="search-box">
                <input type="text" placeholder="ابحث عن منتج..." id="searchInput">
                <button><i class="fas fa-search"></i></button>
            </div>
            <button class="cart-btn" id="cartBtn">
                <i class="fas fa-shopping-cart"></i>
                <span class="cart-count" id="cartCount">0</span>
            </button>
            <button class="mobile-toggle" id="mobileToggle">
                <i class="fas fa-bars"></i>
            </button>
        </div>
    </div>
</header>

<!-- Hero -->
<section class="hero">
    <div class="container">
        <div class="hero-content">
            <div class="hero-badge">🌿 منتجات طبيعية 100% معتمدة عالمياً</div>
            <h2>اكتشف قوة<br><span>الجانوديرما</span><br>مع DXN Djerba</h2>
            <p>منتجات صحية طبيعية من فطر الجانوديرما وسبيرولينا لحياة أكثر صحة وحيوية. متوفرة في جربة تونس مع توصيل لجميع أنحاء تونس.</p>
            <div class="hero-buttons">
                <a href="#products" class="btn btn-primary"><i class="fas fa-shopping-bag"></i> تسوق الآن</a>
                <a href="https://wa.me/21622750578" target="_blank" class="btn btn-outline"><i class="fab fa-whatsapp"></i> تواصل معنا</a>
            </div>
            <div class="hero-stats">
                <div class="stat-item">
                    <div class="number">+500</div>
                    <div class="label">منتج طبيعي</div>
                </div>
                <div class="stat-item">
                    <div class="number">+180</div>
                    <div class="label">دولة حول العالم</div>
                </div>
                <div class="stat-item">
                    <div class="number">جربة</div>
                    <div class="label">تونس 🇹🇳</div>
                </div>
            </div>
        </div>
        <div class="hero-image">
            <div class="hero-product-card">
                <span class="product-emoji">🍄</span>
                <h3>قهوة لينجزي السوداء</h3>
                <p style="opacity:0.8;font-size:14px;margin:10px 0">الأكثر مبيعاً في العالم</p>
                <div class="price">12 د.ت</div>
            </div>
        </div>
    </div>
</section>

<!-- Features Bar -->
<div class="features-bar">
    <div class="container">
        <div class="features-grid">
            <div class="feature-item">
                <div class="feature-icon">🚚</div>
                <div><h4>توصيل سريع</h4><p>لجميع أنحاء تونس</p></div>
            </div>
            <div class="feature-item">
                <div class="feature-icon">✅</div>
                <div><h4>منتجات أصلية</h4><p>مضمونة 100%</p></div>
            </div>
            <div class="feature-item">
                <div class="feature-icon">💳</div>
                <div><h4>دفع آمن</h4><p>نقداً عند الاستلام</p></div>
            </div>
            <div class="feature-item">
                <div class="feature-icon">🎧</div>
                <div><h4>دعم متواصل</h4><p>عبر واتساب 24/7</p></div>
            </div>
        </div>
    </div>
</div>

<!-- Categories -->
<section class="categories" id="categories">
    <div class="container">
        <div class="section-header">
            <div class="badge">🏷️ الأقسام</div>
            <h2>تصفح حسب <span>الفئة</span></h2>
            <p>اختر القسم المناسب لك واكتشف مجموعة متنوعة من المنتجات الصحية</p>
        </div>
        <div class="categories-grid">
            <div class="category-card active" onclick="filterProducts('all', this)">
                <span class="cat-icon">🌟</span>
                <h4>جميع المنتجات</h4>
                <span>+50 منتج</span>
            </div>
            <div class="category-card" onclick="filterProducts('coffee', this)">
                <span class="cat-icon">☕</span>
                <h4>القهوة والمشروبات</h4>
                <span>15 منتج</span>
            </div>
            <div class="category-card" onclick="filterProducts('supplements', this)">
                <span class="cat-icon">💊</span>
                <h4>المكملات الغذائية</h4>
                <span>12 منتج</span>
            </div>
            <div class="category-card" onclick="filterProducts('skincare', this)">
                <span class="cat-icon">🧴</span>
                <h4>العناية بالبشرة</h4>
                <span>10 منتجات</span>
            </div>
            <div class="category-card" onclick="filterProducts('personal', this)">
                <span class="cat-icon">🪥</span>
                <h4>العناية الشخصية</h4>
                <span>8 منتجات</span>
            </div>
            <div class="category-card" onclick="filterProducts('food', this)">
                <span class="cat-icon">🍯</span>
                <h4>المنتجات الغذائية</h4>
                <span>7 منتجات</span>
            </div>
        </div>
    </div>
</section>

<!-- Products -->
<section class="products" id="products">
    <div class="container">
        <div class="section-header">
            <div class="badge">🛍️ منتجاتنا</div>
            <h2>منتجات <span>DXN Djerba</span> المميزة</h2>
            <p>مجموعة مختارة من أفضل المنتجات الصحية الطبيعية متوفرة في جربة تونس</p>
        </div>
        <div class="products-grid" id="productsGrid"></div>
    </div>
</section>

<!-- Special Offer -->
<section class="special-offer">
    <div class="container">
        <div class="offer-card">
            <div class="offer-content">
                <div class="offer-badge">🔥 عرض محدود</div>
                <h2>خصم 30% على<br>باقة الصحة المتكاملة</h2>
                <p>احصل على مجموعة كاملة من منتجات DXN الأساسية بسعر مخفض - جربة تونس</p>
                <div class="countdown">
                    <div class="countdown-item"><span class="num" id="days">07</span><span class="label">يوم</span></div>
                    <div class="countdown-item"><span class="num" id="hours">12</span><span class="label">ساعة</span></div>
                    <div class="countdown-item"><span class="num" id="minutes">45</span><span class="label">دقيقة</span></div>
                    <div class="countdown-item"><span class="num" id="seconds">30</span><span class="label">ثانية</span></div>
                </div>
                <button class="btn btn-primary" onclick="addToCart({id:99,name:'باقة الصحة المتكاملة',price:89,emoji:'🎁',category:'bundle'})">
                    <i class="fas fa-bolt"></i> اطلب الآن
                </button>
            </div>
            <div class="offer-image">🎁</div>
        </div>
    </div>
</section>

<!-- Why DXN -->
<section class="why-dxn" id="about">
    <div class="container">
        <div class="section-header">
            <div class="badge">💚 لماذا DXN</div>
            <h2>لماذا تختار <span>DXN Djerba</span>؟</h2>
            <p>شركة DXN العالمية الرائدة في المنتجات الصحية منذ 1993 - متوفرة الآن في جربة تونس</p>
        </div>
        <div class="why-grid">
            <div class="why-card">
                <div class="icon">🌿</div>
                <h3>طبيعية 100%</h3>
                <p>جميع منتجاتنا مصنوعة من مكونات طبيعية بدون أي مواد كيميائية أو إضافات صناعية</p>
            </div>
            <div class="why-card">
                <div class="icon">🏭</div>
                <h3>مصانع خاصة</h3>
                <p>تمتلك DXN مزارعها ومصانعها الخاصة مما يضمن أعلى معايير الجودة من البذرة إلى المنتج النهائي</p>
            </div>
            <div class="why-card">
                <div class="icon">🌍</div>
                <h3>انتشار عالمي</h3>
                <p>متواجدون في أكثر من 180 دولة حول العالم مع ملايين الأعضاء والعملاء السعداء</p>
            </div>
            <div class="why-card">
                <div class="icon">🏅</div>
                <h3>شهادات دولية</h3>
                <p>حاصلون على شهادات ISO, GMP, TGA وغيرها من الشهادات الدولية المعتمدة</p>
            </div>
            <div class="why-card">
                <div class="icon">🔬</div>
                <h3>أبحاث علمية</h3>
                <p>مدعومة بأبحاث علمية موثقة تثبت فعالية فطر الجانوديرما والسبيرولينا</p>
            </div>
            <div class="why-card">
                <div class="icon">💰</div>
                <h3>فرصة عمل</h3>
                <p>نظام تسويق شبكي يمنحك فرصة لبناء دخل إضافي وتحقيق الاستقلال المالي في تونس</p>
            </div>
        </div>
    </div>
</section>

<!-- Testimonials -->
<section class="testimonials">
    <div class="container">
        <div class="section-header">
            <div class="badge">⭐ آراء العملاء</div>
            <h2>ماذا يقول <span>عملاؤنا</span></h2>
            <p>تجارب حقيقية من عملاء DXN Djerba في تونس</p>
        </div>
        <div class="testimonials-grid">
            <div class="testimonial-card">
                <i class="fas fa-quote-right quote-icon"></i>
                <div class="testimonial-stars">
                    <i class="fas fa-star"></i><i class="fas fa-star"></i>
                    <i class="fas fa-star"></i><i class="fas fa-star"></i><i class="fas fa-star"></i>
                </div>
                <p>منتجات DXN غيرت حياتي! قهوة لينجزي أصبحت جزءاً من روتيني اليومي وأشعر بطاقة ونشاط لم أعرفه من قبل. التوصيل لجربة سريع جداً.</p>
                <div class="testimonial-author">
                    <div class="author-avatar">م</div>
                    <div class="author-info"><h4>محمد العربي</h4><span>جربة، تونس</span></div>
                </div>
            </div>
            <div class="testimonial-card">
                <i class="fas fa-quote-right quote-icon"></i>
                <div class="testimonial-stars">
                    <i class="fas fa-star"></i><i class="fas fa-star"></i>
                    <i class="fas fa-star"></i><i class="fas fa-star"></i><i class="fas fa-star"></i>
                </div>
                <p>منتجات العناية بالبشرة رائعة جداً. أنصح الجميع في تونس بتجربة منتجات DXN الطبيعية. الخدمة ممتازة والأسعار منافسة.</p>
                <div class="testimonial-author">
                    <div class="author-avatar">ف</div>
                    <div class="author-info"><h4>فاطمة الزهراء</h4><span>مدنين، تونس</span></div>
                </div>
            </div>
            <div class="testimonial-card">
                <i class="fas fa-quote-right quote-icon"></i>
                <div class="testimonial-stars">
                    <i class="fas fa-star"></i><i class="fas fa-star"></i>
                    <i class="fas fa-star"></i><i class="fas fa-star"></i><i class="fas fa-star-half-alt"></i>
                </div>
                <p>سبيرولينا DXN ساعدتني كثيراً في تحسين مناعتي. شكراً لمحسن على الخدمة الممتازة والتوصيل السريع لصفاقس.</p>
                <div class="testimonial-author">
                    <div class="author-avatar">ع</div>
                    <div class="author-info"><h4>علي بن سالم</h4><span>صفاقس، تونس</span></div>
                </div>
            </div>
        </div>
    </div>
</section>

<!-- Join Section -->
<section class="join-section" id="join">
    <div class="container">
        <div class="join-card">
            <div class="join-content">
                <h2>انضم لعائلة <span>DXN Djerba</span></h2>
                <p>ابدأ رحلتك في عالم الصحة والأعمال مع DXN في تونس واحصل على خصومات حصرية وفرصة لبناء دخل إضافي</p>
                <ul class="join-benefits">
                    <li><i class="fas fa-check-circle"></i> خصم يصل إلى 25% على جميع المنتجات</li>
                    <li><i class="fas fa-check-circle"></i> فرصة ربح من التسويق الشبكي في تونس</li>
                    <li><i class="fas fa-check-circle"></i> عضوية مدى الحياة بتسجيل واحد</li>
                    <li><i class="fas fa-check-circle"></i> دعم وتدريب مستمر من محسن</li>
                    <li><i class="fas fa-check-circle"></i> مكافآت ورحلات سنوية</li>
                    <li><i class="fas fa-check-circle"></i> عمل من أي مكان في تونس والعالم</li>
                </ul>
            </div>
            <div class="join-form" id="contact">
                <h3>📋 سجل الآن مجاناً</h3>
                <form onsubmit="handleJoinForm(event)">
                    <div class="form-group">
                        <label>الاسم الكامل</label>
                        <input type="text" placeholder="أدخل اسمك الكامل" required>
                    </div>
                    <div class="form-group">
                        <label>رقم الهاتف</label>
                        <input type="tel" placeholder="+216 XX XXX XXX" required>
                    </div>
                    <div class="form-group">
                        <label>البريد الإلكتروني</label>
                        <input type="email" placeholder="example@email.com">
                    </div>
                    <div class="form-group">
                        <label>المدينة</label>
                        <select required>
                            <option value="">اختر مدينتك</option>
                            <option>جربة</option>
                            <option>مدنين</option>
                            <option>تونس العاصمة</option>
                            <option>صفاقس</option>
                            <option>سوسة</option>
                            <option>قابس</option>
                            <option>قفصة</option>
                            <option>بنزرت</option>
                            <option>نابل</option>
                            <option>أخرى</option>
                        </select>
                    </div>
                    <button type="submit" class="submit-btn">
                        <i class="fas fa-paper-plane"></i> أرسل الطلب
                    </button>
                </form>
            </div>
        </div>
    </div>
</section>

<!-- Newsletter -->
<section class="newsletter">
    <div class="container">
        <h2>📬 اشترك في نشرتنا البريدية</h2>
        <p>احصل على أحدث العروض والمنتجات الجديدة من DXN Djerba مباشرة في بريدك</p>
        <form class="newsletter-form" onsubmit="handleNewsletter(event)">
            <input type="email" placeholder="أدخل بريدك الإلكتروني" required>
            <button type="submit">اشترك الآن</button>
        </form>
    </div>
</section>

<!-- Footer -->
<footer class="footer">
    <div class="container">
        <div class="footer-grid">
            <div class="footer-about">
                <a href="#" class="logo">
                    <div class="logo-icon">DXN</div>
                    <div class="logo-text">
                        <h1 style="color:white">DXN Djerba</h1>
                        <span style="color:#999">HEALTHY LIFESTYLE</span>
                    </div>
                </a>
                <p>متجر DXN Djerba - وجهتك الأولى للمنتجات الصحية الطبيعية في جزيرة جربة تونس. نقدم لك أفضل منتجات شركة DXN العالمية مع توصيل لجميع أنحاء تونس.</p>
                <div class="footer-social">
                    <a href="#"><i class="fab fa-facebook-f"></i></a>
                    <a href="#"><i class="fab fa-instagram"></i></a>
                    <a href="#"><i class="fab fa-youtube"></i></a>
                    <a href="https://wa.me/21622750578" target="_blank"><i class="fab fa-whatsapp"></i></a>
                    <a href="mailto:mohsen.by77@yahoo.fr"><i class="fas fa-envelope"></i></a>
                </div>
            </div>
            <div>
                <h4>روابط سريعة</h4>
                <ul class="footer-links">
                    <li><a href="#"><i class="fas fa-chevron-left"></i> الرئيسية</a></li>
                    <li><a href="#products"><i class="fas fa-chevron-left"></i> المنتجات</a></li>
                    <li><a href="#about"><i class="fas fa-chevron-left"></i> عن DXN</a></li>
                    <li><a href="#join"><i class="fas fa-chevron-left"></i> انضم إلينا</a></li>
                    <li><a href="#contact"><i class="fas fa-chevron-left"></i> تواصل معنا</a></li>
                </ul>
            </div>
            <div>
                <h4>الأقسام</h4>
                <ul class="footer-links">
                    <li><a href="#"><i class="fas fa-chevron-left"></i> القهوة والمشروبات</a></li>
                    <li><a href="#"><i class="fas fa-chevron-left"></i> المكملات الغذائية</a></li>
                    <li><a href="#"><i class="fas fa-chevron-left"></i> العناية بالبشرة</a></li>
                    <li><a href="#"><i class="fas fa-chevron-left"></i> العناية الشخصية</a></li>
                    <li><a href="#"><i class="fas fa-chevron-left"></i> المنتجات الغذائية</a></li>
                </ul>
            </div>
            <div>
                <h4>تواصل معنا</h4>
                <ul class="footer-contact">
                    <li><i class="fas fa-map-marker-alt"></i> Guellala, Djerba, Tunisie</li>
                    <li><i class="fas fa-phone"></i>
                        <a href="tel:+21622750578" style="color:#999;text-decoration:none">+216 22 750 578</a>
                    </li>
                    <li><i class="fas fa-envelope"></i>
                        <a href="mailto:mohsen.by77@yahoo.fr" style="color:#999;text-decoration:none">mohsen.by77@yahoo.fr</a>
                    </li>
                    <li><i class="fas fa-clock"></i> الإثنين - السبت: 9:00 - 18:00</li>
                </ul>
            </div>
        </div>
        <div class="footer-bottom">
            <p>© 2025 DXN Djerba. جميع الحقوق محفوظة 🇹🇳</p>
            <div class="payment-methods">
                <span>💵 نقداً</span>
                <span>📱 واتساب</span>
                <span>🏦 تحويل بنكي</span>
            </div>
        </div>
    </div>
</footer>

<!-- Cart Sidebar -->
<div class="cart-overlay" id="cartOverlay"></div>
<div class="cart-sidebar" id="cartSidebar">
    <div class="cart-header">
        <h3><i class="fas fa-shopping-cart"></i> سلة المشتريات</h3>
        <button class="cart-close" id="cartClose"><i class="fas fa-times"></i></button>
    </div>
    <div class="cart-items" id="cartItems"></div>
    <div class="cart-footer" id="cartFooter">
        <div class="cart-total">
            <span>المجموع:</span>
            <span class="total-amount" id="totalAmount">0 د.ت</span>
        </div>
        <button class="checkout-btn" onclick="checkout()">
            <i class="fab fa-whatsapp"></i> إتمام الطلب عبر واتساب
        </button>
    </div>
</div>

<!-- WhatsApp Float -->
<div class="whatsapp-float">
    <a href="https://wa.me/21622750578" target="_blank">
        <i class="fab fa-whatsapp" style="font-size:22px"></i>
        تواصل واتساب
    </a>
</div>

<!-- Scroll Top -->
<button class="scroll-top" id="scrollTop">
    <i class="fas fa-chevron-up"></i>
</button>

<!-- Admin Button -->
<button class="admin-btn" id="adminBtn" title="لوحة التحكم">
    <i class="fas fa-cog"></i>
</button>

<!-- Admin Login Modal -->
<div class="admin-overlay" id="adminOverlay"></div>
<div class="admin-login" id="adminLogin">
    <div class="lock-icon"><i class="fas fa-lock"></i></div>
    <h3>لوحة التحكم</h3>
    <p>أدخل كلمة المرور للدخول</p>
    <input type="password" id="adminPassword" placeholder="● ● ● ● ● ●" maxlength="20">
    <button class="login-btn" onclick="checkAdminPassword()">
        <i class="fas fa-sign-in-alt"></i> دخول
    </button>
    <button class="cancel-btn" onclick="closeAdminLogin()">إلغاء</button>
    <p class="error-msg" id="errorMsg">❌ كلمة المرور غير صحيحة</p>
</div>

<!-- Admin Panel -->
<div class="admin-panel" id="adminPanel">
    <div class="admin-panel-header">
        <h2><i class="fas fa-tachometer-alt"></i> لوحة تحكم DXN Djerba</h2>
        <button class="close-admin" onclick="closeAdminPanel()">
            <i class="fas fa-times"></i>
        </button>
    </div>
    <div class="admin-content">

        <!-- Stats -->
        <div class="admin-stats">
            <div class="admin-stat-card">
                <div class="stat-icon">🛒</div>
                <div class="stat-number" id="adminOrderCount">0</div>
                <div class="stat-label">طلبات اليوم</div>
            </div>
            <div class="admin-stat-card">
                <div class="stat-icon">💰</div>
                <div class="stat-number" id="adminRevenue">0</div>
                <div class="stat-label">إجمالي المبيعات (د.ت)</div>
            </div>
            <div class="admin-stat-card">
                <div class="stat-icon">📦</div>
                <div class="stat-number">12</div>
                <div class="stat-label">عدد المنتجات</div>
            </div>
            <div class="admin-stat-card">
                <div class="stat-icon">👥</div>
                <div class="stat-number" id="adminVisitors">0</div>
                <div class="stat-label">زوار الموقع</div>
            </div>
        </div>

        <!-- Orders -->
        <div class="admin-section">
            <h3>📋 الطلبات الأخيرة</h3>
            <div style="overflow-x:auto">
                <table class="orders-table" id="ordersTable">
                    <thead>
                        <tr>
                            <th>#</th>
                            <th>المنتجات</th>
                            <th>المجموع</th>
                            <th>التاريخ</th>
                            <th>الحالة</th>
                        </tr>
                    </thead>
                    <tbody id="ordersBody">
                        <tr>
                            <td colspan="5" style="text-align:center;color:#999;padding:30px">
                                لا توجد طلبات بعد
                            </td>
                        </tr>
                    </tbody>
                </table>
            </div>
        </div>

        <!-- Products Management -->
        <div class="admin-section">
            <h3>📦 إدارة المنتجات - تعديل الأسعار</h3>
            <div class="admin-products-grid" id="adminProductsGrid"></div>
        </div>

        <!-- Settings -->
        <div class="admin-section">
            <h3>⚙️ إعدادات المتجر</h3>
            <div class="settings-grid">
                <div class="setting-item">
                    <label>اسم المتجر</label>
                    <input type="text" id="settingStoreName" value="DXN Djerba">
                </div>
                <div class="setting-item">
                    <label>رقم الواتساب</label>
                    <input type="text" id="settingWhatsapp" value="+21622750578">
                </div>
                <div class="setting-item">
                    <label>البريد الإلكتروني</label>
                    <input type="text" id="settingEmail" value="mohsen.by77@yahoo.fr">
                </div>
                <div class="setting-item">
                    <label>العنوان</label>
                    <input type="text" id="settingAddress" value="Guellala, Djerba, Tunisie">
                </div>
                <div class="setting-item">
                    <label>تغيير كلمة المرور</label>
                    <input type="password" id="settingNewPassword" placeholder="أدخل كلمة المرور الجديدة">
                </div>
                <div class="setting-item">
                    <label>العملة</label>
                    <input type="text" id="settingCurrency" value="د.ت">
                </div>
            </div>
            <button class="save-settings" onclick="saveSettings()">
                <i class="fas fa-save"></i> حفظ الإعدادات
            </button>
        </div>

    </div>
</div>

<!-- Toast -->
<div class="toast" id="toast">
    <i class="fas fa-check-circle"></i>
    <span id="toastMessage">تم إضافة المنتج للسلة</span>
</div>

<script>
// ===== PRODUCTS DATA =====
let products = [
    { id:1, name:"قهوة لينجزي السوداء", description:"قهوة سوداء ممزوجة بخلاصة فطر الجانوديرما، منشطة وصحية", price:12, oldPrice:15, category:"coffee", emoji:"☕", badge:"best", badgeText:"الأكثر مبيعاً", rating:5, reviews:328 },
    { id:2, name:"قهوة لينجزي 3 في 1", description:"قهوة لينجزي بالكريمة والسكر مع خلاصة الجانوديرما", price:14, oldPrice:null, category:"coffee", emoji:"☕", badge:"new", badgeText:"جديد", rating:4.5, reviews:215 },
    { id:3, name:"كبسولات ريشي جانو RG", description:"كبسولات فطر الجانوديرما لتعزيز المناعة وتحسين الصحة العامة", price:35, oldPrice:42, category:"supplements", emoji:"💊", badge:"sale", badgeText:"خصم 20%", rating:5, reviews:189 },
    { id:4, name:"سبيرولينا DXN", description:"أقراص السبيرولينا الغنية بالفيتامينات والمعادن الطبيعية", price:25, oldPrice:null, category:"supplements", emoji:"🌿", badge:"best", badgeText:"الأكثر مبيعاً", rating:4.5, reviews:276 },
    { id:5, name:"معجون أسنان الجانوديرما", description:"معجون أسنان طبيعي بخلاصة الجانوديرما بدون فلورايد", price:8, oldPrice:10, category:"personal", emoji:"🪥", badge:"sale", badgeText:"خصم 20%", rating:4, reviews:412 },
    { id:6, name:"كريم الجانوديرما للوجه", description:"كريم مرطب ومغذي للبشرة بخلاصة فطر الجانوديرما الطبيعي", price:18, oldPrice:null, category:"skincare", emoji:"🧴", badge:"new", badgeText:"جديد", rating:4.5, reviews:98 },
    { id:7, name:"عسل الجانوديرما", description:"عسل طبيعي ممزوج بخلاصة فطر الجانوديرما الأحمر", price:22, oldPrice:28, category:"food", emoji:"🍯", badge:"sale", badgeText:"خصم 21%", rating:5, reviews:156 },
    { id:8, name:"شاي لينجزي الأسود", description:"شاي أسود فاخر مع خلاصة الجانوديرما لمذاق رائع وفوائد صحية", price:10, oldPrice:null, category:"coffee", emoji:"🍵", badge:null, badgeText:null, rating:4, reviews:143 },
    { id:9, name:"كبسولات GL جانوسيليوم", description:"كبسولات ميسيليوم الجانوديرما لدعم الجهاز الهضمي والمناعة", price:30, oldPrice:null, category:"supplements", emoji:"💊", badge:null, badgeText:null, rating:4.5, reviews:167 },
    { id:10, name:"شامبو الجانوديرما", description:"شامبو طبيعي للشعر بخلاصة الجانوديرما يقوي الشعر ويمنع التساقط", price:12, oldPrice:15, category:"personal", emoji:"🧴", badge:"sale", badgeText:"خصم 20%", rating:4, reviews:201 },
    { id:11, name:"كوكوزي - مشروب الكاكاو", description:"مشروب الكاكاو الصحي بخلاصة الجانوديرما مناسب للأطفال والكبار", price:16, oldPrice:null, category:"coffee", emoji:"🍫", badge:"new", badgeText:"جديد", rating:4.5, reviews:134 },
    { id:12, name:"صابون الجانوديرما", description:"صابون طبيعي بخلاصة الجانوديرما للعناية بالبشرة وترطيبها", price:6, oldPrice:null, category:"skincare", emoji:"🧼", badge:null, badgeText:null, rating:4, reviews:256 }
];

// ===== CART =====
let cart = JSON.parse(localStorage.getItem('dxnDjerbaCart')) || [];

// ===== ORDERS =====
let orders = JSON.parse(localStorage.getItem('dxnDjerbaOrders')) || [];

// ===== ADMIN PASSWORD =====
let adminPassword = localStorage.getItem('dxnAdminPassword') || 'dxn2025';

// ===== VISITORS =====
let visitors = parseInt(localStorage.getItem('dxnVisitors') || '0');
visitors++;
localStorage.setItem('dxnVisitors', visitors);

// ===== RENDER PRODUCTS =====
function renderProducts(filter = 'all') {
    const grid = document.getElementById('productsGrid');
    if(!grid) return;
    const filtered = filter === 'all' ? products : products.filter(p => p.category === filter);
    grid.innerHTML = filtered.map(product => buildProductCard(product)).join('');
}

function buildProductCard(product) {
    const starsHtml = getStarsHtml(product.rating);
    return `
        <div class="product-card" data-id="${product.id}">
            ${product.badge ? `<span class="product-badge badge-${product.badge}">${product.badgeText}</span>` : ''}
            <button class="product-wishlist" onclick="toggleWishlist(this)">
                <i class="far fa-heart"></i>
            </button>
            <div class="product-image">
                ${product.emoji}
                <div class="product-actions">
                    <button onclick='addToCart(${JSON.stringify(product)})' title="إضافة للسلة">
                        <i class="fas fa-cart-plus"></i>
                    </button>
                    <button onclick='orderViaWhatsapp(${JSON.stringify(product)})' title="اطلب عبر واتساب">
                        <i class="fab fa-whatsapp"></i>
                    </button>
                </div>
            </div>
            <div class="product-info">
                <div class="product-category">${getCategoryName(product.category)}</div>
                <h3>${product.name}</h3>
                <p class="description">${product.description}</p>
                <div class="product-rating">
                    <div class="stars">${starsHtml}</div>
                    <span class="rating-count">(${product.reviews})</span>
                </div>
                <div class="product-footer">
                    <div class="product-price">
                        <span class="current-price">${product.price} د.ت</span>
                        ${product.oldPrice ? `<span class="old-price">${product.oldPrice} د.ت</span>` : ''}
                    </div>
                    <button class="add-cart-btn" onclick='addToCart(${JSON.stringify(product)})'>
                        <i class="fas fa-plus"></i> أضف
                    </button>
                </div>
            </div>
        </div>
    `;
}

function getStarsHtml(rating) {
    let html = '';
    for(let i = 1; i <= 5; i++) {
        if(i <= Math.floor(rating)) html += '<i class="fas fa-star"></i>';
        else if(i - 0.5 <= rating) html += '<i class="fas fa-star-half-alt"></i>';
        else html += '<i class="far fa-star"></i>';
    }
    return html;
}

function getCategoryName(cat) {
    const names = { coffee:'القهوة والمشروبات', supplements:'المكملات الغذائية', skincare:'العناية بالبشرة', personal:'العناية الشخصية', food:'المنتجات الغذائية' };
    return names[cat] || cat;
}

// ===== FILTER =====
function filterProducts(category, el) {
    document.querySelectorAll('.category-card').forEach(c => c.classList.remove('active'));
    el.classList.add('active');
    renderProducts(category);
}

// ===== CART FUNCTIONS =====
function addToCart(product) {
    const existing = cart.find(i => i.id === product.id);
    if(existing) existing.qty++;
    else cart.push({ ...product, qty: 1 });
    saveCart();
    updateCartUI();
    showToast(`✅ تم إضافة "${product.name}" إلى السلة`);
}

function removeFromCart(id) {
    cart = cart.filter(i => i.id !== id);
    saveCart();
    updateCartUI();
}

function updateQty(id, change) {
    const item = cart.find(i => i.id === id);
    if(item) {
        item.qty += change;
        if(item.qty <= 0) { removeFromCart(id); return; }
    }
    saveCart();
    updateCartUI();
}

function saveCart() {
    localStorage.setItem('dxnDjerbaCart', JSON.stringify(cart));
}

function updateCartUI() {
    const totalQty = cart.reduce((s, i) => s + i.qty, 0);
    const totalPrice = cart.reduce((s, i) => s + (i.price * i.qty), 0);
    const countEl = document.getElementById('cartCount');
    if(countEl) countEl.textContent = totalQty;

    const cartFooter = document.getElementById('cartFooter');
    const cartItems = document.getElementById('cartItems');
    if(!cartItems) return;

    if(cart.length === 0) {
        cartItems.innerHTML = `<div class="empty-cart"><i class="fas fa-shopping-cart"></i><p>سلة المشتريات فارغة</p></div>`;
        if(cartFooter) cartFooter.style.display = 'none';
    } else {
        if(cartFooter) cartFooter.style.display = 'block';
        cartItems.innerHTML = cart.map(item => `
            <div class="cart-item">
                <div class="cart-item-image">${item.emoji}</div>
                <div class="cart-item-details">
                    <h4>${item.name}</h4>
                    <span class="cart-item-price">${item.price} د.ت</span>
                    <div class="qty-controls">
                        <button onclick="updateQty(${item.id},-1)">-</button>
                        <span>${item.qty}</span>
                        <button onclick="updateQty(${item.id},1)">+</button>
                    </div>
                </div>
                <button class="remove-item" onclick="removeFromCart(${item.id})">
                    <i class="fas fa-trash-alt"></i>
                </button>
            </div>
        `).join('');
        const totalEl = document.getElementById('totalAmount');
        if(totalEl) totalEl.textContent = totalPrice + ' د.ت';
    }
}

// ===== ORDER VIA WHATSAPP =====
function orderViaWhatsapp(product) {
    const msg = `🛒 طلب جديد - DXN Djerba\n\n📦 المنتج: ${product.name}\n💰 السعر: ${product.price} د.ت\n\nمن فضلك أريد طلب هذا المنتج`;
    window.open(`https://wa.me/21622750578?text=${encodeURIComponent(msg)}`, '_blank');
}

// ===== CHECKOUT =====
function checkout() {
    if(cart.length === 0) { showToast('❌ السلة فارغة'); return; }
    const total = cart.reduce((s, i) => s + (i.price * i.qty), 0);
    const itemsList = cart.map(i => `▪ ${i.name} × ${i.qty} = ${i.price * i.qty} د.ت`).join('\n');
    const msg = `🛒 طلب جديد من DXN Djerba\n\n${itemsList}\n\n💰 المجموع الكلي: ${total} د.ت\n\n📍 يرجى إرسال عنوان التوصيل`;

    // Save order
    const order = {
        id: orders.length + 1,
        items: cart.map(i => `${i.name}×${i.qty}`).join(', '),
        total: total,
        date: new Date().toLocaleDateString('ar-TN'),
        status: 'new'
    };
    orders.push(order);
    localStorage.setItem('dxnDjerbaOrders', JSON.stringify(orders));

    window.open(`https://wa.me/21622750578?text=${encodeURIComponent(msg)}`, '_blank');
    cart = [];
    saveCart();
    updateCartUI();
    closeCart();
    showToast('✅ تم إرسال طلبك عبر واتساب!');
}

// ===== CART TOGGLE =====
const cartBtn = document.getElementById('cartBtn');
const cartSidebar = document.getElementById('cartSidebar');
const cartOverlay = document.getElementById('cartOverlay');
const cartClose = document.getElementById('cartClose');

if(cartBtn) {
    cartBtn.onclick = () => {
        if(cartSidebar) cartSidebar.classList.add('active');
        if(cartOverlay) cartOverlay.classList.add('active');
        document.body.style.overflow = 'hidden';
    };
}

function closeCart() {
    if(cartSidebar) cartSidebar.classList.remove('active');
    if(cartOverlay) cartOverlay.classList.remove('active');
    document.body.style.overflow = '';
}

if(cartClose) cartClose.onclick = closeCart;
if(cartOverlay) cartOverlay.onclick = closeCart;

// ===== WISHLIST =====
function toggleWishlist(btn) {
    btn.classList.toggle('active');
    const icon = btn.querySelector('i');
    if(btn.classList.contains('active')) {
        icon.classList.replace('far', 'fas');
        showToast('❤️ تم إضافة المنتج إلى المفضلة');
    } else {
        icon.classList.replace('fas', 'far');
    }
}

// ===== TOAST =====
function showToast(message) {
    const toast = document.getElementById('toast');
    if(!toast) return;
    const msgEl = document.getElementById('toastMessage');
    if(msgEl) msgEl.textContent = message;
    toast.classList.add('show');
    setTimeout(() => toast.classList.remove('show'), 3000);
}

// ===== MOBILE MENU =====
const mobileToggle = document.getElementById('mobileToggle');
if(mobileToggle) {
    mobileToggle.onclick = () => {
        const navMenu = document.getElementById('navMenu');
        if(navMenu) navMenu.classList.toggle('active');
    };
}

// ===== SCROLL =====
const scrollTopBtn = document.getElementById('scrollTop');
window.onscroll = () => {
    const header = document.getElementById('header');
    if(header) header.classList.toggle('scrolled', window.scrollY > 100);
    if(scrollTopBtn) scrollTopBtn.classList.toggle('active', window.scrollY > 100);
};
if(scrollTopBtn) scrollTopBtn.onclick = () => window.scrollTo({ top: 0, behavior: 'smooth' });

// ===== COUNTDOWN =====
function startCountdown() {
    const end = new Date();
    end.setDate(end.getDate() + 7);
    setInterval(() => {
        const diff = end - new Date();
        const daysEl = document.getElementById('days');
        const hoursEl = document.getElementById('hours');
        const minsEl = document.getElementById('minutes');
        const secsEl = document.getElementById('seconds');
        
        if(daysEl) daysEl.textContent = String(Math.floor(diff / 86400000)).padStart(2,'0');
        if(hoursEl) hoursEl.textContent = String(Math.floor((diff % 86400000) / 3600000)).padStart(2,'0');
        if(minsEl) minsEl.textContent = String(Math.floor((diff % 3600000) / 60000)).padStart(2,'0');
        if(secsEl) secsEl.textContent = String(Math.floor((diff % 60000) / 1000)).padStart(2,'0');
    }, 1000);
}

// ===== FORMS =====
function handleJoinForm(e) {
    e.preventDefault();
    const formData = e.target;
    const name = formData.querySelector('input[type="text"]').value;
    const phone = formData.querySelector('input[type="tel"]').value;
    const city = formData.querySelector('select').value;
    const msg = `📋 طلب انضمام جديد - DXN Djerba\n\n👤 الاسم: ${name}\n📱 الهاتف: ${phone}\n🏙️ المدينة: ${city}\n\nأريد الانضمام لعائلة DXN`;
    window.open(`https://wa.me/21622750578?text=${encodeURIComponent(msg)}`, '_blank');
    showToast('✅ تم إرسال طلب التسجيل عبر واتساب!');
    e.target.reset();
}

function handleNewsletter(e) {
    e.preventDefault();
    showToast('✅ تم الاشتراك في النشرة البريدية بنجاح!');
    e.target.reset();
}

// ===== SEARCH =====
const searchInput = document.getElementById('searchInput');
if(searchInput) {
    searchInput.oninput = function() {
        const q = this.value.trim().toLowerCase();
        const grid = document.getElementById('productsGrid');
        if(!grid) return;
        if(q.length > 1) {
            const filtered = products.filter(p => p.name.includes(q) || p.description.includes(q));
            grid.innerHTML = filtered.length
                ? filtered.map(p => buildProductCard(p)).join('')
                : '<div style="grid-column:1/-1;text-align:center;padding:50px;color:#999">لم يتم العثور على منتجات</div>';
        } else {
            renderProducts();
        }
    };
}

// ===== SMOOTH SCROLL =====
document.querySelectorAll('a[href^="#"]').forEach(a => {
    a.addEventListener('click', function(e) {
        const target = document.querySelector(this.getAttribute('href'));
        if(target) {
            e.preventDefault();
            target.scrollIntoView({ behavior: 'smooth' });
            const navMenu = document.getElementById('navMenu');
            if(navMenu) navMenu.classList.remove('active');
        }
    });
});

// ===== ADMIN LOGIN =====
const adminBtn = document.getElementById('adminBtn');
if(adminBtn) {
    adminBtn.onclick = () => {
        const loginEl = document.getElementById('adminLogin');
        const overlayEl = document.getElementById('adminOverlay');
        const passEl = document.getElementById('adminPassword');
        if(loginEl) loginEl.classList.add('active');
        if(overlayEl) overlayEl.classList.add('active');
        if(passEl) passEl.focus();
    };
}

const adminPassInput = document.getElementById('adminPassword');
if(adminPassInput) {
    adminPassInput.onkeypress = function(e) {
        if(e.key === 'Enter') checkAdminPassword();
    };
}

function checkAdminPassword() {
    const passInput = document.getElementById('adminPassword');
    if(!passInput) return;
    const input = passInput.value;
    const errorMsg = document.getElementById('errorMsg');
    if(input === adminPassword) {
        closeAdminLogin();
        openAdminPanel();
    } else {
        if(errorMsg) errorMsg.style.display = 'block';
        passInput.value = '';
        passInput.style.borderColor = '#e74c3c';
        setTimeout(() => {
            if(errorMsg) errorMsg.style.display = 'none';
            passInput.style.borderColor = '';
        }, 3000);
    }
}

function closeAdminLogin() {
    const loginEl = document.getElementById('adminLogin');
    const overlayEl = document.getElementById('adminOverlay');
    const passEl = document.getElementById('adminPassword');
    const errorMsg = document.getElementById('errorMsg');
    if(loginEl) loginEl.classList.remove('active');
    if(overlayEl) overlayEl.classList.remove('active');
    if(passEl) passEl.value = '';
    if(errorMsg) errorMsg.style.display = 'none';
}

const adminOverlay = document.getElementById('adminOverlay');
if(adminOverlay) adminOverlay.onclick = closeAdminLogin;

// ===== ADMIN PANEL =====
function openAdminPanel() {
    const panel = document.getElementById('adminPanel');
    if(panel) panel.classList.add('active');
    document.body.style.overflow = 'hidden';
    loadAdminData();
}

function closeAdminPanel() {
    const panel = document.getElementById('adminPanel');
    if(panel) panel.classList.remove('active');
    document.body.style.overflow = '';
}

function loadAdminData() {
    const countEl = document.getElementById('adminOrderCount');
    const revEl = document.getElementById('adminRevenue');
    const visEl = document.getElementById('adminVisitors');
    
    if(countEl) countEl.textContent = orders.length;
    const totalRevenue = orders.reduce((s, o) => s + o.total, 0);
    if(revEl) revEl.textContent = totalRevenue + ' د.ت';
    if(visEl) visEl.textContent = visitors;

    // Orders Table
    const tbody = document.getElementById('ordersBody');
    if(tbody) {
        if(orders.length === 0) {
            tbody.innerHTML = `<tr><td colspan="5" style="text-align:center;color:#999;padding:30px">لا توجد طلبات بعد</td></tr>`;
        } else {
            tbody.innerHTML = orders.slice().reverse().map(o => `
                <tr>
                    <td>#${o.id}</td>
                    <td style="max-width:200px">${o.items}</td>
                    <td><strong>${o.total} د.ت</strong></td>
                    <td>${o.date}</td>
                    <td><span class="status-badge status-${o.status}">
                        ${o.status === 'new' ? '🆕 جديد' : o.status === 'pending' ? '⏳ قيد التنفيذ' : '✅ مكتمل'}
                    </span></td>
                </tr>
            `).join('');
        }
    }

    // Products Grid
    const adminProdGrid = document.getElementById('adminProductsGrid');
    if(adminProdGrid) {
        adminProdGrid.innerHTML = products.map(p => `
            <div class="admin-product-item">
                <div class="prod-emoji">${p.emoji}</div>
                <div class="prod-name">${p.name}</div>
                <div class="prod-price">${p.price} د.ت</div>
                <input type="number" id="price_${p.id}" value="${p.price}" placeholder="السعر الجديد">
                <button class="save-price" onclick="updatePrice(${p.id})">
                    <i class="fas fa-save"></i> حفظ
                </button>
            </div>
        `).join('');
    }
}

function updatePrice(id) {
    const priceInput = document.getElementById(`price_${id}`);
    if(!priceInput) return;
    const newPrice = parseFloat(priceInput.value);
    if(isNaN(newPrice) || newPrice <= 0) { showToast('❌ أدخل سعراً صحيحاً'); return; }
    const product = products.find(p => p.id === id);
    if(product) {
        product.price = newPrice;
        renderProducts();
        loadAdminData();
        showToast(`✅ تم تحديث سعر "${product.name}" إلى ${newPrice} د.ت`);
    }
}

function saveSettings() {
    const newPassInput = document.getElementById('settingNewPassword');
    if(newPassInput) {
        const newPassword = newPassInput.value;
        if(newPassword.length >= 4) {
            adminPassword = newPassword;
            localStorage.setItem('dxnAdminPassword', newPassword);
            newPassInput.value = '';
        }
    }
    showToast('✅ تم حفظ الإعدادات بنجاح!');
}

// ===== INIT =====
renderProducts();
updateCartUI();
startCountdown();
</script>
</body>
</html>
