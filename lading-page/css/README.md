# Style.CSS

O código CSS fornecido é usado para estilizar uma página web, incluindo fontes, cores, layout e responsividade. Vou explicar cada parte em detalhes:

## Importação de Fontes

~~~css
@import url('https://fonts.googleapis.com/css2?family=Poppins:ital,wght@0,100;0,200;0,300;0,400;0,500;0,600;0,700;0,800;0,900;1,100;1,200;1,300;1,400;1,500;1,600;1,700;1,800;1,900&display=swap');
@import url('https://fonts.googleapis.com/css2?family=Montserrat:wght@100;200;300;400;500;600;700;800;900&display=swap');
~~~

Essas linhas importam as fontes "Poppins" e "Montserrat" do Google Fonts, que são utilizadas em diferentes partes da página.

## Variáveis de Cores
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

Definem as cores e a fonte padrão que serão utilizadas ao longo do CSS, facilitando a manutenção e a consistência visual

## Estilos Globais

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

Esses estilos garantem que todos os elementos tenham margens e espaçamentos zerados, utilizem o box-sizing: border-box para incluir padding e border no tamanho total dos elementos e utilizem a fonte padrão definida anteriormente.

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
~~~

Estiliza a barra de navegação para que fique fixa no topo, com espaçamento e sombra para destacá-la.

~~~css
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
~~~

Define o estilo do logotipo, incluindo a imagem e o texto.

~~~css
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

Estiliza a lista de navegação, removendo a marcação padrão e ajustando o espaçamento.

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

Define o estilo do menu móvel (hambúrguer) para dispositivos menores.

## Seções e Banner

~~~css
.section {
  background-color: var(--cor-branca);
  padding: 80px 50px;
}
~~~

Define o estilo geral das seções da página.

Vamos analisar e explicar o CSS para a classe `.banner` passo a passo:

```css
.banner {
  margin-top: 80px; /* Define uma margem superior de 80 pixels. */
  display: flex; /* Define o elemento como um contêiner flexível, permitindo o uso de flexbox para alinhar seus filhos. */
  align-items: center; /* Alinha os itens filhos ao centro verticalmente dentro do contêiner flexível. */
  background: linear-gradient(to right, /* Inicia um gradiente linear que vai da esquerda para a direita. */
    rgba(243, 222, 26, 1) 0%, /* Cor #F3DE1A com 100% de opacidade no início do gradiente (0%). */
    rgba(243, 222, 26, 1) 10%, /* Cor #F3DE1A com 100% de opacidade até 10% do gradiente. */
    rgba(243, 222, 26, 0.86) 24%, /* Cor #F3DE1A com 86% de opacidade em 24% do gradiente. */
    rgba(243, 222, 26, 0.42) 58%, /* Cor #F3DE1A com 42% de opacidade em 58% do gradiente. */
    rgba(243, 222, 26, 0.26) 74%, /* Cor #F3DE1A com 26% de opacidade em 74% do gradiente. */
    rgba(243, 222, 26, 0) 100% /* Cor #F3DE1A com 0% de opacidade (transparente) no final do gradiente (100%). */
  ), 
  url("../assets/image/background.png") no-repeat center center; /* Adiciona uma imagem de fundo que não se repete e está centralizada. */
  background-size: cover; /* Redimensiona a imagem de fundo para cobrir todo o elemento. */
  height: 90vh; /* Define a altura do elemento como 90% da altura da janela de visualização (viewport height). */
}
```

#### Explicação dos principais pontos:

1. **`margin-top: 80px;`**
   - Define um espaço de 80 pixels acima do elemento `.banner`.

2. **`display: flex;`**
   - Transforma o `.banner` em um contêiner flexível, permitindo a utilização das propriedades de layout flexbox.

3. **`align-items: center;`**
   - Alinha verticalmente os itens filhos do contêiner flexível ao centro.

4. **`background: linear-gradient(to right, ... ), url("../assets/image/background.png") no-repeat center center;`**
   - Define um plano de fundo composto por um gradiente linear e uma imagem.
   - O gradiente vai da esquerda para a direita (`to right`).
   - Especifica várias paradas de cor (`color stops`) no gradiente com diferentes níveis de opacidade.
   - Adiciona uma imagem de fundo que não se repete (`no-repeat`) e é centralizada horizontalmente e verticalmente (`center center`).

5. **`background-size: cover;`**
   - Redimensiona a imagem de fundo para garantir que ela cubra completamente o elemento, mantendo suas proporções.

6. **`height: 90vh;`**
   - Define a altura do elemento como 90% da altura da janela de visualização, ajustando-se dinamicamente ao tamanho da janela.

