# Design Guidelines — Clínica Teste Storage

> **Nota do consolidation:** Tokens CSS derivados diretamente da paleta definida
> em brand-book.md. Coerência garantida entre os dois documentos.
> Sistema baseado em escala de 8pt para espaçamento.
> **(decisão do consolidation)**

---

## 1. Design Tokens CSS

### 1.1 Cores

```css
:root {
  /* === CORES PRIMÁRIAS === */
  --color-primary:         #1B4F8A;   /* Azul Confiança — CTAs, botões, logotipo */
  --color-primary-hover:   #153E6E;   /* Azul escurecido para hover states */
  --color-primary-light:   #E8F0FA;   /* Tint de 10% para fundos de destaque */

  --color-secondary:       #34A0A4;   /* Teal Saúde — badges, ícones ativos */
  --color-secondary-hover: #27878B;   /* Teal escurecido para hover */
  --color-secondary-light: #E6F5F5;   /* Tint de 10% para fundos suaves */

  --color-accent:          #52B788;   /* Verde Vitalidade — confirmações, status */
  --color-accent-hover:    #3E9268;
  --color-accent-light:    #EAF7F0;

  /* === CORES NEUTRAS === */
  --color-gray-900:        #1A202C;   /* Grafite Escuro — texto principal */
  --color-gray-600:        #64748B;   /* Cinza Ardósia — texto secundário */
  --color-gray-400:        #94A3B8;   /* Cinza Suave — placeholder, disabled */
  --color-gray-100:        #F0F7FF;   /* Azul Névoa — fundo de seções alternadas */
  --color-white:           #FFFFFF;   /* Branco Clínico — cards, superfícies */

  /* === CORES DE ESTADO === */
  --color-success:         #27AE60;
  --color-success-light:   #E8F8EE;
  --color-warning:         #F59E0B;
  --color-warning-light:   #FEF3C7;
  --color-error:           #E53E3E;
  --color-error-light:     #FEE2E2;
  --color-info:            #3B82F6;
  --color-info-light:      #EFF6FF;

  /* === GRADIENTES === */
  --gradient-primary:  linear-gradient(135deg, #1B4F8A 0%, #34A0A4 100%);
  --gradient-soft:     linear-gradient(180deg, #F0F7FF 0%, #FFFFFF 100%);
  --gradient-hero:     linear-gradient(135deg, #1B4F8A 0%, #1A202C 100%);
}
```

---

### 1.2 Tipografia

```css
:root {
  /* === FAMÍLIAS === */
  --font-display: 'Playfair Display', Georgia, serif;
  --font-body:    'Inter', system-ui, -apple-system, sans-serif;

  /* === TAMANHOS === */
  --text-display:  3.5rem;    /* 56px */
  --text-h1:       2.5rem;    /* 40px */
  --text-h2:       2rem;      /* 32px */
  --text-h3:       1.5rem;    /* 24px */
  --text-h4:       1.25rem;   /* 20px */
  --text-body-lg:  1.125rem;  /* 18px */
  --text-body:     1rem;      /* 16px */
  --text-body-sm:  0.875rem;  /* 14px */
  --text-caption:  0.75rem;   /* 12px */
  --text-overline: 0.6875rem; /* 11px */

  /* === PESOS === */
  --font-regular:   400;
  --font-medium:    500;
  --font-semibold:  600;
  --font-bold:      700;

  /* === LINE-HEIGHT === */
  --leading-tight:   1.15;
  --leading-snug:    1.25;
  --leading-normal:  1.5;
  --leading-relaxed: 1.6;
  --leading-loose:   1.7;

  /* === LETTER-SPACING === */
  --tracking-tight:    -0.01em;
  --tracking-normal:    0;
  --tracking-wide:     +0.04em;
  --tracking-wider:    +0.08em;  /* Para text-overline uppercase */
}
```

---

### 1.3 Espaçamento (Sistema 8pt)

```css
:root {
  --space-1:   0.25rem;   /*  4px */
  --space-2:   0.5rem;    /*  8px */
  --space-3:   0.75rem;   /* 12px */
  --space-4:   1rem;      /* 16px */
  --space-5:   1.25rem;   /* 20px */
  --space-6:   1.5rem;    /* 24px */
  --space-8:   2rem;      /* 32px */
  --space-10:  2.5rem;    /* 40px */
  --space-12:  3rem;      /* 48px */
  --space-16:  4rem;      /* 64px */
  --space-20:  5rem;      /* 80px */
  --space-24:  6rem;      /* 96px */
  --space-32:  8rem;      /* 128px */
}
```

