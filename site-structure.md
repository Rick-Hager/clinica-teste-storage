# Site Structure — Clínica Teste Storage

> **Nota do consolidation:** Estrutura construída sobre as boas práticas do vertical
> (site próprio com foco em conversão via WhatsApp/agendamento, mobile-first) e
> na estratégia de posicionamento definida em strategy.md.
> **(decisão do consolidation)**

---

## 1. Hierarquia de URLs

```
/                          → Home
/sobre                     → Sobre a Clínica
/servicos                  → Serviços (listagem)
  /servicos/consulta-geral           → Consultas de Clínica Geral
  /servicos/check-up-preventivo      → Check-up Preventivo
  /servicos/telemedicina             → Telemedicina
  /servicos/acompanhamento           → Acompanhamento de Saúde
  /servicos/exames-e-laudos          → Exames e Laudos
/equipe                    → Nossa Equipe
/blog                      → Blog (conteúdo educativo)
  /blog/[slug]             → Artigo individual
/contato                   → Contato e Agendamento
/agendamento               → Página de agendamento online (ou redirect para Calendly/WA)
/privacidade               → Política de Privacidade (LGPD)
/termos                    → Termos de Uso
```

> **Nota:** As páginas `/equipe` e `/blog` são opcionais para o MVP; podem ser
> implantadas em fase posterior. As páginas de serviços individuais são prioritárias
> para SEO local.

---

## 2. Menu Principal (Header)

### Desktop

```
[Logo]    Início   Sobre   Serviços ▾   Equipe   Blog   Contato   [Agendar Consulta →]
```

- **Serviços** possui dropdown com os 5 serviços listados.
- **"Agendar Consulta"** é um botão CTA com estilo primário (Azul Confiança).
- Menu fixo (sticky) ao scroll.

### Mobile (Hamburger Menu)

```
[Logo]                              [☰]

— Drawer lateral —
Início
Sobre
Serviços
  → Consulta Geral
  → Check-up Preventivo
  → Telemedicina
  → Acompanhamento de Saúde
  → Exames e Laudos
Equipe
Blog
Contato

[Agendar Consulta — botão CTA completo]
[Ícone WhatsApp — botão secundário]
```

---

## 3. Footer

### Estrutura

```
┌─────────────────────────────────────────────────────────────────┐
│  [Logo + Tagline]                                               │
│  "Cuidado que transforma. Tecnologia que facilita."             │
│                                                                 │
│  Navegação         Serviços             Contato                 │
│  ─────────         ────────             ───────                 │
│  Início            Consulta Geral       Endereço completo        │
│  Sobre             Check-up             Telefone                 │
│  Equipe            Telemedicina         WhatsApp                 │
│  Blog              Acompanhamento       E-mail                   │
│  Contato           Exames e Laudos      Horários                 │
│                                                                 │
│  Redes sociais: [Instagram] [WhatsApp]                          │
│                                                                 │
│  ─────────────────────────────────────────────────────────────  │
│  © 2025 Clínica Teste Storage. CRM nº [XXX] — Dr(a). [Nome]    │
│  Política de Privacidade | Termos de Uso                        │
└─────────────────────────────────────────────────────────────────┘
```

> **Obrigatório (CFM nº 2.336/2023):** Nome e CRM do Diretor Técnico Médico
> devem constar no rodapé do site.

---

## 4. CTAs Fixas (Persistentes)

### Botão Flutuante WhatsApp

- Posição: **canto inferior direito**, fixo ao scroll, presente em todas as páginas.
- Ícone: logo do WhatsApp.
- Tooltip ao hover: "Agendar pelo WhatsApp".
- Cor de fundo: `#25D366` (verde oficial do WhatsApp).
- Visível em desktop e mobile.

### Barra de CTA Mobile (Fundo da Tela)

Em mobile, exibir barra fixa no fundo com dois botões:
```
[📱 Ligar agora]    [💬 Agendar no WhatsApp]
```

---

## 5. Fluxos de Jornada do Visitante

### Jornada 1 — Novo Paciente em Busca de Consulta

```
Pesquisa no Google
  → Clica no site (orgânico ou GMB)
    → Home (lê hero + benefícios)
      → Clica em "Ver nossos serviços" ou no card do serviço relevante
        → Página do Serviço (lê descrição, equipe, CTA)
          → Clica "Agendar Consulta"
            → Página de Agendamento / WhatsApp
              → Confirmação de agendamento
```

### Jornada 2 — Paciente que Quer Saber Mais Antes de Decidir

```
Pesquisa no Google (dúvida de saúde)
  → Cai no Blog (artigo educativo)
    → Lê artigo completo
      → Vê CTA ao final: "Precisa de avaliação médica? Agende com a gente."
        → Clica em CTA
          → Página de Agendamento / WhatsApp
```

### Jornada 3 — Indicação (Chega pelo Nome da Clínica)

```
Indicação de amigo ou médico
  → Pesquisa "Clínica Teste Storage" no Google
    → Clica no site (resultado de marca)
      → Home → Sobre (valida credibilidade)
        → Equipe (confirma profissional de interesse)
          → CTA de Agendamento
```

### Jornada 4 — Retorno de Paciente

```
Mensagem de WhatsApp automática (lembrete de retorno)
  → Acessa link direto para agendamento
    → Seleciona horário disponível
      → Confirmação automática
```

---

## 6. Regras de SEO On-Page

| Elemento | Regra |
|---|---|
| `<title>` | Padrão: "[Nome da Página] — Clínica Teste Storage | [Cidade]" |
| `<meta description>` | 150–160 caracteres; incluir especialidade + localização + CTA |
| H1 | Apenas 1 por página; incluir keyword principal |
| H2 / H3 | Hierarquia lógica; H2 para seções principais de cada página |
| URLs | Slug em português, sem acento, sem underline: `/servicos/check-up-preventivo` |
| Alt text de imagens | Descritivo + contextual; nunca vazio em imagens de conteúdo |
| Schema Markup | `LocalBusiness` + `MedicalClinic` na home; `MedicalWebPage` nas páginas de serviço |
| Sitemap XML | Gerado automaticamente pelo Astro; incluir todas as URLs públicas |
| Robots.txt | Bloquear `/agendamento/confirmacao` e URLs de parâmetros de UTM |

---

## 7. Performance e Acessibilidade

| Requisito | Meta |
|---|---|
| Core Web Vitals (LCP) | ≤ 2.5s |
| Core Web Vitals (CLS) | ≤ 0.1 |
| Core Web Vitals (FID/INP) | ≤ 200ms |
| Lighthouse Performance | ≥ 90 (mobile) |
| Lighthouse Accessibility | ≥ 95 |
| Imagens | WebP/AVIF, lazy loading, dimensões explícitas no HTML |
| Fontes | `font-display: swap`; preload das duas famílias tipográficas |

---

*Documento gerado pelo Consolidation Agent — Renovo Pipeline v0.2*
*Tenant ID: 902e4c7f-86c9-4be1-b7a3-b49226d4d479 | Attempt: 1*
