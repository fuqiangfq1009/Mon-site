<html lang="fr">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Voyage en Chine - Découvrez la Chine</title>
    <style>
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
            background-color: #a23;
        }
        
        footer {
            background-color: #333;
            color: white;
            text-align: center;
            padding: 20px 0;
            margin-top: 30px;
        }
        
        @media (max-width: 768px) {
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

    <div class="container">
        <section class="hero">
            <h1>Découvrez la Chine</h1>
            <p>Un pays aux mille visages, riche en histoire et en paysages spectaculaires. Explorez la culture millénaire et les merveilles naturelles de la Chine.</p>
            <a href="https://fr.wikipedia.org/wiki/Chine" class="btn">Commencer l'aventure</a>
        </section>
    </div>
