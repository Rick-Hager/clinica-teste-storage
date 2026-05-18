# Validation Report — Clínica Teste Storage — attempt 1

**Severidade máxima:** FAIL
**Critérios FAIL:** F (Estrutura incompleta), G (Placeholders presentes)
**Critérios WARN:** nenhum
**Marcadores de decisão pendente:**
- brand-book.md: (1) identidade visual construída sem ativos do cliente; (2) tipografia definida pelo consolidation; (3) logotipo inexistente — especificação criada; (4) estilo de ilustrações definido pelo consolidation
- strategy.md: (5) framework estratégico construído sem dados proprietários; (6) ICP baseado em perfil médio do vertical; (7) diferenciação derivada de oportunidades do research-agent
- business-goals.md: (8) metas são benchmarks do setor, não metas reais do cliente; (9) benchmarks financeiros a confirmar; (10) iniciativas sem datas
- brand-voice.md: (11) tom construído sobre recomendações do research-agent
- site-content.md: (12) conteúdo redigido integralmente sem dados do cliente; (13) nota CFM sobre depoimentos; (14) nota CFM sobre apresentação de médicos/equipe

---

## Detalhes por critério

### A) Identidade consistente — OK
"Clínica Teste Storage" aparece nominalmente em strategy.md (seções de missão, posicionamento e promessa de marca), business-goals.md (seções de metas e iniciativas) e site-content.md (hero, subtítulos, metas SEO e textos de todas as páginas). Nenhuma divergência entre nome fantasia do tenant e o nome utilizado nos canônicos.

### B) Paleta de cores casa — OK
Todas as 12 cores da paleta de brand-book.md possuem tokens CSS exatos em design-guidelines.md: #1B4F8A (`--color-primary`), #34A0A4 (`--color-secondary`), #52B788 (`--color-accent`), #1A202C (`--color-gray-900`), #64748B (`--color-gray-600`), #94A3B8 (`--color-gray-400`), #F0F7FF (`--color-gray-100`), #FFFFFF (`--color-white`), #27AE60 (`--color-success`), #F59E0B (`--color-warning`), #E53E3E (`--color-error`), #3B82F6 (`--color-info`). Os tokens extras `_hover` e `_light` (ex.: #153E6E, #E8F0FA) são derivações de tint/shade legítimas para estados de UI — não constituem "cores fantasma". O #25D366 (WhatsApp) é cor de marca externa esperada, não pertence à paleta da clínica. Os três gradientes de brand-book.md estão exatamente reproduzidos em `--gradient-primary`, `--gradient-soft` e `--gradient-hero`.

### C) Tipografia casa — OK
brand-book.md define duas famílias: **Inter** (corpo, navegação, botões) e **Playfair Display** (títulos de exibição, H1, H2). design-guidelines.md espelha exatamente: `--font-body: 'Inter', system-ui, -apple-system, sans-serif` e `--font-display: 'Playfair Display', Georgia, serif`. Escala tipográfica (tamanhos, pesos, line-heights, letter-spacings) é consistente entre os dois documentos.

### D) Tom consistente — OK
brand-voice.md define personalidade "médico de família experiente e atualizado" — acolhedor, competente, claro, direto, humano — posicionado em "profissional-caloroso" no espectro formal/informal. site-content.md reflete esse tom de forma coerente: hero usa "atendimento que realmente escuta" (humanização sem sensacionalismo), textos de serviço são descritivos e diretos ("Você agenda online ou pelo WhatsApp em minutos"), CTAs são convidativos sem urgência artificial ("Agende minha primeira consulta"), a seção de telemedicina usa "segura, regularizada e tão eficaz" em vez de "é o futuro da medicina hoje!" — alinhado às proibições de brand-voice.md. Não foram identificados trechos com tom discordante.

### E) ICP coerente — OK
strategy.md descreve a persona principal "Carla, 38 anos" — profissional ativa, classe B/C+, motivada por prevenção, pesquisa no Google, usa WhatsApp diariamente, valoriza rapidez e conveniência. site-content.md é coerente: o check-up preventivo é indicado especificamente para "profissionais com rotina estressante e pouco tempo para acompanhamento médico"; o passo a passo de agendamento enfatiza agilidade; WhatsApp aparece como canal primário em todas as páginas; o tom de prevenção proativa ("Não espere os sintomas aparecerem") está alinhado com a motivação de prevenção e qualidade de vida da persona. A persona secundária "Roberto, 52 anos" é atendida pela seção de Acompanhamento de Saúde (condições crônicas).

### F) Estrutura incompleta — FAIL
**Página ausente:** `/termos` (Termos de Uso) está listada em site-structure.md — aparece no footer em `"Política de Privacidade | Termos de Uso"` — mas não existe conteúdo correspondente em site-content.md. A Política de Privacidade (`/privacidade`) tem conteúdo completo; os Termos de Uso não. Adicionalmente, `/blog` e `/agendamento` estão em site-structure.md sem conteúdo em site-content.md, porém site-structure.md contém notas explícitas de opcionalidade ("opcionais para o MVP") e redirect ("redirect para Calendly/WA"), respectivamente — essas duas ausências são intencionais e documentadas. A ausência de `/termos` não está documentada como intencional.