Este CSS cria uma seção de banner com um gradiente amarelo que vai se tornando transparente, sobreposto a uma imagem de fundo que cobre todo o elemento e é centralizada.

~~~css
.banner-text {
  color: var(--cor-azul);
  text-align: center;
  font-size: 50px;
  font-weight: 500;
  width: 80%;
  height: 500px;
  text-shadow: 2px 2px 4px rgba(0, 0, 0, 0.5);
  display: flex;
  justify-content: center;
  align-items: flex-end;
  margin: 0 auto;
}
~~~

Define o texto do banner, incluindo cor, tamanho da fonte e sombra do texto.

## Layout de Duas Colunas e Cartões

~~~css
.section {
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

Define o estilo das seções com layout de duas colunas, centralizando o texto e ajustando o espaçamento.

~~~css
.double-column {
  display: flex;
  flex-direction: row;
  justify-content: center;
  align-items: flex-start;
  width: 100%;
  margin-top: 40px;
}
~~~

Configura o layout de duas colunas para alinhar elementos lado a lado.

~~~css
.text {
  flex: 5;
  margin-right: 20px;
  width: auto;
  height: auto;
  text-align: left;
  color: var(--cor-cinza-3);
  font-size: 38px;
}
~~~

Define o estilo do texto nas seções de duas colunas.

~~~css
.image {
  width: 40%;
}
~~~

Configura o tamanho da imagem nas seções de duas colunas.

~~~css
.card-group {
  display: flex;
  flex-direction: row;
  justify-content: center;
  gap: 20px;
  flex-wrap: nowrap;
  overflow-x: auto;
  padding: 0 20px;
  margin: 20px 0px;
}
~~~

Estiliza um grupo de cartões para permitir rolagem horizontal e espaçamento entre eles.

~~~css
.card-model {
  flex: 0 0 250px;
  box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
  transition: transform 0.3s ease-in-out, box-shadow 0.3s ease-in-out;
  margin: 10px;
}

.card-model:hover {
  transform: translateY(-10px);
  box-shadow: 0 12px 16px rgba(0, 0, 0, 0.2);
}
~~~

Define o estilo dos cartões, incluindo efeitos de hover para destacá-los.

~~~css
.card-body {
  padding: 20px;
  border-radius: 0 0 32px 32px;
}

.card-title {
  color: var(--cor-azul);
  margin-bottom: 10px;
}

.card-text {
  color: var(--cor-cinza-3);
  font-size: 16px;
  line-height: 1.5;
}

.card-vector {
  width: 80px;
  height: auto;
  margin-bottom: -20px;
}
~~~

Define o estilo interno dos cartões, incluindo título, texto e vetor (imagem).

## Seção "Como Fazemos" e Contato

~~~css
#how-we-do .double-column {
  display: flex;
  justify-content: space-around;
  align-items: stretch;
  flex-wrap: wrap;
}
~~~

Estiliza a seção "Como Fazemos" para distribuir elementos em duas colunas, adaptando-se ao tamanho da tela.

~~~css
#how-we-do .card-group-topic {
  flex: 1;
  max-width: 45%; 
  background-color: var(--cor-azul);
  padding: 20px; 
  border-radius: 10px; 
  box-shadow: 0 4px 8px rgba(0,0,0,0.2); 
}
~~~

Define o estilo dos grupos de tópicos na seção "Como Fazemos".

~~~css
#how-we-do .text, .card-group-topic {
  flex: 1;
  max-width: 45%;
  display: flex;
  flex-direction: column;
}

#how-we-do .text {
  color: var(--cor-cinza-3);
  font-size: 28px;
  margin: 0 10px;
  padding: 20px;
  background-color: var(--cor-cinza-1);
  border-radius: 10px;
  box-shadow: 0 2px 5px rgba(0,0,0,0.1); 
}
~~~

Estiliza o texto e os grupos de tópicos na seção "Como Fazemos".

~~~css
.card-group-topic {
  background-color: var(--cor-azul);
}

#how-we-do .card-title-topic {
  color: var(--cor-amarela);
  font-size: 24px;
  margin-bottom: 10px;
}

#how-we-do .card-text-topic {
  color: var(--cor-branca);
  font-size: 18px;
  line-height: 1.5;
}
~~~

Define o estilo dos cartões de tópicos na seção "Como Fazemos".

## Contato

~~~css
#contact .group-contact-information {
  display: flex;
  justify-content: space-around;
  flex-wrap: wrap;
  width: 100%;
}
~~~

