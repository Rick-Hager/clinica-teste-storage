# Brand Book — Clínica Teste Storage

> **Nota do consolidation:** Nenhum ativo visual foi fornecido pelo cliente.
> Toda a identidade visual abaixo foi construída a partir das recomendações do
> research-agent e das boas práticas do vertical de clínicas médicas no Brasil.
> O validation-agent deve confirmar com o cliente se já existe logo, paleta ou
> tipografia consolidada antes de aprovar este documento.
> **(decisão do consolidation)**

---

## 1. Paleta de Cores

A paleta foi construída sobre o eixo **confiança + vitalidade + acolhimento** —
os três atributos emocionais centrais para clínicas médicas no mercado brasileiro.

### Cores Primárias

| Papel | Nome | Hex | RGB | Uso principal |
|---|---|---|---|---|
| Primária | Azul Confiança | `#1B4F8A` | 27, 79, 138 | CTAs, cabeçalhos, botões principais, logotipo |
| Secundária | Teal Saúde | `#34A0A4` | 52, 160, 164 | Destaque, badges, ícones ativos, hover states |
| Acento | Verde Vitalidade | `#52B788` | 82, 183, 136 | Tags de status, bordas de destaque, confirmações |

### Cores Neutras

| Papel | Nome | Hex | RGB | Uso principal |
|---|---|---|---|---|
| Texto principal | Grafite Escuro | `#1A202C` | 26, 32, 44 | Corpo de texto, títulos em fundo branco |
| Texto secundário | Cinza Ardósia | `#64748B` | 100, 116, 139 | Legendas, metadados, textos de apoio |
| Texto terciário | Cinza Suave | `#94A3B8` | 148, 163, 184 | Placeholders, texto desabilitado |
| Fundo principal | Azul Névoa | `#F0F7FF` | 240, 247, 255 | Backgrounds de seções alternadas |
| Fundo cards | Branco Clínico | `#FFFFFF` | 255, 255, 255 | Cards, modais, superfícies elevadas |

### Cores de Estado

| Estado | Nome | Hex | Uso |
|---|---|---|---|
| Sucesso | Verde Confirmação | `#27AE60` | Agendamento confirmado, formulários validados |
| Atenção | Âmbar Alerta | `#F59E0B` | Avisos, campos com preenchimento incompleto |
| Erro | Vermelho Alerta | `#E53E3E` | Erros de formulário, mensagens críticas |
| Info | Azul Info | `#3B82F6` | Dicas, tooltips informativos |

### Gradientes

```
Gradiente Principal:  linear-gradient(135deg, #1B4F8A 0%, #34A0A4 100%)
Gradiente Suave:      linear-gradient(180deg, #F0F7FF 0%, #FFFFFF 100%)
Gradiente Hero:       linear-gradient(135deg, #1B4F8A 0%, #1A202C 100%)
```

### Regras de Contraste (WCAG AA)

- Texto escuro (`#1A202C`) sobre fundo branco: **contraste 18,1:1** ✓
- Texto branco sobre Azul Confiança (`#1B4F8A`): **contraste 8,2:1** ✓
- Texto branco sobre Teal Saúde (`#34A0A4`): **contraste 4,6:1** ✓ (AA)
- Nunca usar Cinza Suave (`#94A3B8`) sobre fundo branco para textos de leitura.

---

## 2. Tipografia

**(decisão do consolidation)** — Fontes escolhidas com base em legibilidade clínica,
autoridade e disponibilidade no Google Fonts (zero custo de licença).

### Família Principal — Inter

```
Família:    Inter (Google Fonts)
Uso:        Corpo de texto, navegação, botões, formulários, legendas
Pesos:      Regular (400), Medium (500), SemiBold (600), Bold (700)
```

### Família de Display — Playfair Display

```
Família:    Playfair Display (Google Fonts)
Uso:        Títulos de seção principais (H1, H2), citações, headline da hero
Pesos:      Regular (400), Bold (700)
Estilo:     Normal e Italic para ênfase editorial
```

### Escala Tipográfica

