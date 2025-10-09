<!doctype html>
<html lang="fr">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Voyage en Chine - Découvrez la Chine</title>
  <style>
    * { margin:0; padding:0; box-sizing:border-box; font-family: Arial, sans-serif; }
    body { background:#f5f5f5; color:#333; line-height:1.6; }
    .container { max-width:1200px; margin:0 auto; padding:0 15px; }
    header { background:#c00; color:#fff; padding:15px 0; }
    nav { display:flex; justify-content:space-between; align-items:center; }
    .logo { font-size:24px; font-weight:bold; }
    .nav-links { display:flex; list-style:none; }
    .nav-links li { margin-left:20px; }
    .nav-links a { color:white; text-decoration:none; padding:5px 10px; border-radius:3px; }
    .nav-links a:hover { background:#a00; }
    .nav-links a.active { background:#8b1a18; text-decoration:underline; }
    .hero { text-align:center; padding:60px 0; background:#fff; border-radius:5px; margin:30px 0; }
    .hero h1 { font-size:2.5em; margin-bottom:15px; color:#c00; }
    .hero p { font-size:1.2em; max-width:800px; margin:0 auto 30px; }
    .btn { display:inline-block; background:#c00; color:#fff; padding:12px 25px; border-radius:5px; text-decoration:none; font-weight:bold; }
    .btn:hover { background:#a23; }
    footer { background:#333; color:#fff; text-align:center; padding:20px 0; margin-top:30px; }

    /* 可滚动的内容区域（初始高度会由 JS 调整） */
    #content-area {
      background:#fff;
      border-radius:5px;
      padding:20px;
      margin:30px 0;
      overflow-y:auto;
      min-height:280px;
      height:500px; /* JS 会根据窗口自动调整高度 */
      box-shadow: 0 0 0 1px #eee;
    }

    @media (max-width:768px) {
      nav { flex-direction:column; align-items:flex-start; }
      .nav-links { margin-top:12px; flex-wrap:wrap; gap:8px; }
      .nav-links li { margin-left:0; }
      .hero { padding:30px 10px; }
    }
  </style>
</head>
<body>
  <header>
    <div class="container">
      <nav>
        <div class="logo">Voyage en Chine</div>
        <ul class="nav-links">
          <!-- 使用锚 hash，便于回退/收藏 -->
          <li><a class="nav-link" href="#accueil" data-title="Accueil">Accueil</a></li>
          <li><a class="nav-link" href="#destinations" data-title="Destinations">Destinations</a></li>
          <li><a class="nav-link" href="#culture" data-title="Culture">Culture</a></li>
          <li><a class="nav-link" href="#conseils" data-title="Conseils">Conseils</a></li>
          <li><a class="nav-link" href="#contact" data-title="Contact">Contact</a></li>
        </ul>
      </nav>
    </div>
  </header>

  <div class="container">
    <section class="hero">
      <h1>Découvrez la Chine</h1>
      <p>Un pays aux mille visages, riche en histoire et en paysages spectaculaires. Explorez la culture millénaire et les merveilles naturelles de la Chine.</p>
      <a href="https://fr.wikipedia.org/wiki/Chine" class="btn" target="_blank" rel="noopener">Commencer l'aventure</a>
    </section>

    <!-- 这是我们要把其他页面内容加载到的可滚动窗口 -->
    <div id="content-area">
      <p style="text-align:center; color:#777;">Bienvenue ! Cliquez sur le menu pour explorer la Chine.</p>
    </div>
  </div>

  <footer>
    <div class="container">© 2025 Voyage en Chine</div>
  </footer>

  <script>
    const contentArea = document.getElementById('content-area');
    const navLinks = document.querySelectorAll('.nav-link');

    // 根据 header + hero 高度动态计算 content-area 的高度（使其能占满剩余视窗高度）
    function adjustContentHeight(){
      const header = document.querySelector('header');
      const hero = document.querySelector('.hero');
      const used = header.offsetHeight + (hero ? hero.offsetHeight : 0) + 60; // 60 是容器上下间距的一个安全值
      const available = window.innerHeight - used;
      contentArea.style.height = (available > 250 ? available : 250) + 'px';
    }
    window.addEventListener('resize', adjustContentHeight);
    window.addEventListener('load', adjustContentHeight);

    // 设置导航激活样式
    function setActive(page){
      navLinks.forEach(a => {
        const href = a.getAttribute('href') || '';
        const name = href.startsWith('#') ? href.slice(1) : '';
        a.classList.toggle('active', name === page);
      });
    }

    // 加载片段 pages/{page}.html
    async function loadFragment(pageName){
      const url = `pages/${pageName}.html`;
      contentArea.innerHTML = '<p style="text-align:center; color:#777;">加载中...</p>';
      try {
        const res = await fetch(url);
        if (!res.ok) throw new Error('Erreur ' + res.status);
        const html = await res.text();
        contentArea.innerHTML = html;

        // 告诉外部页面：内容加载完成（方便在 index 中初始化 JS）
        document.dispatchEvent(new CustomEvent('contentLoaded', { detail: { page: pageName } }));
      } catch (err) {
        contentArea.innerHTML = `<p style="color:red;">无法加载内容：${err.message}</p>`;
      }
    }

    function route(){
      const hash = location.hash ? location.hash.slice(1) : 'accueil';
      setActive(hash);
      loadFragment(hash);
      const link = document.querySelector(`.nav-link[href="#${hash}"]`);
      if (link && link.dataset.title) {
        document.title = `${link.dataset.title} - Voyage en Chine`;
      } else {
        document.title = 'Voyage en Chine';
      }
    }

    window.addEventListener('hashchange', route);
    window.addEventListener('load', route);

    */
    function executeInlineScripts(container){
      const scripts = container.querySelectorAll('script');
      scripts.forEach(s => {
        const newScript = document.createElement('script');
        if (s.src) {
          newScript.src = s.src;
          newScript.async = false;
        } else {
          newScript.textContent = s.textContent;
        }
        document.body.appendChild(newScript);
        newScript.onload = () => newScript.remove();
        if (!s.src) newScript.remove();
      });
    }

   
  </script>
</body>
</html>
