
<html lang="pt-BR">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Nckzxz | Portfólio</title>
  <link href="https://fonts.googleapis.com/css2?family=Inter:wght@400;600;800&display=swap" rel="stylesheet" />
  <style>
    * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
      font-family: 'Inter', sans-serif;
    }
    html {
      scroll-behavior: smooth;
    }
    body {
      background-color: #0f0f0f;
      color: #ffffff;
      line-height: 1.6;
    }
    /* Cabeçalho */
    header {
      display: flex;
      justify-content: space-between;
      align-items: center;
      padding: 2rem;
      background-color: #0f0f0f;
      position: sticky;
      top: 0;
      z-index: 999;
    }
    .logo {
      font-size: 2rem;
      font-weight: 800;
      color: #fff;
    }
    nav a {
      margin-left: 2rem;
      color: #ccc;
      text-decoration: none;
      font-weight: 500;
      transition: color 0.3s;
    }
    nav a:hover {
      color: #ff9800;
    }

    /* Responsividade */
    @media(max-width: 768px) {
      header {
        flex-direction: column;
        align-items: center;
      }
      nav {
        margin-top: 1rem;
      }
      .hero {
        padding: 2rem 1rem;
      }
      .portfolio img {
        max-width: 150px;
      }
    }

    /* Seção Hero */
    .hero {
      display: flex;
      flex-direction: column;
      align-items: flex-start;
      padding: 4rem 2rem;
    }
    .hero h1 {
      font-size: 2.5rem;
      font-weight: 800;
    }
    .hero span {
      font-size: 1.25rem;
      margin-top: 1rem;
      color: #ccc;
    }
    .hero button {
      margin-top: 2rem;
      padding: 0.75rem 1.5rem;
      background-color: #ff9800;
      border: none;
      border-radius: 8px;
      color: #0f0f0f;
      font-weight: bold;
      cursor: pointer;
      transition: background-color 0.3s;
    }
    .hero button:hover {
      background-color: #e68a00;
    }

    /* Seções gerais */
    section {
      padding: 3rem 2rem;
    }

    /* Sobre */
    .sobre {
      background-color: #1a1a1a;
      border-radius: 12px;
      padding: 2rem;
    }
    .sobre h2 {
      font-size: 2rem;
      margin-bottom: 1rem;
    }
    .sobre ul {
      margin-top: 1rem;
      list-style-type: disc;
      padding-left: 1.5rem;
    }

    /* Portfólio - Galeria de projetos */
    .portfolio h2 {
      margin-bottom: 1.5rem;
    }
    .galeria {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
      gap: 2rem;
    }
    .card {
      background-color: #222;
      border-radius: 12px;
      overflow: hidden;
      transition: transform 0.3s, box-shadow 0.3s;
    }
    .card:hover {
      transform: translateY(-5px);
      box-shadow: 0 4px 20px rgba(0,0,0,0.4);
    }
    .card img {
      width: 100%;
      display: block;
      max-height: 150px;
      object-fit: cover;
      transition: transform 0.3s;
    }
    .card:hover img {
      transform: scale(1.05);
    }
    .card h3 {
      margin: 1rem;
      font-size: 1.2rem;
    }
    .card p {
      margin: 0 1rem 1rem;
      font-size: 0.95rem;
      color: #ccc;
    }
    .card a {
      display: block;
      margin: 0 1rem 1rem;
      padding: 0.5rem 1rem;
      background-color: #ff9800;
      color: #000;
      text-align: center;
      border-radius: 8px;
      text-decoration: none;
      font-weight: bold;
      transition: background-color 0.3s;
    }
    .card a:hover {
      background-color: #e68a00;
    }

    /* Contato */
    .contato h2 {
      margin-bottom: 1.5rem;
    }
    .contato-buttons a {
      display: inline-block;
      margin-top: 1rem;
      margin-right: 1rem;
      padding: 0.75rem 1.5rem;
      background-color: #ff9800;
      color: #000;
      font-weight: bold;
      border-radius: 8px;
      text-decoration: none;
      transition: background-color 0.3s;
    }
    .contato-buttons a:hover {
      background-color: #e68a00;
    }

    /* Rodapé */
    footer {
      text-align: center;
      padding: 2rem;
      background-color: #0f0f0f;
      color: #777;
    }

    /* Modal de contato */
    .modal {
      display: none;
      position: fixed;
      z-index: 9999;
      top: 0;
      left: 0;
      width: 100%;
      height: 100%;
      background: rgba(0,0,0,0.7);
      justify-content: center;
      align-items: center;
    }
    .modal-content {
      background-color: #222;
      padding: 2rem;
      border-radius: 12px;
      max-width: 500px;
      width: 90%;
      position: relative;
    }
    .modal-close {
      position: absolute;
      top: 10px;
      right: 15px;
      font-size: 1.5rem;
      cursor: pointer;
      color: #ccc;
    }
    .modal-content h3 {
      margin-bottom: 1rem;
    }
    .modal-content form {
      display: flex;
      flex-direction: column;
    }
    .modal-content input,
    .modal-content textarea {
      padding: 1rem;
      margin-bottom: 1rem;
      border: none;
      border-radius: 8px;
      background-color: #1f1f1f;
      color: #fff;
    }
    .modal-content button {
      padding: 0.75rem;
      border: none;
      border-radius: 8px;
      background-color: #ff9800;
      color: #000;
      font-weight: bold;
      cursor: pointer;
      transition: background-color 0.3s;
    }
    .modal-content button:hover {
      background-color: #e68a00;
    }
  </style>