**Regra geral:**
- Padding interno de seções: `--space-16` a `--space-24` (64–96px) no desktop;
  `--space-10` a `--space-12` (40–48px) no mobile.
- Gap entre cards: `--space-6` (24px) no desktop; `--space-4` (16px) no mobile.
- Margin entre texto e CTA: `--space-8` (32px).

---

### 1.4 Border Radius

```css
:root {
  --radius-sm:   4px;
  --radius-md:   8px;    /* Cards, inputs, dropdowns */
  --radius-lg:   16px;   /* Modais, imagens, cards grandes */
  --radius-xl:   24px;   /* Cards hero, painéis destacados */
  --radius-full: 9999px; /* Badges, pills, avatares circulares */
}
```

---

### 1.5 Sombras

```css
:root {
  --shadow-sm:   0 1px 3px rgba(26, 32, 44, 0.08), 0 1px 2px rgba(26, 32, 44, 0.04);
  --shadow-md:   0 4px 6px rgba(26, 32, 44, 0.07), 0 2px 4px rgba(26, 32, 44, 0.04);
  --shadow-lg:   0 10px 15px rgba(26, 32, 44, 0.08), 0 4px 6px rgba(26, 32, 44, 0.04);
  --shadow-xl:   0 20px 25px rgba(26, 32, 44, 0.1), 0 8px 10px rgba(26, 32, 44, 0.04);
  --shadow-focus: 0 0 0 3px rgba(27, 79, 138, 0.25);  /* Azul Confiança a 25% */
}
```

---

### 1.6 Z-index

```css
:root {
  --z-base:     0;
  --z-raised:   10;
  --z-dropdown: 100;
  --z-sticky:   200;
  --z-overlay:  300;
  --z-modal:    400;
  --z-toast:    500;
}
```

---

## 2. Componentes

### 2.1 Botões

#### Botão Primário

```css
.btn-primary {
  display:          inline-flex;
  align-items:      center;
  gap:              var(--space-2);
  padding:          var(--space-3) var(--space-6);    /* 12px 24px */
  background-color: var(--color-primary);
  color:            var(--color-white);
  font-family:      var(--font-body);
  font-size:        var(--text-body);
  font-weight:      var(--font-semibold);
  line-height:      1;
  border:           2px solid transparent;
  border-radius:    var(--radius-md);
  cursor:           pointer;
  transition:       background-color 200ms ease, transform 150ms ease, box-shadow 200ms ease;
  text-decoration:  none;
  white-space:      nowrap;
}

.btn-primary:hover {
  background-color: var(--color-primary-hover);
  transform:        translateY(-1px);
  box-shadow:       var(--shadow-md);
}

.btn-primary:active {
  transform:   translateY(0);
  box-shadow:  none;
}

.btn-primary:focus-visible {
  outline:    none;
  box-shadow: var(--shadow-focus);
}

.btn-primary:disabled {
  background-color: var(--color-gray-400);
  cursor:           not-allowed;
  transform:        none;
  box-shadow:       none;
}
```

#### Botão Secundário (Outline)

```css
.btn-secondary {
  /* Mesma base do primário, com as diferenças: */
  background-color: transparent;
  color:            var(--color-primary);
  border:           2px solid var(--color-primary);
}

.btn-secondary:hover {
  background-color: var(--color-primary-light);
  transform:        translateY(-1px);
}
```

#### Botão Fantasma (Ghost)

```css
.btn-ghost {
  background-color: transparent;
  color:            var(--color-primary);
  border:           2px solid transparent;
  /* Sem sombra no hover, apenas cor de fundo suave */
}

.btn-ghost:hover {
  background-color: var(--color-primary-light);
}
```

#### Tamanhos de Botão

```css
.btn-sm  { padding: var(--space-2) var(--space-4); font-size: var(--text-body-sm); }
.btn-md  { padding: var(--space-3) var(--space-6); font-size: var(--text-body); }   /* Padrão */
.btn-lg  { padding: var(--space-4) var(--space-8); font-size: var(--text-body-lg); }
```

#### Botão WhatsApp (especial)

```css
.btn-whatsapp {
  background-color: #25D366;
  color:            #FFFFFF;
  /* Demais estilos herdam do btn-primary */
}
.btn-whatsapp:hover { background-color: #1DAE54; }
```

---

### 2.2 Cards

