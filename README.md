# Valura — site institucional

Site da Valura (saúde baseada em valor), na identidade **Cálice Solar**. Arquitetura
**hub-and-spoke** (2026-07-16): a home faz a triagem por público; cada página segue o
público até o fim, sem misturar linguagem de paciente com linguagem de investidor.
Estático, sem dependências (HTML/CSS/JS inline por página, SVG). Pronto para GitHub Pages.

## Arquivos
- `index.html` — home: hero + as 3 portas, fundadores (autoridade), "quem somos" e princípios.
- `consultas.html` — porta do paciente: quem atende, onde, quanto custa, como agendar.
- `instituicoes.html` — porta de hospitais/operadoras: eficiência auditável, EBITDA/sinistralidade.
- `tese.html` — porta de investidor/imprensa/talento: manifesto, pilares, verticalização (Fases 0–5).
- `academy/` — Valura Academy, produto separado (não editado por este README).
- `favicon.svg` — a marca (Cálice Solar) para a aba/atalho.
- `.nojekyll` — desliga o Jekyll no GitHub Pages (servimos HTML puro).

Cada página é um arquivo HTML autossuficiente (CSS e JS inline, duplicados entre páginas
de propósito — zero build, zero dependência externa). Nav, bloco de contato (WhatsApp) e
rodapé são idênticos em todas as páginas (WCAG 3.2.6 — Ajuda Consistente).

## Publicar no GitHub Pages
1. Criar repositório (ex.: `valura-site`) e enviar estes arquivos ao branch `main`.
2. Settings → Pages → Source: `Deploy from a branch` → `main` / `/ (root)`.
3. Em ~1 min o site fica em `https://<usuario>.github.io/valura-site/`.

## Domínio próprio (opcional)
- Comprar `valura.health` (ou similar).
- Settings → Pages → Custom domain: `valura.health`.
- No DNS do domínio, apontar `CNAME`/`A` para o GitHub Pages.

## Notas
- Site público desde 2026-07-15: `noindex` e selo "Versão preliminar" removidos (aprovação do Dr. Igor). O Academy (`/academy`) segue com `noindex` + "Versão preliminar" até a Fase 2.
- Contato é só WhatsApp dos dois sócios (bloco "contato", igual em todas as páginas). `contato@valura.health` foi removido em 2026-07-16 — domínio não existe; e-mail morto frustra e viola diretriz de credibilidade (Fogg #10).
- Conformidade CFM (Resolução 2.336/2023) revisada em 2026-07-16: no máximo 2 especialidades por médico divulgadas, palavra "MÉDICO" nas linhas de credencial, sem selo de nota do Doctoralia, sem "oncogeriatria" como titulação. Detalhe em `Vault-Softwares/40-Conhecimento/Gestao-RPT/Publicidade medica CFM - o que a Valura pode e nao pode.md`.
- **Pendência conhecida, fora do escopo deste README:** `academy/index.html` (linha ~334) ainda lista `RQE 59902/59904/66254` (três especialidades) na credencial de login do Dr. Igor — mesma violação corrigida aqui no site institucional. Não foi tocado por instrução explícita (Academy é outro produto); precisa de correção própria.
