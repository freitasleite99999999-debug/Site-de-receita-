<!DOCTYPE html>  <html lang="pt-BR">    <head>    
<meta charset="UTF-8" />    
<meta name="viewport" content="width=device-width,initial-scale=1.0"/>    
<title>Site de Receitas</title>    
<style>    
  /* --- Fundo e texto --- */    
  body{    
    margin:0;    
    font-family: Arial, sans-serif;    
    color:#fff;    
    background-image: url('https://images.unsplash.com/photo-1504674900247-0877df9cc836');    
    background-size: cover;    
    background-position: center;    
    background-repeat: no-repeat;    
    min-height:100vh;    
  }    
  /* overlay escuro para deixar o texto visível */    
  body::before{    
    content:"";    
    position:fixed;    
    inset:0;    
    background: rgba(0,0,0,0.55);    
    z-index:-1;    
  }  /* --- Layout centralizado --- */  
.container{  
width:92%;  
max-width: 1000px;  
margin: 0 auto;  
padding: 18px 12px 80px 12px;  
}  /* --- Navbar --- */
nav{
display:flex;
justify-content:center;
gap:20px;
padding:10px 0;
background: rgba(0,0,0,0.6);
border-bottom: 1px solid rgba(255,255,255,0.06);
position: sticky;
top: 0;
z-index: 5;
}
nav a{
color:#fff;
text-decoration:none;
font-weight:700;
padding:6px 10px;
border-radius:6px;
}
nav a:hover{ background: rgba(255,215,0,0.12); color:#ffd700; }

/* --- Cabeçalho --- */
header{ text-align:center; margin-top:12px; }
h1{ margin:6px 0; font-size:28px; letter-spacing:0.5px; }
p.lead{ margin:6px 0 14px 0; opacity:0.9; }

/* --- Categorias (linha) --- */
.cats{
display:flex;
justify-content:center;
gap:12px;
flex-wrap:wrap;
margin:6px 0 18px 0;
}
.cat{
background: rgba(255,255,255,0.06);
padding:8px 12px;
border-radius:20px;
font-weight:600;
}

/* --- Cards de receita (caixas) --- */
.grid{
display:grid;
grid-template-columns: repeat(auto-fit, minmax(260px, 1fr));
gap:16px;
margin-top:18px;
}
.card{
background: rgba(0,0,0,0.65);
border-radius:12px;
padding:14px;
box-shadow: 0 6px 20px rgba(0,0,0,0.4);
transform-origin: center;
animation: fadeUp .45s ease;
}

@keyframes fadeUp{
from{ opacity:0; transform: translateY(8px); }
to{ opacity:1; transform: translateY(0); }
}

.card h3{ margin:0 0 8px 0; }
.card ul{ margin:6px 0 8px 16px; }
.card ol{ margin:6px 0 8px 20px; }

/* --- Dica do Chef --- */
.chef{
background: linear-gradient(135deg, rgba(255,215,0,0.12), rgba(255,255,255,0.02));
border-left: 4px solid #ffd700;
padding:12px;
border-radius:8px;
margin-top:8px;
color:#fff;
}

/* --- Tabela nutricional --- */
.nutri{
margin: 20px auto;
background: rgba(0,0,0,0.65);
padding:12px;
border-radius:10px;
max-width:520px;
}
table{ width:100%; border-collapse:collapse; color:#fff; }
th, td{ padding:8px 10px; text-align:left; border-bottom: 1px solid rgba(255,255,255,0.05); }
th{ font-weight:700; }

/* --- Sobre --- */
#sobre{ margin-top:18px; background: rgba(0,0,0,0.6); padding:12px; border-radius:10px; }

/* --- Botão voltar ao topo --- */
#topo{
position:fixed;
right:14px;
bottom:14px;
background:#ffd700;
color:#000;
padding:10px 12px;
border-radius:10px;
text-decoration:none;
font-weight:700;
box-shadow: 0 6px 18px rgba(0,0,0,0.35);
z-index:10;
}

/* --- Responsivo --- */
@media (max-width:420px){
h1{ font-size:22px; }
nav{ gap:10px; padding:8px 0; }
.card{ padding:12px; }
}

</style>    
</head>    
<body>    
  <div class="container">    
    <!-- NAV -->    
    <nav>    
      <a href="#inicio">Início</a>    
      <a href="#receitas">Receitas</a>    
      <a href="#sobre">Sobre</a>    
    </nav>  <!-- HEADER -->    
<header id="inicio">    
  <h1>🍽️ Site de Receitas</h1>    
  <p class="lead">Receitas simples e rápidas — criado enquanto aprendo programação.</p>      <div class="cats" aria-hidden="true">    
    <span class="cat">🍳 Ovos</span>    
    <span class="cat">🍝 Massas</span>    
    <span class="cat">🍚 Arroz</span>    
    <span class="cat">🥘 Feijão</span>    
  </div>      <p id="data" style="opacity:0.9"></p>    
</header>    <!-- RECEITAS -->    <section id="receitas" class="grid">    
  <article class="card">    
    <h3>🍳 Omelete Rápido</h3>    
    <p><strong>Ingredientes:</strong></p>    
    <ul>    
      <li>2 ovos</li>    
      <li>Sal a gosto</li>    
      <li>1 colher de manteiga</li>    
      <li>Queijo (opcional)</li>    
    </ul>    
    <p><strong>Modo de preparo:</strong></p>    
    <ol>    
      <li>Bata os ovos.</li>    
      <li>Aqueça a manteiga e despeje os ovos.</li>    
      <li>Dobre e sirva.</li>    
    </ol>    
    <div class="chef"><strong>💡 Dica do Chef:</strong> adicione orégano ou cebolinha para mais sabor.</div>    
  </article>      <article class="card">    
    <h3>🍝 Macarrão Simples</h3>    
    <p><strong>Ingredientes:</strong></p>    
    <ul>    
      <li>250g de macarrão</li>    
      <li>Molho de tomate</li>    
      <li>Alho</li>    
    </ul>    
    <p><strong>Modo de preparo:</strong></p>    
    <ol>    
      <li>Cozinhe o macarrão conforme embalagem.</li>    
      <li>Refogue o alho e aqueça o molho.</li>    
      <li>Misture e sirva com queijo.</li>    
    </ol>    
    <div class="chef"><strong>💡 Dica do Chef:</strong> reserve uma concha da água do cozimento para o molho.</div>    
  </article>      <article class="card">    
    <h3>🍚 Arroz Simples</h3>    
    <p><strong>Ingredientes:</strong></p>    
    <ul>    
      <li>1 xícara de arroz</li>    
      <li>2 xícaras de água</li>    
      <li>1 dente de alho</li>    
    </ul>    
    <p><strong>Modo de preparo:</strong></p>    
    <ol>    
      <li>Refogue o alho, junte o arroz.</li>    
      <li>Adicione água e sal.</li>    
      <li>Cozinhe até secar e deixe descansar.</li>    
    </ol>    
  </article>      <article class="card">    
    <h3>🥘 Feijão Simples</h3>    
    <p><strong>Ingredientes:</strong></p>    
    <ul>    
      <li>2 xícaras de feijão</li>    
      <li>Água</li>    
      <li>Alho</li>    
    </ul>    
    <p><strong>Modo de preparo:</strong></p>    
    <ol>    
      <li>Cozinhe na pressure por 20–25 min.</li>    
      <li>Refogue alho e adicione ao feijão.</li>    
      <li>Deixe engrossar o caldo.</li>    
    </ol>    
  </article>    
</section>    <!-- Tabela nutricional -->    <section class="nutri">    
  <h3 style="margin-top:0;">Tabela Nutricional</h3>    
  <table>    
    <tr><th>Comida</th><th>Calorias</th><th>Proteína</th></tr>    
    <tr><td>Ovo (1 un)</td><td>~70 kcal</td><td>6 g</td></tr>    
    <tr><td>Arroz (100g cozido)</td><td>~120 kcal</td><td>2 g</td></tr>    
    <tr><td>Feijão (100g cozido)</td><td>~90 kcal</td><td>6 g</td></tr>    
  </table>    
</section>    <!-- SOBRE -->    <section id="sobre" style="margin-top:18px;">    
  <div id="sobre" class="card">    
    <h3>Sobre o Site</h3>    
    <p>Este site foi criado enquanto aprendo HTML e CSS. Aqui reúno receitas simples e treino a criação de páginas. Tudo feito por mim — iniciante, mas com vontade de aprender!</p>    
    <p>Instagram: <a href="https://www.instagram.com/andrefreitas9898" target="_blank" style="color:#ffd700;">@andrefreitas9898</a></p>    
  </div>    
</section>    </div> <!-- /container -->    <!-- botão voltar ao topo -->  <a id="topo" href="#inicio">⬆ Topo</a>  <script>    
  // coloca data    
  const hoje = new Date();    
  document.getElementById('data').textContent = 'Data: ' + hoje.toLocaleDateString();    
    
  // smooth scroll (suaviza o clique nos links da navbar e topo)    
  document.querySelectorAll('nav a, #topo').forEach(el => {    
    el.addEventListener('click', function(e){    
      e.preventDefault();    
      const id = this.getAttribute('href').replace('#','');    
      const target = document.getElementById(id);    
      if(target) target.scrollIntoView({behavior:'smooth', block:'start'});    
    });    
  });    
</script>  </body>    </html>  Olha esse site que eu criei com sua ajuda