#### Card Padrão

```css
.card {
  background:    var(--color-white);
  border-radius: var(--radius-lg);
  padding:       var(--space-6);     /* 24px */
  box-shadow:    var(--shadow-md);
  transition:    box-shadow 200ms ease, transform 200ms ease;
}

.card:hover {
  box-shadow: var(--shadow-lg);
  transform:  translateY(-2px);
}
```

#### Card de Serviço

```css
.card-service {
  /* Herda .card */
  display:        flex;
  flex-direction: column;
  gap:            var(--space-4);
  border-top:     3px solid var(--color-secondary);
}

.card-service .card-icon {
  width:            48px;
  height:           48px;
  background-color: var(--color-secondary-light);
  border-radius:    var(--radius-md);
  display:          flex;
  align-items:      center;
  justify-content:  center;
  color:            var(--color-secondary);
}

.card-service .card-title {
  font-family: var(--font-body);
  font-size:   var(--text-h4);
  font-weight: var(--font-semibold);
  color:       var(--color-gray-900);
}

.card-service .card-body {
  font-size:   var(--text-body);
  color:       var(--color-gray-600);
  line-height: var(--leading-relaxed);
  flex:        1;
}
```

#### Card de Depoimento

```css
.card-testimonial {
  /* Herda .card */
  position:   relative;
  padding-top: var(--space-8);
}

.card-testimonial::before {
  content:     '"';
  position:    absolute;
  top:         var(--space-4);
  left:        var(--space-6);
  font-family: var(--font-display);
  font-size:   4rem;
  color:       var(--color-secondary);
  line-height: 1;
}

.card-testimonial .testimonial-text {
  font-size:   var(--text-body-lg);
  color:       var(--color-gray-900);
  font-style:  italic;
  line-height: var(--leading-loose);
}

.card-testimonial .testimonial-author {
  margin-top:  var(--space-4);
  font-size:   var(--text-body-sm);
  font-weight: var(--font-semibold);
  color:       var(--color-gray-600);
}
```

#### Card de Diferencial (Feature)

```css
.card-feature {
  text-align: center;
  padding:    var(--space-8) var(--space-6);
  background: var(--color-gray-100);
  border-radius: var(--radius-lg);
  /* Sem sombra — visual mais plano para seções de features */
}

.card-feature .feature-icon {
  width:            64px;
  height:           64px;
  background-color: var(--color-primary-light);
  border-radius:    var(--radius-full);
  display:          flex;
  align-items:      center;
  justify-content:  center;
  margin:           0 auto var(--space-4);
  color:            var(--color-primary);
}
```

---

### 2.3 Formulários

#### Input Padrão

```css
.form-input {
  width:         100%;
  padding:       var(--space-3) var(--space-4);   /* 12px 16px */
  background:    var(--color-white);
  border:        1.5px solid var(--color-gray-400);
  border-radius: var(--radius-md);
  font-family:   var(--font-body);
  font-size:     var(--text-body);
  color:         var(--color-gray-900);
  transition:    border-color 150ms ease, box-shadow 150ms ease;
  outline:       none;
}

.form-input::placeholder {
  color: var(--color-gray-400);
}

.form-input:hover {
  border-color: var(--color-gray-600);
}

.form-input:focus {
  border-color: var(--color-primary);
  box-shadow:   var(--shadow-focus);
}

.form-input.error {
  border-color: var(--color-error);
  background:   var(--color-error-light);
}

.form-input:disabled {
  background:   var(--color-gray-100);
  color:        var(--color-gray-400);
  cursor:       not-allowed;
}
```

#### Label

```css
.form-label {
  display:       block;
  margin-bottom: var(--space-2);
  font-size:     var(--text-body-sm);
  font-weight:   var(--font-medium);
  color:         var(--color-gray-900);
}

.form-label.required::after {
  content: ' *';
  color:   var(--color-error);
}
```

#### Mensagem de Erro

```css
.form-error-msg {
  margin-top: var(--space-1);
  font-size:  var(--text-caption);
  color:      var(--color-error);
  display:    flex;
  align-items: center;
  gap:        var(--space-1);
}
```

#### Checkbox (LGPD consent)

```css
.form-checkbox {
  display:     flex;
  align-items: flex-start;
  gap:         var(--space-3);
  cursor:      pointer;
}

.form-checkbox input[type="checkbox"] {
  width:         18px;
  height:        18px;
  accent-color:  var(--color-primary);
  flex-shrink:   0;
  margin-top:    2px;
}

.form-checkbox label {
  font-size:   var(--text-body-sm);
  color:       var(--color-gray-600);
  line-height: var(--leading-normal);
}
```

