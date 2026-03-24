# Colégio Maria Auxiliadora — Site Institucional

Site institucional do **Colégio Maria Auxiliadora**, localizado em Rio Claro – SP.
Domínio: [colegiomariauxiliadora.org](https://colegiomariauxiliadora.org)

---

## Estrutura do projeto

```
site_maria_auxiliadora/
└── index (3).html   # Arquivo único — todo o HTML, CSS e JS estão aqui
```

O site é um **SPA (Single Page Application)** sem framework — a navegação entre páginas é feita por JavaScript puro que alterna a classe `active` nas `div.page`.

---

## Páginas

| ID | Nome | Conteúdo principal |
|----|------|--------------------|
| `page-home` | Home | Hero com banner flutuante, diferenciais, CTA final |
| `page-sobre` | Sobre | Missão, visão, valores e história da escola |
| `page-matriculas` | Matrículas | Turmas, etapas de ensino e CTA de inscrição |
| `page-contato` | Contato | Formulário de contato e mapa |

---

## Tecnologias

- **HTML5 / CSS3 / JavaScript** — sem frameworks ou bibliotecas externas
- **Fetch API** — envio do formulário de contato via POST (async/await)
- **CSS Custom Properties** — paleta e tokens de design centralizados em `:root`
- **Responsive Design** — menu mobile com `toggleMenu()` e media queries

---

## Recursos externos

### Fontes — Google Fonts
| Família | Pesos | Uso |
|---------|-------|-----|
| [Cormorant Garamond](https://fonts.google.com/specimen/Cormorant+Garamond) | 300, 400, 500, 600 (normal e itálico) | Títulos e destaques serif |
| [Jost](https://fonts.google.com/specimen/Jost) | 300, 400, 500 | Corpo de texto e UI |

### Imagens
| Descrição | URL |
|-----------|-----|
| Banner principal (hero flutuante) | `https://i.postimg.cc/SxJsLxFx/banner-site-mariaux.jpg` |

Hospedagem de imagens: **[PostImg](https://postimg.cc)**

### Mapa
- **Google Maps Embed** — localização fixa: Av. 54A, nº 11 – Jardim América, Rio Claro – SP

---

## Integrações e serviços

### Formspree — Formulário de contato
- **Serviço:** [formspree.io](https://formspree.io)
- **Endpoint:** `https://formspree.io/f/xeeryggw`
- **Método:** POST / JSON
- **Campos:** `nome`, `email`, `whatsapp`, `assunto`, `mensagem`
- **Destino:** `contato@colegiomariauxiliadora.org`

### WhatsApp
- **Número:** (19) 99920-6136
- **Link agendar visita:** `https://wa.me/5519999206136?text=Olá! Gostaria de agendar uma visita ao Colégio Maria Auxiliadora.`
- **Link informações:** `https://wa.me/5519999206136?text=Olá! Gostaria de informações sobre o Colégio Maria Auxiliadora.`

### E-mail
- `contato@colegiomariauxiliadora.org`

---

## Paleta de cores

| Token | Hex | Uso |
|-------|-----|-----|
| `--navy` | `#0D2545` | Cor primária, fundos escuros |
| `--navy-mid` | `#1A3A6B` | Variação intermediária |
| `--navy-soft` | `#243F6E` | Variação suave |
| `--gold` | `#B8963E` | Destaque, bordas, ícones |
| `--gold-light` | `#D4AF67` | Textos em fundo escuro |
| `--gold-pale` | `#F7F0E0` | Fundos de seção |
| `--cream` | `#FAF8F3` | Background padrão da página |
| `--white` | `#FFFFFF` | Seções brancas |
| `--text` | `#1C1C1C` | Texto principal |
| `--text-mid` | `#3A3A3A` | Texto secundário |
| `--text-muted` | `#5A5A5A` | Texto suavizado |
| `--border` | `#E2D9C8` | Bordas e divisores |

---

## Variáveis de layout

```css
--max:   1140px   /* Largura máxima do conteúdo */
--nav-h: 72px     /* Altura da barra de navegação */
```

---

## Funções JavaScript principais

| Função | Descrição |
|--------|-----------|
| `showPage(id)` | Alterna entre páginas alterando a classe `active` |
| `toggleMenu()` | Abre/fecha o menu mobile |
| `submitForm(e)` | Valida e envia o formulário via Fetch → Formspree |

---

## Como editar

O site é um arquivo HTML único. Basta abrir `index (3).html` em qualquer editor de texto.
Não há processo de build, dependências npm ou configuração de servidor necessária.

Para testar localmente, abra o arquivo diretamente no navegador:
```bash
xdg-open "index (3).html"   # Linux
open "index (3).html"        # macOS
```
