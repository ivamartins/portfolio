# Ivã Martins — Portfolio (candidatura)

Site portfólio pessoal focado em recrutadores. Single-page, bilíngue (PT/EN), com Skills Matrix, timeline de carreira, cases com impacto, e botão de download de CV.

**URL ao vivo (após deploy)**: `https://ivamartins.github.io/`

## Stack

- HTML5 semântico + Tailwind CSS (CDN)
- Font Awesome (ícones)
- Google Fonts: Inter, Space Grotesk, JetBrains Mono
- Zero build step. Zero framework JS.
- Single-page com troca de idioma via JS puro

## Estrutura

```
portfolio/
├── index.html              # single-page com 9 seções
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

1. **Hero** — "Open to Senior Backend / Tech Lead opportunities" + CTAs (Download CV, LinkedIn, Email)
2. **Trust bar** — Sicredi · Panvel · Quartile · CIEE (4 empresas chave)
3. **About** — bio do currículo (PT/EN)
4. **Career Timeline** — 6 empresas em timeline vertical (Tecno → Intelly → MSDevelop → CWI → Panvel → SoftDesign → Quartile)
5. **Featured Cases** — 3 cases com bullets de impacto (Quartile, Sicredi, Panvel)
6. **Skills Matrix** — proficiência ●●●●○ + anos por tecnologia
7. **Tech Radar** — Adopt / Trial / Assess / Hold
8. **What I'm looking for / NOT** — fit explícito em duas colunas
9. **Open Source** — 6 repos no GitHub
10. **Education + Certifications**
11. **Contact** — Email, LinkedIn, GitHub, WhatsApp, Download CV
12. **Footer** — cross-link para `code-solutions-site` (serviços PJ)

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