</head>
<body>
  <header>
    <div class="logo">Nckzxz</div>
    <nav>
      <a href="#sobre">Sobre</a>
      <a href="#portfolio">Portfólio</a>
      <a href="#contato">Contato</a>
      <a href="#" onclick="abrirModal()">Fale comigo</a>
    </nav>
  </header>

  <section class="hero">
    <h1>Programador e Gerente de Sistemas</h1>
    <span>Transformando ideias em soluções eficientes.</span>
    <button onclick="scrollToPortfolio()">Ver Projetos em Breve</button>
  </section>

  <section id="sobre" class="sobre">
    <h2>Sobre Mim</h2>
    <p>Sou um profissional apaixonado por tecnologia, com experiência em desenvolvimento de software e gerenciamento de sistemas complexos. Busco sempre entregar soluções que unem desempenho, segurança e inovação.</p>
    <ul>
      <li>Desenvolvimento fullstack</li>
      <li>Gerência de servidores e banco de dados</li>
      <li>Automação de processos e integração de sistemas</li>
    </ul>
  </section>

  <section id="portfolio" class="portfolio">
    <h2>Portfólio</h2>
    <div class="galeria">
      <!-- Exemplo de projeto -->
      <div class="card">
        <img src="https://images.unsplash.com/photo-1506744038136-46273834b3fb?ixlib=rb-4.0.3&auto=format&fit=crop&w=800&q=80" alt="Projeto 1" />
        <h3>Projeto 1</h3>
        <p>Descrição breve do projeto 1.</p>
        <a href="#" target="_blank">Ver projeto</a>
      </div>
      <!-- Adicione mais cards aqui -->
      <div class="card">
        <img src="https://images.unsplash.com/photo-1521747116042-5a810fda9664?ixlib=rb-4.0.3&auto=format&fit=crop&w=800&q=80" alt="Projeto 2" />
        <h3>Projeto 2</h3>
        <p>Descrição breve do projeto 2.</p>
        <a href="#" target="_blank">Ver projeto</a>
      </div>
    </div>
  </section>

  <section id="contato" class="contato">
    <h2>Contato</h2>
    <div class="contato-buttons">
      <a href="https://instagram.com/nckzxz" target="_blank">Instagram: @nckzxz</a>
      <a href="https://wa.me/5514998798097" target="_blank">WhatsApp</a>
    </div>
    <p style="margin-top: 2rem;">Quer enviar uma mensagem direta? Clique aqui para abrir o formulário:</p>
    <button onclick="abrirModal()">Fale comigo</button>
  </section>

  <footer>
    &copy; 2025 Nckzxz. Todos os direitos reservados.
  </footer>

  <!-- Modal de contato -->
  <div class="modal" id="modalContato">
    <div class="modal-content">
      <div class="modal-close" onclick="fecharModal()">&times;</div>
      <h3>Enviar mensagem</h3>
      <form id="formContato">
        <input type="text" placeholder="Seu nome" required />
        <input type="email" placeholder="Seu email" required />
        <textarea rows="4" placeholder="Sua mensagem" required></textarea>
        <button type="submit">Enviar</button>
      </form>
    </div>
  </div>

  <script>
    // Função para scroll suave até o portfólio
    function scrollToPortfolio() {
      document.getElementById('portfolio').scrollIntoView({ behavior: 'smooth' });
    }

    // Funções para abrir e fechar modal
    function abrirModal() {
      document.getElementById('modalContato').style.display = 'flex';
    }
    function fecharModal() {
      document.getElementById('modalContato').style.display = 'none';
    }
    // Fechar modal ao clicar fora
    window.onclick = function(event) {
      const modal = document.getElementById('modalContato');
      if (event.target == modal) {
        fecharModal();
      }
    };

    // Enviar formulário (exemplo)
    document.getElementById('formContato').addEventListener('submit', function(e) {
      e.preventDefault();
      alert('Mensagem enviada! Obrigado por entrar em contato.');
      fecharModal();
    });
  </script>
</body>
</html>
