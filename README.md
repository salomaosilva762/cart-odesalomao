<!DOCTYPE html>

<html lang="pt-br">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1">


<title>Meu servidor mano</title>

<style>
  :root {
    
    --cor: #6c5ce7;

    --fundo: #0f1020;
    --cartao: #1a1b2e;
    --texto: #e8e8f0;
    --suave: #9a9bb5;
  }
  * { box-sizing: border-box; margin: 0; padding: 0; }
  body {
    font-family: "Segoe UI", system-ui, -apple-system, Roboto, Arial, sans-serif;
    background: var(--fundo);
    background-image:
      radial-gradient(circle at 15% 10%, color-mix(in srgb, var(--cor) 35%, transparent), transparent 40%),
      radial-gradient(circle at 85% 90%, color-mix(in srgb, var(--cor) 25%, transparent), transparent 40%);
    background-attachment: fixed;
    color: var(--texto);
    line-height: 1.6;
    padding: 24px 16px 40px;
  }
  .container { max-width: 880px; margin: 0 auto; display: grid; gap: 20px; }

 
  .hero {
    background: var(--cartao);
    border: 1px solid #ffffff14;
    border-radius: 20px;
    padding: 32px 24px;
    text-align: center;
    position: relative;
    overflow: hidden;
  }
  .hero::before {
    content: ""; position: absolute; inset: 0 0 auto 0; height: 6px;
    background: linear-gradient(90deg, var(--cor), #ffffff88, var(--cor));
  }
  .avatar {
    width: 120px; height: 120px; border-radius: 50%;
    margin: 0 auto 16px;
    display: grid; place-items: center;
    font-size: 44px; font-weight: 800; color: #fff;
    background: linear-gradient(135deg, var(--cor), #000000aa);
    box-shadow: 0 0 0 6px #ffffff10, 0 0 40px color-mix(in srgb, var(--cor) 60%, transparent);
    overflow: hidden;
  }
  .avatar img { width: 100%; height: 100%; object-fit: cover; }
  h1 { font-size: clamp(28px, 6vw, 42px); line-height: 1.2; }
  .subtitulo { color: var(--suave); margin-top: 6px; font-size: 18px; }
  .badges { display: flex; flex-wrap: wrap; justify-content: center; gap: 8px; margin-top: 18px; }
  .badge {
    padding: 6px 14px; border-radius: 999px; font-size: 14px;
    background: color-mix(in srgb, var(--cor) 20%, transparent);
    border: 1px solid color-mix(in srgb, var(--cor) 50%, transparent);
  }

  
  .grid { display: grid; grid-template-columns: repeat(auto-fit, minmax(260px, 1fr)); gap: 20px; }
  .card {
    background: var(--cartao);
    border: 1px solid #ffffff14;
    border-radius: 16px;
    padding: 22px;
    transition: transform .2s, border-color .2s;
  }
  .card:hover { transform: translateY(-3px); border-color: var(--cor); }
  .card h2 { font-size: 18px; margin-bottom: 12px; display: flex; align-items: center; gap: 8px; }
  .card h2::before { content: ""; width: 10px; height: 10px; border-radius: 3px; background: var(--cor); }
  .card p { color: #cfd0e0; }

  .chips { display: flex; flex-wrap: wrap; gap: 8px; list-style: none; }
  .chips li {
    padding: 6px 12px; border-radius: 8px; font-size: 14px;
    background: #ffffff0d; border: 1px solid #ffffff1a;
  }

  .curiosidades { list-style: none; display: grid; gap: 10px; }
  .curiosidades li { display: flex; gap: 10px; align-items: baseline; }
  .curiosidades b { color: var(--suave); font-weight: 600; min-width: 110px; font-size: 14px; }

  .contatos { display: flex; flex-wrap: wrap; gap: 10px; }
  .contatos a {
    flex: 1 1 140px; text-align: center; text-decoration: none; color: #fff;
    padding: 10px 14px; border-radius: 10px; font-weight: 600;
    background: var(--cor);
    transition: filter .2s;
  }
  .contatos a:hover { filter: brightness(1.2); }

  
  .terminal {
    background: #05060c; border-radius: 14px; overflow: hidden;
    border: 1px solid #ffffff1a; font-family: Consolas, "Courier New", monospace; font-size: 14px;
  }
  .terminal .barra { background: #1d1e2c; padding: 10px 14px; display: flex; gap: 6px; align-items: center; }
  .terminal .barra span { width: 12px; height: 12px; border-radius: 50%; }
  .terminal .barra small { margin-left: 10px; color: var(--suave); font-family: inherit; }
  .terminal pre { padding: 16px; color: #b8f5c8; white-space: pre-wrap; word-break: break-word; min-height: 190px; }
  .terminal .ok { color: #55efc4; font-weight: bold; }
  .terminal .prompt { color: var(--cor); filter: brightness(1.4); }
  .cursor { display: inline-block; width: 8px; background: #b8f5c8; animation: pisca 1s steps(1) infinite; }
  @keyframes pisca { 50% { opacity: 0; } }

  footer { text-align: center; color: var(--suave); font-size: 14px; margin-top: 8px; }
  footer .online { display: inline-flex; align-items: center; gap: 6px; }
  footer .online::before {
    content: ""; width: 8px; height: 8px; border-radius: 50%; background: #00e676;
    box-shadow: 0 0 8px #00e676; animation: pisca 2s infinite;
  }
</style>
</head>
<body>
<div class="container">

  
  <header class="hero">
    <!-- ✏️ DESAFIO 1: troque "SN" pelas suas iniciais
         ✏️ BÔNUS: para usar uma foto, apague SN e coloque:
         <img src="https://github.com/SEU_USUARIO_GITHUB.png" alt="Minha foto"> -->
    <div class="avatar">SN</div>

    <!-- ✏️ DESAFIO 1: o seu nome completo -->
    <h1>SALOMAO SILVA DE JESUS</h1>

    <!-- ✏️ uma frase sobre você -->
    <p class="subtitulo">Futuro  administrador de servidores em nuvem ☁️</p>

    <div class="badges">
      <!-- ✏️ curso, período e cidade -->
      <span class="badge">🎓 Curso:sistemas para internet </span>
      <span class="badge">📅 Período: 2º</span>
      <span class="badge">📍 Cidade - AP </span>
    </div>
  </header>

  <div class="grid">
    
    <section class="card">
      <h2>Sobre mim</h2>
      <!-- ✏️ DESAFIO 3: escreva de 2 a 3 frases sobre você -->
      <p>
      sou o Salomão silva de jesus.sou de santana vila de anauerapu, gosoto de toca bateria,violão.gosto da da natureza.
      </p>
    </section>

  
    <section class="card">
      <h2>Habilidades</h2>
   
      <ul class="chips">
        <li>🐧 Linux</li>
        <li>🔐 SSH</li>
        <li>🌐 Nginx</li>
        <li>🧱 HTML</li>
        <li>🎨 CSS</li>
        <li>☁️ Cloud</li>
      </ul>
    </section>

   
    <section class="card">
      <h2>Curiosidades</h2>
      <!-- ✏️ DESAFIO 5: preencha com as suas preferências -->
      <ul class="curiosidades">
        <li><b>🍕 Comida</b> <span>mapará com açai</span></li>
        <li><b>🎬 Série/Filme</b> <span>dia do chacal</span></li>
        <li><b>🎵 Música</b> <span>banda H7</span></li>
        <li><b>⚽ Time</b> <span>pra quem tiver ganhando </span></li>
        <li><b>🎮 Hobby</b> <span>ganha dinheiro </span></li>
      </ul>
    </section>

   
    <section class="card">
      <h2>Meu objetivo na TI</h2>
     
      <p>
        Quero trabalhar com infraestrutura e computação em nuvem, ajudando empresas
        a manter os seus sistemas sempre no ar.ser um empresario de empresas de onibos,e de alugamento de imoveis. 🚀
      </p>
    </section>
  </div>

 
  <section class="card">
    <h2>Contato</h2>
    <!-- ✏️ DESAFIO 7: coloque os seus links (troque o que está entre aspas no href) -->
    <div class="contatos">
      <a href="https://github.com/" target="_blank">isntagram</a>
      <a href="https://www.linkedin.com/" target="_blank">wsatsapp</a>
      <a href="https://www.instagram.com/" target="_blank">tik tok </a>
    </div>
  </section>

  <!-- ================= STATUS DO SERVIDOR (não precisa editar) ================= -->
  <section class="terminal" aria-label="Status do servidor">
    <div class="barra">
      <span style="background:#ff5f57"></span><span style="background:#febc2e"></span><span style="background:#28c840"></span>
      <small id="titulo-terminal">ssh</small>
    </div>
    <pre id="saida"></pre>
  </section>

  <footer>
    <p class="online">Servidor online • Administração de Servidores em Nuvem • 2026</p>
  </footer>
</div>

<script>
  // Informações reais da conexão, preenchidas automaticamente pelo navegador
  const usuario = (location.pathname.match(/~([^/]+)/) || [, "aluno"])[1];
  const host = location.hostname || "localhost";
  const agora = new Date().toLocaleString("pt-BR");
  document.getElementById("titulo-terminal").textContent = usuario + "@" + host;

  const linhas = [
    ['<span class="prompt">' + usuario + '@servidor:~$</span> ', 'whoami'],
    ['', usuario],
    ['<span class="prompt">' + usuario + '@servidor:~$</span> ', 'systemctl status nginx'],
    ['', '● nginx.service - A high performance web server\n   Active: <span class="ok">active (running)</span>'],
    ['<span class="prompt">' + usuario + '@servidor:~$</span> ', 'echo "Acesso em $(date)"'],
    ['', 'Endereço: ' + location.protocol + '//' + host + (location.port ? ':' + location.port : '') + location.pathname +
         '\nAcesso em: ' + agora],
    ['<span class="prompt">' + usuario + '@servidor:~$</span> ', '']
  ];

  const saida = document.getElementById("saida");
  let html = "";
  let l = 0;

  function proxima() {
    if (l >= linhas.length) { saida.innerHTML = html + '<span class="cursor">&nbsp;</span>'; return; }
    const [prefixo, texto] = linhas[l];
    const ehComando = prefixo !== "";
    html += prefixo;
    if (!ehComando) {               // resposta do "servidor": aparece de uma vez
      html += texto + "\n";
      saida.innerHTML = html;
      l++; setTimeout(proxima, 350);
      return;
    }
    let c = 0;                      // comando: efeito de digitação
    (function digita() {
      saida.innerHTML = html + texto.slice(0, c) + '<span class="cursor">&nbsp;</span>';
      if (c++ < texto.length) { setTimeout(digita, 55); }
      else { html += texto + (texto ? "\n" : ""); l++; setTimeout(proxima, 300); }
    })();
  }
  proxima();
</script>
</body>
</html>
