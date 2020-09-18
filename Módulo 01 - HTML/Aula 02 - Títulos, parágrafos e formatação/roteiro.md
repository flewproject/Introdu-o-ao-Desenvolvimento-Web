# Títulos, parágrafos e formatação
Agora que já temos a estrutura básica do nosso documento HTML, vamos explorar um pouco sobre formas básicas de mostrar textos em nossos sites.

## Títulos
Um título não é importante apenas para o usuário entender do que se trata o conteúdo da página, mas também para mecânismos de busca e softwares de acessibilidade filtrarem corretamente nosso conteudo.
A tag ``h1`` se trata do principal título de nosso site, como o nome, e deve se repetir apenas uma vez no documento HTML.
Para organizar nosso conteudo em ordem de importância, temos as tags que vão de ``h2`` até ``h6``, sendo ``h2`` o mais importante e ``h6`` o menos importante. Podem ser usadas para representar, por exemplo: títulos e subtitulos de matérias, nomes e descrições de produtos.
É importante frisar que alguns navegadores aplicam alguns estilos personalizados nos elementos de título, como o tamanho. No entanto, não se deve utilizar esses elementos com o propósito de deixar o texto maior ou menor, pois aprenderemos a lidar corretamente com o tamanho do texto nas próximas aulas.

`<h1>Principal título da página</h1>`
`<h1>Título de importância 2</h1>`
`<h2>Título de importância 2</h2>`
`<h3>Título de importância 3</h3>`
`<h4>Título de importância 4</h4>`
`<h5>Título de importância 5</h5>`
`<h6>Título de importância 6</h6>`

## Parágrafos
Para declarar um parágrafo em um documento HTML, utilizamos a tag ``p``.

```html
    <p>Exemplo de parágrafo</p>
    <p>Exemplo de mais um parágrafo</p>
```

Perceba que ao adicionar espaços, quebras de linha, ou qualquer outro tipo de formatação nosso parágrafo não sera afetado.

```html
    <p>   Exemplo     de mais um
parágrafo</p>
```

Caso desejemos adicionar uma quebra de linha em nosso parágrafo, utilizamos a tag ``br`` para representar onde o texo irá quebrar.

```html
    <p>Exemplo de <br/> mais um parágrafo</p>
```

## Formatação
Agora vamos explorar um pouco algumas tags que servem para formatar nossos textos.
Caso você queira destacar uma palavra no texto, basta envolver a palavra na tag ``i`` para que ela fique em itálico ou em ``b`` para que ela fique em negrito.
```html
    <p>Essa palavra esta em <i>itálico</i> e essa em <b>negrito</b></p>
```