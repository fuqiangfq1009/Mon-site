<!DOCTYPE html>
<html lang="fr">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Voyage en Chine - Découvrez la Chine</title>
  <style>
    * {
      margin: 0; padding: 0; box-sizing: border-box;
      font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
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
      position: sticky;
      top: 0;
      z-index: 1000;
      box-shadow: 0 2px 5px rgba(0,0,0,0.2);
    }
    nav {
      display: flex;
      justify-content: space-between;
      align-items: center;
      height: 60px;
      padding: 0 15px;
    }
    .logo {
      font-size: 28px;
      font-weight: bold;
      color: white;
    }
    .nav-links {
      display: flex;
      list-style: none;
      height: 100%;
      margin: 0;
      padding: 0;
    }
    .nav-links li {
      margin-left: 20px;
      display: flex;
      align-items: center;
    }
    .nav-links a {
      color: white;
      text-decoration: none;
      display: flex;
      align-items: center;
      height: 100%;
      padding: 0 10px;
      font-weight: 500;
      transition: background 0.3s;
      cursor: pointer;
    }
    .nav-links a:hover {
      background-color: #a00;
      border-radius: 3px;
    }
    #content-area {
      background: #fff;
      border-radius: 8px;
      padding: 40px 30px;
      margin: 30px 0;
      min-height: 500px;
      box-shadow: 0 4px 15px rgba(0,0,0,0.1);
      text-align: center;
      transition: opacity 0.3s;
    }
    #content-area h1 {
      color: #c00;
      font-size: 48px;
      margin-bottom: 25px;
      text-shadow: 1px 1px 2px rgba(0,0,0,0.2);
    }
    #content-area p {
      font-size: 20px;
      color: #444;
      margin-bottom: 30px;
      line-height: 1.8;
    }
    .btn {
      display: inline-block;
      background-color: #c00;
      color: white;
      padding: 14px 30px;
      border-radius: 6px;
      text-decoration: none;
      font-weight: bold;
      font-size: 18px;
      transition: background 0.3s, transform 0.2s;
    }
    .btn:hover {
      background-color: #a23;
      transform: translateY(-2px);
    }
    footer {
      background-color: #333;
      color: white;
      text-align: center;
      padding: 20px 0;
      margin-top: 30px;
    }
    @media (max-width: 768px) {
      nav { flex-direction: column; height: auto; }
      .nav-links { margin-top: 10px; flex-wrap: wrap; justify-content: center; }
      .nav-links li { margin: 5px; }
      #content-area { padding: 30px 20px; }
      #content-area h1 { font-size: 36px; }
      #content-area p { font-size: 18px; }
      .btn { font-size: 16px; padding: 12px 25px; }
    }
  </style>
</head>
<body>
  <header>
    <div class="container">
      <nav>
        <div class="logo">Voyage en Chine</div>
        <ul class="nav-links">
          <li><a onclick="loadPage('home')">Accueil</a></li>
          <li><a onclick="loadPage('destination')">Destinations</a></li>
          <li><a onclick="loadPage('culture')">Culture</a></li>
          <li><a onclick="loadPage('conseils')">Conseils</a></li>
          <li><a onclick="loadPage('contact')">Contact</a></li>
        </ul>
      </nav>
    </div>
  </header>

  <div class="container">
    <div id="content-area">
      <h1>Découvrez la Chine</h1>
      <p>Un pays aux mille visages, riche en histoire et en paysages spectaculaires.<br>
         Explorez la culture millénaire et les merveilles naturelles de la Chine.</p>
      <a href="https://fr.wikipedia.org/wiki/Chine" target="_blank" class="btn">Commencer l'aventure</a>
    </div>
  </div>

  <footer>
    <p>&copy; 2025 FU Qiang.</p>
  </footer>

  <script>
    const contentArea = document.getElementById('content-area');

    const pages = {
      home: `
        <h1>Découvrez la Chine</h1>
        <p>Un pays aux mille visages, riche en histoire et en paysages spectaculaires.<br>
        Explorez la culture millénaire et les merveilles naturelles de la Chine.</p>
        <a href="https://fr.wikipedia.org/wiki/Chine" target="_blank" class="btn">Commencer l'aventure</a>
      `,
      destination: `
        <h1>Destinations</h1>
        <p>De la Grande Muraille aux rizières en terrasses, découvrez les sites incontournables de la Chine.</p>
      `,
      culture: `
        <h1>Culture</h1>
        <p>Plongez dans les traditions, la gastronomie et les festivals chinois.</p>
      `,
      conseils: `
        <h1>Conseils</h1>
        <p>Informations pratiques pour voyager en toute sérénité en Chine.</p>
      `,
      contact: `
        <h1>Contact</h1>
        <p>Pour toute question ou réservation, contactez-nous via notre formulaire.</p>
      `
    };

    function loadPage(page) {
      if(!pages[page]) return;
      contentArea.style.opacity = 0; // fade out
      setTimeout(() => {
        contentArea.innerHTML = pages[page];
        contentArea.style.opacity = 1; // fade in
      }, 200);
      window.scrollTo({ top: 0, behavior: 'smooth' });
    }
  </script>
</body>
</html>