#### Select

```css
.form-select {
  /* Mesma base do form-input */
  appearance:   none;
  background-image: url("data:image/svg+xml,..."); /* chevron-down icon */
  background-repeat:   no-repeat;
  background-position: right var(--space-4) center;
  padding-right: var(--space-10);
}
```

---

### 2.4 Navegação (Header)

```css
.header {
  position:         sticky;
  top:              0;
  z-index:          var(--z-sticky);
  background:       var(--color-white);
  box-shadow:       var(--shadow-sm);
  padding:          0 var(--space-6);
  height:           72px;
  display:          flex;
  align-items:      center;
  justify-content:  space-between;
}

.nav-link {
  font-size:       var(--text-nav);
  font-weight:     var(--font-medium);
  color:           var(--color-gray-600);
  text-decoration: none;
  padding:         var(--space-2) var(--space-3);
  border-radius:   var(--radius-sm);
  transition:      color 150ms ease, background-color 150ms ease;
}

.nav-link:hover,
.nav-link.active {
  color:            var(--color-primary);
  background-color: var(--color-primary-light);
}
```

---

### 2.5 Badge / Pill

```css
.badge {
  display:       inline-flex;
  align-items:   center;
  padding:       var(--space-1) var(--space-3);
  border-radius: var(--radius-full);
  font-size:     var(--text-caption);
  font-weight:   var(--font-semibold);
  line-height:   1;
  white-space:   nowrap;
}

.badge-primary  { background: var(--color-primary-light);  color: var(--color-primary); }
.badge-success  { background: var(--color-success-light);  color: var(--color-success); }
.badge-warning  { background: var(--color-warning-light);  color: #92400E; }
.badge-error    { background: var(--color-error-light);    color: var(--color-error); }
.badge-teal     { background: var(--color-secondary-light); color: var(--color-secondary); }
```

---

### 2.6 Overline (Rótulo de Seção)

```css
.overline {
  display:         block;
  font-family:     var(--font-body);
  font-size:       var(--text-overline);
  font-weight:     var(--font-bold);
  letter-spacing:  var(--tracking-wider);
  text-transform:  uppercase;
  color:           var(--color-secondary);
  margin-bottom:   var(--space-3);
}
```

---

### 2.7 Botão Flutuante WhatsApp

```css
.fab-whatsapp {
  position:        fixed;
  bottom:          var(--space-6);
  right:           var(--space-6);
  z-index:         var(--z-toast);
  width:           56px;
  height:          56px;
  background-color: #25D366;
  border-radius:   var(--radius-full);
  display:         flex;
  align-items:     center;
  justify-content: center;
  box-shadow:      var(--shadow-lg);
  color:           white;
  transition:      transform 200ms ease, box-shadow 200ms ease;
  text-decoration: none;
}

.fab-whatsapp:hover {
  transform:  scale(1.08);
  box-shadow: var(--shadow-xl);
}

.fab-whatsapp:focus-visible {
  outline:    none;
  box-shadow: 0 0 0 3px rgba(37, 211, 102, 0.4);
}
```

---

## 3. Estados de UI

| Estado | Comportamento |
|---|---|
| **:hover** | Transição 200ms ease; leve escurecimento de cor ou elevação (translateY -1px/−2px) |
| **:focus-visible** | Anel de foco azul de 3px: `box-shadow: 0 0 0 3px rgba(27, 79, 138, 0.25)`. Nunca remover outline sem substituir por alternativa visível. |
| **:active** | Reset de transform (translateY 0); sem sombra extra |
| **:disabled** | Opacidade reduzida (via cor `--color-gray-400`); cursor `not-allowed`; sem transições |
| **:checked** (checkbox) | `accent-color: var(--color-primary)` |
| **loading** | Botões com estado de loading exibem spinner inline (18px) e ficam desabilitados; texto muda para "Enviando…" |
| **error** | Borda vermelha `var(--color-error)`, fundo `var(--color-error-light)`, mensagem de erro abaixo |
| **success** | Toast verde no canto superior direito; duração de 4s; dismissível |

---

## 4. Acessibilidade (WCAG AA)

### Requisitos Mínimos

