# Scripts.JS

Este documento descreve a funcionalidade de dois scripts JavaScript incluídos na página HTML. Ambos os scripts são executados quando o DOM é completamente carregado e fornecem interatividade para o menu de navegação e a rolagem suave entre seções da página.

## Alternância do Menu Mobile

Este script permite a alternância do menu de navegação para dispositivos móveis. Ele adiciona e remove a classe `active` à lista de navegação (`nav-list`) quando o botão do menu mobile (`mobile-menu`) é clicado.

~~~javascript
document.addEventListener('DOMContentLoaded', function() {
  const menuToggle = document.querySelector('.mobile-menu');
  const navList = document.querySelector('.nav-list');

  menuToggle.addEventListener('click', function() {
      navList.classList.toggle('active');
  });
});
~~~

- **`DOMContentLoaded` Event**: Garante que o script só seja executado após o carregamento completo do DOM.

- **`menuToggle`**: Seleciona o elemento com a classe mobile-menu.

- **`navList`**: Seleciona o elemento com a classe nav-list.

- **`click` Event Listener**: Adiciona um ouvinte de evento ao menuToggle. Quando o botão é clicado, a classe active é adicionada ou removida do navList, alternando a visibilidade do menu.

## Rolagem Suave

Este script habilita a rolagem suave entre seções da página quando links de navegação são clicados. Ele intercepta o comportamento padrão do clique em links e realiza uma rolagem suave até a seção alvo.

~~~javascript
document.addEventListener('DOMContentLoaded', function() {
  document.querySelectorAll('.nav-link').forEach(anchor => {
    anchor.addEventListener('click', function(e) {
      e.preventDefault();

      const targetId = this.getAttribute('href').substring(1);
      const targetSection = document.getElementById(targetId);
      const offsetTop = targetSection.offsetTop;

      window.scrollTo({
        top: offsetTop,
        behavior: 'smooth'
      });
    });
  });
});
~~~

- **`DOMContentLoaded` Event**: Garante que o script só seja executado após o carregamento completo do DOM.

- **`document.querySelectorAll('.nav-link')`**: Seleciona todos os elementos de link de navegação com a classe nav-link.

- **`forEach Method`**: Itera sobre cada link selecionado.

- **`click` Event Listener**: Adiciona um ouvinte de evento a cada link. Quando um link é clicado:

| Método/Propriedade                                 | Descrição                                                                                   |
|-----------------------------------------------------|---------------------------------------------------------------------------------------------|
| `e.preventDefault()`                               | Previne o comportamento padrão do clique em um link.                                        |
| `getAttribute('href')`                             | Obtém o valor do atributo `href` do elemento selecionado.                                   |
| `substring(1)`                                     | Remove o caractere `#` do início do `href` para obter o ID do alvo.                         |
| `document.getElementById(targetId)`                | Seleciona o elemento alvo com o ID correspondente.                                          |
| `offsetTop`                                        | Obtém a posição vertical do elemento em relação ao topo do documento.                        |
| `window.scrollTo({ top: offsetTop, behavior: 'smooth' })` | Realiza a rolagem suave até a posição vertical do elemento alvo.                           |

# Conclusão

Estes scripts fornecem funcionalidades essenciais para a navegação em dispositivos móveis e uma experiência de rolagem suave em uma página web. O primeiro script lida com a alternância do menu de navegação mobile, enquanto o segundo script implementa a rolagem suave para uma navegação mais intuitiva entre as seções da página.