# Painéis Flexíveis com CSS e JavaScript

Este projeto demonstra o uso de CSS Flexbox e JavaScript para criar painéis interativos que se expandem e exibem animações suaves ao serem clicados.
Feito juntamente ao curso JavaScript30

## Funcionalidades

- **Painéis Interativos**: Cada painel pode ser clicado para expandir e revelar texto adicional.
- **Animações Suaves**: Transições suaves para tamanho, fonte e posição do texto.
- **Design Responsivo**: Os painéis se ajustam ao tamanho da tela.

## Estrutura do Projeto

O projeto é composto por um único arquivo HTML que contém:

- **HTML**: Estrutura dos painéis e do conteúdo.
- **CSS**: Estilização dos painéis, incluindo imagens de fundo e animações.
- **JavaScript**: Lógica para alternar classes e controlar as animações.

## Pré-visualização

A interface inclui:

- Cinco painéis com imagens de fundo.
- Texto estilizado que se move e redimensiona durante as transições.
- Animações suaves ao clicar nos painéis.

## Como Usar

1. Faça o download ou clone este repositório.
2. Abra o arquivo `index.htm` em qualquer navegador moderno.
3. Clique nos painéis para interagir com as animações.

## Código Principal

### CSS
O CSS utiliza Flexbox para organizar os painéis e transições para criar animações suaves.

```css
.panel {
    flex: 1;
    transition: 
        font-size 0.7s cubic-bezier(0.61, -0.19, 0.7, -0.11),
        flex 0.7s cubic-bezier(0.61, -0.19, 0.7, -0.11),
        background 0.2s;
}

.panel.open {
    flex: 5;
    font-size: 40px;
}

.panel.open-active p:first-child {
    transform: translateY(0);
}

JavaScript
O JavaScript adiciona e remove classes para controlar o estado dos painéis.

const panels = document.querySelectorAll('.panel');

function toggleOpen() {
    this.classList.toggle('open');
}

function toggleActive(e) {
    if (e.propertyName.includes('flex')) {
        this.classList.toggle('open-active');
    }
}

panels.forEach(panel => panel.addEventListener('click', toggleOpen));
panels.forEach(panel => panel.addEventListener('transitionend', toggleActive));
```

## Tecnologias Utilizadas
- HTML5: Estrutura do documento.
- CSS3: Estilização e animações com Flexbox.
- JavaScript: Manipulação do DOM para interatividade.

## Licença
Este projeto é de uso livre para fins educacionais e pessoais. 

