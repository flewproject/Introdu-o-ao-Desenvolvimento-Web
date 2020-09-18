# Seletores
Na aula anterior vimos o básico sobre como selecionar um elemento no CSS, nessa aula nos aprofundaremos em como selecionar elementos de forma mais especifica.


## Selecionando por elemento
A forma mais simples, porém bem pouco especifica, de se selecionar algo é referenciar o elemento a ser estilizado pelo nome da tag. Dessa forma, estaremos estilizando todos os elementos desse tipo (p, div, span, etc...);

```css
span{color: red;}
```

```html
<!DOCTYPE html>
<html>
    <head>
        <title>Seletores</title>
        <link href="estilos.css" rel="stylesheet">
    </head>
    <body>
        <p>Nesse documento, todas as tags <span>span</span> são <span>vermelhas</span></p>
    </body>
</html>
 ```

 ## Selecionando por classe
 Também podemos utilizar o atributo *class* em tags HTML para indicar que ela pertence a uma classe, que poderemos referenciar no CSS e estiliza-la.
 Para indicar que o seletor se trata de uma classe, deve-se colocar o nome da classe desejada após um '.'. Por exemplo, vamos atribuir *class* em um *span* com o valor *TextoVermelho*, nesse caso *TextoVermelho* se trata do nome da classe e para referencia-la no CSS escrevemos da seguinte forma: *.TextoVermelho*. O nome de uma classe aceita apenas letras e números, e deve iniciar com uma letra.
 Vários elementos podem receber a mesma classe, a ideia desse seletor é atribuir um conjunto de regras em comum tanto para diversos elementos, quanto para um elemento em específico.

```css
.TextoVermelho{color: red;}
```

```html
    <p>Nesse documento, as tags com a classe <span class="TextoVermelho">TextoVermelho</span> são <span>vermelhas</span></p>
```

 ## Selecionando por identificador
 Caso desejemos selecionar um elemento de forma única, ou seja, para um elemento que não deve se repetir na página, selecionamos pelo seu identificador único que é representado pelo atributo *id*.
 Para indicar que o seletor se trata de um id, deve-se colocar o nome do id desejado após um '#'. Por exemplo, vamos atribuir *id* em um *span* com o valor *TextoVermelho*, nesse caso *TextoVermelho* se trata do nome do id e para referencia-la no CSS escrevemos da seguinte forma: *#TextoVermelho*. Assim como uma classe, o nome do id aceita apenas letras e números, e deve iniciar com uma letra.

```css
#TextoVermelho{color: red;}
```

```html
    <p>Nesse documento, a tags com o id <span id="TextoVermelho">TextoVermelho</span> é <span>vermelho</span></p>
```

## Selecionando por estado
Também existe a possibilidade de atribuirmos um estilo a um elemento em apenas um determinado estado, como por exemplo um link que já foi visitado ou com o mouse em cima dele. Para isso utilizamos pseudo-classes para representar alguns estados do elemento, para isso devemos escrever um seletor do jeito que já sabemos seguidos de um ':' e o nome da pseudo-classe.

```css
    seletor:pseudo-classe{propriedade: valor;} 
```

Nesse exemplo utilizaremos um seletor por elemento, mas também poderiamos usar por classe ou id. Vamos aplicar duas pseudo-classses: *:hover* para atribuir um estilo quando o mouse estiver em cima do elemento e *:visited* para indicar que é um link que já visitamos.

```css
    a{color: black;}
    a:hover{color: blue;}
    a:visited{color: gray;}
```

```html
    <a href="google.com">Google</a>
    <a href="google.com">Bing</a>
    <a href="yahoo.com">Yahoo</a>
```

Caso deseje ver a lista completa de pseudo-classes, basta acessar esse link disponível na descrição: https://developer.mozilla.org/pt-BR/docs/Web/CSS/Pseudo-classes.

## Selecionando por parte especifica do elemento
Em alguns casos pode haver a necessidade de atribuir em estilo especifico apenas para uma parte do elemento. Como seu começo, fim ou até mesmo a primeira letra. Para isso utilizamos pseudo-elementos para representar porções do elemento, para isso, nosso seletor normal devemos será seguido de um '::' e o nome do pseudo-elemento.

```css
    seletor::pseudo-elemento{propriedade: valor;} 
```

Nesse exemplo vamos atribuir um estilo para a primeira letra de um parágrafo utilizando o *::first-letter*.

```css
    p{color: black;}
    p::first-letter{color: red;}
```

```html
    <p>Lorem ipsum dolor sit amet.</p>
```

Caso deseje ver a lista completa de pseudo-elementos, basta acessar esse link disponível na descrição: https://developer.mozilla.org/pt-BR/docs/Web/CSS/Pseudo-elementos.

## Selecionando elementos como seletores em comum
Podem existir situações em que precisemos selecionar apenas os elementos que possuam duas classes específicas, ou apenas as classes que sejam de um elemento *<div>*, mas não de um *<span>*. Para isso, basta escrever os seletores juntos.
Nesse exemplo, vamos selecionar apenas as classes *.Texto* que estão em um elemento *<p>*.

```css
    p.Texto{color: red;}
```

```html
    <div class="Texto">Classe Texto em uma DIV</div>
    <p class="Texto">Classe Texto em um P</p>
```

## Selecionando todos os elementos
Em raros casos, pode existir a necessidade de atribuir um estilo para todos os elementos, independente de classe ou id. Para isso basta utilizar o seletor `*`.