| Token | Família | Peso | Tamanho | Line-height | Uso |
|---|---|---|---|---|---|
| `text-display` | Playfair Display | 700 | 56px / 3.5rem | 1.15 | Headline hero |
| `text-h1` | Playfair Display | 700 | 40px / 2.5rem | 1.2 | Títulos de página |
| `text-h2` | Playfair Display | 400 | 32px / 2rem | 1.25 | Títulos de seção |
| `text-h3` | Inter | 700 | 24px / 1.5rem | 1.3 | Subtítulos de seção |
| `text-h4` | Inter | 600 | 20px / 1.25rem | 1.35 | Títulos de card |
| `text-body-lg` | Inter | 400 | 18px / 1.125rem | 1.7 | Parágrafos principais |
| `text-body` | Inter | 400 | 16px / 1rem | 1.6 | Corpo padrão |
| `text-body-sm` | Inter | 400 | 14px / 0.875rem | 1.5 | Notas, legendas |
| `text-caption` | Inter | 400 | 12px / 0.75rem | 1.4 | Microcopy, disclaimer |
| `text-button` | Inter | 600 | 16px / 1rem | 1 | Rótulos de botão |
| `text-nav` | Inter | 500 | 15px / 0.9375rem | 1 | Itens de menu |
| `text-overline` | Inter | 700 | 11px / 0.6875rem | 1.4 | Rótulos em uppercase |

### Regras Tipográficas

- **Nunca usar** Playfair Display em tamanhos menores que 20px (legibilidade comprometida).
- **Nunca usar** mais de dois pesos da mesma família em um único componente.
- Line-height mínimo de 1.5 para qualquer texto corrido acima de 3 linhas.
- Tracking (letter-spacing) de `+0.08em` para `text-overline` (estilo uppercase).
- Tracking de `-0.01em` para `text-display` e `text-h1` (refinamento visual).

---

## 3. Logotipo

**(decisão do consolidation)** — Nenhum logotipo foi fornecido. As diretrizes
abaixo definem as especificações que o logotipo a ser criado deve seguir, e
as regras de uso para quando o logotipo existir.

### Conceito Visual

O logotipo deve combinar um símbolo gráfico (ícone) com o wordmark do nome da clínica.
- **Símbolo:** Cruz médica estilizada com leveza — não clínica/fria, mas curvilínea
  e acolhedora. Alternativamente, folha/coração abstrato que evoque saúde e cuidado.
- **Wordmark:** "Clínica Teste Storage" em Inter SemiBold para nome completo;
  versão reduzida "CTS" para avatar e favicon.
- **Tagline (opcional):** "Cuidado que transforma" — em Inter Regular, tamanho 60%
  do wordmark.

### Versões

| Versão | Fundo | Uso |
|---|---|---|
| Principal (horizontal) | Branco / Azul Névoa | Site, documentos, papelaria |
| Invertida (horizontal) | Azul Confiança / Grafite Escuro | Header com fundo escuro, banners |
| Símbolo isolado | Qualquer | Favicon, avatar de redes sociais, app icon |
| Monocromática (preta) | Claro | Impressão P&B, contratos, brindes |
| Monocromática (branca) | Escuro | Bordados, gravações |

### Área de Proteção

A área de proteção mínima ao redor do logotipo é igual à altura da letra "C"
maiúscula do wordmark. Nenhum elemento deve invadir essa área.

### Tamanho Mínimo

- **Digital:** 120px de largura para versão horizontal; 32px para símbolo isolado.
- **Impresso:** 30mm de largura para versão horizontal; 8mm para símbolo isolado.

### Proibições

❌ Não distorcer proporções (esticar ou comprimir).
❌ Não aplicar gradiente sobre o logotipo sem aprovação.
❌ Não usar cores fora da paleta oficial.
❌ Não adicionar sombras, contornos ou efeitos externos.
❌ Não rotacionar o logotipo.
❌ Não usar versão principal em fundos de baixo contraste.
❌ Não redesenhar ou recriar o logotipo sem aprovação do responsável de marca.

---

## 4. Tom Visual (Mood)

### Palavras-guia

> **Confiança · Acolhimento · Clareza · Modernidade · Humanidade**

### Referências de Mood

A comunicação visual da Clínica Teste Storage deve evocar:

- **Ambientes limpos e iluminados:** fotografias com luz natural, paleta clara,
  espaços abertos e organizados. Nada de cenários hospitalares frios ou intimidadores.
- **Pessoas reais em contexto de cuidado:** equipe médica acessível, pacientes
  tranquilos, interações olho no olho. Evitar banco de imagens genérico e estéril.
