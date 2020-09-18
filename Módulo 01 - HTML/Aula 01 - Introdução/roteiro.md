# Introdução curso

Nesse curso vamos explorar o básico para começar a desenvolver sites, aplicações e sistemas web.  

Para começar a explicar mais a fundo sobre as tecnologias envolvidas na criação de um site, eu gosto de compará-lo a uma casa.   

Primeiro a casa precisa ter sua estrura: o alicerce, erguer paredes, etc...
No caso de um site sua estrutura: textos, páginas, conteudos, mídias e afins são organizados utilizando o *HTML*.  
Tão importante quanto uma boa estrutura, uma casa necessita de um bom acabamento: paredes pintadas, pisos bem colocados, entre outros.
Para um site ter uma boa aparência é utilizado o *CSS*.

## Introdução HTML

Primeiramente, vamos nos focar no HTML.
HTML é a abreviação de Hypertext Markup Language, ou seja, ele é uma linguagem de marcação de texto, ele utiliza de marcações (ou "tags", que veremos ainda nessa aula) para definir a estrutura do seu site.
O HTML foi criado nos anos 90, em todo esse tempo foram criados algumas versões dele, sendo que a versão mais atual é o HTML5.  

*Primeiro site publicado: https://www.w3.org/History/19921103-hypertext/hypertext/WWW/TheProject.html*  


### Tags em HTML
Antes de começarmos a criar nosso site, precisamos saber um pouco mais sobre as tags.

#### Como escrever uma tag
Todas tags geralmente são escritas de apenas uma maneira, sendo que há dois jeitos que podemos escrever uma tag:

1. **Tags normais**
`<elemento atributo1="valor" atributo2="valor">conteudo do elemento</elemento>`

     
   Elas geralmente possuem um conteúdo _dentro_ delas. Um exemplo real seria um parágrafo (tag ``p``):
``<p>Programação é o processo de escrita, teste e manutenção de um programa de computador. O programa é escrito em uma linguagem de programação.</p>``

2. **Self-closing tags**
`<elemento atributo1="valor" atributo2="valor" />`
Estas tags abrem e fecham ao mesmo tempo, sendo assim, elas não possuem um conteúdo.

#### Estrutura de uma tag
As tags de HTML podem ter até 3 partes para compor sua estrutura:
1. **Elemento:** o elemento é o DNA da tag, toda tag possui um elemento e ele identifica o que aquela tag faz no nosso site. Por exemplo, uma tag de elemento ``p`` escreve um parágrafo, e uma tag de elemento ``a`` escreve um link no nosso site.  

2. **Atributos:** Eles variam de elemento pra elemento e nem sempre estão presentes em uma tag. Eles servem para complementar um elemento. O exemplo mais simples é um link (tag ``a``), ele sempre espera um atributo ``href``, que deve informar para qual link o nosso usuário será enviado ao clicar naquele elemento, por exemplo, podemos mandar o usuário para o site do Google colocando o ``href="www.google.com"`` na tag ``a``.  

3. **Conteúdo:** O conteúdo é a parte mais simples, ele é simplesmente tudo que vai _dentro_ de uma tag. Ele pode ser um texto ou até outra tag! Por exemplo, um parágrafo pode ter o seguinte conteúdo:
``<p>Para acessar o site do Google <a href="www.google">clique aqui</a></p>``

## Introdução ao VS Code

*Abrir o site do VS Code (https://code.visualstudio.com/).*
Nesse curso usaremos esse editor de código, pois ele é especifico para desenvolvimento web.

## Primeiro HTML
Primeiro, vamos criar uma pasta para nosso projeto e dentro dela criar um arquivo chamado _inicio_ com a extensão _.html_
_Criar nova pasta e arquivo no VS Code e salvar como inicio.html._

No início de todo documento HTML é uma boa prática indicar ao navegador em que versão do HTML estamos trabalhando para evitar qualquer falha de interpretação por parte do navegador, no nosso caso usaremos esse código para indicar que estamos utilizando HTML5.

`<!DOCTYPE html>`
>_Esta é uma declaração especial do HTML, por isso ela pode fugir um pouco da estrutura de uma tag convencional que vimos anteriormente._

Após especificar a versão, vamos definir a estrutura de nosso site.
Dentro de um documento HTML, todos os elementos são definidos utilizando tags, que são as reponsáveis por passar as informações ao navegador de como interpretar certo trecho do site.

Agora vamos inserir em nosso documento o seu primeiro elemento, o `<html>`, ele é responsável por conter todo o conteudo de uma página web.
```html
<!DOCTYPE html>
<html>
</html>
```

Dentro da tag ``<html>``, nós vamos dividir a estrutura de nossa página em duas seções com responsabilidades diferentes.
A primeira seção é definida pela tag ``<body>``, dentro dela colocaremos todos os elementos que seram desenhados na tela do usuário.
```html
<!DOCTYPE html>
<html>
    <body>
    Olá, mundo!
    </body>
</html>
```

Agora vamos ver como nosso site esta ficando no navegador.
Como você pode ver, o texto esta sendo exibido.
Outro detalhe que podemos notar é que o título que esta sendo na aba do navegador é o nome do documento, isso acontece por que não passamos ao navegador nenhum título.

Para isso, vamos implementar a seção da tag ``<head>``, dentro dela colocaremos todas as informações sobre nossa página que devem ser vistas pelos navegadores e macânismos de buscas (como o Google).
```html
<!DOCTYPE html>
<html>
    <head>
    </head>
    <body>
        Olá, mundo!
    </body>
</html>
```

E a tag que informa ao navegador o título de nossa página é a ``<title>``, basta inseri-lo dentro da ``<head>``
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

Nas proximas aulas veremos mais tags e técnicas de como elaborar seu site.