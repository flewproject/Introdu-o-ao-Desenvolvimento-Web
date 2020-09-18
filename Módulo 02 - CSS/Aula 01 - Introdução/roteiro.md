# Introdução ao módulo
Seja bem-vindo ao módulo de CSS. No módulo anterior vimos o básico de como definir a estrutura de um site e organizar seu conteúdo utilizando o HTML, agora vamos aprender a definir o visual de uma página web.

# Introdução ao CSS
O CSS utiliza regras simples para selecionar elementos de um documento HTML e atribuí-lo uma aparência, como tamanho, cor, etc...
Para colocar o CSS em prática, vamos criar uma pasta para nosso curso e dentro dela um documento HTML chamado *index.html*, nele vamos inserir a estrutura básica de uma página. E nessa mesma pasta criaremos o arquivo *estilos.css*, vamos deixa-lo em branco por enquanto.

```html
<!DOCTYPE html>
<html>
    <head>
        <title>Meu primeiro site</title>
    </head>
    <body>
        Olá, mundo!
    </body>
</html>
 ```

Existem diversas maneiras de víncular regras CSS a um documento HTML, nesse curso vou ensinar a forma mais eficiente e de acordo com as boas práticas. Para isso, utilizaremos a tag *link* dentro de *head* para importar as regras que definiremos em *estilos.css*.
Na tag link, o atributo *href* indica o caminho do arquivo css que vamos importar, e o atributo *rel* indica a relação entre o arquivo que estamos importando e o nosso documento HTML, para um arquivo .css utilizamos o valor *stylesheet*.

```html
<head>
    <title>Meu primeiro site</title>
    <link href="estilos.css" rel="stylesheet">
</head>
```

## Sintaxe
Agora que já temos um documento HTML importando um conjunto de regras CSS, vamos começar a escrever CSS.

### Seletor
A primeira parte de uma regra CSS é o *seletor*, seguido de um abre e fecha chaves.
O seletor funciona como o "nome" do elemento em nosso documento HTML que será afetado pelas regras CSS que serão envolvidas pelas chaves.

```css
seletor{}
```

### Propriedades
Dentro das chaves nós podemos inserir diversas propriedades que dizem como nosso elemento deve ser desenhado na tela.
A estrutura de uma propriedade é definida pelo seu nome, seguido de dois pontos e seu valor. Caso você deseje atribuir mais de uma propriedade a um elemento, basta separa-las por ;

```css
seletor{propriedade1: valor;propriedade2: valor}
```
### Exemplo
A fim de curisidade, vamos deixar o fundo de nossa página azul.
Para isso vamos selecionar o elemento *body* e atribuí-lo a propriedade *background-color* com o valor *blue*
```css
body{background-color: blue}
```
# Resumo
Nessa aula começamos a entender o papel do CSS em um site, além de aprender a importar um arquivo .css em um documento HTML e sua sintaxe básica.