### G) Sem placeholders — FAIL
**site-content.md** contém **30+ marcadores `[PREENCHER]`** e **`[Cidade]`** distribuídos em todas as páginas:
- Home: imagem de fundo da hero; exames e laudos (card na seção de serviços); 3 depoimentos completos
- Sobre: história real da clínica; cards de médicos (foto, nome, CRM, RQE, bio); descrição de espaços físicos; fotos da estrutura
- Serviços: `/servicos/consulta-geral` — lista de convênios aceitos e valor particular; `/servicos/check-up-preventivo` — lista de exames incluídos no pacote; `/servicos/telemedicina` — plataforma de telemedicina adotada; `/servicos/acompanhamento` — outras condições tratadas; `/servicos/exames-e-laudos` — subtítulo e descrição inteira
- Equipe: todos os profissionais (foto, nome, especialidade, CRM, RQE, formação, bio)
- Contato: horário de funcionamento do WhatsApp, número de telefone, e-mail institucional, endereço completo com CEP, horários de atendimento, como chegar
- Privacidade: razão social, CNPJ, endereço, e-mail de exercício de direitos LGPD, data de publicação
- Meta SEO: `[Cidade]` em todos os `<title>` e `<meta description>` (12 ocorrências)

**site-structure.md** contém `CRM nº [XXX] — Dr(a). [Nome]` no footer (dado obrigatório por CFM nº 2.336/2023).

---

## Compensações sugeridas ao sitebuild

### FAIL F — Página `/termos` ausente em site-content.md
**Ação:** Gerar conteúdo placeholder estruturado para `/termos` durante o sitebuild, usando como base o conteúdo de `/privacidade` já existente. O arquivo `/termos` deve incluir: título "Termos de Uso — Clínica Teste Storage", data de última atualização como `[PREENCHER]`, seções padrão (Aceitação dos Termos, Uso do Site, Propriedade Intelectual, Limitação de Responsabilidade, Lei Aplicável) em branco/com texto genérico, e CTA para contato com a clínica. O link no footer deve apontar para `/termos` e permanecer funcional mesmo que o conteúdo seja provisório.

### FAIL G — Múltiplos [PREENCHER] e [Cidade] em site-content.md e site-structure.md

1. **`[Cidade]` nos meta SEO (12 ocorrências):** sitebuild deve substituir por `São Paulo` como fallback seguro genérico, ou deixar o campo vazio sem o placeholder visível. Não renderizar o token literal `[Cidade]` no HTML final. Critério: todas as tags `<title>` e `<meta name="description">`.

2. **Imagem de fundo da hero em Home:** sitebuild deve usar imagem de banco de imagens (Unsplash/Pexels, critério de "naturalidade" conforme brand-book.md) como fallback — ambiente clínico iluminado, pessoas reais. Aplicar o gradiente `--gradient-hero` sobre a imagem conforme design-guidelines.md para garantir contraste de texto.

3. **Depoimentos (3 slots em Home):** sitebuild deve renderizar a seção de depoimentos em estado "aguardando" — exibir 3 cards com avatar placeholder circular em `--color-gray-100` e texto "Depoimento em breve" em `--color-gray-400`. Não omitir a seção; manter estrutura visual.

4. **Exames e Laudos (`/servicos/exames-e-laudos`):** subtítulo e body inteiros são `[PREENCHER]`. Sitebuild deve renderizar a página com headline H1 presente ("Exames e Laudos") e um parágrafo de fallback: "Em breve, mais informações sobre os exames disponíveis na clínica. Entre em contato para saber mais." + CTA para `/contato`.

5. **Cards de Equipe (`/equipe` e seção em `/sobre`):** sitebuild deve renderizar cards com avatar circular placeholder (`--color-gray-100`, ícone de pessoa em `--color-gray-400`), nome "Dr(a). [A confirmar]" e CRM "[A confirmar]" em `--color-gray-400`. Não omitir a seção — manter estrutura do grid.

6. **Dados de Contato (WhatsApp, telefone, e-mail, endereço, horários):** sitebuild deve renderizar a página `/contato` com os cards de canal visíveis, mas os campos de número/e-mail/endereço devem exibir "A preencher" em `--color-gray-400` (italic). O formulário de contato pode ser construído normalmente — não depende desses dados. O mapa embed deve ser omitido até que o endereço seja fornecido.

7. **Política de Privacidade (`/privacidade`) — CNPJ, razão social, endereço, e-mail, data:** sitebuild deve renderizar a página com os campos `[PREENCHER]` substituídos por `_____` (underline) em `--color-gray-400` — visualmente indicam lacuna sem expor o token literal. Adicionar banner de aviso no topo: "Esta política está em revisão. Entre em contato para mais informações."

8. **`CRM nº [XXX] — Dr(a). [Nome]` no footer (obrigatório CFM):** sitebuild deve renderizar o footer com este campo como "CRM: a preencher" em `--color-gray-400`. Não omitir o campo — sua presença é obrigatória pela Resolução CFM nº 2.336/2023; apenas o dado precisa ser fornecido pelo cliente antes do go-live.

9. **`/servicos/consulta-geral` — convênios e valor:** sitebuild deve renderizar "Convênios: consulte nossa equipe" e "Valor: consulte nossa equipe" como fallback até receber os dados reais.

10. **`/servicos/telemedicina` — plataforma:** sitebuild deve omitir o campo "Tecnologia utilizada" ou renderizar como "Plataforma a informar" até que o cliente defina.

---

*Relatório gerado pelo Validation Agent — Renovo Pipeline v0.2*
*Tenant ID: 902e4c7f-86c9-4be1-b7a3-b49226d4d479 | Attempt: 1*
