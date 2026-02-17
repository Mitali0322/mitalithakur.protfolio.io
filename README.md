<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Mitali Thakur - Digital Marketing & Social Media Strategy</title>
    <link href="https://fonts.googleapis.com/css2?family=DM+Serif+Display:ital@0;1&family=Newsreader:ital,opsz,wght@0,6..72,300;0,6..72,400;0,6..72,600;1,6..72,300&display=swap" rel="stylesheet">
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        :root {
            --deep-blue: #0A2463;
            --royal-blue: #3E5C76;
            --soft-cream: #F8F6F4;
            --warm-white: #FEFEFE;
            --accent-gold: #C5A572;
            --text-dark: #1A1A1A;
            --text-soft: #5A5A5A;
        }

        html {
            scroll-behavior: smooth;
        }

        body {
            font-family: 'Newsreader', serif;
            background-color: var(--soft-cream);
            color: var(--text-dark);
            line-height: 1.7;
            overflow-x: hidden;
        }

        /* Typography */
        h1, h2, h3 {
            font-family: 'DM Serif Display', serif;
            font-weight: 400;
            letter-spacing: -0.02em;
        }

        h1 {
            font-size: clamp(2.5rem, 6vw, 5rem);
            line-height: 1.1;
            margin-bottom: 1.5rem;
        }

        h2 {
            font-size: clamp(2rem, 4vw, 3.5rem);
            line-height: 1.2;
            margin-bottom: 1rem;
        }

        h3 {
            font-size: clamp(1.5rem, 2.5vw, 2rem);
            line-height: 1.3;
        }

        /* Container */
        .container {
            max-width: 1400px;
            margin: 0 auto;
            padding: 0 2rem;
        }

        .narrow-container {
            max-width: 900px;
            margin: 0 auto;
            padding: 0 2rem;
        }

        /* Navigation */
        nav {
            position: fixed;
            top: 0;
            width: 100%;
            background: rgba(248, 246, 244, 0.95);
            backdrop-filter: blur(10px);
            z-index: 1000;
            padding: 1.5rem 0;
            border-bottom: 1px solid rgba(10, 36, 99, 0.1);
            opacity: 0;
            animation: slideDown 0.8s ease forwards;
        }

        @keyframes slideDown {
            to {
                opacity: 1;
            }
        }

        nav .container {
            display: flex;
            justify-content: space-between;
            align-items: center;
        }

        .logo {
            font-family: 'DM Serif Display', serif;
            font-size: 1.5rem;
            color: var(--deep-blue);
            text-decoration: none;
            letter-spacing: -0.02em;
        }

        .nav-links {
            display: flex;
            gap: 2.5rem;
            list-style: none;
        }

        .nav-links a {
            color: var(--text-dark);
            text-decoration: none;
            font-size: 0.95rem;
            position: relative;
            transition: color 0.3s ease;
        }

        .nav-links a::after {
            content: '';
            position: absolute;
            bottom: -4px;
            left: 0;
            width: 0;
            height: 1px;
            background: var(--deep-blue);
            transition: width 0.3s ease;
        }

        .nav-links a:hover {
            color: var(--deep-blue);
        }

        .nav-links a:hover::after {
            width: 100%;
        }

        /* Hero Section */
        .hero {
            min-height: 100vh;
            display: flex;
            align-items: center;
            padding: 8rem 0 4rem;
            background: linear-gradient(135deg, var(--soft-cream) 0%, #E8E6E3 100%);
            position: relative;
            overflow: hidden;
        }

        .hero::before {
            content: '';
            position: absolute;
            top: -50%;
            right: -20%;
            width: 80%;
            height: 150%;
            background: radial-gradient(circle, rgba(10, 36, 99, 0.03) 0%, transparent 70%);
            animation: float 20s ease-in-out infinite;
        }

        @keyframes float {
            0%, 100% { transform: translate(0, 0) rotate(0deg); }
            50% { transform: translate(-30px, 30px) rotate(5deg); }
        }

        .hero-content {
            max-width: 900px;
            position: relative;
            z-index: 1;
            opacity: 0;
            animation: fadeInUp 1s ease 0.3s forwards;
        }

        @keyframes fadeInUp {
            from {
                opacity: 0;
                transform: translateY(30px);
            }
            to {
                opacity: 1;
                transform: translateY(0);
            }
        }

        .hero-tag {
            display: inline-block;
            background: var(--deep-blue);
            color: white;
            padding: 0.5rem 1.5rem;
            font-size: 0.85rem;
            letter-spacing: 0.1em;
            text-transform: uppercase;
            margin-bottom: 2rem;
            border-radius: 2px;
        }

        .hero-subtitle {
            font-size: clamp(1.1rem, 2vw, 1.4rem);
            color: var(--text-soft);
            margin-bottom: 3rem;
            line-height: 1.8;
            font-weight: 300;
        }

        .hero-buttons {
            display: flex;
            gap: 1.5rem;
            flex-wrap: wrap;
        }

        .btn {
            padding: 1rem 2.5rem;
            text-decoration: none;
            font-size: 1rem;
            border-radius: 2px;
            transition: all 0.3s ease;
            display: inline-block;
            border: none;
            cursor: pointer;
            font-family: 'Newsreader', serif;
        }

        .btn-primary {
            background: var(--deep-blue);
            color: white;
            box-shadow: 0 4px 20px rgba(10, 36, 99, 0.2);
        }

        .btn-primary:hover {
            background: #051637;
            transform: translateY(-2px);
            box-shadow: 0 6px 30px rgba(10, 36, 99, 0.3);
        }

        .btn-secondary {
            background: transparent;
            color: var(--deep-blue);
            border: 2px solid var(--deep-blue);
        }

        .btn-secondary:hover {
            background: var(--deep-blue);
            color: white;
        }

        /* Positioning Statement */
        .positioning {
            padding: 6rem 0;
            background: var(--deep-blue);
            color: white;
            position: relative;
            overflow: hidden;
        }

        .positioning::after {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: url("data:image/svg+xml,%3Csvg width='60' height='60' viewBox='0 0 60 60' xmlns='http://www.w3.org/2000/svg'%3E%3Cg fill='none' fill-rule='evenodd'%3E%3Cg fill='%23ffffff' fill-opacity='0.03'%3E%3Cpath d='M36 34v-4h-2v4h-4v2h4v4h2v-4h4v-2h-4zm0-30V0h-2v4h-4v2h4v4h2V6h4V4h-4zM6 34v-4H4v4H0v2h4v4h2v-4h4v-2H6zM6 4V0H4v4H0v2h4v4h2V6h4V4H6z'/%3E%3C/g%3E%3C/g%3E%3C/svg%3E");
            opacity: 0.5;
        }

        .positioning-content {
            max-width: 1000px;
            margin: 0 auto;
            text-align: center;
            position: relative;
            z-index: 1;
            font-size: clamp(1.3rem, 2.5vw, 2rem);
            line-height: 1.6;
            font-weight: 300;
            font-style: italic;
        }

        /* Section Styles */
        section {
            padding: 8rem 0;
        }

        .section-header {
            text-align: center;
            margin-bottom: 5rem;
            opacity: 0;
            transform: translateY(20px);
        }

        .section-header.visible {
            animation: fadeInUp 0.8s ease forwards;
        }

        .section-subtitle {
            color: var(--text-soft);
            font-size: 1.1rem;
            margin-top: 1rem;
            font-weight: 300;
        }

        /* About Section */
        .about-content {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 4rem;
            align-items: start;
        }

        .about-text {
            font-size: 1.15rem;
            line-height: 1.9;
            color: var(--text-soft);
        }

        .about-text p {
            margin-bottom: 1.5rem;
        }

        .about-highlights {
            background: white;
            padding: 3rem;
            border-radius: 4px;
            box-shadow: 0 10px 40px rgba(0, 0, 0, 0.05);
        }

        .about-highlights h3 {
            margin-bottom: 1.5rem;
            color: var(--deep-blue);
        }

        .highlight-list {
            list-style: none;
        }

        .highlight-list li {
            padding: 0.8rem 0;
            border-bottom: 1px solid rgba(0, 0, 0, 0.05);
            color: var(--text-soft);
            position: relative;
            padding-left: 2rem;
        }

        .highlight-list li:last-child {
            border-bottom: none;
        }

        .highlight-list li::before {
            content: '→';
            position: absolute;
            left: 0;
            color: var(--accent-gold);
            font-weight: bold;
        }

        /* Skills Grid */
        .skills-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
            gap: 2rem;
        }

        .skill-card {
            background: white;
            padding: 3rem 2rem;
            border-radius: 4px;
            transition: all 0.4s ease;
            border-top: 3px solid transparent;
            opacity: 0;
            transform: translateY(20px);
        }

        .skill-card.visible {
            animation: fadeInUp 0.6s ease forwards;
        }

        .skill-card:nth-child(2) {
            animation-delay: 0.1s;
        }

        .skill-card:nth-child(3) {
            animation-delay: 0.2s;
        }

        .skill-card:nth-child(4) {
            animation-delay: 0.3s;
        }

        .skill-card:hover {
            transform: translateY(-10px);
            box-shadow: 0 20px 50px rgba(0, 0, 0, 0.1);
            border-top-color: var(--deep-blue);
        }

        .skill-icon {
            width: 60px;
            height: 60px;
            background: linear-gradient(135deg, var(--deep-blue), var(--royal-blue));
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            margin-bottom: 1.5rem;
            font-size: 1.8rem;
        }

        .skill-card h3 {
            margin-bottom: 1rem;
            color: var(--deep-blue);
        }

        .skill-card ul {
            list-style: none;
            color: var(--text-soft);
            line-height: 2;
        }

        .skill-card ul li::before {
            content: '•';
            color: var(--accent-gold);
            font-weight: bold;
            display: inline-block;
            width: 1.5rem;
        }

        /* Results Section */
        .results {
            background: white;
        }

        .results-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 3rem;
        }

        .result-item {
            text-align: center;
            padding: 2rem;
            border-radius: 4px;
            background: var(--soft-cream);
            transition: transform 0.3s ease;
        }

        .result-item:hover {
            transform: scale(1.05);
        }

        .result-number {
            font-family: 'DM Serif Display', serif;
            font-size: 3rem;
            color: var(--deep-blue);
            margin-bottom: 0.5rem;
            font-style: italic;
        }

        .result-text {
            color: var(--text-soft);
            font-size: 1rem;
            line-height: 1.6;
        }

        /* Case Studies */
        .case-studies-grid {
            display: grid;
            gap: 4rem;
        }

        .case-study {
            background: white;
            border-radius: 4px;
            overflow: hidden;
            box-shadow: 0 10px 40px rgba(0, 0, 0, 0.05);
            transition: all 0.4s ease;
        }

        .case-study:hover {
            box-shadow: 0 20px 60px rgba(0, 0, 0, 0.1);
            transform: translateY(-5px);
        }

        .case-study-header {
            background: linear-gradient(135deg, var(--deep-blue), var(--royal-blue));
            color: white;
            padding: 3rem;
        }

        .case-study-header h3 {
            margin-bottom: 1rem;
        }

        .case-study-tag {
            display: inline-block;
            background: rgba(255, 255, 255, 0.2);
            padding: 0.4rem 1rem;
            border-radius: 20px;
            font-size: 0.85rem;
            margin-bottom: 1rem;
        }

        .case-study-body {
            padding: 3rem;
        }

        .case-study-section {
            margin-bottom: 2.5rem;
        }

        .case-study-section:last-child {
            margin-bottom: 0;
        }

        .case-study-section h4 {
            font-family: 'DM Serif Display', serif;
            color: var(--deep-blue);
            margin-bottom: 1rem;
            font-size: 1.3rem;
        }

        .case-study-section p,
        .case-study-section ul {
            color: var(--text-soft);
            line-height: 1.8;
        }

        .case-study-section ul {
            list-style: none;
            padding-left: 0;
        }

        .case-study-section ul li {
            padding: 0.5rem 0;
            position: relative;
            padding-left: 2rem;
        }

        .case-study-section ul li::before {
            content: '✓';
            position: absolute;
            left: 0;
            color: var(--accent-gold);
            font-weight: bold;
        }

        /* Gallery */
        .gallery-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 2rem;
        }

        .gallery-item {
            position: relative;
            aspect-ratio: 1;
            background: white;
            border-radius: 4px;
            overflow: hidden;
            cursor: pointer;
            box-shadow: 0 5px 20px rgba(0, 0, 0, 0.08);
            transition: all 0.4s ease;
        }

        .gallery-item:hover {
            transform: scale(1.03);
            box-shadow: 0 15px 40px rgba(0, 0, 0, 0.15);
        }

        .gallery-placeholder {
            width: 100%;
            height: 100%;
            display: flex;
            flex-direction: column;
            align-items: center;
            justify-content: center;
            background: linear-gradient(135deg, var(--soft-cream), #E8E6E3);
            padding: 2rem;
            text-align: center;
        }

        .gallery-icon {
            font-size: 3rem;
            margin-bottom: 1rem;
            color: var(--deep-blue);
        }

        .gallery-label {
            font-family: 'DM Serif Display', serif;
            font-size: 1.2rem;
            color: var(--deep-blue);
        }

        /* Why Work With Me */
        .why-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
            gap: 2rem;
            text-align: center;
        }

        .why-item {
            padding: 2rem 1rem;
        }

        .why-item h4 {
            font-family: 'DM Serif Display', serif;
            font-size: 1.3rem;
            color: var(--deep-blue);
            margin-bottom: 0.5rem;
        }

        .why-item p {
            color: var(--text-soft);
            font-size: 0.95rem;
        }

        /* Resume Snapshot */
        .resume-snapshot {
            background: white;
        }

        .resume-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
            gap: 3rem;
        }

        .resume-section h3 {
            color: var(--deep-blue);
            margin-bottom: 1.5rem;
            font-size: 1.5rem;
        }

        .resume-item {
            margin-bottom: 1.5rem;
            padding-bottom: 1.5rem;
            border-bottom: 1px solid rgba(0, 0, 0, 0.05);
        }

        .resume-item:last-child {
            border-bottom: none;
        }

        .resume-title {
            font-weight: 600;
            color: var(--text-dark);
            margin-bottom: 0.3rem;
        }

        .resume-detail {
            color: var(--text-soft);
            font-size: 0.95rem;
        }

        .tools-list {
            display: flex;
            flex-wrap: wrap;
            gap: 0.8rem;
        }

        .tool-tag {
            background: var(--soft-cream);
            padding: 0.5rem 1.2rem;
            border-radius: 20px;
            font-size: 0.9rem;
            color: var(--text-dark);
        }

        /* Services */
        .services-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 2rem;
        }

        .service-item {
            background: white;
            padding: 2.5rem 2rem;
            border-radius: 4px;
            border-left: 4px solid var(--deep-blue);
            box-shadow: 0 5px 20px rgba(0, 0, 0, 0.05);
            transition: all 0.3s ease;
        }

        .service-item:hover {
            transform: translateX(10px);
            box-shadow: 0 10px 30px rgba(0, 0, 0, 0.1);
        }

        .service-item h4 {
            font-family: 'DM Serif Display', serif;
            color: var(--deep-blue);
            margin-bottom: 0.8rem;
            font-size: 1.2rem;
        }

        .service-item p {
            color: var(--text-soft);
            font-size: 0.95rem;
        }

        /* CTA Section */
        .cta-section {
            background: var(--deep-blue);
            color: white;
            text-align: center;
            padding: 8rem 0;
            position: relative;
            overflow: hidden;
        }

        .cta-section::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: url("data:image/svg+xml,%3Csvg width='60' height='60' viewBox='0 0 60 60' xmlns='http://www.w3.org/2000/svg'%3E%3Cg fill='none' fill-rule='evenodd'%3E%3Cg fill='%23ffffff' fill-opacity='0.03'%3E%3Cpath d='M36 34v-4h-2v4h-4v2h4v4h2v-4h4v-2h-4zm0-30V0h-2v4h-4v2h4v4h2V6h4V4h-4zM6 34v-4H4v4H0v2h4v4h2v-4h4v-2H6zM6 4V0H4v4H0v2h4v4h2V6h4V4H6z'/%3E%3C/g%3E%3C/g%3E%3C/svg%3E");
        }

        .cta-content {
            position: relative;
            z-index: 1;
        }

        .cta-content h2 {
            color: white;
            margin-bottom: 2rem;
            font-size: clamp(2.5rem, 5vw, 4rem);
        }

        .cta-content p {
            font-size: 1.3rem;
            margin-bottom: 3rem;
            color: rgba(255, 255, 255, 0.9);
            font-weight: 300;
        }

        /* Footer */
        footer {
            background: var(--text-dark);
            color: white;
            text-align: center;
            padding: 3rem 0;
        }

        .footer-content {
            display: flex;
            flex-direction: column;
            align-items: center;
            gap: 1.5rem;
        }

        .footer-links {
            display: flex;
            gap: 2rem;
            list-style: none;
        }

        .footer-links a {
            color: rgba(255, 255, 255, 0.7);
            text-decoration: none;
            transition: color 0.3s ease;
        }

        .footer-links a:hover {
            color: white;
        }

        .footer-copyright {
            color: rgba(255, 255, 2
