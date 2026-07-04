# Ivã Martins — Portfolio (candidatura)

Site portfólio pessoal focado em recrutadores internacionais. Single-page, bilíngue (PT/EN) com **auto-detecção do idioma do navegador**, com Skills Matrix, timeline de carreira, cases com impacto, e botão de download de CV.

**URL ao vivo (após deploy)**: `https://ivamartins.github.io/`

## Posicionamento

- **Foco**: Senior Java Backend Engineer, aberto a **International Contractor (PJ)** — remoto, US/EU/BR.
- **Também**: Scala + Akka + Flink + Kafka (5+ anos em produção) e Python (uso diário no Quartile).
- **Direção 2026**: AI-Driven Development (LangChain4j, RAG, MCP, AI Agents).
- **Stack primário** mantido: Java 17+, Spring Boot 3, Quarkus, Kafka, Azure/AWS, Docker.

## Stack

- HTML5 semântico + Tailwind CSS (CDN)
- Font Awesome (ícones)
- Google Fonts: Inter, Space Grotesk, JetBrains Mono
- Zero build step. Zero framework JS.
- Single-page com troca de idioma via JS puro
- **Auto-detecção de idioma** via `navigator.languages` (igual ao `code-solutions-site`)

## Estrutura

```
portfolio/
├── index.html              # single-page com 13 seções
├── assets/
│   └── portrait.jpg        # foto de perfil
├── docs/                   # PDFs de currículo (PT + EN)
│   ├── Iva_Martins_Resume_EN.pdf
│   ├── Iva_Martins_Cover_Letter_EN.pdf
│   ├── Iva_Martins_Curriculo_PT.pdf
│   └── Iva_Martins_Carta_Apresentacao_PT.pdf
├── robots.txt
├── sitemap.xml
└── README.md
```

## Seções (em ordem)

1. **Hero** — "Open to International Contractor (PJ) opportunities" + CTAs (Download CV, LinkedIn, Email) + retrato suavizado (quadrado, fade-in)
2. **Trust bar** — Sicredi · Panvel · Quartile · CIEE (4 empresas chave)
3. **About** — bio do currículo (PT/EN) + cards de engagement
4. **Career Timeline** — 6 empresas em timeline vertical (Intelly → MSDevelop → CWI → TechnoCorp/Panvel → SoftDesign → Quartile)
5. **Featured Cases** — 3 cases com bullets de impacto (Quartile, Sicredi, Panvel)
6. **Beyond Java** — cards de Scala + Akka + Flink e Python + data + APIs
7. **Skills Matrix** — proficiência + anos por tecnologia (Backend/JVM, Data/Messaging, Cloud/DevOps, AI-Driven)
8. **Current Focus** — Mapa honesto do foco 2026 (Stack principal · AI-Driven Development · Event-driven · Exploring)
9. **What I'm looking for / NOT** — fit explícito em duas colunas (incluindo: não CLT, não relocação)
10. **Open Source** — 6 repos no GitHub (com destaque para `springboot-langchain4j-rag-mcp`)
11. **Education + Certifications**
12. **Contact** — Email, LinkedIn, GitHub, WhatsApp, Download CV
13. **Footer** — cross-link para `code-solutions-site` (serviços PJ)

## Bilíngue automático

- `lang-pt` e `lang-en` em cada texto trocável
- `switchLang(lang)` aplica idioma no `<html lang>` e persiste só em escolha explícita do usuário
- `initLang()` na carga:
  1. Lê `localStorage` (`ivamartins_portfolio_lang`) → se existir, usa
  2. Senão, auto-detecta de `navigator.languages[0]` / `navigator.language` — se começar com `pt`, usa PT; senão EN
  3. **Não persiste** a auto-detecção (assim o idioma segue a config do navegador em cada visita até o usuário clicar PT/EN)

## Deploy (GitHub Pages)

### Opção A: User site (recomendado — URL mais forte)

1. Criar um repo **com o nome exato `ivamartins.github.io`** na sua conta GitHub
2. `git remote add origin git@github.com:ivamartins/ivamartins.github.io.git`
3. `git push -u origin main`
4. Settings → Pages → Source: `main` branch, root → Save
5. Pronto. Site disponível em `https://ivamartins.github.io/` em ~1 min

### Opção B: Project site (alternativa)

1. Criar um repo chamado `portfolio` (ou outro nome)
2. Renomear a pasta local para o mesmo nome
3. Push para `main`
4. Settings → Pages → Source: `main` branch, root → Save
5. Disponível em `https://ivamartins.github.io/portfolio/`

## Custom domain (opcional)

Se você tem um domínio (ex: `ivamartins.dev`):

1. Apontar CNAME do domínio para `ivamartins.github.io`
2. Criar arquivo `CNAME` na raiz do repo com o domínio
3. Em Settings → Pages → Custom domain: informar o domínio
4. Habilitar "Enforce HTTPS"

## Atualizando o CV

1. Substituir o PDF correspondente em `docs/`
2. Manter o mesmo nome de arquivo
3. `git add docs/ && git commit -m "docs: update CV"` e push

## Cross-linking com code-solutions-site

- Portfólio (este) → footer tem link "Hire as contractor →" para `code-solutions-site`
- code-solutions-site → pode adicionar link "For recruiters: see my portfolio →" (a fazer)

## SEO

- Meta tags OG, Twitter Card
- hreflang PT-BR / EN
- JSON-LD com `Person` schema (LinkedIn, GitHub, knowAbout, alumniOf)
- Sitemap + robots.txt
- Bilingual content com `lang-pt` / `lang-en` toggles

## Licença

Conteúdo e código: © Ivã Martins. PDFs de currículo: uso pessoal.