Estiliza a seção de contato para distribuir informações de contato de forma flexível.

~~~css
#contact .group-contact-information .card-group-contact {
  flex: 1;
  display: flex;
  justify-content: center;
  max-width: 100%;
}

#contact .group-contact-information .card-group-contact .card-contact {
  display: flex;
  flex-direction: row;
  align-items: center;
  justify-content: space-between;
  background-color: var(--cor-azul);
  color: var(--cor-branca);
  width: calc(50% - 20px);
  padding: 20px;
  margin: 10px;
  border-radius: 10px;
  box-shadow: 0 4px 8px rgba(0,0,0,0.2);
}
~~~

Define o estilo dos cartões de contato, incluindo layout, cores e sombra.

~~~css
#contact .group-contact-information .card-group-contact .card-contact .information-group {
  display: flex;
  flex-direction: column;
}

#contact .group-contact-information .card-group-contact .card-contact .information-group .card-title,
#contact .group-contact-information .card-group-contact .card-contact .information-group .card-text {
  text-align: left; 
  margin-bottom: 5px; 
}
~~~

Estiliza as informações dentro dos cartões de contato, garantindo alinhamento e espaçamento adequado.

# Rodapé

~~~css
.footer {
  background-color: var(--cor-azul); 
  color: var(--cor-branca);
  text-align: center; 
  padding: 20px 0; 
  font-size: 16px; 
  line-height: 1.5; 
  border-top: 3px solid var(--cor-amarela); 
}

.footer .copyright-information {
  margin: 10px 0; 
  padding: 0 20px; 
}
~~~

Define o estilo do rodapé, incluindo cores, alinhamento de texto e espaçamento.

# Responsividade

~~~css
@media only screen and (max-width: 999px) {
  .nav-list {
    flex-direction: column;
    position: absolute;
    width: 60%;
    height: 350px;
    top: 80px;
    left: -100%;
    background-color: #FFFFFF;
    box-shadow: 0 4px 8px rgba(0, 0, 0, 0.5);
    transition: all 0.3s;
    justify-content: space-around;
  }

  .nav-list.active {
      left: 0;
  }

  .nav-list a {
    font-size: 20px;
    padding: 20px 0px;
  }

  .mobile-menu {
      display: flex;
  }
  .section {
    padding: 40px 20px;
    margin: 60px 0;
  }

  .banner {
    margin-top: 60px;
    height: 70vh;
  }

  .banner-text {
    font-size: 30px;
  }

  .title {
    font-size: 24px;
  }

  .double-column {
    flex-direction: column;
    align-items: center;
    margin-top: 20px;
  }

  .text {
    width: 100%;
    text-align: center;
    font-size: 16px;
    margin: 20px 0;
  }

  .image {
    width: 80%;
  }

  .card-group {
    flex-direction: column;
    align-items: center; 
    overflow-x: hidden; 
    gap: 10px; 
    padding: 10px 0;
  }

  .card-model {
    flex: 0 0 auto;
    width: 90%; 
    margin: 10px 0; 
  }

  .card-body {
    padding: 15px;
  }

  .card-title {
    margin-bottom: 5px;
  }

  .card-text {
    font-size: 14px;
  }

  .card-vector {
    width: 60px;
    margin-bottom: -15px;
  }

  #how-we-do .double-column {
    flex-direction: column;
    align-items: center;
  }

  #how-we-do .text {
    font-size: 18px;
    padding: 20px;
    margin: 0;
    text-align: center;
    max-width: 90%;
  }

  #how-we-do .card-group-topic {
    margin-top: 20px;
    padding: 20px;
    border-radius: 10px;
    max-width: 90%;
  }

  #how-we-do .card-text-topic {
    font-size: 14px;
    line-height: 1.5;
    margin-bottom: 15px;
    text-indent: 0;
  }

  #contact .group-contact-information .card-group-contact {
    max-width: 100%;
  }
  
  #contact .group-contact-information .card-group-contact .card-contact {
    width: calc(100% - 20px);
  }

  .footer {
    padding: 10px 0;
  }

  .footer .copyright-information {
    padding: 0 10px;
  }
}
~~~

Define estilos responsivos para adaptar o layout em telas menores, como celulares e tablets, garantindo que a página continue visualmente atraente e funcional.

>O código CSS garante que a página seja visualmente atraente, funcional e responsiva, utilizando uma paleta de cores sofisticada e fontes elegantes. A estrutura flexível permite que o conteúdo se ajuste automaticamente a diferentes tamanhos de tela, proporcionando uma boa experiência do usuário em dispositivos de diversos formatos.