| Critério | Implementação |
|---|---|
| Contraste de texto (nível AA) | Mínimo 4.5:1 para texto normal; 3:1 para texto grande (18px+). Ver paleta em brand-book.md. |
| Foco visível | Todo elemento interativo deve ter estado `:focus-visible` com anel claramente visível. Proibido `outline: none` sem alternativa. |
| Textos alternativos | Todo `<img>` de conteúdo deve ter `alt` descritivo. Imagens decorativas: `alt=""`. |
| Hierarquia de headings | Somente 1 H1 por página. H2 → H3 em ordem lógica, sem pular níveis. |
| Labels em formulários | Todo campo de formulário deve ter `<label>` associado via `for`/`id`. Nunca usar apenas `placeholder` como label. |
| Áreas de toque (mobile) | Mínimo 44×44px para qualquer elemento interativo. |
| Skip link | Link "Ir para o conteúdo principal" como primeiro elemento focável do DOM. |
| Linguagem da página | `<html lang="pt-BR">` |
| ARIA | Usar atributos ARIA apenas quando HTML semântico não for suficiente. Preferir `<button>` a `<div role="button">`. |

### Ferramentas de Verificação

- Lighthouse Accessibility (meta: ≥ 95)
- axe DevTools (zero erros críticos e graves)
- Teste manual com teclado (Tab, Enter, Escape, setas)

---

## 5. Motion (Animações e Transições)

### Durações

```css
:root {
  --duration-instant: 100ms;
  --duration-fast:    150ms;
  --duration-normal:  200ms;
  --duration-slow:    300ms;
  --duration-slower:  500ms;
}
```

### Easings

```css
:root {
  --ease-out:    cubic-bezier(0.0, 0.0, 0.2, 1);  /* Entrada de elementos */
  --ease-in:     cubic-bezier(0.4, 0.0, 1, 1);    /* Saída de elementos */
  --ease-in-out: cubic-bezier(0.4, 0.0, 0.2, 1);  /* Transições de estado */
  --ease-spring: cubic-bezier(0.34, 1.56, 0.64, 1); /* Feedback táctil (botões) */
}
```

### Padrões de Uso

| Tipo de animação | Duração | Easing |
|---|---|---|
| Hover em botões/cards | `--duration-normal` (200ms) | `--ease-out` |
| Abertura de dropdown/menu | `--duration-slow` (300ms) | `--ease-out` |
| Fechamento de dropdown/menu | `--duration-fast` (150ms) | `--ease-in` |
| Fade-in de toast/alerta | `--duration-slow` (300ms) | `--ease-out` |
| Transição de página (Astro View Transitions) | `--duration-slower` (500ms) | `--ease-in-out` |
| Scroll animations (reveal) | `--duration-slower` (500ms) | `--ease-out` |
| Transform de botão (active) | `--duration-instant` (100ms) | `--ease-spring` |

### Respeitar `prefers-reduced-motion`

```css
@media (prefers-reduced-motion: reduce) {
  *,
  *::before,
  *::after {
    animation-duration:   0.01ms !important;
    animation-iteration-count: 1 !important;
    transition-duration:  0.01ms !important;
    scroll-behavior:      auto !important;
  }
}
```

---

## 6. Grid e Layout

```css
:root {
  --container-max:  1280px;
  --container-pad:  var(--space-6);   /* 24px lateral no desktop */
  --grid-cols:      12;
  --grid-gap:       var(--space-6);   /* 24px entre colunas */
}

/* Mobile first */
.container {
  width:       100%;
  max-width:   var(--container-max);
  margin:      0 auto;
  padding-left:  var(--container-pad);
  padding-right: var(--container-pad);
}

/* Breakpoints */
/* sm:  640px  — tablet portrait */
/* md:  768px  — tablet landscape */
/* lg:  1024px — desktop pequeno */
/* xl:  1280px — desktop padrão */
/* 2xl: 1536px — desktop grande */
```

### Grids Comuns

```css
/* 3 colunas de cards (diferenciais, serviços) */
.grid-3 {
  display:               grid;
  grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
  gap:                   var(--grid-gap);
}

/* 2 colunas (sobre, conteúdo + imagem) */
.grid-2 {
  display:               grid;
  grid-template-columns: repeat(auto-fit, minmax(320px, 1fr));
  gap:                   var(--space-12);
  align-items:           center;
}
```

---

*Documento gerado pelo Consolidation Agent — Renovo Pipeline v0.2*
*Tenant ID: 902e4c7f-86c9-4be1-b7a3-b49226d4d479 | Attempt: 1*
