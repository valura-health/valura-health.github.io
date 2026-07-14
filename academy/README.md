# Valura Academy — educação médica continuada

Plataforma da Valura (Dr. Igor Morais e Bernardo Tardin) para venda de aulas online
a alunos de graduação em medicina: aula semanal (vídeo, slides ou material) → pós-teste → certificado,
com assinatura de R$ 39,90/mês que inclui o acervo de diretrizes e referência (exclusivo da área
do aluno). Identidade **Cálice Solar** (mesma família do site institucional).

## Arquivos
- `index.html` — o aplicativo completo (SPA de arquivo único, sem dependências externas).
- `favicon.svg` — a marca (Cálice Solar).
- `docs/` — biblioteca de downloads (Nova AGA Completa SBGG 2023 + resumos FCMMG).
- `.nojekyll` — desliga o Jekyll no GitHub Pages.

## O que o MVP faz
- Home pública com notícias reais de inovação em medicina (curadas), plano e catálogo.
- Login/cadastro (simulado em `localStorage`), papéis aluno/professor.
- Catálogo com filtro por área; formato livre por aula — vídeo (embed YouTube/Vimeo), deck de
  slides navegável, vídeo + slides, ou só material de estudo (o rótulo é derivado do conteúdo).
- Pós-teste com feedback comentado — aprovação ≥ 70%, até 3 tentativas, liberado só após concluir a aula.
- Certificado em pergaminho, imprimível, com código de verificação (rotulado como demonstração).
- Central de referência: guidelines (AHA/ACC/ESC/SBC/SBGG/GOLD/ADA/KDIGO/IDSA/PCDT),
  ACR Appropriateness Criteria, Sanford Guide/Stanford Bugs & Drugs/Anvisa/interações, MDCalc, downloads.
- Administração (professores): CRUD de aulas e notícias, visão de alunos.

**Contas de demonstração** — aluno: `aluno@demo`/`demo` · professores: `igor@valura.health` ou
`bernardo@valura.health`/`valura2026`.

## Limitações conhecidas do MVP (decisão registrada)
- Gabarito, assinatura e certificado rodam no cliente (`localStorage`) — na Fase 2 migram para
  Supabase (região SP) com correção/emissão em Edge Function e RLS.
- Nenhum pagamento real: o fluxo de assinatura é simulado e **não coleta dado de cartão**.
  Produção: Mercado Pago Assinaturas (cartão ou Pix Automático).
- Senhas de demonstração em texto no seed — trocado por Supabase Auth na Fase 2.
- Vídeos: URL de incorporação (YouTube não listado/Vimeo) no MVP; Cloudflare Stream na produção.

Decisão de arquitetura: `Vault-Softwares/30-Decisoes/valura-academy-arquitetura.md`.
Requisitos: `Vault-Softwares/20-Requisitos/valura-academy-requisitos.md`.

## Publicar no GitHub Pages
1. Criar repositório (ex.: `valura-academy`) e enviar estes arquivos ao branch `main`.
2. Settings → Pages → Source: `Deploy from a branch` → `main` / `/ (root)`.
3. Em ~1 min: `https://<usuario>.github.io/valura-academy/`.
4. Domínio próprio (futuro): `academy.valura.health` (após registrar `valura.health`).
