# 🎨 Branco's Design System

**Version 1.0.0** · Mobile & Desktop

Sistema de design completo com tokens, componentes e padrões prontos para uso.

---

## 📁 Arquivos

| Arquivo | Descrição |
|---|---|
| `tokens.css` | Todas as variáveis CSS (cores, tipografia, espaçamento, sombras, etc.) |
| `components.css` | Classes de componentes prontas para uso |
| `index.html` | Showcase interativo com todos os componentes |

---

## 🚀 Como usar

### 1. Importe os arquivos no seu HTML

```html
<link rel="stylesheet" href="tokens.css" />
<link rel="stylesheet" href="components.css" />
```

### 2. Importe as fontes (opcional, recomendado)

```html
<link href="https://fonts.googleapis.com/css2?family=Sora:wght@400;600;700;800&family=DM+Sans:wght@400;500;600&family=JetBrains+Mono:wght@400;500&display=swap" rel="stylesheet" />
```

### 3. Use os tokens e classes

```html
<!-- Botões -->
<button class="ds-btn ds-btn--primary ds-btn--md">Confirmar</button>
<button class="ds-btn ds-btn--secondary ds-btn--md">Cancelar</button>

<!-- Cards -->
<div class="ds-card">
  <div class="ds-card__body">Conteúdo</div>
</div>

<!-- Badges -->
<span class="ds-badge ds-badge--success ds-badge--dot">Ativo</span>
```

---

## 🌗 Dark Mode

O dark mode é ativado adicionando `data-theme="dark"` no elemento `<html>`:

```html
<html data-theme="dark">
```

Para alternar via JavaScript:
```javascript
document.documentElement.setAttribute('data-theme', 'dark');
```

---

## 🎨 Tokens Principais

### Cores

```css
/* Brand */
var(--color-brand-500)   /* #4a6cf7 — primária */
var(--color-brand-600)   /* hover */

/* Semânticas */
var(--color-success-base) /* #22c55e */
var(--color-warning-base) /* #f59e0b */
var(--color-error-base)   /* #ef4444 */
var(--color-info-base)    /* #3b82f6 */

/* Superfícies */
var(--surface-page)       /* fundo principal */
var(--surface-subtle)     /* fundo alternado */
var(--surface-muted)      /* fundo desabilitado */

/* Texto */
var(--text-primary)       /* texto principal */
var(--text-secondary)     /* texto auxiliar */
var(--text-tertiary)      /* texto desabilitado */
```

### Tipografia

```css
--font-display: 'Sora'     /* headings, display */
--font-body:    'DM Sans'  /* corpo de texto */
--font-mono:    'JetBrains Mono'  /* código */
```

### Espaçamento (base 4px)

```css
--space-1:  4px
--space-2:  8px
--space-3:  12px
--space-4:  16px
--space-6:  24px
--space-8:  32px
--space-10: 40px
--space-12: 48px
--space-16: 64px
```

---

## 📱 Breakpoints (Mobile-first)

| Token | Tamanho | Uso |
|---|---|---|
| `--container-xs` | 320px | Smartphones pequenos |
| `--container-sm` | 480px | Smartphones |
| `--container-md` | 768px | Tablets |
| `--container-lg` | 1024px | Laptops |
| `--container-xl` | 1280px | Desktops |
| `--container-2xl` | 1440px | Telas largas |

```css
/* Exemplo mobile-first */
@media (min-width: 768px)  { /* tablet+ */ }
@media (min-width: 1024px) { /* desktop+ */ }
@media (min-width: 1280px) { /* wide+ */ }
```

---

## 🧩 Componentes Disponíveis

### Fundação
- **Tokens CSS** — cores, tipografia, espaçamento, raios, sombras, z-index, animações
- **Reset & Base** — normalize e estilos base

### Tipografia
- `.ds-display-xl/lg/md` — títulos hero
- `.ds-heading-xl/lg/md/sm` — títulos de seção
- `.ds-body-lg/md/sm/xs` — texto de conteúdo
- `.ds-label-lg/md` — labels e tags
- `.ds-code` — código inline

### Botões
- `.ds-btn` + variante (`--primary`, `--secondary`, `--ghost`, `--neutral`, `--destructive`)
- Tamanhos: `--xs`, `--sm`, `--md`, `--lg`, `--xl`
- Modificadores: `--icon`, `--full`, `--loading`

### Formulários
- `.ds-field` — wrapper de campo
- `.ds-label` + `.ds-label--required`
- `.ds-input` / `.ds-select` / `.ds-textarea`
- `.ds-input-wrapper` — input com ícone
- `.ds-hint` — mensagem auxiliar/erro/sucesso
- `.ds-check-group` — checkbox
- `.ds-radio-group` — radio
- `.ds-toggle` — switch/toggle

### Cards
- `.ds-card` + `.ds-card__header` + `.ds-card__body` + `.ds-card__footer`
- Variantes: `--elevated`, `--flat`, `--subtle`, `--interactive`

### Feedback
- `.ds-badge` (6 variantes + `--dot`)
- `.ds-alert` (4 variantes)
- `.ds-toast` / `.ds-toast-container`
- `.ds-progress` + `.ds-progress__fill`
- `.ds-skeleton` (loading state)

### Navegação
- `.ds-tabs` + `.ds-tabs__list` + `.ds-tabs__tab`
- `.ds-breadcrumb`
- `.ds-sidebar` (desktop)
- `.ds-bottom-nav` (mobile)
- `.ds-index-bar` (scroll alfabético mobile)
- `.ds-topnav` (header desktop)

### Overlays
- `.ds-backdrop` + `.ds-modal`
- `.ds-menu` (dropdown)
- `.ds-tooltip`

### Data
- `.ds-table-wrapper` + `.ds-table`
- `.ds-avatar` + `.ds-avatar-group`
- `.ds-divider`

---

## 🛠 Customização

Para adaptar o DS ao seu projeto, sobrescreva as variáveis em `:root`:

```css
:root {
  /* Troque a cor primária */
  --color-brand-500: #7c3aed;  /* roxo */
  --color-brand-600: #6d28d9;

  /* Troque a fonte */
  --font-display: 'Playfair Display', serif;
  --font-body: 'Inter', sans-serif;
}
```

---

## ♿ Acessibilidade

- Todos os componentes suportam `:focus-visible`
- Contraste mínimo WCAG 2.1 AA em tokens de texto
- `.ds-sr-only` para conteúdo screen-reader only
- Roles ARIA nos componentes interativos
- Redução de movimento respeitada via `prefers-reduced-motion`
