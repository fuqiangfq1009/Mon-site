<!DOCTYPE html>
<html lang="fr">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Voyage en Chine - Découvrez la Chine</title>
  <style>
    * {
      margin: 0; padding: 0; box-sizing: border-box;
      font-family: Arial, sans-serif;
    }
    body {
      background-color: #f5f5f5;
      color: #333; line-height: 1.6;
    }
    .container {
      max-width: 1200px; margin: 0 auto; padding: 0 15px;
    }
    header {
      background-color: #c00; color: white; padding: 15px 0;
    }
    nav {
      display: flex; justify-content: space-between; align-items: center;
    }
    .logo {
      font-size: 24px; font-weight: bold;
    }
    .nav-links {
      display: flex; list-style: none;
    }
    .nav-links li {
      margin-left: 20px;
    }
    .nav-links a {
      color: white; text-decoration: none; padding: 5px 10px;
    }
    .nav-links a:hover {
      background-color: #a00; border-radius: 3px;
    }
    #content-area {
      background: #fff; border-radius: 5px;
      padding: 20px; margin: 30px 0;
      height: 500px; overflow-y: auto;
    }
    .btn {
      display: inline-block; background-color: #c00; color: white;
      padding: 12px 25px; border-radius: 5px;
      text-decoration: none; font-weight: bold;
    }
    .btn:hover {
      background-color: #a23;
    }
    footer {
      background-color: #333; color: white;
      text-align: center; padding: 20px 0; margin-top: 30px;
    }
    @media (max-width: 768px) {
      nav { flex-direction: column; }
      .nav-links { margin-top: 15px; }
      .nav-links li { margin: 0 10px; }
    }
  </style>
</head>
<body>
  <header>
    <div class="container">
      <nav>
        <div class="logo">Voyage en Chine</div>
        <ul class="nav-links">
          <li><a href="#" onclick="loadPage('accueil.html')">Accueil</a></li>
          <li><a href="#" onclick="loadPage('destinations.html')">Destinations</a></li>
          <li><a href="#" onclick="loadPage('culture.html')">Culture</a></li>
          <li><a href="#" onclick="loadPage('conseils.html')">Conseils</a></li>
          <li><a href="#" onclick="loadPage('contact.html')">Contact</a></li>
        </ul>
      </nav>
    </div>
  </header>

  <div class="container">
    <!-- 这里就是首页显示的可滚动区域 -->
    <div id="content-area">
      <h1 style="color:#c00; margin-bottom:15px;">Découvrez la Chine</h1>
      <p>Un pays aux mille visages, riche en histoire et en paysages spectaculaires. 
         Explorez la culture millénaire et les merveilles naturelles de la Chine.</p>
      <a href="https://fr.wikipedia.org/wiki/Chine" class="btn">Commencer l'aventure</a>
    </div>
  </div>

  <footer>
    <p>&copy; 2025 Voyage en Chine. Tous droits réservés.</p>
  </footer>

  <script>
    function loadPage(page) {
      const content = document.getElementById('content-area');
      content.innerHTML = "<p style='text-align:center; color:#777;'>Chargement...</p>";
      fetch(page)
        .then(res => {
          if (!res.ok) throw new Error("Erreur " + res.status);
          return res.text();
        })
        .then(html => { content.innerHTML = html; })
        .catch(err => {
          content.innerHTML = "<p style='color:red;'>Impossible de charger : " + err.message + "</p>";
        });
    }
  </script>
</body>
</html>
