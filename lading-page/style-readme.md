# Style.CSS

Este arquivo CSS é utilizado para estilizar uma página web com uma navegação fixa, banner, seções de conteúdo e um rodapé. Ele utiliza as fontes "Poppins" e "Montserrat" importadas do Google Fonts.

~~~css
@import url('https://fonts.googleapis.com/css2?family=Poppins:ital,wght@0,100;0,200;0,300;0,400;0,500;0,600;0,700;0,800;0,900;1,100;1,200;1,300;1,400;1,500;1,600;1,700;1,800;1,900&display=swap');
@import url('https://fonts.googleapis.com/css2?family=Montserrat:wght@100;200;300;400;500;600;700;800;900&display=swap');
~~~

## Variáveis CSS

~~~css
:root {
  --cor-cinza-1: #D9DADC;
  --cor-cinza-2: #A7A7A7;
  --cor-cinza-3: #4A4D55;
  --cor-azul: #324065;
  --cor-branca: #FFFFFF;
  --cor-amarela: #DDC700;
  --fonte-padrao: "Montserrat", sans-serif;
}
~~~

Definição de cores e fontes usadas ao longo do arquivo

## Reset e Configurações Globais

~~~css
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
  font-family: var(--fonte-padrao);
}

html, body {
  width: 100%;
  overflow-x: hidden;
}
~~~

Configuração global para remover margens e preenchimentos, definir a fonte padrão, e evitar overflow horizontal.

## Navegação

~~~css
.nav {
  display: flex;
  justify-content: space-between;
  align-items: center;
  padding: 10px 20px;
  position: fixed;
  top: 0;
  left: 0;
  width: 100%;
  z-index: 1000;
  background-color: var(--cor-branca);
  box-shadow: 0 2px 4px rgba(0, 0, 0, 0.1); 
}

.logo {
  display: flex;
  align-items: center;
}

.logo-image {
  height: 60px;
}

.logo-text {
  width: 150px;
  font-size: 20px;
  margin-left: 10px;
  text-decoration: none;
  color: var(--cor-azul);
  font-weight: bold;
  word-wrap: break-word;
}

.nav-list {
  list-style: none;
  display: flex;
  margin: 0;
  padding: 0;
}

.nav-list li {
  padding: 0 15px;
}

.nav-list a {
  text-decoration: none;
  color: var(--cor-azul);
  font-size: 16px;
  font-weight: bold;
}
~~~

Estilo para a barra de navegação fixa no topo da página.

## Menu Mobile

~~~css
.mobile-menu {
  display: none;
  flex-direction: column;
  cursor: pointer;
}

.line1, .line2, .line3 {
  width: 30px;
  height: 3px;
  background-color: var(--cor-azul);
  margin: 5px 0;
}
~~~

Estilo para o menu de navegação em dispositivos móveis.

## Seções Gerais

~~~css
.section {
  background-color: var(--cor-branca);
  padding: 80px 50px ;
  display: flex;
  flex-direction: column;
  align-items: center;
  text-align: center;
  margin: 120px 0px;
}

.title {
  color: var(--cor-azul);
  font-weight: 500;
  font-size: 40px;
}
~~~

Estilo para as seções gerais da página.