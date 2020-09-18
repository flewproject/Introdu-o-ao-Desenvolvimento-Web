# Links e caminhos de arquivo
Até esse ponto você já aprendeu a criar páginas HTML e inserir um pouco de conteudo nela, mas normalmente um site é composto de diversas páginas, como fazer para navegar entre elas?

## Caminho do nosso site
_Abir o arquivo inicio.html no navegador_.
Caso você olhe para a barra de navegação do seu navegador, você verá algo parecido com ``C:/Users/Usuario/Desktop/CursoHtml/inicio.html``.
Esse caminho descreve a localização do arquivo aberto em relação ao seu computador, similar a uma URL de um site.

## Nova página
Agora vamos na pasta do nosso projeto para criar mais um arquivo HTML, vou nomear o arquivo de _contato_ e com a extensão _html_.
É muito importante que nosso novo arquivo esteja na mesma pasta que ``inicio.html``.
_Criar novo arquivo na pasta do projeto e salvar como contato.html_.
_Voltar para o navegador_.
Em _contato.html_ vamos copiar e colar a estrutura padrão do HTML, vamos trocar o conteudo do ``title`` pelo nome que desejamos para a página e o conteudo do ``body`` por um ``h1`` com o nome da página.

```html
<!DOCTYPE html>
<html>
    <head>
        <title>Contato</title>
    </head>
    <body>
        <h1>Contato</h1>
    </body>
</html>
 ```

Se você substituir a palavra inicio por contato na barra de navegação e acessar o link, você irá abrir a nossa nova página (que esta vazia).

## Links
Para navegar de uma página para a outra, utilizaremos a tag ``a``, ela serve para indicar que elemento de nosso site deve servir para redirecionar para outro.
Dentro dela iremos inserir o texto que deve redirecionar para a outra pagina.
E para indicar ao navegador o caminho da página, basta inserir o atributo ``href``, e em seu valor o caminho da página, no caso ``contato.html``.

```html
    <a href="contato.html">Ir para contato</a>
 ```

## Caminhos de arquivo
Basta inserir ``contato.html`` no valor do href, pois esse arquivo se encontra na mesma pasta em relação a página atual, que é ``inicio.html``.
Essa forma de descrever a localização do arquivo chama-se _caminho relativo_ 
Caso o arquivo que eu desejo referenciar esteja dentro de uma pasta que esta na mesma pasta que a página atual, basta colocar o nome da pasta seguido de uma barra e do nome do arquivo.

_Criar esses arquivos e pastas para ir exemplificando com o windows explorer enquanto mostra o código_.

 ```html
    <a href="nome-da-pasta/arquivo.html">Ir para arquivo</a>
 ```

Se o arquivo que eu desejo referenciar estiver em alguma pasta anterior em relação a página atual, eu devo inserir dois pontos seguidos de barra para cada pasta que eu devo retornar para referenciar o arquivo.

 ```html
    <a href="../arquivo.html">Ir para arquivo</a>
 ```

Outro modo de referenciar um arquivo é pelo seu _caminho absoluto_.
No caso de um arquivo local, seu caminho absoluto é aquele que podemos ver na barra de navegação, ou seja, se colocarmos ``C:/Users/Usuario/Desktop/CursoHtml/contato.html`` no ``href``, também irá funcionar.
Caminhos absolutos são mais recomendados quando o objetivo é abrir uma página externa ao meu site, como ``https://www.google.com.br/``.

```html
    <a href="https://www.google.com.br/">Ir para o google</a>
 ```

 ## Abrindo link em uma nova aba
 Por padrão a tag ``a`` abre o link na mesma aba.
 Caso desejemos abrir o link em uma nova aba, precisamos definir o atributo ``target`` com o valor ``_blank`` na tag ``a``.
 O ``target`` possui dois valores principais: 
    1. ``_self (Padrão)``: abre a url na mesma aba;
    2. ``_blank``: abre a url em uma nova aba;
O ``target`` aceita alguns outros valores, mas você não precisa se preocupar com isso agora.

 
```html
    <a href="https://www.google.com.br/" target="_blank">Ir para o google</a>
 ```