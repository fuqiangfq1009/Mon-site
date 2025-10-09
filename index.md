<script src="https://cdn.jsdelivr.net/npm/marked/marked.min.js"></script>
<script>
  async function loadPage(page) {
    const content = document.getElementById('content-area');
    content.innerHTML = "<p style='text-align:center; color:#777;'>Chargement...</p>";
    try {
      const res = await fetch(page);
      if (!res.ok) throw new Error("Erreur " + res.status);
      const md = await res.text();
      content.innerHTML = marked.parse(md);
    } catch (err) {
      content.innerHTML = "<p style='color:red;'>Impossible de charger : " + err.message + "</p>";
    }
  }
</script>