```css
    *{color: red;}
```

```html
    <div class="Texto">Classe Texto em uma DIV</div>
    <p class="Texto">Classe Texto em um P</p>
```

## Selecionando por combinadores
Também temos a possibilidade de selecionar elementos por sua relação com outros elementos. Como se ele está dentro, do lado ou seguido de um elemento específico, por exemplo.

### Selecionando elementos descendentes
Para exemplificar a relação entre elementos, costumamos chamar todos os elementos dentro de um elemento específico de descendentes. Então para selecionar as tags *<p>* que estão dentro do elemento *Principal* devemos combinar o seletor do elemento *Principal* seguido do seletor do *<p>* separados por um espaço.

```css
    #Principal p{color: red;}
```

```html
    <div id="Principal">
        <p>Parágrafo descendente do elemento principal.</p>
        <p>Parágrafo descendente do elemento principal.</p>
        <p>Parágrafo descendente do elemento principal.</p>
    </div>
    <div id="Secundario">
        <p>Parágrafo descendente do elemento secundário.</p>
        <p>Parágrafo descendente do elemento secundário.</p>
        <p>Parágrafo descendente do elemento secundário.</p>
    </div>
```

Podemos perceber que nesse caso, existem varios parágrafos, mas apenas os que estão dentro do elemento com o identificador *Principal* recebem o estilo(ou seja, são descendentes de *#Principal*). Caso mudemos a regra e selecionemos um elemento dentro de *<p>*, esse elemento ainda receberá a estilização, pois continua estando dentro de *#Principal*.

```css
    #Principal span{color: red;}
```

```html
    <div id="Principal">
        <p>Parágrafo descendente do <span>elemento principal.</span></p>
        <p>Parágrafo descendente do <span>elemento principal.</span></p>
        <p>Parágrafo descendente do <span>elemento principal.</span></p>
    </div>
    <div id="Secundario">
        <p>Parágrafo descendente do <span>elemento secundário.</span></p>
        <p>Parágrafo descendente do <span>elemento secundário.</span></p>
        <p>Parágrafo descendente do <span>elemento secundário.</span></p>
    </div>
```

### Selecionando elementos filhos
Os elementos que estão diretamente dentro de principal, são chamados de elementos filhos, como por exemplo esses *<p>*s. No entanto os *<span>*s (embora sejam descendentes de *Principal*) não são elementos filhos de *Principal*, mas sim de seus respectivos *<p>*s.
Caso eu deseje selecionar apenas os *<span>*s que são filhos de *#Principal*, eu devo combinar o seletor do elementro *Principal* seguido do seletor do *<span>* separados por um *>*.

```css
    #Principal > span{color: red;}
```

```html
    <div id="Principal">
        <span>Parágrafos:</span>
        <p>Parágrafo descendente do <span>elemento principal.</span></p>
        <p>Parágrafo descendente do <span>elemento principal.</span></p>
        <p>Parágrafo descendente do <span>elemento principal.</span></p>
    </div>
    <div id="Secundario">
        <p>Parágrafo descendente do <span>elemento secundário.</span></p>
        <p>Parágrafo descendente do <span>elemento secundário.</span></p>
        <p>Parágrafo descendente do <span>elemento secundário.</span></p>
    </div>
```

### Selecionando elementos irmãos adjacentes
Elementos que compartilham o mesmo pai, são chamados de irmãos. Caso eu deseje selecionar um elemento logo após outro elemento específico, eu devo combinar o seletor de ambos separados por um *+*.
Nesse exemplo, vamos selecionar apenas o *<p>*s que vem após um *<span>*.

```css
    span + p{color: red;}
```

```html
    <div id="Principal">
        <span>Parágrafos:</span>
        <p>Parágrafo descendente do <span>elemento principal.</span></p>
        <p>Parágrafo descendente do <span>elemento principal.</span></p>
        <p>Parágrafo descendente do <span>elemento principal.</span></p>
    </div>
    <div id="Secundario">
        <span>Parágrafos:</span>
        <p>Parágrafo descendente do <span>elemento secundário.</span></p>
        <p>Parágrafo descendente do <span>elemento secundário.</span></p>
        <p>Parágrafo descendente do <span>elemento secundário.</span></p>
    </div>
```

### Selecionando elementos caso haja um irmão em específico
Caso você deseje selecionar os elementos que possuem um irmão em específico, independente da ordem, deve-se combinar ambos seletores separados por *~*.

```css
    span ~ p{color: red;}
```

```html
    <div id="Principal">
        <span>Parágrafos:</span>
        <p>Parágrafo descendente do <span>elemento principal.</span></p>
        <p>Parágrafo descendente do <span>elemento principal.</span></p>
        <p>Parágrafo descendente do <span>elemento principal.</span></p>
    </div>
    <div id="Secundario">
        <p>Parágrafo descendente do <span>elemento secundário.</span></p>
        <p>Parágrafo descendente do <span>elemento secundário.</span></p>
        <p>Parágrafo descendente do <span>elemento secundário.</span></p>
    </div>
```

# Resumo
Nessa aula aprendemos técnicas para selecionar elementos no CSS de forma completa. Primeiro vimos os exemplos de seletores simples por elemento, classe e id e também vimos como selecionar um elemento dado suas relações de parentesco com outros elementos.