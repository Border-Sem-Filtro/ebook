# Border Sem Filtro - Ebook Landing Page

Landing page estatica para a pagina de confirmacao do ebook Border Sem Filtro.

## Estrutura

```text
.
├── index.html          # Pagina final publicada no GitHub Pages
├── design.html         # Bancada visual para montar e revisar componentes
├── assets/
│   ├── fonts/          # Fontes locais licenciadas, se fornecidas
│   ├── icons/          # Icones exportados do Figma ou SVGs finais
│   └── images/         # Mockups, rasgos e imagens do Figma
└── styles/
    └── main.css        # Tokens, base, componentes e layout compartilhados
```

## Desenvolvimento Local

Como o projeto nao depende de build, o `npm start` apenas sobe um servidor estatico e abre `design.html`.

```powershell
npm start
```

Depois abra:

- `http://localhost:8080/`
- `http://localhost:8080/design.html`

## Publicacao

O projeto foi pensado para GitHub Pages servindo diretamente a branch principal.

Repositorio remoto:

```text
git@github.com:Border-Sem-Filtro/ebook.git
```

## Workflow

- Use `design.html` para montar, comparar e ajustar os componentes visuais.
- Promova os componentes estabilizados para `index.html`.
- Mantenha estilos compartilhados em `styles/main.css`.
- Coloque assets exportados do Figma em `assets/images`, `assets/icons` ou `assets/fonts`.
