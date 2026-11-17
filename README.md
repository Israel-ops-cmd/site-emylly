# Site Toque da Deusa (Emylly Oliveira, massoterapeuta em Natal)

Site estático, sem etapa de build. HTML, CSS e JS ficam em `index.html`.

## Rodar localmente

```bash
cd site-emylly
python -m http.server 8080
```

Abra http://localhost:8080 no navegador. (No Windows, se `python` não existir, use `py -m http.server 8080`, ou `npx serve .`.)

## Estrutura

- `index.html`: página única com CSS e JS embutidos
- `img/`: fotos em .webp (800 e 1600px; recortes em 700 e 1200px)
- `vendor/`: GSAP 3.12.5, ScrollTrigger 3.12.5 e Lenis 1.1.13 (versões fixas, servidas pelo próprio site)
- `favicon.svg`, `apple-touch-icon.png`, `og-image.jpg`
- `vercel.json`: cleanUrls e cache longo para /img e /vendor

## Publicar

Cada push na branch `main` publica sozinho na Vercel (projeto importado do GitHub, Framework Preset: Other, Build Command vazio, Output Directory `./`).

## Trocar uma foto

Gere as duas larguras em .webp com o mesmo nome (ex.: `img/04-relaxante-800.webp` e `img/04-relaxante-1600.webp`) e substitua os arquivos.
