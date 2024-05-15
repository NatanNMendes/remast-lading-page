# Index.HTML

Este código HTML descreve a estrutura de uma página web para a empresa Remast Consultoria em Gestão Empresarial. A seguir, explico cada parte do código:

## Cabeçalho (`<head>`)

- **Metadados e configurações básicas**:

~~~html
<meta charset="UTF-8" />
<meta http-equiv="X-UA-Compatible" content="IE=edge" />
<meta name="viewport" content="width=device-width, initial-scale=1.0" />
~~~

Esses elementos garantem que a página tenha a codificação de caracteres correta (UTF-8), seja compatível com diferentes versões do Internet Explorer, e seja responsiva para diferentes tamanhos de tela.

- **Título e links para recursos externos**:

~~~html
<title>Remast</title>
<link rel="stylesheet" href="style.css" />
<link rel="icon" href="assets/logo/favicon/favicon-16x16.png" type="image/x-icon">
~~~

Define o título da página, inclui um link para o arquivo CSS externo para estilos, e especifica um favicon.

## Corpo (`<body>`)

### Cabeçalho e Navegação (`<header>`)

- **Barra de navegação**:

~~~html
<nav class="nav">
  <div class="logo">
    <img class="logo-image" src="assets/logo/remast-logo_1.png" alt="logo-image">
    <a class="logo-text" href="/">Remast Consultoria</a>
  </div>
  <div class="mobile-menu">
    <div class="line1"></div>
    <div class="line2"></div>
    <div class="line3"></div>
  </div>
  <ul class="nav-list">
    <li><a class="nav-link" href="#banner">HOME</a></li>
    <li><a class="nav-link" href="#who-we-are">QUEM SOMOS</a></li>
    <li><a class="nav-link" href="#our-services">NOSSOS SERVIÇOS</a></li>
    <li><a class="nav-link" href="#how-we-do">COMO FAZEMOS</a></li>
    <li><a class="nav-link" href="#contact">CONTATO</a></li>
  </ul>
</nav>
~~~

Contém o logotipo, o nome da empresa, um menu de navegação para dispositivos móveis, e uma lista de links para diferentes seções da página.

### Seções da Página (`<section>`)

- **Banner**:

~~~html
<section class="banner" id="banner">
  <p class="banner-text">Transforme desafios em oportunidades com a Remast Consultoria em Gestão Empresarial. Consulte-nos e impulsione seu negócio</p>
</section>
~~~

Uma seção de destaque com um texto promocional.

- **Quem Somos:**:

~~~html
<section class="section" id="who-we-are">
  <h1 class="title">Remast Consultoria em Gestão Empresarial</h1>
  <div class="double-column">
    <p class="text">Somos uma empresa jovem e inovadora localizada em Dias D'Ávila-BA, comprometida em oferecer soluções inteligentes e econômicas para gestão empresarial. Desde 2015, ajudamos nossos clientes a crescerem de forma consciente e integrada, promovendo mudanças positivas em seus negócios.</p>
    <img src="assets/image/remast-1 1.png" alt="" class="image">
  </div>
</section>
~~~

Apresenta a empresa, incluindo um texto descritivo e uma imagem.

- **Nossos Serviços:**:

~~~html
<section class="section" id="our-services">
  <h5 class="title">Nossos Serviços</h5>
  <div class="card-group">
    <div class="card-model">
      <img src="assets/vetores/combo-chart.png" alt="combo-chart" class="card-vector">
      <div class="card-body">
        <h6 class="card-title">Consultoria em Gestão</h6>
        <p class="card-text">Oferecemos serviços de consultoria em gestão empresarial, ajudando nossos clientes a alcançarem seus objetivos e superarem desafios.</p>
      </div>
    </div>
    <!-- Outras cartas de serviços -->
  </div>
</section>
~~~

Descreve os serviços oferecidos pela empresa, usando um formato de cartão com imagem e texto.

- **Por Que Contratar uma Consultoria?:**:

~~~html
<section class="section" id="consultancy">
  <h5 class="title">Por Que Contratar uma Consultoria?</h5>
  <div class="double-column">
    <p class="text">A consultoria empresarial se fortalece como uma forma de imprimir agilidade aos negócios e promover mudanças difíceis de serem executadas internamente. Contrate a Remast e garanta vantagem competitiva para sua empresa.</p>
    <img src="assets/image/remast-vector.png" alt="" class="image">
  </div>
</section>
~~~

Explica os benefícios de contratar uma consultoria empresarial, com texto e imagem.

- **Como Fazemos:**:

~~~html
<section class="section" id="how-we-do">
  <h5 class="title">Como Fazemos</h5>
  <div class="double-column">
    <p class="text">Na Remast, nosso método de trabalho é pautado pela excelência e eficiência. Seguimos um processo cuidadoso em cada etapa, garantindo resultados superiores e satisfação total de nossos clientes. Veja como trabalhamos:</p>
    <div class="card-group-topic">
      <p class="card-text-topic">1. Análise Detalhada: Iniciamos com uma análise minuciosa das necessidades e características específicas de cada cliente.</p>
      <!-- Outros passos do processo -->
    </div>
  </div>
</section>
~~~

Descreve o processo de trabalho da empresa, passo a passo.

- **Contato:**:

~~~html
<section class="section" id="contact">
  <h5 class="title">Contato</h5>
  <div class="map-container">
    <iframe class="map" src="https://www.google.com/maps/embed?pb=..."></iframe>
  </div>
  <div class="group-contact-information">
    <div class="card-group-contact">
      <div class="card-contact">
        <img src="assets/vetores/map-marker.png" alt="map-marker" class="card-vector">
        <div class="information-group">
          <h5 class="card-title">Localização</h5>
          <p class="card-text">42850-000 Dias D'Ávila - Bahia/Brasil</p>
        </div>
      </div>
      <!-- Outros contatos -->
    </div>
  </div>
</section>
~~~

Fornece informações de contato, incluindo um mapa, endereço, número de WhatsApp, e email.

### Rodapé (`<footer>`)

- **Informações de Direitos Autorais**:

~~~html
<footer class="footer">
  <p class="copyright-information">
    © 2023 - Todos os direitos reservados - Remast Consultoria em Gestão Empresarial
  </p>
  <p class="copyright-information">
    Portal Conexão Azul Digital Ltda - conexaoazul.com
  </p>
</footer>
~~~

Exibe informações de direitos autorais.

### JavaScript (`<script>`)

- **Script externo:**:

~~~html
<script src="scripts.js"></script>
~~~

Inclui um arquivo JavaScript externo, provavelmente para funcionalidades adicionais como o menu móvel.

>Este código cria uma página web completa com uma estrutura bem definida, seções claras para diferentes tipos de conteúdo, e estilos e scripts externos para aparência e funcionalidade.