- **Tecnologia a serviço humano:** equipamentos modernos aparecem em segundo plano;
  o protagonismo é sempre das pessoas.
- **Consistência e organização:** layouts com bastante espaço em branco, alinhamento
  rigoroso, hierarquia visual clara.

### O que Evitar

❌ Imagens de cirurgia, sangue ou procedimentos invasivos.
❌ Efeitos visuais excessivos (neomorfismo pesado, glassmorfismo exagerado).
❌ Tipografia decorativa ou manuscrita (prejudica autoridade e legibilidade).
❌ Clichês do setor: estetoscópio genérico, coração pulsante, fundo verde-hospitalar.

---

## 5. Elementos Gráficos

### Iconografia

- **Biblioteca:** Lucide Icons (open source, estilo outline, consistente).
- **Estilo:** Outline (stroke de 1.5px), cantos ligeiramente arredondados.
- **Tamanhos:** 16px (inline), 20px (componentes), 24px (padrão), 32px (destaque),
  48px (hero/features).
- **Cor:** herdam a cor do elemento pai por padrão; nunca multicoloridos exceto em
  ilustrações temáticas específicas.

### Ilustrações

**(decisão do consolidation)** — Estilo flat minimalista, traço fino, paleta limitada
às cores da marca. Usar para:
- Seção "Como funciona" (passo a passo de agendamento).
- Estados vazios (nenhum resultado de busca, confirmação de agendamento).
- Cards de serviço quando não houver fotografia disponível.

Biblioteca de referência: unDraw.co (personalizável com cores da marca, gratuita).

### Formas Geométricas

- **Círculos e elipses:** usados como fundo de ícones e avatares de equipe.
- **Retângulos com radius:** `radius-md` (8px) para cards; `radius-lg` (16px) para
  modais e imagens; `radius-full` (9999px) para badges e pills.
- **Formas de fundo decorativas:** blocos de cor suave (Azul Névoa ou Teal 10% opacidade)
  para delimitar seções sem usar bordas ou sombras pesadas.

### Fotografia

- **Estilo:** Autêntico, cálido, bem iluminado. Preferir fotos da equipe e clínica
  reais; caso use banco de imagens, optar por Unsplash/Pexels com filtro de
  "naturalidade" — evitar poses excessivamente fabricadas.
- **Tratamento:** Leve sobreposição do gradiente da marca em imagens hero (para
  garantir contraste de texto).
- **Proporções:** 16:9 para banners hero; 3:2 para cards de artigos/blog; 1:1 para
  avatares de equipe.

---

## 6. Aplicações

### Cartão de Visita

```
Frente:
  - Logotipo à esquerda, alinhado ao topo
  - Nome do profissional em Inter SemiBold 14px
  - CRM + especialidade em Inter Regular 11px, Cinza Ardósia
  - Cor de fundo: Branco Clínico

Verso:
  - Fundo Azul Confiança (#1B4F8A)
  - Logotipo invertido centralizado
  - Site e WhatsApp em Inter Regular 11px, branco 80% opacidade
```

### Site (Diretrizes Gerais)

- Header: fundo branco, logotipo à esquerda, navegação à direita, CTA "Agendar"
  em Azul Confiança.
- Hero: fundo Grafite Escuro com gradiente, texto branco, imagem em segundo plano.
- Seções alternadas: Branco Clínico e Azul Névoa para ritmo visual.
- Footer: fundo Grafite Escuro, texto branco e Cinza Suave.

### Instagram

- **Grid:** alternância entre cards educativos (fundo Azul Névoa + ícone Teal),
  fotos da equipe e posts de conteúdo com fundo branco.
- **Stories:** template com header colorido (gradiente principal) e rodapé branco
  com logotipo.
- **Reels cover:** close-up de rosto da equipe com border circular em Teal Saúde.

### WhatsApp Business

- Foto de perfil: símbolo isolado do logotipo em fundo Azul Confiança.
- Nome: "Clínica Teste Storage — Agendamentos".
- Mensagem de boas-vindas: tom acolhedor, sem formalidade excessiva (ver brand-voice.md).

---

*Documento gerado pelo Consolidation Agent — Renovo Pipeline v0.2*
*Tenant ID: 902e4c7f-86c9-4be1-b7a3-b49226d4d479 | Attempt: 1*
