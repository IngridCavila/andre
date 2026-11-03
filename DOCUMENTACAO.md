# Documentação do projeto

## Visão geral

Site institucional de página única para apresentação do profissional, áreas de atuação e informações de contato. O projeto é estático: HTML, CSS e JavaScript no navegador, sem framework de aplicação, servidor ou banco de dados próprios.

## Paleta de cores

A página carrega `css/templatemo-style.css`, que define o visual ativo. A paleta combina tons acolhedores com um verde discreto nos elementos de ação:

| Cor | Código | Aplicação e intenção |
| --- | --- | --- |
| Vinho | `#B83A45` | Cor de destaque original: borda superior da navegação, item ativo e formulário. Acrescenta personalidade e calor. |
| Vinho escuro | `#922D37` | Estados de interação herdados do tema, como hover em alguns links. |
| Verde-sálvia | `#627D69` | Botões de chamada para ação e ícone de telefone. É um verde menos saturado, associado a equilíbrio e cuidado, e suaviza o contraste com o vinho. |
| Verde-sálvia escuro | `#506956` | Hover dos botões de chamada para ação, oferecendo feedback sem introduzir outra cor. |
| Verde WhatsApp | `#25D366` | Mantido no botão flutuante para preservar a identificação visual do serviço; no hover usa `#1EBE5D`. |
| Branco | `#FFFFFF` | Fundo principal e texto sobre superfícies escuras. Mantém a página clara e legível. |
| Cinza muito claro | `#F9F9F9` | Fundo alternativo de algumas seções, criando separação sutil entre blocos. |

### Sensação transmitida

A combinação busca transmitir **acolhimento, confiança e serenidade**, sem perder profissionalismo. O vinho acrescenta calor e personalidade; o verde-sálvia evoca equilíbrio e cuidado; e os brancos e cinzas claros deixam a experiência mais leve e organizada. O verde mais vivo do WhatsApp funciona como um destaque familiar e facilita identificar o canal de contato. Em conjunto, a paleta procura comunicar um espaço humano, calmo e confiável, adequado a um serviço de psicologia.

### Observação sobre a paleta alternativa

O arquivo `css/psicologo.css` declara outra paleta por variáveis CSS — creme (`#F5EFE5`), linho (`#D8C7B6`), vinho (`#713D4B`), verde-floresta (`#344B40`) e dourado (`#B39A69`). Essa paleta propõe uma direção visual mais editorial e natural, mas **não está vinculada ao `index.html`**; portanto, não é aplicada à página atual. A cor verde-sálvia dos CTAs foi escolhida para harmonizar com o vinho e os neutros do tema que está efetivamente carregado.

## Arquitetura do projeto

```text
ANDRE/
├── index.html                 # Estrutura e conteúdo da página
├── css/
│   ├── bootstrap.min.css      # Grid, componentes e responsividade
│   ├── font-awesome.min.css   # Ícones
│   ├── owl.carousel.css       # Estrutura do carrossel
│   ├── owl.theme.default.min.css # Tema do carrossel
│   ├── templatemo-style.css   # Estilos ativos do site e ajustes visuais
│   └── psicologo.css          # Estilos alternativos, não carregados atualmente
├── js/
│   ├── jquery.js              # Biblioteca base para interações
│   ├── bootstrap.min.js       # Comportamentos do Bootstrap, como menu móvel
│   ├── owl.carousel.min.js    # Componente de carrossel
│   ├── smoothscroll.js        # Rolagem suave
│   └── custom.js              # Inicialização e comportamentos da página
├── images/                    # Fotos, imagens do carrossel e depoimentos
└── fonts/                     # Arquivos da fonte de ícones Font Awesome
```

### Organização do HTML

O `index.html` reúne o conteúdo em seções com âncoras para navegação interna: menu, início/carrossel (`#home`), apresentação (`#about`), trajetória e formação (`#feature`), atendimento (`#atendimento`), áreas de atuação (`#team`), livros/cursos (`#courses`), depoimentos (`#testimonial`), contato (`#contact`) e rodapé (`#footer`). O botão fixo do WhatsApp também está no HTML, separado do conteúdo principal e posicionado por CSS.

### Responsabilidades dos estilos

- **Bootstrap:** colunas, alinhamentos, componentes e adaptação responsiva.
- **Font Awesome:** ícones de telefone, WhatsApp e outros elementos gráficos.
- **Owl Carousel:** estilos do carrossel inicial e de listas deslizantes.
- **`templatemo-style.css`:** aparência da página, cores, imagens de fundo, estados de hover e regras para diferentes larguras de tela.
- **`psicologo.css`:** folha alternativa; só passa a influenciar o site se for adicionada explicitamente ao HTML.

### Responsabilidades do JavaScript

`js/custom.js` configura o desaparecimento da tela de carregamento, fecha o menu móvel após selecionar um link, atualiza a classe da navegação durante a rolagem, inicializa os carrosséis e anima a rolagem até as seções. As bibliotecas necessárias são carregadas ao final do `body` em `index.html`.

## Orientações para manutenção

1. Para alterar conteúdo e destinos de navegação, edite `index.html`.
2. Para mudar as cores visíveis atualmente, edite `css/templatemo-style.css`; as variáveis em `css/psicologo.css` não afetam a página enquanto essa folha não for carregada.
3. Ao alterar cores de botões, mantenha o estado normal e o hover relacionados e confira o contraste do texto.
4. Para substituir imagens, mantenha os arquivos em `images/` e atualize os caminhos no HTML ou no CSS.
5. Mudanças em carrosséis e navegação interativa podem exigir ajustes em `js/custom.js` e nos arquivos de estilo correspondentes.
