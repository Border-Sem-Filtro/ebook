# CLAUDE.md

Este arquivo orienta o trabalho conjunto entre IA e humano neste projeto. O objetivo e transformar um frame do Figma em uma landing page estatica, responsiva, bonita e pronta para publicar no GitHub Pages.

## Objetivo do Projeto

Criar uma unica pagina de confirmacao/pos-compra para o projeto Border Sem Filtro, baseada no frame aprovado no Figma.

A pagina deve:

- Ficar visualmente muito proxima do Figma, sem exigir pixel perfect absoluto.
- Ser responsiva e elegante de `320px` ate telas desktop grandes.
- Usar HTML/CSS/JS estatico profissional, com imagens apenas onde fizer sentido.
- Ser simples de publicar no GitHub Pages.
- Funcionar inicialmente no dominio padrao do GitHub Pages.
- Permitir migracao futura para dominio proprio quando a Letty aprovar.

Repositorio alvo:

```text
git@github.com:Border-Sem-Filtro/ebook.git
```

## Principios De Trabalho

Este projeto e uma colaboracao entre humano e IA.

A IA deve:

- Codar a estrutura, estilos, responsividade, otimizacoes e ajustes finos.
- Ler este arquivo antes de tomar decisoes relevantes.
- Fazer perguntas sempre que uma resposta humana, medida do Figma ou asset exportado aumentar a qualidade final.
- Preferir clareza, simplicidade e manutencao ao excesso de framework.
- Evitar usar um print inteiro como pagina; o layout deve ser construido em HTML/CSS, usando assets apenas onde necessario.
- Manter o codigo organizado, sem overengineering.
- Testar visualmente em multiplas larguras sempre que alterar layout.
- Ser pragmatica: quando faltar um detalhe, pode usar um placeholder bem nomeado e pedir o asset/dado exato depois.

O humano pode:

- Exportar assets do Figma em PNG/WebP/SVG quando solicitado.
- Confirmar fontes, tamanhos, espacamentos e medidas no Figma.
- Revisar textos antes da publicacao.
- Cuidar de GitHub, aprovacao com a cliente, dominio e publicacao final se necessario.

Regra importante: a IA pode e deve fazer perguntas a qualquer momento para esclarecer algo, pedir um asset, confirmar uma fonte, medir um elemento no Figma ou validar uma decisao responsiva. O objetivo e trabalhar junto, nao fingir autonomia quando a colaboracao melhora o resultado.

## Stack Recomendada

Preferencia atual: pagina estatica simples.

Opcoes aceitaveis:

- `index.html` + `styles.css` + assets, publicado diretamente pelo GitHub Pages.
- Vite apenas se houver beneficio claro para pipeline, otimizacao ou organizacao.

Como a pagina e unica e nao tem interatividade complexa, a solucao preferida e evitar build step se isso nao prejudicar qualidade. Publicacao direta via GitHub Pages tende a ser suficiente e reduz atrito.

Se for escolhido Vite:

- O build deve gerar `dist`.
- O deploy deve ser simples e documentado.
- Nao adicionar React/Astro/etc. sem necessidade clara.

## Conteudo Da Pagina

A pagina e puramente informativa. Nao ha CTA principal. Os unicos links esperados sao redes sociais.

Links:

- Instagram: `https://www.instagram.com/border_sem_filtro/`
- YouTube: `https://www.youtube.com/@border_sem_filtro`

Textos principais definidos:

```text
SUA COMPRA FOI CONCLUIDA
O PRIMEIRO PASSO PARA A CONSCIENCIA FOI DADO.
OBRIGADO POR CONFIAR NO PROJETO BORDER SEM FILTRO

ANOTE NA SUA AGENDA
Lancamento:
05 de Maio
O ebook esta passando pelos ultimos ajustes de diagramacao para que voce tenha a melhor experiencia possivel. Sua copia exclusiva sera liberada nesta data.

O QUE ACONTECE AGORA?
E-MAIL
ACESSO
AVISOS

"VINCULO NAO PRECISA SER ABANDONO.
PODE SER ESCOLHA. PODE SER CONTINUIDADE.
PODE SER CONSTRUCAO."

Letty Amorim

Respira. Eu nao vou te abandonar agora que a gente comecou.
E voce tambem nao vai sumir, combinado? Nos vemos no proximo capitulo.

VAMOS MANTER
O VINCULO?

Acompanhe os conteudos diarios e tire suas duvidas diretamente comigo nas redes sociais.

@BORDER_SEM_FILTRO
```

