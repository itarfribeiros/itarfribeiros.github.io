# itarfribeiros.github.io
<!doctype html>
<html lang="pt-BR">
<head>
  <meta charset="utf-8" />
  <meta name="viewport" content="width=device-width,initial-scale=1" />
  <title>Minha Loja - Catálogo</title>
  <meta name="description" content="Catálogo rápido da minha loja — toque e veja nosso Instagram, catálogo e contatos." />
  <style>
    :root{
      --bg:#f6f7fb;
      --card:#ffffff;
      --accent:#0f7a5b;
      --muted:#6b7280;
      --radius:14px;
      --maxw:760px;
      --shadow: 0 6px 20px rgba(16,24,40,0.08);
      font-family: Inter, system-ui, -apple-system, "Segoe UI", Roboto, "Helvetica Neue", Arial;
    }
    *{box-sizing:border-box}
    body{
      margin:0;
      background: linear-gradient(180deg, #f7fbf9, var(--bg));
      color:#111827;
      -webkit-font-smoothing:antialiased;
      -moz-osx-font-smoothing:grayscale;
      padding:24px;
      display:flex;
      justify-content:center;
      font-size:16px;
      line-height:1.45;
    }
    .wrap{
      width:100%;
      max-width:var(--maxw);
    }
    .card{
      background:var(--card);
      border-radius:var(--radius);
      box-shadow:var(--shadow);
      padding:20px;
      margin-bottom:18px;
    }
    header.sitehead{
      display:flex;
      gap:16px;
      align-items:center;
    }
    .logo{
      width:64px;
      height:64px;
      border-radius:12px;
      background:linear-gradient(180deg,#e6fff2,#dff8ee);
      display:flex;
      align-items:center;
      justify-content:center;
      font-weight:700;
      color:var(--accent);
      font-size:20px;
      flex-shrink:0;
    }
    h1{
      margin:0;
      font-size:20px;
      letter-spacing: -0.2px;
    }
    p.lead{margin:6px 0 0;color:var(--muted);font-size:14px}
    .urlbox{
      display:flex;
      gap:12px;
      align-items:center;
      background:linear-gradient(90deg,#ffffff,#fbfdff);
      border-radius:12px;
      padding:12px;
      margin-top:16px;
      border:1px solid #eef2f6;
    }
    .url-left{flex:1;display:flex;flex-direction:column;gap:6px}
    .url-title{font-weight:600;font-size:14px}
    .url-link{
      display:flex;
      gap:8px;
      align-items:center;
      color:var(--accent);
      font-weight:600;
      font-size:13px;
      text-decoration:none;
      word-break:break-all;
    }
    .btns{display:flex;gap:8px}
    .btn{
      border:0;
      padding:9px 12px;
      border-radius:10px;
      font-weight:600;
      cursor:pointer;
      background:var(--accent);
      color:white;
      box-shadow: 0 2px 8px rgba(15,122,91,0.18);
    }
    .btn.secondary{
      background:transparent;
      color:var(--accent);
      border:1px solid #e6f0ea;
      box-shadow:none;
      font-weight:600;
    }
    .info-grid{
      display:grid;
      grid-template-columns:1fr 1fr;
      gap:12px;
      margin-top:14px;
    }
    .info-item{background:#fbfdff;padding:12px;border-radius:10px;border:1px solid #eef3f8}
    .info-item h4{margin:0 0 6px;font-size:13px}
    .info-item p{margin:0;color:var(--muted);font-size:14px}
    footer.small{font-size:13px;color:var(--muted);text-align:center;margin-top:6px}
    /* mobile */
    @media (max-width:560px){
      .info-grid{grid-template-columns:1fr}
      .logo{width:56px;height:56px}
      body{padding:16px}
    }
    /* small helper (hidden input style copy feedback) */
    .copied{
      font-size:12px;color: #065f46; background:#ecfdf5;padding:6px 8px;border-radius:8px; display:inline-block;margin-left:8px;
    }
  </style>
</head>
<body>
  <div class="wrap">

    <!--
      EDITAR AQUI: bloco siteData abaixo.
      Substitua textos e links. Mantenha as aspas e vírgulas.
    -->
    <script>
      const siteData = {
        shopName: "Minha Loja Exemplo",
        subtitle: "Produtos artesanais • Entrega em todo o Brasil",
        instagram: "https://instagram.com/seu_usuario",   // coloque seu perfil
        instagramLabel: "@seu_usuario",
        catalogLink: "https://link.do.seu.catalogo",     // link para catálogo (opcional)
        phone: "+55 85 9XXXX-XXXX",
        address: "Rua Exemplo, 123, Bairro, Cidade - CE",
        hours: "Seg - Sex: 09:00 - 18:00",
        shortIntro: "Peças únicas feitas com carinho. Atendimento rápido via DM ou WhatsApp.",
        themeColor: "#0f7a5b"
      };
      document.documentElement.style.setProperty('--accent', siteData.themeColor);
    </script>

    <!-- === HEADER / TITLE === -->
    <div class="card sitehead" style="padding:16px 18px;">
      <div class="logo" id="logo">ML</div>
      <div>
        <h1 id="shopName">Minha Loja Exemplo</h1>
        <p class="lead" id="subtitle">Produtos artesanais • Entrega em todo o Brasil</p>
      </div>
    </div>

    <!-- === URL BOX (Instagram) === -->
    <div class="card">
      <div class="urlbox">
        <div class="url-left">
          <div class="url-title">Instagram</div>
          <a id="instalink" class="url-link" href="#" target="_blank" rel="noopener noreferrer">
            <span id="instaLabel">@seu_usuario</span>
          </a>
          <div style="margin-top:6px;color:var(--muted);font-size:13px" id="shortIntro">Peças únicas feitas com carinho.</div>
        </div>

        <div style="display:flex;flex-direction:column;align-items:flex-end;justify-content:center">
          <div class="btns">
            <button class="btn" id="openInsta">Abrir</button>
            <button class="btn secondary" id="copyInsta">Copiar</button>
          </div>
          <div id="copyFeedback" style="margin-top:8px;height:18px"></div>
        </div>
      </div>

      <!-- Informações rápidas -->
      <div class="info-grid" style="margin-top:14px">
        <div class="info-item">
          <h4>Catálogo</h4>
          <p id="catalogText">Link para o catálogo / loja</p>
        </div>
        <div class="info-item">
          <h4>Contato</h4>
          <p id="phoneText">Telefone: -</p>
        </div>
        <div class="info-item">
          <h4>Local</h4>
          <p id="addressText">Endereço</p>
        </div>
        <div class="info-item">
          <h4>Horário</h4>
          <p id="hoursText">Horário de funcionamento</p>
        </div>
      </div>
    </div>

    <!-- CTA card -->
    <div class="card" style="text-align:center">
      <p style="margin:0 0 12px 0;font-weight:600">Quer comprar agora?</p>
      <div style="display:flex;gap:8px;justify-content:center;flex-wrap:wrap">
        <a id="ctaCatalog" class="btn" href="#" target="_blank" style="text-decoration:none">Ver Catálogo</a>
        <a id="ctaWhats" class="btn secondary" href="#" target="_blank" style="text-decoration:none;color:var(--accent)">Enviar WhatsApp</a>
      </div>
    </div>

    <div class="card" style="text-align:center">
      <footer class="small">Toque na tag NFC para abrir esta página. Atualize as informações editando o arquivo <code>index.html</code>.</footer>
    </div>
  </div>

  <script>
    // Inicializa elementos com dados do siteData
    (function(){
      const s = window.siteData || {};
      document.getElementById('shopName').innerText = s.shopName || 'Minha Loja';
      document.getElementById('subtitle').innerText = s.subtitle || '';
      document.getElementById('instalink').href = s.instagram || '#';
      document.getElementById('instaLabel').innerText = s.instagramLabel || s.instagram || '@perfil';
      document.getElementById('shortIntro').innerText = s.shortIntro || '';
      document.getElementById('catalogText').innerText = s.catalogLink ? s.catalogLink : 'Sem link de catálogo definido.';
      document.getElementById('phoneText').innerText = s.phone ? s.phone : 'Não informado';
      document.getElementById('addressText').innerText = s.address ? s.address : 'Não informado';
      document.getElementById('hoursText').innerText = s.hours ? s.hours : 'Não informado';
      document.getElementById('ctaCatalog').href = s.catalogLink || '#';
      // WhatsApp quick link (preenche mensagem)
      let phoneForLink = (s.phone || '').replace(/\D/g,'');
      if(phoneForLink) {
        document.getElementById('ctaWhats').href = 'https://wa.me/' + phoneForLink + '?text=' + encodeURIComponent('Olá! Vi sua tag NFC e quero mais informações sobre a loja.');
      } else {
        document.getElementById('ctaWhats').style.display = 'none';
      }
      // Logo initials
      const initials = (s.shopName || 'Minha Loja').split(' ').map(w => w[0]).slice(0,2).join('').toUpperCase();
      document.getElementById('logo').innerText = initials;
    })();

    // Botões: abrir e copiar
    document.getElementById('openInsta').addEventListener('click', function(){
      const href = document.getElementById('instalink').href;
      window.open(href, '_blank');
    });
    document.getElementById('copyInsta').addEventListener('click', function(){
      const href = document.getElementById('instalink').href;
      navigator.clipboard.writeText(href).then(function(){
        const f = document.getElementById('copyFeedback');
        f.innerHTML = '<span class="copied">Copiado!</span>';
        setTimeout(()=> f.innerHTML='',1500);
      }).catch(()=> {
        alert('Não foi possível copiar — copie manualmente: ' + href);
      });
    });

    // Faz a página ficar responsiva ao abrir de NFC (opcional)
    if ('standalone' in navigator && navigator.standalone) {
      // nothing for now
    }
  </script>
</body>
</html>
