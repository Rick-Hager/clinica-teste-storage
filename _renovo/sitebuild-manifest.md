# Sitebuild Manifest — Clínica Teste Storage

**Tenant ID:** 902e4c7f-86c9-4be1-b7a3-b49226d4d479  
**Attempt:** 2  
**Fase:** sitebuild → deploy  
**Gerado por:** Sitebuild Agent — Renovo Pipeline v0.2

---

## 1. Arquivos Gerados

| Arquivo | Descrição |
|---|---|
| `public/favicon.svg` | Favicon SVG — cruz médica branca em fundo azul primário (#1B4F8A) |
| `src/styles/tokens.css` | CSS custom properties completos derivados de design-guidelines.md |
| `src/styles/global.css` | Reset, tipografia base, utilitários, botões, grids, forms, badges |
| `src/layouts/Base.astro` | Layout HTML shell: head (fonts, meta, schema), Header, Footer, FloatingCTAs |
| `src/components/Header.astro` | Header sticky com logo, nav desktop, dropdown de serviços, hamburger mobile |
| `src/components/Footer.astro` | Footer 4 colunas: brand + nav + serviços + contato; rodapé com CFM placeholder |
| `src/components/FloatingCTAs.astro` | FAB WhatsApp (desktop) + barra CTA mobile (Ligar / WhatsApp) |
| `src/components/SectionHeading.astro` | Componente reutilizável: overline + h2 + subtitle |
| `src/components/FeatureCard.astro` | Card de diferencial: ícone circular + título + texto |
| `src/components/ServiceCard.astro` | Card de serviço: ícone + título + texto + link |
| `src/components/StepCard.astro` | Card de passo: número + ícone + título + texto |
| `src/components/PageHero.astro` | Hero de páginas internas: gradiente + overline + H1 + subtitle |
| `src/components/CTABanner.astro` | Seção CTA dark: título + texto + 1-2 botões |
| `src/pages/index.astro` | Home (`/`) |
| `src/pages/sobre.astro` | Sobre (`/sobre`) |
| `src/pages/servicos/index.astro` | Listagem de Serviços (`/servicos`) |
| `src/pages/servicos/consulta-geral.astro` | Consulta de Clínica Geral (`/servicos/consulta-geral`) |
| `src/pages/servicos/check-up-preventivo.astro` | Check-up Preventivo (`/servicos/check-up-preventivo`) |
| `src/pages/servicos/telemedicina.astro` | Telemedicina (`/servicos/telemedicina`) |
| `src/pages/servicos/acompanhamento.astro` | Acompanhamento de Saúde (`/servicos/acompanhamento`) |
| `src/pages/servicos/exames-e-laudos.astro` | Exames e Laudos (`/servicos/exames-e-laudos`) |
| `src/pages/equipe.astro` | Nossa Equipe (`/equipe`) |
| `src/pages/contato.astro` | Contato e Agendamento (`/contato`) |
| `src/pages/privacidade.astro` | Política de Privacidade (`/privacidade`) |
| `src/pages/termos.astro` | Termos de Uso (`/termos`) — gerado como placeholder estruturado |
| `src/pages/blog/index.astro` | Blog (`/blog`) — placeholder "em breve" |
| `src/pages/agendamento.astro` | Agendamento (`/agendamento`) — 3 canais: WhatsApp, formulário, telefone |

**Total: 28 arquivos**

---

## 2. Mapeamento Página → Canônico de Origem

| Página | Seção de site-content.md utilizada |
|---|---|
| `index.astro` | Seções 1–6 da página Home: Hero, Diferenciais, Serviços, Como Funciona, Depoimentos, CTA Final |
| `sobre.astro` | Página Sobre: História, MVV, Equipe, Estrutura |
| `servicos/index.astro` | Página Serviços — listagem com copy da seção Serviços |
| `servicos/consulta-geral.astro` | Página Consulta de Clínica Geral: O que é, Quando consultar, Como funciona |
| `servicos/check-up-preventivo.astro` | Página Check-up Preventivo: O que é, Para quem, O que inclui, Periodicidade |
| `servicos/telemedicina.astro` | Página Telemedicina: O que é, Ideal para, Como funciona, Privacidade |
| `servicos/acompanhamento.astro` | Página Acompanhamento de Saúde: O que é, Condições, Como funciona |
| `servicos/exames-e-laudos.astro` | Página Exames e Laudos — conteúdo parcial (FAIL G compensado) |
| `equipe.astro` | Página Equipe — placeholder (FAIL G compensado) |
| `contato.astro` | Página Contato: canais, formulário LGPD, localização |
| `privacidade.astro` | Página Política de Privacidade — completa com placeholders `_____` |
| `termos.astro` | Gerado como placeholder estruturado (FAIL F compensado) |
| `blog/index.astro` | Placeholder "em breve" — sem conteúdo em site-content.md |
| `agendamento.astro` | Baseado em site-structure.md ("redirect para Calendly/WA") |

---

## 3. Decisões de Design

| Decisão | Justificativa |
|---|---|
| Cor primária `#1B4F8A` | Extraída de brand-book.md — "Azul Confiança"; confirmada em design-guidelines.md (`--color-primary`) |
| Cor secundária `#34A0A4` | Extraída de brand-book.md — "Teal Saúde"; usada em overlines, bordas de cards de serviço, ícones ativos |
| Cor de acento `#52B788` | Extraída de brand-book.md — "Verde Vitalidade"; usada em overlines no hero dark e elementos de confirmação |
| Gradiente hero `135deg #1B4F8A → #1A202C` | Conforme brand-book.md seção Gradientes; aplicado no hero da Home e PageHero |
| Fonte display: Playfair Display | Conforme brand-book.md e design-guidelines.md — titulações H1, H2, hero; Google Fonts |
| Fonte body: Inter 400/500/600/700 | Conforme brand-book.md e design-guidelines.md; Google Fonts |
| Hero sem imagem fotográfica | Imagem de fundo `[PREENCHER]` — substituída por gradiente CSS + decoração radial Teal (FAIL G, compensação 2) |
| Depoimentos em estado placeholder | 3 cards com avatar circular cinza e texto "Depoimento em breve" (FAIL G, compensação 3) |
| Cards de equipe com placeholder | Avatar + "Dr(a). A confirmar" + "CRM: a preencher" em `--color-gray-400` (FAIL G, compensação 5) |
| `[Cidade]` substituído por São Paulo | Compensação 1 do validation report |
| Dados de contato como "a preencher" | Telefone, e-mail, endereço, horários em `--color-gray-400` italic (FAIL G, compensação 6) |
| `/privacidade` — campos `_____` + banner | CNPJ, razão social, e-mail DPO com `_____`; banner de aviso no topo (FAIL G, compensação 7) |
| Footer CRM placeholder | "CRM: a preencher" em `--color-gray-400`; campo presente (CFM obrigatório) (FAIL G, compensação 8) |
| Convênios/valor — "Consulte nossa equipe" | Aplicado em consulta-geral.astro (FAIL G, compensação 9) |
| Telemedicina plataforma — omitida | Renderizado como "Plataforma a informar" (FAIL G, compensação 10) |
| `/termos` gerado como placeholder | Estrutura completa com seções padrão; dados a preencher pelo responsável jurídico (FAIL F, compensação F) |
| `/blog` como placeholder | Sem conteúdo em site-content.md; página "em breve" com CTA para contato |
| `/agendamento` com 3 opções | WhatsApp (primário), formulário, telefone — sem redirect externo pois URL do Calendly não fornecida |

---

## 4. Componentes e Onde São Usados

| Componente | Usado em |
|---|---|
| `Header.astro` | `Base.astro` (todas as páginas) |
| `Footer.astro` | `Base.astro` (todas as páginas) |
| `FloatingCTAs.astro` | `Base.astro` (todas as páginas) |
| `SectionHeading.astro` | `index.astro`, `sobre.astro`, `servicos/index.astro`, `equipe.astro` |
| `FeatureCard.astro` | `index.astro` (seção Diferenciais) |
| `ServiceCard.astro` | `index.astro` (seção Serviços), `servicos/index.astro` |
| `StepCard.astro` | `index.astro` (seção Como Funciona) |
| `PageHero.astro` | Todas as páginas internas (sobre, servicos/*, equipe, contato, privacidade, termos, blog, agendamento) |
| `CTABanner.astro` | `index.astro`, `sobre.astro`, `servicos/*.astro`, `equipe.astro`, `blog/index.astro` |

---

## 5. Compensações do Validation Report Aplicadas

| Código | Status | Ação tomada |
|---|---|---|
| FAIL F — `/termos` ausente | ✅ Compensado | Gerado `src/pages/termos.astro` com estrutura completa e banner de aviso |
| FAIL G — `[Cidade]` (12 ocorrências) | ✅ Compensado | Substituído por "São Paulo" em todos os `<title>` e `<meta description>` |
| FAIL G — Imagem hero `[PREENCHER]` | ✅ Compensado | Hero usa `--gradient-hero` CSS + decoração radial Teal — sem dependência externa |
| FAIL G — Depoimentos (3 slots) | ✅ Compensado | 3 cards placeholder com avatar cinza e texto "Depoimento em breve" |
| FAIL G — Exames e Laudos (conteúdo vazio) | ✅ Compensado | Página com `notice-banner` + parágrafo de fallback + CTA para /contato |
| FAIL G — Cards de equipe | ✅ Compensado | Avatares placeholder + "Dr(a). A confirmar" + "CRM: a preencher" |
| FAIL G — Dados de contato | ✅ Compensado | Campos renderizados como "A preencher" em `--color-gray-400` italic |
| FAIL G — Política de Privacidade | ✅ Compensado | Campos `[PREENCHER]` → `_____`; banner de aviso no topo |
| FAIL G — Footer CRM (CFM obrigatório) | ✅ Compensado | Campo presente com "CRM: a preencher" — estrutura mantida por exigência CFM |
| FAIL G — Convênios/valor consulta geral | ✅ Compensado | "Consulte nossa equipe" como fallback |
| FAIL G — Plataforma telemedicina | ✅ Compensado | "Plataforma a informar" renderizado em parágrafo placeholder |

---

## 6. Próximos Passos para o Cliente (Antes do Go-Live)

### Obrigatórios (bloqueantes)
- [ ] **CRM + Nome do Diretor Técnico Médico** — inserir no footer (exigência CFM nº 2.336/2023)
- [ ] **Política de Privacidade** — preencher razão social, CNPJ, endereço e e-mail do DPO
- [ ] **Termos de Uso** — revisar com responsável jurídico e preencher dados em branco
- [ ] **Dados de contato** — WhatsApp real, telefone, e-mail institucional, endereço com CEP
- [ ] **Horários de funcionamento** — inserir em `/contato` e Footer

### Alta prioridade
- [ ] **Fotos da clínica** — recepção, consultórios, sala de espera — substituir placeholders
- [ ] **Foto e dados da equipe** — nome, foto, CRM, RQE, especialidade e bio de cada profissional
- [ ] **Lista de convênios aceitos** — inserir em `/servicos/consulta-geral`
- [ ] **Valor das consultas** — inserir ou confirmar política de "consulte nossa equipe"
- [ ] **Exames e Laudos** — detalhar exames disponíveis na clínica e parceiros de encaminhamento
- [ ] **Plataforma de telemedicina** — definir e inserir nome/link em `/servicos/telemedicina`
- [ ] **WhatsApp real** — substituir `5511999999999` pelo número real em todos os hrefs
- [ ] **Instagram** — inserir URL real no Footer

### Recomendados
- [ ] **Depoimentos** — coletar autorização assinada dos pacientes e publicar (CFM nº 2.336/2023)
- [ ] **Integração do formulário de contato** — configurar backend (Formspree, EmailJS, Netlify Forms ou similar)
- [ ] **Google Analytics 4** — adicionar tag de medição no `<head>` de Base.astro
- [ ] **Google Search Console** — verificar propriedade após go-live
- [ ] **Google Meu Negócio** — criar/otimizar perfil com fotos reais
- [ ] **Favicon** — substituir o SVG placeholder por versão aprovada pelo designer
- [ ] **Imagem hero** — foto real da clínica (iluminada, acolhedora) com gradiente overlay
- [ ] **Sitemap XML** — configurar em astro.config.mjs (`@astrojs/sitemap`)
- [ ] **URL do Calendly** — se adotado, configurar link real em `/agendamento`
- [ ] **Historia da clínica** — preencher seção em `/sobre`
- [ ] **Blog** — publicar primeiros 4 artigos educativos (keywords locais)
- [ ] **Schema Markup** — revisar JSON-LD na home após preenchimento do endereço real

---

*Manifest gerado pelo Sitebuild Agent — Renovo Pipeline v0.2*  
*Tenant ID: 902e4c7f-86c9-4be1-b7a3-b49226d4d479 | Attempt: 2*