Observacao: o humano vai revisar o texto antes de publicar. Se houver divergencia entre este arquivo e o Figma, pedir confirmacao.

## Fontes

O visual e mais importante que SEO neste projeto, mas texto real em HTML e preferivel quando viavel.

Fontes por trecho:

- `SUA COMPRA FOI CONCLUIDA`: Open Sans Extra Bold.
- `O PRIMEIRO PASSO PARA A CONSCIENCIA FOI DADO.`: Providence Sans Regular.
- `OBRIGADO POR CONFIAR NO PROJETO BORDER SEM FILTRO`: Open Sans Hebrew Regular.
- `ANOTE NA SUA AGENDA`: Open Sans Hebrew Bold.
- `Lancamento:`: Open Sans Hebrew Regular.
- `05 de Maio`: Providence Sans Regular.
- Texto descritivo do ebook: Open Sans Light.
- `O QUE ACONTECE AGORA?`: Open Sans Extra Bold.
- `E-MAIL`, `ACESSO`, `AVISOS`: Open Sans Hebrew Bold.
- Descricoes manuscritas dos cards: Providence Sans Regular.
- Frase sobre vinculo: Providence Sans Regular.
- Assinatura `Letty Amorim`: Amsterdam Regular, cor `#EF7800`.
- Texto `Respira...`: Open Sans Regular.
- `VAMOS MANTER O VINCULO?`: Open Sans Extra Bold.
- Texto das redes sociais: Providence Sans Regular.
- `@BORDER_SEM_FILTRO`: Open Sans Hebrew Regular.

Decisao de implementacao:

- Usar Google Fonts quando a fonte estiver disponivel e isso preservar bem o visual.
- Servir fontes localmente quando o humano puder fornecer arquivos licenciados.
- Usar imagem para algum texto apenas se a fonte for muito especifica, dificil de servir ou essencial para o resultado visual.

Perguntar ao humano antes de substituir uma fonte importante por aproximacao visual.

## Cores

Cores principais:

```css
--color-orange: #EF7800;
--color-black: #000000;
--color-white: #FFFFFF;
```

O tema deve permanecer preto, branco e laranja, com cuidado para preservar contraste e legibilidade.

## Assets Do Figma

O humano consegue exportar qualquer layer do Figma.

Assets provavelmente necessarios:

- Mockup do ebook/produtos em alta resolucao, preferencialmente PNG ou WebP com transparencia.
- Bordas rasgadas superiores/inferiores como imagens exportadas do Figma.
- Icones de e-mail, chave/acesso, sino/avisos, se nao forem recriados fielmente com SVG/CSS.
- Texturas ou shapes rasgados de transicao entre secoes.
- Assinatura da Letty, caso a fonte Amsterdam nao esteja disponivel ou o resultado em texto nao fique fiel.

Boas praticas:

- Nomear assets de forma semantica, por exemplo `hero-tear-top.webp`, `product-mockup.webp`, `footer-tear-orange.webp`.
- Preferir WebP para imagens fotograficas/mockups e SVG para icones simples.
- Manter versoes fonte dos assets em uma pasta clara, se houver necessidade.
- Exportar em resolucao suficiente para telas retina.

## Layout De Referencia

Frame original do Figma:

```text
2486.27 x 6900
```

Estrutura visual esperada:

1. Secao inicial preta com mensagem de compra concluida.
2. Transicao rasgada para bloco claro.
3. Bloco `ANOTE NA SUA AGENDA` com texto a esquerda e mockup do ebook a direita no desktop.
4. Secao branca `O QUE ACONTECE AGORA?` com tres itens: e-mail, acesso, avisos.
5. Transicao rasgada para secao preta.
6. Secao preta com frase manuscrita, assinatura e texto curto.
7. Transicao para rodape laranja.
8. Rodape laranja com chamada `VAMOS MANTER O VINCULO?` e links sociais.

