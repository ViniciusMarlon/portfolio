# Portfólio Profissional - Vinicius Marlon

**Nome do Aluno:** Vinicius Marlon Nogueira

## Descrição do Portfólio
Este é o meu portfólio profissional e acadêmico. O site foi desenvolvido para apresentar meu perfil, as tecnologias que estou estudando, meus projetos práticos e as formas de entrar em contato comigo. O design foi pensado para ser limpo, moderno e totalmente responsivo.

## Tecnologias Utilizadas
*   **HTML5:** Estruturação semântica do conteúdo.
*   **Bootstrap 5:** Framework CSS utilizado para criar o layout responsivo, o menu de navegação (Navbar), o carrossel de imagens (Carousel), os cards e os botões.
*   **Bootstrap Icons:** Biblioteca de ícones vetoriais.
*   **Devicon:** Ícones específicos de tecnologias (HTML, CSS, Python, etc.).
*   **JavaScript (Nativo do Bootstrap):** Utilizado para inicializar os componentes interativos.

## Link do Site Publicado
[Acesse o Portfólio Aqui](https://viniciusmarlon.github.io/portfolio/)

## Funcionamento do Projeto
O site é uma *Single Page* (página única) dividida em seções: Perfil, Projetos e Contato. A navegação é feita através de âncoras no menu superior fixo (sticky-top). Utilizei o sistema de grid do Bootstrap (`container`, `row`, `col`) para garantir que o layout se adapte perfeitamente a celulares, tablets e desktops.

## Descrição do Recurso Novo Adicionado
**Recurso:** Implementação de Tooltips (Dicas de Tela) e Bootstrap Icons.
**O que faz:** Ao passar o mouse sobre os links do menu e sobre as tecnologias listadas na seção de perfil, uma caixa de texto flutuante (tooltip) aparece explicando a função daquele item. Além disso, os botões de contato receberam ícones visuais para facilitar a identificação.

## Explicação de como esse recurso foi implementado
Para adicionar esse recurso, incluí a biblioteca **Bootstrap Icons** via CDN no `<head>` do documento e utilizei a tag `<i class="bi bi-..."></i>` dentro dos botões de contato. 

Para os **Tooltips**, utilizei a estrutura nativa do Bootstrap. Nos elementos HTML (links do menu e itens de tecnologia), adicionei os atributos `data-bs-toggle="tooltip"`, `data-bs-placement="bottom"` (para definir a posição) e o atributo `title="..."` contendo o texto da dica. Por fim, incluí um script JavaScript no final do documento que seleciona todos esses elementos e inicializa o componente:
```javascript
const tooltipTriggerList = document.querySelectorAll('[data-bs-toggle="tooltip"]');
const tooltipList = [...tooltipTriggerList].map(tooltipTriggerEl => new bootstrap.Tooltip(tooltipTriggerEl));