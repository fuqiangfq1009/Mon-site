<html lang="fr">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Voyage en Chine - Découvrez la Chine</title>
<style>
* { margin:0; padding:0; box-sizing:border-box; font-family:'Segoe UI', Tahoma, Geneva, Verdana, sans-serif; }
body { background-color:#f5f5f5; color:#333; line-height:1.6; }
.container { max-width:1200px; margin:0 auto; padding:0 15px; }
header { background-color:#c00; color:white; position:sticky; top:0; z-index:1000; box-shadow:0 2px 5px rgba(0,0,0,0.2); }
nav { display:flex; justify-content:space-between; align-items:center; height:60px; padding:0 15px; }
.logo { font-size:28px; font-weight:bold; color:white; }
.nav-links { display:flex; list-style:none; height:100%; margin:0; padding:0; }
.nav-links li { margin-left:20px; display:flex; align-items:center; }
.nav-links a { color:white; text-decoration:none; display:flex; align-items:center; height:100%; padding:0 10px; font-weight:500; transition:background 0.3s; }
.nav-links a:hover { background-color:#a00; border-radius:3px; }

#content-area { background:#fff; border-radius:8px; padding:40px 30px; margin:30px 0; min-height:500px; box-shadow:0 4px 15px rgba(0,0,0,0.1); text-align:center; }
#content-area h1,h2,h3 { color:#c00; margin:20px 0; }
#content-area h1 { font-size:40px; }
#content-area h2 { font-size:32px; }
#content-area h3 { font-size:28px; }
#content-area p { font-size:18px; color:#444; margin-bottom:20px; line-height:1.8; }
#content-area a { color:#c00; text-decoration:none; }
#content-area a:hover { text-decoration:underline; }
#content-area img { max-width:100%; border-radius:8px; margin:15px 0; display:block; }
#content-area ul, #content-area ol { margin-left:20px; margin-bottom:20px; }
#content-area table { width:100%; border-collapse:collapse; margin:20px 0; }
#content-area table, #content-area th, #content-area td { border:1px solid #ccc; }
#content-area th, #content-area td { padding:10px; text-align:left; }
#content-area pre { background:#f0f0f0; padding:10px; border-radius:6px; overflow-x:auto; }
#content-area code { background:#f0f0f0; padding:2px 5px; border-radius:4px; }

/* 按钮居中 */
#content-area a.btn {
    display:block;
    margin:20px auto;
    background-color:#c00;
    color:white;
    padding:14px 30px;
    border-radius:6px;
    text-decoration:none;
    font-weight:bold;
    font-size:18px;
    text-align:center;
    width:max-content;
}
#content-area a.btn:hover {
    background-color:#a23;
    transform:translateY(-2px);
}

footer { background-color:#333; color:white; text-align:center; padding:20px 0; margin-top:30px; }

@media(max-width:768px) {
    nav { flex-direction:column; height:auto; }
    .nav-links { margin-top:10px; flex-wrap:wrap; justify-content:center; }
    .nav-links li { margin:5px; }
    #content-area { padding:30px 20px; }
    #content-area h1 { font-size:32px; }
    #content-area h2 { font-size:28px; }
    #content-area h3 { font-size:24px; }
    #content-area p { font-size:16px; }
    #content-area a.btn { font-size:16px; padding:12px 25px; }
}
</style>
</head>
<body>

<header>
<div class="container">
<nav>
<div class="logo">Voyage en Chine</div>
<ul class="nav-links">
<li><a href="#" onclick="loadPage('accueil.md')">Accueil</a></li>
<li><a href="#" onclick="loadPage('destination.md')">Destinations</a></li>
<li><a href="#" onclick="loadPage('culture.md')">Culture</a></li>
<li><a href="#" onclick="loadPage('conseils.md')">Conseils</a></li>
<li><a href="#" onclick="loadPage('contact.md')">Contact</a></li>
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

<!-- marked.js -->
<script src="https://cdn.jsdelivr.net/npm/marked/marked.min.js"></script>
<script>
function loadPage(page) {
  const content = document.getElementById('content-area');

  // Accueil 单独处理，不请求文件
  if(page === 'accueil.md') {
    content.innerHTML = `
      <h1>Découvrez la Chine</h1>
      <p>Un pays aux mille visages, riche en histoire et en paysages spectaculaires.<br>
      Explorez la culture millénaire et les merveilles naturelles de la Chine.</p>
      <a href="https://fr.wikipedia.org/wiki/Chine" target="_blank" class="btn">Commencer l'aventure</a>
    `;
    window.scrollTo({ top:0, behavior:'smooth' });
    return;
  }

  content.innerHTML = "<p style='text-align:center; color:#777;'>Chargement...</p>";

  fetch(page)
    .then(res => {
      if(!res.ok) throw new Error("Erreur " + res.status);
      return res.text();
    })
    .then(md => {
      content.innerHTML = marked.parse(md);
      window.scrollTo({ top:0, behavior:'smooth' });
    })
    .catch(err => {
      content.innerHTML = "<p style='color:red;'>Impossible de charger : " + err.message + "</p>";
    });
}
</script>
</body>
</html>
