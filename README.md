# Dr Lucas HR Almeida

Microsite autoral de **Dr Lucas HR Almeida**, médico generalista (FMRP-USP) e fundador da Iniciativa VIA — Vida Integrada e Autônoma.

## Conteúdo

- `index.html` — página autoral + oferta da Mentoria Sincronismo Híbrido
- `styles.css` — identidade visual (paleta VIA)
- `wrangler.jsonc` — configuração para Cloudflare Workers (Static Assets)

## Publicação

Site estático destinado a **Cloudflare Workers** (Static Assets).

O VIA-HUB permanece a identidade institucional. Este repositório representa a presença autoral do fundador e referencia o Hub sem absorvê-lo.

## Deploy

1. Conectar o repositório no Cloudflare Dashboard via OAuth (Workers & Pages → Connect to Git).
2. Deploy command padrão: `npx wrangler deploy`.
3. Cada push em `main` dispara rebuild automático.
