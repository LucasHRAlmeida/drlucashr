# Dr Lucas HR Almeida

Microsite autoral de **Dr Lucas HR Almeida**, médico generalista (FMRP-USP) e fundador da Iniciativa VIA — Vida Integrada e Autônoma.

## Arquitetura

- `public/index.html` — página autoral e oferta da Mentoria Sincronismo Híbrido;
- `public/styles.css` — identidade visual e comportamento responsivo;
- `public/404.html` — resposta de erro compatível com `not_found_handling`;
- `public/robots.txt` e `public/sitemap.xml` — descoberta e indexação;
- `public/_headers` — cabeçalhos de segurança aplicados pela Cloudflare;
- `wrangler.jsonc` — configuração do Cloudflare Worker com Static Assets.

Somente `public/` é publicado. Arquivos de configuração e documentação permanecem fora da superfície HTTP.

## Publicação

O site é destinado a **Cloudflare Workers — Static Assets**. Não há etapa de build.

1. Conecte `LucasHRAlmeida/drlucashr` ao Worker `drlucashr` em **Workers & Pages → Settings → Builds**.
2. Use `main` como branch de produção.
3. Mantenha o comando de deploy padrão: `npx wrangler deploy`.
4. Cada push em `main` dispara um novo deploy.

## Domínio próprio

Para ligar um domínio ou subdomínio ao Worker, use **Settings → Domains & Routes → Add → Custom Domain**. A Cloudflare cria o registro DNS e o certificado. Não crie previamente um CNAME no mesmo hostname.

Depois de ativar o domínio próprio, substitua `https://drlucashr.workers.dev/` no `index.html`, `robots.txt` e `sitemap.xml` pelo endereço canônico definitivo.

O VIA-HUB permanece a identidade institucional. Este repositório representa a presença autoral do fundador e referencia o Hub sem absorvê-lo.
