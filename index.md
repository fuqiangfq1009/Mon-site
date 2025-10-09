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
      background-color: #c00; color: white; padding: 0;
    }
    nav {
      display: flex; justify-content: space-between; align-items: center;
      height: 60px; /* 固定导航栏高度 */
    }
    .logo {
      font-size: 24px; font-weight: bold;
    }
    .nav-links {
      display: flex; list-style: none; height: 100%; margin: 0; padding: 0;
    }
    .nav-links li {
      margin-left: 20px;
      display: flex;
      align-items: center; /* 垂直居中 li 内文字 */
    }
    .nav-links a {
      color: white; text-decoration: none;
      display: flex; align-items: center; height: 100%; /* 垂直居中 */
      padding: 0 10px; /* 左右间距 */
    }
    .nav-links a:hover {
      background-color: #a00; border-radius: 3px;
    }
    #content-area {
      background: #fff; border-radius: 5px;
      padding: 20px; margin: 30px 0;
      height: 500px; overflow-y: auto;
      text-align: center; /* 按钮居中 */
    }
    .btn {
      display: inline-block; background-color: #c00; color: white;
      padding: 12px 25px; border-radius: 5px;
      text-decoration: none; font-weight: bold;
      margin: 20px auto 0 auto;
      position: relative; z-index: 10;
    }
    .btn:hover {
      background-color: #a23;
    }
    footer {
      background-color: #333; color: white;
      text-align: center; padding: 20px 0; margin-top: 30px;
    }
    @media (max-width: 768px) {
      nav { flex-direction: column; height: auto; }
      .nav-links { margin-top: 15px; }
      .nav-links li { margin: 0 10px; }
      .logo { margin-bottom: 10px; }
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
          <li><a href="https://fuqiangfq1009.github.io/Mon-site/destination" target="_blank">Destinations</a></li>
          <li><a href="#" onclick="loadPage('culture.html')">Culture</a></li>
          <li><a href="#" onclick="loadPage('conseils.html')">Conseils</a></li>
          <li><a href="#" onclick="loadPage('contact.html')">Contact</a></li>
        </ul>
      </nav>
    </div>
  </header>

  <div class="container">
    <div id="content-area">
      <h1 style="color:#c00; margin-bottom:15px;">Découvrez la Chine</h1>
      <p>Un pays aux mille visages, riche en histoire et en paysages spectaculaires. 
         Explorez la culture millénaire et les merveilles naturelles de la Chine.</p>
      <a href="https://fr.wikipedia.org/wiki/Chine" target="_blank" class="btn">Commencer l'aventure</a>
    </div>
  </div>

  <footer>
    <p>&copy; 2025 FU Qiang.</p>
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
