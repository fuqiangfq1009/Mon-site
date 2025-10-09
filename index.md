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
                    <li><a href="#" onclick="loadInitialContent()">Accueil</a></li>
          <li><a href="#" onclick="loadPage('destination.html')">Destinations</a></li>
          <li><a href="#" onclick="loadPage('culture.html')">Culture</a></li>
          <li><a href="#" onclick="loadPage('conseils.html')">Conseils</a></li>
          <li><a href="#" onclick="loadPage('contact.html')">Contact</a></li>
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
    // 2. Fonction pour charger le contenu des autres pages
    function loadPage(page) {
      const content = document.getElementById('content-area');
      content.innerHTML = "<p style='text-align:center; color:#777;'>Chargement...</p>";
      // 3. Mise à jour du titre de l'onglet (pour corriger "Mon site" s'il y était)
      document.title = 'Voyage en Chine - ' + page.replace('.html', '').charAt(0).toUpperCase() + page.replace('.html', '').slice(1);

      fetch(page)
        .then(res => {
          if (!res.ok) throw new Error("Erreur " + res.status);
          return res.text();
        })
        .then(html => {
          content.innerHTML = html;
          // Appliquer les styles après le chargement
          applyContentStyles(content);
        })
        .catch(err => {
          content.innerHTML = "<p style='color:red;'>Impossible de charger : " + err.message + " (Vérifiez si " + page + " existe)</p>";
          document.title = 'Voyage en Chine - Erreur';
        });
    }

    // Contenu HTML initial de la page d'accueil (pour éviter l'effet '套娃')
    const initialContentHTML = `
      <h1>Découvrez la Chine</h1>
      <p>Un pays aux mille visages, riche en histoire et en paysages spectaculaires.<br>
         Explorez la culture millénaire et les merveilles naturelles de la Chine.</p>
      <a href="https://fr.wikipedia.org/wiki/Chine" target="_blank" class="btn">Commencer l'aventure</a>
    `;
    
    // 2. Nouvelle fonction pour revenir au contenu initial de la page d'accueil
    function loadInitialContent() {
      const content = document.getElementById('content-area');
      content.innerHTML = initialContentHTML;
      applyContentStyles(content);
      document.title = 'Voyage en Chine - Découvrez la Chine'; // Réinitialiser le titre
    }

    // Fonction utilitaire pour appliquer les styles
    function applyContentStyles(content) {
      content.style.background = "#fff";
      content.style.borderRadius = "8px";
      content.style.padding = "40px 30px";
      content.style.boxShadow = "0 4px 15px rgba(0,0,0,0.1)";
      content.style.textAlign = "center";
    }
  </script>
</body>
</html>