## Responsividade

Nao existe frame mobile no Figma. A adaptacao sera feita a partir do desktop.

Requisitos:

- Largura minima suportada: `320px`.
- O layout deve continuar bonito durante resize continuo, nao apenas em alguns breakpoints fixos.
- Evitar overflow horizontal.
- Garantir que textos nao colidam com imagens, bordas rasgadas ou outros blocos.
- Usar `clamp()`, grids flexiveis, `max-width`, `aspect-ratio` e espacamentos fluidos quando apropriado.

Comportamentos esperados:

- No desktop, o bloco `ANOTE NA SUA AGENDA` pode manter texto a esquerda e mockup a direita.
- No mobile, se nao couber lado a lado, o mockup deve ir para baixo do texto.
- Os tres itens `E-MAIL`, `ACESSO`, `AVISOS` ficam lado a lado quando houver espaco.
- Quando nao couberem bem lado a lado, devem virar lista vertical.
- Na lista vertical mobile, o icone fica a esquerda e o texto a direita, em vez de icone acima.

Breakpoints sugeridos para verificacao:

- `320px`
- `360px`
- `390px`
- `430px`
- `768px`
- `1024px`
- `1280px`
- `1440px`
- largura desktop grande

## Qualidade Visual

Prioridade: ficar o mais perto possivel do Figma, mantendo uma implementacao responsiva real.

Antes de considerar a pagina pronta:

- Comparar visualmente com o frame do Figma.
- Validar mobile estreito em `320px`.
- Validar tablet e desktop.
- Validar que bordas rasgadas estao bem posicionadas.
- Validar que o mockup do produto nao fica pequeno demais nem grande demais.
- Validar contraste e legibilidade dos textos.
- Validar links sociais.
- Conferir carregamento de fontes.
- Otimizar imagens para peso razoavel sem degradar visual.

## Acessibilidade E HTML

Mesmo com foco visual, manter boas praticas:

- Usar estrutura semantica: `main`, `section`, `footer`, headings reais.
- Usar texto real sempre que viavel.
- Incluir `alt` descritivo em imagens relevantes.
- Usar `aria-hidden="true"` em imagens puramente decorativas.
- Garantir foco e links acessiveis.
- Nao depender de JavaScript para conteudo essencial.

## GitHub Pages

Publicacao inicial via GitHub Pages no dominio padrao.

Preferencia:

- Se a pagina for puramente estatica, publicar direto a partir da branch principal.
- Se houver build step, documentar claramente o processo e garantir que a pasta final seja gerada corretamente.

O projeto deve ficar pronto para o humano fazer commit/push e configurar o Pages com minimo atrito.

## Protocolo Para A IA

Ao iniciar trabalho neste projeto:

1. Ler este `CLAUDE.md`.
2. Verificar estrutura atual do repo.
3. Identificar quais assets existem e quais faltam.
4. Perguntar ao humano pelos assets/detalhes do Figma que forem realmente necessarios.
5. Implementar incrementalmente.
6. Rodar/verificar localmente.
7. Reportar o que foi feito, o que falta revisar e quais perguntas continuam abertas.

Ao pedir algo ao humano, ser especifico:

- Dizer exatamente qual layer/export e necessario.
- Sugerir formato, tamanho e nome do arquivo.
- Explicar por que isso melhora o resultado.

Exemplo:

```text
Preciso do mockup do ebook exportado como PNG ou WebP com fundo transparente, idealmente com pelo menos 1800px de largura. Nome sugerido: assets/product-mockup.webp. Isso permite manter nitidez em desktop e retina sem depender do print inteiro.
```

## Perguntas Abertas Para Iteracoes Futuras

- Confirmar se as fontes Providence Sans e Amsterdam serao fornecidas como arquivos locais ou substituidas por imagem/aproximacao.
- Exportar mockup do ebook em alta resolucao com transparencia.
- Exportar bordas rasgadas separadas do Figma.
- Confirmar descricoes exatas dos tres itens `E-MAIL`, `ACESSO`, `AVISOS`.
- Confirmar copy final antes da publicacao.
- Confirmar se icones serao assets do Figma ou recriados em SVG/CSS.

