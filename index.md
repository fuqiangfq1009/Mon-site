# Mon-site
C'est un chien.
[Click ici](https://fr.wikipedia.org/wiki/Chien)

[![d2253152](https://github.com/user-attachments/assets/7ce63cf7-f618-4255-9868-c8a4ac0f3814)](https://fr.wikipedia.org/wiki/Chien)

[Don't click ici!!!](https://fr.wikipedia.org/wiki/Chien)
[![单击按钮，手指单击-单击此处web按钮-孤立网站手指点击光标-—-矢量-股票矢量-164541958](https://github.com/user-attachments/assets/bb7b7f9c-f57b-48fa-ac84-94c2f7c421e0)](https://mail.google.com/mail/u/0/#inbox/FMfcgzQcpnPVlgHdDgggdmfsJDllDbCQ)
<html lang="fr">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Voyage en Chine - Découvrez la Chine</title>
    <style>
        /* Styles de base */
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: Arial, sans-serif;
        }
        
        body {
            background-color: #f5f5f5;
            color: #333;
            line-height: 1.6;
        }
        
        .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 15px;
        }
        
        /* En-tête */
        header {
            background-color: #c00;
            color: white;
            padding: 15px 0;
        }
        
        nav {
            display: flex;
            justify-content: space-between;
            align-items: center;
        }
        
        .logo {
            font-size: 24px;
            font-weight: bold;
        }
        
        .nav-links {
            display: flex;
            list-style: none;
        }
        
        .nav-links li {
            margin-left: 20px;
        }
        
        .nav-links a {
            color: white;
            text-decoration: none;
            padding: 5px 10px;
        }
        
        .nav-links a:hover {
            background-color: #a00;
            border-radius: 3px;
        }
        
        /* Section héros */
        .hero {
            text-align: center;
            padding: 60px 0;
            background-color: #fff;
            border-radius: 5px;
            margin: 30px 0;
        }
        
        .hero h1 {
            font-size: 2.5em;
            margin-bottom: 15px;
            color: #c00;
        }
        
        .hero p {
            font-size: 1.2em;
            max-width: 800px;
            margin: 0 auto 30px;
        }
        
        .btn {
            display: inline-block;
            background-color: #c00;
            color: white;
            padding: 12px 25px;
            border-radius: 5px;
            text-decoration: none;
            font-weight: bold;
        }
        
        .btn:hover {
            background-color: #a00;
        }
        
        /* Section destinations */
        .section-title {
            text-align: center;
            margin: 40px 0 30px;
            color: #c00;
        }
        
        .destinations {
            display: flex;
            justify-content: space-between;
            flex-wrap: wrap;
        }
        
        .destination {
            width: 32%;
            background-color: white;
            margin-bottom: 30px;
            border-radius: 5px;
            overflow: hidden;
            box-shadow: 0 2px 5px rgba(0,0,0,0.1);
        }
        
        .destination img {
            width: 100%;
            height: 200px;
            object-fit: cover;
        }
        
        .destination-content {
            padding: 15px;
        }
        
        .destination h3 {
            margin-bottom: 10px;
            color: #c00;
        }
        
        /* Section à propos */
        .about {
            background-color: white;
            padding: 30px;
            border-radius: 5px;
            margin: 40px 0;
            box-shadow: 0 2px 5px rgba(0,0,0,0.1);
        }
        
        .about h2 {
            margin-bottom: 20px;
            color: #c00;
        }
        
        /* Pied de page */
        footer {
            background-color: #333;
            color: white;
            text-align: center;
            padding: 20px 0;
            margin-top: 30px;
        }
        
        /* Responsive */
        @media (max-width: 768px) {
            .destination {
                width: 100%;
            }
            
            nav {
                flex-direction: column;
            }
            
            .nav-links {
                margin-top: 15px;
            }
            
            .nav-links li {
                margin: 0 10px;
            }
        }
    </style>
</head>
<body>
    <!-- En-tête -->
    <header>
        <div class="container">
            <nav>
                <div class="logo">Voyage en Chine</div>
                <ul class="nav-links">
                    <li><a href="#">Accueil</a></li>
                    <li><a href="#">Destinations</a></li>
                    <li><a href="#">Culture</a></li>
                    <li><a href="#">Conseils</a></li>
                    <li><a href="#">Contact</a></li>
                </ul>
            </nav>
        </div>
    </header>

    <!-- Contenu principal -->
    <div class="container">
        <!-- Section héros -->
        <section class="hero">
            <h1>Découvrez la Chine</h1>
            <p>Un pays aux mille visages, riche en histoire et en paysages spectaculaires. Explorez la culture millénaire et les merveilles naturelles de la Chine.</p>
            <a href="#" class="btn">Commencer l'aventure</a>
        </section>


        <div class="container">
            <p>&copy; 2023 Voyage en Chine - Site créé pour un projet scolaire</p>
        </div>
    </footer>
</body>
</html>


<!DOCTYPE html>
<html lang="fr">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Carte Interactive de la Chine</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
        }
        
        body {
            background: linear-gradient(135deg, #1a2a6c, #b21f1f, #fdbb2d);
            color: #fff;
            min-height: 100vh;
            padding: 20px;
            display: flex;
            flex-direction: column;
            align-items: center;
        }
        
        .container {
            width: 100%;
            max-width: 1000px;
            background-color: rgba(255, 255, 255, 0.1);
            backdrop-filter: blur(10px);
            border-radius: 15px;
            box-shadow: 0 10px 30px rgba(0, 0, 0, 0.3);
            overflow: hidden;
            margin-top: 20px;
            padding: 20px;
        }
        
        header {
            text-align: center;
            padding: 20px;
            margin-bottom: 10px;
        }
        
        h1 {
            font-size: 2.5rem;
            margin-bottom: 10px;
            text-shadow: 2px 2px 4px rgba(0, 0, 0, 0.5);
        }
        
        .subtitle {
            font-size: 1.2rem;
            opacity: 0.9;
        }
        
        .map-container {
            position: relative;
            width: 100%;
            height: 600px;
            background-color: rgba(255, 255, 255, 0.05);
            border-radius: 10px;
            overflow: hidden;
        }
        
        .info-panel {
            background-color: rgba(0, 0, 0, 0.7);
            border-radius: 10px;
            padding: 15px;
            margin-top: 20px;
            text-align: center;
        }
        
        .province-name {
            font-size: 1.8rem;
            font-weight: bold;
            color: #fdbb2d;
            margin-bottom: 10px;
        }
        
        .province-info {
            font-size: 1rem;
            line-height: 1.5;
        }
        
        /* SVG样式 */
        svg {
            width: 100%;
            height: 100%;
        }
        
        .province {
            fill: #2a6f97;
            stroke: #fff;
            stroke-width: 0.5;
            transition: all 0.3s ease;
            cursor: pointer;
        }
        
        .province:hover {
            fill: #fdbb2d;
            stroke-width: 1.5;
            filter: drop-shadow(0 0 8px rgba(253, 187, 45, 0.7));
        }
        
        .water {
            fill: #1a659e;
        }
        
        .legend {
            display: flex;
            justify-content: center;
            margin-top: 15px;
            gap: 20px;
        }
        
        .legend-item {
            display: flex;
            align-items: center;
            gap: 5px;
        }
        
        .legend-color {
            width: 20px;
            height: 20px;
            border-radius: 4px;
        }
        
        .normal {
            background-color: #2a6f97;
        }
        
        .hover {
            background-color: #fdbb2d;
        }
        
        .instructions {
            margin-top: 15px;
            text-align: center;
            font-style: italic;
            opacity: 0.8;
        }
        
        @media (max-width: 768px) {
            .map-container {
                height: 400px;
            }
            
            h1 {
                font-size: 1.8rem;
            }
        }
    </style>
</head>
<body>
    <header>
        <h1>Carte Interactive de la Chine</h1>
        <p class="subtitle">Passez votre souris sur une province pour voir son nom en français</p>
    </header>
    
    <div class="container">
        <div class="map-container">
            <svg viewBox="0 0 1000 800" xmlns="http://www.w3.org/2000/svg">
                <!-- 中国地图轮廓 - 简化版本 -->
                <!-- 东北地区 -->
                <path id="heilongjiang" class="province" d="M600,150 L650,160 L680,180 L700,200 L720,220 L700,250 L680,270 L650,280 L620,270 L600,250 L580,230 L590,200 Z" />
                <path id="jilin" class="province" d="M650,280 L680,270 L700,250 L720,270 L740,290 L720,310 L700,330 L670,320 L650,300 Z" />
                <path id="liaoning" class="province" d="M670,320 L700,330 L720,350 L700,370 L670,360 L650,340 Z" />
                
                <!-- 华北地区 -->
                <path id="hebei" class="province" d="M550,320 L580,330 L600,350 L580,370 L550,360 L530,340 Z" />
                <path id="beijing" class="province" d="M560,340 L570,350 L560,360 L550,350 Z" />
                <path id="tianjin" class="province" d="M580,350 L590,360 L580,370 L570,360 Z" />
                <path id="shandong" class="province" d="M600,370 L630,380 L650,400 L630,420 L600,410 L580,390 Z" />
                <path id="shanxi" class="province" d="M500,320 L530,330 L550,350 L530,370 L500,360 L480,340 Z" />
                <path id="henan" class="province" d="M530,370 L560,380 L580,400 L560,420 L530,410 L510,390 Z" />
                
                <!-- 华东地区 -->
                <path id="jiangsu" class="province" d="M600,410 L630,420 L650,440 L630,460 L600,450 L580,430 Z" />
                <path id="zhejiang" class="province" d="M630,460 L660,470 L680,490 L660,510 L630,500 L610,480 Z" />
                <path id="shanghai" class="province" d="M640,440 L650,450 L640,460 L630,450 Z" />
                <path id="anhui" class="province" d="M580,430 L610,440 L630,460 L610,480 L580,470 L560,450 Z" />
                <path id="fujian" class="province" d="M630,500 L660,510 L680,530 L660,550 L630,540 L610,520 Z" />
                <path id="jiangxi" class="province" d="M580,470 L610,480 L630,500 L610,520 L580,510 L560,490 Z" />
                
                <!-- 华中地区 -->
                <path id="hubei" class="province" d="M530,410 L560,420 L580,440 L560,460 L530,450 L510,430 Z" />
                <path id="hunan" class="province" d="M530,450 L560,460 L580,480 L560,500 L530,490 L510,470 Z" />
                
                <!-- 华南地区 -->
                <path id="guangdong" class="province" d="M580,520 L610,530 L630,550 L610,570 L580,560 L560,540 Z" />
                <path id="guangxi" class="province" d="M530,490 L560,500 L580,520 L560,540 L530,530 L510,510 Z" />
                <path id="hainan" class="province" d="M590,580 L610,590 L590,600 L570,590 Z" />
                
                <!-- 西南地区 -->
                <path id="sichuan" class="province" d="M450,370 L480,380 L500,400 L480,420 L450,410 L430,390 Z" />
                <path id="chongqing" class="province" d="M480,420 L500,430 L480,440 L460,430 Z" />
                <path id="guizhou" class="province" d="M480,440 L510,450 L530,470 L510,490 L480,480 L460,460 Z" />
                <path id="yunnan" class="province" d="M450,430 L480,440 L500,460 L480,480 L450,470 L430,450 Z" />
                <path id="tibet" class="province" d="M350,350 L380,360 L400,380 L380,400 L350,390 L330,370 Z" />
                
                <!-- 西北地区 -->
                <path id="shaanxi" class="province" d="M480,340 L510,350 L530,370 L510,390 L480,380 L460,360 Z" />
                <path id="gansu" class="province" d="M430,300 L460,310 L480,330 L460,350 L430,340 L410,320 Z" />
                <path id="qinghai" class="province" d="M380,320 L410,330 L430,350 L410,370 L380,360 L360,340 Z" />
                <path id="ningxia" class="province" d="M460,320 L470,330 L460,340 L450,330 Z" />
                <path id="xinjiang" class="province" d="M300,250 L330,260 L350,280 L330,300 L300,290 L280,270 Z" />
                <path id="inner-mongolia" class="province" d="M450,250 L480,260 L500,280 L480,300 L450,290 L430,270 Z" />
                
                <!-- 海洋 -->
                <path class="water" d="M0,0 L1000,0 L1000,800 L0,800 Z" />
            </svg>
        </div>
        
        <div class="info-panel">
            <div class="province-name">Passez votre souris sur une province</div>
            <div class="province-info">Les noms des provinces chinoises s'afficheront ici en français</div>
        </div>
        
        <div class="legend">
            <div class="legend-item">
                <div class="legend-color normal"></div>
                <span>Province</span>
            </div>
            <div class="legend-item">
                <div class="legend-color hover"></div>
                <span>Survol</span>
            </div>
        </div>
        
        <div class="instructions">
            Cette carte montre les principales provinces et régions de Chine
        </div>
    </div>

    <script>
        // 省份法语名称映射
        const provinceNames = {
            "heilongjiang": "Heilongjiang",
            "jilin": "Jilin",
            "liaoning": "Liaoning",
            "hebei": "Hebei",
            "beijing": "Beijing (Pékin)",
            "tianjin": "Tianjin",
            "shandong": "Shandong",
            "shanxi": "Shanxi",
            "henan": "Henan",
            "jiangsu": "Jiangsu",
            "zhejiang": "Zhejiang",
            "shanghai": "Shanghai",
            "anhui": "Anhui",
            "fujian": "Fujian",
            "jiangxi": "Jiangxi",
            "hubei": "Hubei",
            "hunan": "Hunan",
            "guangdong": "Guangdong",
            "guangxi": "Guangxi",
            "hainan": "Hainan",
            "sichuan": "Sichuan",
            "chongqing": "Chongqing",
            "guizhou": "Guizhou",
            "yunnan": "Yunnan",
            "tibet": "Tibet",
            "shaanxi": "Shaanxi",
            "gansu": "Gansu",
            "qinghai": "Qinghai",
            "ningxia": "Ningxia",
            "xinjiang": "Xinjiang",
            "inner-mongolia": "Mongolie-Intérieure"
        };
        
        // 省份额外信息
        const provinceInfo = {
            "heilongjiang": "Province la plus au nord de la Chine, connue pour ses hivers glacials",
            "beijing": "Capitale de la Chine, centre politique et culturel",
            "shanghai": "Plus grande ville de Chine, centre financier mondial",
            "guangdong": "Province côtière du sud, cœur économique de la Chine",
            "tibet": "Région autonome, connue pour ses paysages himalayens",
            "xinjiang": "Plus grande région de Chine, riche en ressources naturelles",
            "hainan": "Île tropicale au sud de la Chine, destination touristique populaire"
        };
        
        // 获取所有省份元素
        const provinces = document.querySelectorAll('.province');
        const provinceNameElement = document.querySelector('.province-name');
        const provinceInfoElement = document.querySelector('.province-info');
        
        // 为每个省份添加事件监听器
        provinces.forEach(province => {
            province.addEventListener('mouseover', function() {
                const provinceId = this.id;
                const frenchName = provinceNames[provinceId] || "Nom non disponible";
                const info = provinceInfo[provinceId] || "Passez votre souris sur d'autres provinces pour plus d'informations";
                
                provinceNameElement.textContent = frenchName;
                provinceInfoElement.textContent = info;
            });
            
            province.addEventListener('mouseout', function() {
                // 可选：恢复默认文本
                // provinceNameElement.textContent = "Passez votre souris sur une province";
                // provinceInfoElement.textContent = "Les noms des provinces chinoises s'afficheront ici en français";
            });
        });
    </script>
</body>
</html>
