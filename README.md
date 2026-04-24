# Casa Dom Farina — Website

Site institucional para a Casa Dom Farina — padaria artesanal em Uberlândia, MG.

## Rodar localmente

Como é um site estático (HTML + CSS + JS vanilla), você tem algumas opções:

### Opção 1 — Abrir direto no navegador

Basta dar duplo-clique no `index.html`. Funciona, mas alguns navegadores bloqueiam o `<iframe>` do Google Maps quando servido via `file://`.

### Opção 2 — Servidor local (recomendado)

Com Python (qualquer máquina que tenha Python 3):

```bash
cd casa-dom-farina
python3 -m http.server 8000
```

Depois abra http://localhost:8000 no navegador.

Com Node (se tiver instalado):

```bash
cd casa-dom-farina
npx serve .
```

## Estrutura

```
casa-dom-farina/
├── index.html           # Página única com todo o site
├── README.md            # Este arquivo
└── images/
    ├── logo.png         # Monograma Casa Dom Farina
    ├── storefront.png   # Fachada principal
    └── storefront-2.png # Fachada alternativa
```

## Tecnologias

- HTML5 semântico
- CSS3 puro (variáveis CSS, Grid, Flexbox, animations)
- JavaScript vanilla (IntersectionObserver para animações de entrada)
- Fontes: Cormorant Garamond, Cormorant SC, Fraunces (via Google Fonts)
- Imagens de apoio das especialidades: Unsplash CDN

## Deploy

O site pode ser publicado em qualquer serviço de hospedagem estática:

- **Vercel** — conecte o repositório e publique sem configuração
- **Netlify** — arraste a pasta `casa-dom-farina/` para deploy manual
- **GitHub Pages** — push no branch `main` + ativar Pages
- **Cloudflare Pages** — deploy direto do repositório

## Ajustes recomendados antes de publicar

1. **Preços do cardápio** — os valores atuais são estimativas. Substitua pelos preços reais.
2. **Handle do Instagram** — atualizar o link no rodapé e na seção "Visite-nos" com `@casadomfarina` ou o handle correto.
3. **WhatsApp** — adicionar o número real no botão do rodapé (`href="https://wa.me/55..."`).
4. **Imagens das especialidades** — atualmente carregando do Unsplash. Para produção, trocar por fotos reais da Casa e salvar em `images/`.
5. **Meta tags OG** — adicionar tags `og:image`, `og:title`, `og:description` para compartilhamento em redes sociais.
