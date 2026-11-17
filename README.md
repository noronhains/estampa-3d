# Estampa 3D

Transforma um PNG, JPG ou SVG num STL bem fino, pra imprimir em 3D e prensar na camisa com ferro ou prensa térmica.

**Usar online:** https://noronhains.github.io/estampa-3d/

Tudo roda no seu navegador. A imagem não é enviada pra lugar nenhum.

## Como usar

1. Abra a página e solte a imagem. Também dá pra colar com Ctrl+V.
2. Digite a largura em mm. A altura acompanha, e as margens vazias da imagem são cortadas.
3. Confira as camadas. O padrão é 0,20 mm de 1ª camada + 0,16 mm = **0,36 mm** (2 camadas).
4. Clique em **Gerar STL**.

No fatiador, use os mesmos valores em `First layer height` e `Layer height`. Assim a peça sai com um número exato de camadas.

## O que ele faz

- **Uma cor**: imprime as partes escuras (traço preto em fundo branco), as partes claras ou tudo que não é transparente. O limiar é ajustável.
- **Várias cores**: separa as cores da imagem e gera um STL por cor, todos alinhados, num `.zip`. Clique numa cor pra pular, por exemplo o fundo. Se quiser, junta tudo num STL só.
- Pinta de vermelho na prévia o que é mais fino que o traço mínimo (0,4 mm por padrão), que talvez não saia na impressão.
- Remove pontinhos de sujeira e furinhos, engrossa traços finos e espelha o desenho.
- Avisa quando o desenho não cabe na mesa da impressora.

O STL sai como malha fechada, com o topo e a base planos.

## Dicas

- `Elephant foot compensation` = 0. Senão a 1ª camada encolhe e o traço fino some.
- `Wall generator` = Arachne ajuda nos traços finos.
- Pra aplicar: papel manteiga por cima e ferro quente parado uns 15 a 20 s. Em desenho grande, vá movendo devagar.
- Várias cores: arraste todos os STLs juntos pro fatiador e responda **Yes** quando perguntar se é um objeto só com várias partes.

## Rodar localmente

É um arquivo só: baixe o `index.html` e abra no navegador.

## Créditos

Triangulação feita com [earcut](https://github.com/mapbox/earcut) (Mapbox, licença ISC), embutido no `index.html`.
