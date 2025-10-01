# Mon-site
C'est un chien.
[Click ici](https://fr.wikipedia.org/wiki/Chien)

[![d2253152](https://github.com/user-attachments/assets/7ce63cf7-f618-4255-9868-c8a4ac0f3814)](https://fr.wikipedia.org/wiki/Chien)

[Don't click ici!!!](https://fr.wikipedia.org/wiki/Chien)
[![单击按钮，手指单击-单击此处web按钮-孤立网站手指点击光标-—-矢量-股票矢量-164541958](https://github.com/user-attachments/assets/bb7b7f9c-f57b-48fa-ac84-94c2f7c421e0)](https://mail.google.com/mail/u/0/#inbox/FMfcgzQcpnPVlgHdDgggdmfsJDllDbCQ)
<!DOCTYPE html>
<html lang="fr">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Découvrez la Chine - Voyage en Chine</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <style>
        /* 基础样式 */
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
        }
        
        body {
            background-color: #f8f9fa;
            color: #333;
            line-height: 1.6;
            overflow-x: hidden;
        }
        
        .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 20px;
        }
        
        /* 导航栏 */
        header {
            background-color: #fff;
            box-shadow: 0 2px 10px rgba(0, 0, 0, 0.1);
            position: sticky;
            top: 0;
            z-index: 1000;
        }
        
        nav {
            display: flex;
            justify-content: space-between;
            align-items: center;
            padding: 20px 0;
        }
        
        .logo {
            font-size: 24px;
            font-weight: bold;
            color: #d32f2f;
        }
        
        .nav-links {
            display: flex;
            list-style: none;
        }
        
        .nav-links li {
            margin-left: 30px;
        }
        
        .nav-links a {
            text-decoration: none;
            color: #333;
            font-weight: 500;
            transition: color 0.3s;
        }
        
        .nav-links a:hover {
            color: #d32f2f;
        }
        
        .menu-toggle {
            display: none;
            font-size: 1.5rem;
            cursor: pointer;
        }
        
        /* 英雄区域 */
        .hero {
            background: linear-gradient(rgba(0, 0, 0, 0.5), rgba(0, 0, 0, 0.5)), url('https://images.unsplash.com/photo-1508804185872-d7badad00f7d?ixlib=rb-1.2.1&auto=format&fit=crop&w=1350&q=80');
            background-size: cover;
            background-position: center;
            height: 70vh;
            display: flex;
            align-items: center;
            justify-content: center;
            text-align: center;
            color: white;
        }
        
        .hero-content {
            max-width: 800px;
            padding: 0 20px;
        }
        
        .hero h1 {
            font-size: 3rem;
            margin-bottom: 20px;
            text-shadow: 2px 2px 4px rgba(0, 0, 0, 0.5);
        }
        
        .hero p {
            font-size: 1.2rem;
            margin-bottom: 30px;
            text-shadow: 1px 1px 2px rgba(0, 0, 0, 0.5);
        }
        
        .btn {
            display: inline-block;
            background-color: #d32f2f;
            color: white;
            padding: 12px 30px;
            border-radius: 5px;
            text-decoration: none;
            font-weight: bold;
            transition: all 0.3s;
            border: none;
            cursor: pointer;
        }
        
        .btn:hover {
            background-color: #b71c1c;
            transform: translateY(-3px);
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.2);
        }
        
        /* 目的地部分 */
        .section {
            padding: 80px 0;
        }
        
        .section-title {
            text-align: center;
            margin-bottom: 50px;
        }
        
        .section-title h2 {
            font-size: 2.5rem;
            color: #333;
            margin-bottom: 15px;
            position: relative;
            display: inline-block;
        }
        
        .section-title h2::after {
            content: '';
            position: absolute;
            bottom: -10px;
            left: 50%;
            transform: translateX(-50%);
            width: 80px;
            height: 3px;
            background-color: #d32f2f;
        }
        
        .section-title p {
            color: #666;
            max-width: 700px;
            margin: 20px auto 0;
        }
        
        .destinations {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 30px;
        }
        
        .destination-card {
            background-color: white;
            border-radius: 10px;
            overflow: hidden;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.1);
            transition: transform 0.3s;
        }
        
        .destination-card:hover {
            transform: translateY(-10px);
        }
        
        .card-img {
            height: 200px;
            overflow: hidden;
        }
        
        .card-img img {
            width: 100%;
            height: 100%;
            object-fit: cover;
            transition: transform 0.5s;
        }
        
        .destination-card:hover .card-img img {
            transform: scale(1.1);
        }
        
        .card-content {
            padding: 20px;
        }
        
        .card-content h3 {
            font-size: 1.5rem;
            margin-bottom: 10px;
            color: #333;
        }
        
        .card-content p {
            color: #666;
            margin-bottom: 15px;
        }
        
        /* 文化部分 */
        .culture {
            background-color: #f0f2f5;
        }
        
        .culture-content {
            display: flex;
            align-items: center;
            gap: 40px;
        }
        
        .culture-text {
            flex: 1;
        }
        
        .culture-text h3 {
            font-size: 1.8rem;
            margin-bottom: 20px;
            color: #333;
        }
        
        .culture-text p {
            margin-bottom: 15px;
            color: #555;
        }
        
        .culture-img {
            flex: 1;
            border-radius: 10px;
            overflow: hidden;
            box-shadow: 0 10px 30px rgba(0, 0, 0, 0.1);
        }
        
        .culture-img img {
            width: 100%;
            height: auto;
            display: block;
        }
        
        /* 旅游贴士 */
        .tips {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 30px;
        }
        
        .tip-card {
            background-color: white;
            padding: 30px;
            border-radius: 10px;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.05);
            text-align: center;
            transition: transform 0.3s;
        }
        
        .tip-card:hover {
            transform: translateY(-5px);
        }
        
        .tip-icon {
            font-size: 2.5rem;
            color: #d32f2f;
            margin-bottom: 20px;
        }
        
        .tip-card h3 {
            font-size: 1.3rem;
            margin-bottom: 15px;
        }
        
        /* 页脚 */
        footer {
            background-color: #333;
            color: white;
            padding: 60px 0 30px;
        }
        
        .footer-content {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
            gap: 40px;
            margin-bottom: 40px;
        }
        
        .footer-column h3 {
            font-size: 1.2rem;
            margin-bottom: 20px;
            position: relative;
            padding-bottom: 10px;
        }
        
        .footer-column h3::after {
            content: '';
            position: absolute;
            left: 0;
            bottom: 0;
            width: 50px;
            height: 2px;
            background-color: #d32f2f;
        }
        
        .footer-links {
            list-style: none;
        }
        
        .footer-links li {
            margin-bottom: 10px;
        }
        
        .footer-links a {
            color: #bbb;
            text-decoration: none;
            transition: color 0.3s;
        }
        
        .footer-links a:hover {
            color: white;
        }
        
        .social-icons {
            display: flex;
            gap: 15px;
            margin-top: 15px;
        }
        
        .social-icons a {
            display: inline-flex;
            align-items: center;
            justify-content: center;
            width: 40px;
            height: 40px;
            background-color: #444;
            border-radius: 50%;
            color: white;
            text-decoration: none;
            transition: background-color 0.3s;
        }
        
        .social-icons a:hover {
            background-color: #d32f2f;
        }
        
        .copyright {
            text-align: center;
            padding-top: 30px;
            border-top: 1px solid #444;
            color: #bbb;
            font-size: 0.9rem;
        }
        
        /* 响应式设计 */
        @media (max-width: 768px) {
            .menu-toggle {
                display: block;
            }
            
            .nav-links {
                position: fixed;
                top: 70px;
                left: -100%;
                width: 100%;
                height: calc(100vh - 70px);
                background-color: white;
                flex-direction: column;
                align-items: center;
                justify-content: flex-start;
                padding-top: 50px;
                transition: left 0.3s;
                box-shadow: 0 5px 10px rgba(0, 0, 0, 0.1);
            }
            
            .nav-links.active {
                left: 0;
            }
            
            .nav-links li {
                margin: 15px 0;
            }
            
            .hero h1 {
                font-size: 2.2rem;
            }
            
            .culture-content {
                flex-direction: column;
            }
            
            .section-title h2 {
                font-size: 2rem;
            }
        }
    </style>
</head>
<body>
    <!-- 导航栏 -->
    <header>
        <div class="container">
            <nav>
                <div class="logo">Chine Voyage</div>
                <div class="menu-toggle" id="menuToggle">
                    <i class="fas fa-bars"></i>
                </div>
                <ul class="nav-links" id="navLinks">
                    <li><a href="#accueil">Accueil</a></li>
                    <li><a href="#destinations">Destinations</a></li>
                    <li><a href="#culture">Culture</a></li>
                    <li><a href="#conseils">Conseils</a></li>
                    <li><a href="#contact">Contact</a></li>
                </ul>
            </nav>
        </div>
    </header>

    <!-- 英雄区域 -->
    <section class="hero" id="accueil">
        <div class="hero-content">
            <h1>Découvrez la Chine, Terre de Contrastes</h1>
            <p>Des paysages époustouflants, une culture millénaire et des expériences uniques vous attendent</p>
            <a href="#destinations" class="btn">Explorer nos destinations</a>
        </div>
    </section>

    <!-- 目的地部分 -->
    <section class="section" id="destinations">
        <div class="container">
            <div class="section-title">
                <h2>Destinations Incontournables</h2>
                <p>Découvrez les merveilles de la Chine, de la Grande Muraille aux rizières en terrasse</p>
            </div>
            <div class="destinations">
                <div class="destination-card">
                    <div class="card-img">
                        <img src="https://images.unsplash.com/photo-1508804185872-d7badad00f7d?ixlib=rb-1.2.1&auto=format&fit=crop&w=1350&q=80" alt="Grande Muraille de Chine">
                    </div>
                    <div class="card-content">
                        <h3>Grande Muraille</h3>
                        <p>Découvrez l'une des merveilles du monde, serpentant à travers les montagnes sur plus de 20 000 km.</p>
                        <a href="#" class="btn">En savoir plus</a>
                    </div>
                </div>
                <div class="destination-card">
                    <div class="card-img">
                        <img src="https://images.unsplash.com/photo-1547981609-4b6bf67b7d12?ixlib=rb-1.2.1&auto=format&fit=crop&w=1350&q=80" alt="Armée de terre cuite">
                    </div>
                    <div class="card-content">
                        <h3>Armée de Terre Cuite</h3>
                        <p>Visitez le mausolée de l'empereur Qin à Xi'an et découvrez cette incroyable armée de soldats en terre cuite.</p>
                        <a href="#" class="btn">En savoir plus</a>
                    </div>
                </div>
                <div class="destination-card">
                    <div class="card-img">
                        <img src="https://images.unsplash.com/photo-1518638150340-f706e86654de?ixlib=rb-1.2.1&auto=format&fit=crop&w=1350&q=80" alt="Rizières en terrasse">
                    </div>
                    <div class="card-content">
                        <h3>Rizières de Yuanyang</h3>
                        <p>Admirez ces paysages spectaculaires façonnés par l'homme dans la province du Yunnan.</p>
                        <a href="#" class="btn">En savoir plus</a>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- 文化部分 -->
    <section class="section culture" id="culture">
        <div class="container">
            <div class="section-title">
                <h2>Culture et Traditions</h2>
                <p>Plongez dans l'une des plus anciennes civilisations du monde</p>
            </div>
            <div class="culture-content">
                <div class="culture-text">
                    <h3>Un héritage millénaire</h3>
                    <p>La Chine possède une culture riche et diversifiée qui s'est développée sur plus de 5 000 ans. Des philosophies ancestrales comme le confucianisme et le taoïsme continuent d'influencer la société moderne.</p>
                    <p>Découvrez l'art de la calligraphie, la délicatesse de la cuisine chinoise, l'élégance de l'opéra de Pékin et la profondeur des arts martiaux.</p>
                    <p>Chaque région offre ses propres traditions, dialectes et spécialités culinaires, créant une tapisserie culturelle fascinante à explorer.</p>
                    <a href="#" class="btn">Découvrir la culture</a>
                </div>
                <div class="culture-img">
                    <img src="https://images.unsplash.com/photo-1545912452-8aea7e25a3d3?ixlib=rb-1.2.1&auto=format&fit=crop&w=1350&q=80" alt="Culture chinoise">
                </div>
            </div>
        </div>
    </section>

    <!-- 旅游贴士 -->
    <section class="section" id="conseils">
        <div class="container">
            <div class="section-title">
                <h2>Conseils de Voyage</h2>
                <p>Préparez votre voyage en Chine avec nos recommandations pratiques</p>
            </div>
            <div class="tips">
                <div class="tip-card">
                    <div class="tip-icon"><i class="fas fa-calendar-alt"></i></div>
                    <h3>Meilleure période</h3>
                    <p>Le printemps (avril-mai) et l'automne (septembre-octobre) sont les saisons idéales pour visiter la Chine.</p>
                </div>
                <div class="tip-card">
                    <div class="tip-icon"><i class="fas fa-file-alt"></i></div>
                    <h3>Visa et formalités</h3>
                    <p>Pensez à faire votre demande de visa plusieurs semaines avant votre départ. Un passeport valide est requis.</p>
                </div>
                <div class="tip-card">
                    <div class="tip-icon"><i class="fas fa-language"></i></div>
                    <h3>Langue</h3>
                    <p>Le mandarin est la langue officielle. Apprenez quelques phrases de base pour faciliter votre séjour.</p>
                </div>
                <div class="tip-card">
                    <div class="tip-icon"><i class="fas fa-money-bill-wave"></i></div>
                    <h3>Devise</h3>
                    <p>La monnaie locale est le yuan (RMB). Les cartes de crédit sont acceptées dans les grands établissements.</p>
                </div>
            </div>
        </div>
    </section>

    <!-- 页脚 -->
    <footer id="contact">
        <div class="container">
            <div class="footer-content">
                <div class="footer-column">
                    <h3>Chine Voyage</h3>
                    <p>Votre guide pour découvrir les merveilles de la Chine. Nous proposons des conseils, des itinéraires et des informations pour planifier votre voyage parfait.</p>
                    <div class="social-icons">
                        <a href="#"><i class="fab fa-facebook-f"></i></a>
                        <a href="#"><i class="fab fa-twitter"></i></a>
                        <a href="#"><i class="fab fa-instagram"></i></a>
                        <a href="#"><i class="fab fa-youtube"></i></a>
                    </div>
                </div>
                <div class="footer-column">
                    <h3>Liens Rapides</h3>
                    <ul class="footer-links">
                        <li><a href="#accueil">Accueil</a></li>
                        <li><a href="#destinations">Destinations</a></li>
                        <li><a href="#culture">Culture</a></li>
                        <li><a href="#conseils">Conseils</a></li>
                    </ul>
                </div>
                <div class="footer-column">
                    <h3>Contact</h3>
                    <ul class="footer-links">
                        <li><i class="fas fa-envelope"></i> Email: info@chinevoyage.fr</li>
                        <li><i class="fas fa-phone"></i> Téléphone: +33 1 23 45 67 89</li>
                        <li><i class="fas fa-map-marker-alt"></i> Adresse: 123 Avenue de Chine, 75001 Paris</li>
                    </ul>
                </div>
                <div class="footer-column">
                    <h3>Newsletter</h3>
                    <p>Inscrivez-vous pour recevoir nos offres spéciales et conseils de voyage.</p>
                    <form>
                        <input type="email" placeholder="Votre email" style="width: 100%; padding: 10px; margin: 10px 0; border: 1px solid #444; background: #222; color: white; border-radius: 4px;">
                        <button type="submit" class="btn" style="width: 100%;">S'inscrire</button>
                    </form>
                </div>
            </div>
            <div class="copyright">
                <p>&copy; 2023 Chine Voyage. Tous droits réservés.</p>
            </div>
        </div>
    </footer>

    <script>
        // 移动端菜单切换
        document.getElementById('menuToggle').addEventListener('click', function() {
            document.getElementById('navLinks').classList.toggle('active');
        });
        
        // 平滑滚动
        document.querySelectorAll('a[href^="#"]').forEach(anchor => {
            anchor.addEventListener('click', function (e) {
                e.preventDefault();
                
                const targetId = this.getAttribute('href');
                if(targetId === '#') return;
                
                const targetElement = document.querySelector(targetId);
                if(targetElement) {
                    window.scrollTo({
                        top: targetElement.offsetTop - 70,
                        behavior: 'smooth'
                    });
                    
                    // 关闭移动端菜单
                    document.getElementById('navLinks').classList.remove('active');
                }
            });
        });
        
        // 添加滚动效果
        window.addEventListener('scroll', function() {
            const sections = document.querySelectorAll('.section');
            const windowHeight = window.innerHeight;
            
            sections.forEach(section => {
                const sectionTop = section.getBoundingClientRect().top;
                if(sectionTop < windowHeight * 0.85) {
                    section.style.opacity = '1';
                    section.style.transform = 'translateY(0)';
                }
            });
        });
        
        // 初始化部分动画
        document.querySelectorAll('.section').forEach(section => {
            section.style.opacity = '0';
            section.style.transform = 'translateY(20px)';
            section.style.transition = 'opacity 0.5s, transform 0.5s';
        });
        
        // 页面加载后触发一次滚动事件以显示初始内容
        window.dispatchEvent(new Event('scroll'));
    </script>
</body>
</html>
